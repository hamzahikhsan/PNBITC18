# Rencana Regenerasi Prototype Awetin (Web App Berbasis Code)

**Disusun:** 6 September 2026 (hasil sesi brainstorming — `superpowers:brainstorming`)
**Status:** Fase 1 selesai. **Link live:** https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172
**Konteks:** Awetin butuh prototype fungsional interaktif untuk validasi flow & demo internal — **bukan pengganti submission Figma** (juklak lomba tetap wajib Figma, frame iPhone 16 393×852px). Prototype ini dipakai untuk memastikan flow benar-benar "tanpa jalan buntu" sebelum dipindah ke Figma, dan sebagai referensi visual yang lebih hidup daripada static mockup saat presentasi internal tim.

---

## 0. Tujuan

Regenerasi `Dokumen Handofff saif/blom_merged (awetin).html` (27 layar, sisi konsumen Awetin) menjadi versi yang:
1. Memakai token resmi dari `Design System/DESIGN-awetin.md` (bukan token ad-hoc lama)
2. Menutup 4 gap flow yang ditemukan di `Audit - Kesesuaian Handoff Saif vs PRD.md`
3. Selaras dengan navbar final PRD (bukan versi yang menyimpang)
4. Bisa diakses lewat link web langsung (Artifact), bukan cuma file lokal
5. Hasil akhirnya **setara atau lebih baik** dari yang dibuat Saif — bukan mengulang dari nol

---

## 1. Keputusan yang Sudah Difiksasi

| Keputusan | Pilihan | Alasan |
|---|---|---|
| **Cakupan** | Awetin sisi **konsumen** dulu (bukan Awetin Mitra) | Mitra belum ada kodenya sama sekali (masih spec doc doang, lihat Audit). Fokus dulu ke yang sudah punya basis solid, biar tuntas & rapi — Mitra bisa jadi fase lanjutan terpisah kalau waktu masih ada |
| **Format output** | **Artifact** (link web live, di-update di URL yang sama tiap fase selesai) | Bisa langsung dibuka & dishare ke tim tanpa perlu buka file lokal; progres tiap fase langsung terlihat |
| **Pendekatan** | **Fork & refactor** kode Saif (bukan rebuild dari nol) | Interaksi/animasi yang sudah dipoles Saif dipertahankan, risiko regresi kecil, lebih cepat — penting karena prototype ini bukan deliverable yang dinilai juri, jadi efisiensi waktu diprioritaskan di atas kebersihan arsitektur kode |

---

## 2. Penyesuaian Teknis yang Diperlukan (Fondasi)

Kode Saif ditulis untuk dibuka sebagai file lokal (`<script src="https://unpkg.com/...">`). Artifact Claude Code punya CSP allowlist CDN yang lebih ketat — `unpkg.com` **tidak** ada di daftar itu. Penyesuaian:

| Dependensi | Sumber Lama (Saif) | Sumber Baru (Artifact-compatible) |
|---|---|---|
| React 18 | `unpkg.com/react@18/umd/...` | `cdnjs.cloudflare.com` atau `cdn.jsdelivr.net/npm/` (UMD build, versi dipin persis) |
| ReactDOM 18 | `unpkg.com/react-dom@18/umd/...` | sama seperti di atas |
| Babel Standalone | `unpkg.com/@babel/standalone/...` | sama seperti di atas |
| Tailwind CDN | `cdn.tailwindcss.com` | **Sudah kompatibel**, tidak perlu diganti |
| Google Fonts (Plus Jakarta Sans, JetBrains Mono) | `fonts.googleapis.com` | **Sudah kompatibel**, tidak perlu diganti |

Fungsinya identik — cuma ganti host, bukan ganti library atau versi.

---

## 3. Breakdown 5 Fase

Setiap fase = satu putaran kerja mandiri dengan checkpoint publish, supaya progres tidak numpuk jadi satu perubahan besar yang susah divalidasi.

### Fase 1 — Fondasi & Migrasi Artifact ✅ SELESAI
**Tujuan:** Kode Saif jalan normal di lingkungan Artifact, dengan token baru terpasang, tanpa mengubah perilaku layar apa pun dulu.
- [x] Fork ke `Prototype/awetin-prototype.html`, sumber CDN diganti (React/ReactDOM 18.3.1, Babel Standalone 7.29.8, semua dipin & diverifikasi hidup di cdnjs) — lihat Bagian 2
- [x] Tailwind config ditambah (bukan diganti) — token lama Saif dipertahankan 100%, 4 warna kategori & token dark mode ditambahkan sebagai grup baru (`category.*`, `dark.*`)
- [x] Scaffolding dark mode: CSS variable `--awetin-bg-frame` di `:root`, mengikuti pola 3-state resmi Artifact (`prefers-color-scheme` digguard `:not([data-theme="light"])` + `[data-theme="dark"]`). **Catatan cakupan:** ini baru backdrop luar frame HP yang mengikuti tema viewer Artifact — dark mode ISI aplikasi (semua layar di dalam `#root`) belum disentuh, itu tugas Fase 4 dengan mekanisme toggle in-app sendiri (bukan ikut tema viewer), sesuai PRD ("mode gelap sebagai pilihan" di dalam app, bukan sinkron ke browser)
- [x] Struktur file disesuaikan ke syarat Artifact (tanpa tag `<!DOCTYPE>/<html>/<head>/<body>`)
- **Checkpoint:** [dipublikasikan](https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172) — tampilan & perilaku semua layar identik dengan punya Saif, murni ganti fondasi

### Fase 2 — Navigasi & Sistem Kategori ✅ SELESAI
**Tujuan:** Struktur navigasi 100% sesuai keputusan final PRD, kategori jasa punya identitas visual konsisten.
- [x] Audit bottom nav — **ternyata sudah sesuai** PRD 5.2 final (5 tab: Home/Pesanan/Perbaiki-FAB/Tukang/Profil), tidak perlu perbaikan struktural
- [x] Satu sumber warna kategori (`CATEGORY_STYLE`) menggantikan 3 definisi ad-hoc berbeda yang sebelumnya ada di kode Saif — salah satunya (Elektronik) sempat pakai hijau primary yang sama persis dengan CTA, sekarang dipisah pakai token `DESIGN-awetin.md`
- [x] Diterapkan di: grid kategori Home, dashboard Dampak Komunitas, kategori populer di Search
- **Checkpoint:** [dipublikasikan](https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172)

### Fase 3 — Menambal Gap Flow (dari Audit) 🔶 SEBAGIAN SELESAI
**Tujuan:** Menutup gap flow yang ditemukan.
- [x] **Prioritas kritis (ditemukan saat verifikasi Fase 1-2, lebih penting dari 4 gap awal):** ScanAI cuma py 1 skenario ter-script (Kulkas) yang salah rute langsung ke chat Barang Kecil, padahal kulkas = Barang Besar per PRD. **Sudah diperbaiki:** Triase 3-arah ditambahkan di ScanAIScreen, dan flow Barang Besar penuh dibangun (Pilih Tukang → Jadwal & Biaya Jasa Tetap (QRIS) → Tukang Menuju Lokasi → Verifikasi Kode → Cek Fisik → Invoice & Persetujuan → Mengerjakan → Before/After → Serah Terima) — MVP backbone PRD Bagian 12 sekarang punya wujud nyata.
- [ ] **Klaim Garansi** — form (foto + keterangan) + status "Sedang Ditinjau" (Flow 7.12) — belum dikerjakan
- [ ] **Direktori Partner Donasi** — saat ini Triase "Jual-Donasi" masih redirect ke form Jual biasa (bukan direktori partner sesuai kategori, Flow 7.6 poin 4) — belum dikerjakan
- [ ] **Direktori Dropbox Daur Ulang Resmi** — saat ini Triase "Daur Ulang" masih placeholder jujur (`FallbackScreen`), belum ada direktori dropbox sungguhan (Flow 7.7) — belum dikerjakan
- [ ] **Riwayat Penyaluran Non-Servis** — layar terpisah (Screen #26) — belum dikerjakan
- **Checkpoint:** [dipublikasikan](https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172) — bagian kritis sudah live, 4 item sisanya masih terbuka

### Fase 4 — Pengetatan UX ("Tanpa Jalan Buntu")
**Tujuan:** Menegakkan Prinsip Desain #3 PRD secara menyeluruh, bukan cuma di layar-layar utama.
- Audit fallback yang PRD wajibkan tapi berpotensi belum lengkap di kode lama: tukang tidak tersedia di radius (Flow 7.3/7.4), negosiasi chat gagal sepakat (Flow 7.4), pembayaran gagal (Flow 7.8)
- Terapkan dark mode ke seluruh layar (bukan cuma fondasi token di Fase 1)
- Terapkan checklist aksesibilitas `DESIGN-awetin.md` (kontras, target sentuh 44×44pt minimum, label deskriptif, status tidak hanya lewat warna)
- Rapikan komponen skeleton/empty-state/error-state pakai copy jujur ala PRD Bagian 9
- **Checkpoint:** publish, uji toggle dark mode + jalur-jalur gagal di atas

### Fase 5 — QA End-to-End & Finalisasi
**Tujuan:** Memastikan journey MVP backbone bisa ditelusuri tuntas tanpa hambatan, sebelum disebut selesai.
- Telusuri penuh journey MVP PRD Bagian 12: **Scan AI → Skor Kelayakan → Triase → Flow Barang Besar → Konfirmasi Jadwal & Biaya → Invoice & Persetujuan → Rating & Bukti → Dashboard Dampak**
- Susun **Requirement Matrix** (Requirement | Implemented | Tested | Status) — meniru praktik baik dari format spec handoff Saif, sebagai bukti tuntas
- Polish visual terakhir (ikon konsisten satu pustaka, ilustrasi empty-state)
- **Checkpoint:** publish versi final + tulis ringkasan status (PASS/masih ada catatan) di dokumen ini

---

## 4. Definition of Done (Keseluruhan)

Prototype dianggap selesai kalau:
- [ ] Semua 27 layar asli Saif + 4 layar baru dari Fase 3 bisa diakses dan saling terhubung (tidak ada layar yatim)
- [ ] Token 100% dari `DESIGN-awetin.md`, tidak ada warna/radius hardcoded yang menyimpang
- [ ] Dark mode berfungsi di semua layar
- [ ] Navbar sesuai PRD 5.2 final
- [ ] Journey MVP Bagian 12 PRD bisa ditelusuri ujung ke ujung tanpa jalan buntu
- [ ] Requirement Matrix tersusun dan status mayoritas PASS

---

## 5. Referensi

- `Dokumen Handofff saif/blom_merged (awetin).html` — basis kode yang di-fork
- `Design System/DESIGN-awetin.md` — sumber token tunggal
- `Audit - Kesesuaian Handoff Saif vs PRD.md` — sumber daftar gap Fase 3 & penyimpangan nav Fase 2
- `PRD Lengkap - Awetin.md` — Bagian 5.2 (Navbar), 7 (User Flow), 9 (Microcopy), 11 (Aksesibilitas), 12 (Ruang Lingkup MVP)

---

## 6. Catatan Penting

Prototype ini **bukan pengganti** mockup Figma yang wajib untuk submission lomba — statusnya alat bantu validasi & demo internal. Kalau ada perbedaan antara apa yang "terasa benar" di prototype ini dengan keputusan final PRD/CLAUDE.md, PRD/CLAUDE.md yang menang, bukan sebaliknya.
