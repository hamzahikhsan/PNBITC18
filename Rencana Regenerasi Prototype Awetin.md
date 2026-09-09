# Rencana & Laporan Regenerasi Prototype Awetin (Web App Berbasis Code)

**Disusun:** 6 September 2026 (brainstorming) — **diselesaikan:** 9 September 2026
**Status:** ✅ **Fase 1–5 SELESAI.** **Link live:** https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172
**Konteks:** Awetin butuh prototype fungsional interaktif untuk validasi flow & demo internal — **bukan pengganti submission Figma** (juklak lomba tetap wajib Figma, frame iPhone 16 393×852px). Prototype ini dipakai untuk memastikan flow benar-benar "tanpa jalan buntu" sebelum dipindah ke Figma, dan sebagai referensi visual yang lebih hidup daripada static mockup saat presentasi internal tim.

---

## 0. Tujuan

Regenerasi `Dokumen Handofff saif/blom_merged (awetin).html` (27 layar, sisi konsumen Awetin) menjadi versi yang:
1. Memakai token resmi dari `Design System/DESIGN-awetin.md` (bukan token ad-hoc lama) ✅
2. Menutup 4 gap flow yang ditemukan di `Audit - Kesesuaian Handoff Saif vs PRD.md` ✅
3. Selaras dengan navbar final PRD (bukan versi yang menyimpang) ✅
4. Bisa diakses lewat link web langsung (Artifact), bukan cuma file lokal ✅
5. Hasil akhirnya **setara atau lebih baik** dari yang dibuat Saif — bukan mengulang dari nol ✅ (31 layar interaktif, flow Barang Besar penuh yang sebelumnya 0%, dark mode, kategori konsisten)

---

## 1. Keputusan yang Sudah Difiksasi

| Keputusan | Pilihan | Alasan |
|---|---|---|
| **Cakupan** | Awetin sisi **konsumen** dulu (bukan Awetin Mitra) | Mitra belum ada kodenya sama sekali (masih spec doc doang, lihat Audit). Awetin Mitra tetap belum dikerjakan — di luar cakupan sesi ini |
| **Format output** | **Artifact** (link web live, di-update di URL yang sama tiap fase selesai) | Bisa langsung dibuka & dishare ke tim tanpa perlu buka file lokal |
| **Pendekatan** | **Fork & refactor** kode Saif (bukan rebuild dari nol) | Interaksi/animasi yang sudah dipoles Saif dipertahankan, risiko regresi kecil |

---

## 2. Penyesuaian Teknis (Fondasi)

| Dependensi | Sumber Lama (Saif) | Sumber Baru (Artifact-compatible) |
|---|---|---|
| React 18 | `unpkg.com/react@18` | `cdnjs.cloudflare.com` — React 18.3.1, dipin & diverifikasi hidup |
| ReactDOM 18 | `unpkg.com/react-dom@18` | cdnjs, 18.3.1 |
| Babel Standalone | `unpkg.com/@babel/standalone` | cdnjs, 7.29.8 |
| Tailwind CDN | `cdn.tailwindcss.com` | Sudah kompatibel |
| Google Fonts | `fonts.googleapis.com` | Sudah kompatibel |

---

## 3. Ringkasan 5 Fase — Semua Selesai

### Fase 1 — Fondasi & Migrasi Artifact ✅
CDN dipindah ke cdnjs (versi dipin), struktur file disesuaikan syarat Artifact (tanpa tag `<!DOCTYPE>/<html>/<head>/<body>`), token Tailwind Saif dipertahankan + diperluas (kategori & dark mode ditambah sebagai grup baru). Zero perubahan visual/flow di fase ini — murni fondasi.

### Fase 2 — Navigasi & Sistem Kategori ✅
Bottom nav diaudit — **ternyata sudah sesuai** PRD 5.2 final (5 tab: Home/Pesanan/Perbaiki-FAB/Tukang/Profil), tidak perlu perbaikan struktural. Warna kategori disatukan lewat `CATEGORY_STYLE` — sebelumnya ada 3 definisi ad-hoc berbeda, salah satunya (Elektronik) memakai hijau primary yang sama persis dengan CTA (ambigu), sekarang dipisah pakai token `DESIGN-awetin.md`.

### Fase 3 — Menambal Gap Flow ✅
**Temuan kritis baru (lebih penting dari 4 gap awal):** ScanAI cuma py 1 skenario ter-script (Kulkas) yang salah rute langsung ke chat Barang Kecil, padahal kulkas = Barang Besar per PRD Flow 7.2. **Diperbaiki:** Triase 3-arah ditambahkan di ScanAIScreen, dan seluruh flow Barang Besar dibangun dari nol — Pilih Tukang → Jadwal & Otorisasi Biaya Jasa Tetap (QRIS) → Tukang Menuju Lokasi → Verifikasi Kode (gate wajib) → Cek Fisik → Invoice Digital & Persetujuan (Setuju/Tolak, dengan konsekuensi Biaya Jasa Tetap tetap milik tukang kalau ditolak) → Mengerjakan → Before/After → Serah Terima. Ini MVP backbone yang PRD Bagian 12 wajibkan, sebelumnya 0% ada wujudnya.

4 gap kecil dari audit juga dituntaskan:
- **Klaim Garansi** (Flow 7.12) — form foto+keterangan dari Riwayat Servis, status Sedang Ditinjau → simulasi tukang menjadwalkan servis ulang (Terjadwal)
- **Jual atau Donasi** (Flow 7.6) — Triase sekarang eksplisit menawarkan Jual vs Donasi (bukan langsung ke form Jual), dengan disclaimer barang domestik
- **Direktori Partner Donasi** (Flow 7.6 poin 4) — partner per kategori, tandai sudah disalurkan
- **Direktori Daur Ulang Resmi** (Flow 7.7) — percabangan pesan B3 elektronik vs bank sampah non-elektronik
- **Riwayat Penyaluran Non-Servis** (Screen #26) — log gabungan Jual/Donasi/Daur Ulang, diakses dari Profil

### Fase 4 — Dark Mode & Aksesibilitas ✅
572 class Tailwind raw hex disatukan ke token semantik di seluruh file (efek samping: konsistensi visual total, bukan cuma buat dark mode). Token warna diubah jadi CSS variable mengikuti pola 3-state resmi Artifact (`prefers-color-scheme` + `[data-theme]`) — satu class Tailwind (`bg-surface`, `text-text-primary`, dst.) otomatis ikut tema tanpa perlu ditulis ulang per elemen. Toggle "Mode Gelap" sungguhan ditambahkan di Profil > Aksesibilitas, tersimpan ke `localStorage`, independen dari tema browser (sesuai PRD: pengaturan di dalam app). Komponen high-leverage (`MTopBar`, `MButton` secondary/destructive, `MBottomSheet`, chat bubble) yang tadinya `bg-white` murni dipindah ke `bg-surface`. `aria-label` ditambahkan ke tombol ikon-saja yang paling sering dipakai (kembali, tutup, hapus).

**Batasan yang diakui secara terbuka, bukan disembunyikan:**
- Icon `color="#HEX"` literal (prop JS, bukan class Tailwind) tidak ikut re-theme otomatis — kontras berkurang di dark mode tapi tetap terbaca, bukan pecah/hilang.
- Segelintir warna dekoratif satu-off (layar Scan AI yang memang sudah gelap by design, beberapa badge kecil ambigu) sengaja tidak disentuh — dampak visual minimal.
- Warna kategori jasa: hue "default" sengaja sama di kedua tema (sudah cukup jenuh untuk kontras di keduanya); hanya container/on-container yang ikut berubah.

### Fase 5 — QA End-to-End & Finalisasi ✅
**Metode:** koneksi browser automation (`claude-in-chrome`) terputus sepanjang sesi regenerasi Fase 3–5 dan tidak berhasil disambung ulang meski ekstensi aktif di sisi user — kemungkinan butuh restart sesi Claude Code untuk refresh koneksi MCP, di luar kendali dari dalam percakapan. **Alternatif Playwright dicoba dan terbukti tidak valid** untuk kasus ini (browser baru tanpa sesi login, artifact private jadi mental ke halaman login). Sebagai gantinya, QA dilakukan dengan **menelusuri kode baris-per-baris** (bukan klik langsung), divalidasi dengan `@babel/core` (compiler JSX sungguhan, bukan cuma hitung kurung) di tiap checkpoint perubahan.

Lihat Requirement Matrix di Bagian 4.

---

## 4. Requirement Matrix

| Requirement | Implemented | Verified (statis) | Status |
|---|:---:|:---:|---|
| Navbar 5-tab user sesuai PRD 5.2 | ✅ | ✅ | PASS |
| Scan AI → deteksi + confidence score | ✅ | ✅ | PASS |
| Triase 3-arah (Perbaiki/Jual-Donasi/Daur Ulang/Batal) | ✅ | ✅ | PASS |
| Segmentasi otomatis Barang Besar vs Kecil dari kategori terdeteksi | ✅ | ✅ | PASS |
| Flow Barang Besar: Jadwal & Biaya Jasa Tetap (QRIS) | ✅ | ✅ | PASS |
| Flow Barang Besar: Verifikasi Kode (gate wajib) | ✅ | ✅ | PASS |
| Flow Barang Besar: Cek Fisik → Invoice & Persetujuan | ✅ | ✅ | PASS |
| Konsekuensi Tolak Invoice (Biaya Jasa Tetap milik tukang) | ✅ | ✅ | PASS |
| Before/After + Rating & Ulasan | ✅ | ✅ | PASS |
| Dashboard Dampak Komunitas ter-update | ✅ | ✅ | PASS |
| Jual atau Donasi — pilihan eksplisit + disclaimer | ✅ | ✅ | PASS |
| Direktori Partner Donasi per kategori | ✅ | ✅ | PASS |
| Direktori Daur Ulang Resmi (B3 vs bank sampah) | ✅ | ✅ | PASS |
| Riwayat Penyaluran Non-Servis | ✅ | ✅ | PASS |
| Klaim Garansi (form → Sedang Ditinjau → Terjadwal) | ✅ | ✅ | PASS |
| Warna kategori konsisten & tidak tabrakan warna semantik | ✅ | ✅ | PASS |
| Dark mode via toggle in-app, tersimpan | ✅ | ✅ | PASS |
| Dark mode — cakupan penuh 100% tanpa kecuali | ⚠️ | ⚠️ | **PARTIAL** — lihat batasan Fase 4 |
| Aksesibilitas — aria-label tombol ikon kritis | ✅ | ✅ | PASS |
| Aksesibilitas — checklist penuh DESIGN-awetin.md (kontras terukur, dll.) | ⚠️ | ❌ | **TIDAK DIUKUR** — perlu alat contrast checker sungguhan |
| Draft Scan AI tersimpan otomatis saat "Belum Yakin" | ❌ | — | **TIDAK DIIMPLEMENTASI** — minor, AI selalu re-deteksi item sama di demo ini |
| Verifikasi visual live (click-through browser sungguhan) | — | ❌ | **BELUM** — browser tools terputus sepanjang sesi |

**Verdict:** **PASS dengan catatan** — seluruh flow fungsional & logika sudah lengkap dan tervalidasi secara statis tanpa satupun bug ditemukan saat penelusuran, tapi verifikasi visual/interaktif live oleh manusia sungguhan **masih jadi langkah wajib terakhir** sebelum prototype ini dipakai demo ke juri atau tim.

---

## 5. Referensi

- `Dokumen Handofff saif/blom_merged (awetin).html` — basis kode yang di-fork
- `Design System/DESIGN-awetin.md` — sumber token tunggal
- `Audit - Kesesuaian Handoff Saif vs PRD.md` — sumber daftar gap Fase 3 & penyimpangan nav Fase 2
- `PRD Lengkap - Awetin.md` — Bagian 5.2 (Navbar), 7 (User Flow), 9 (Microcopy), 11 (Aksesibilitas), 12 (Ruang Lingkup MVP)

---

## 6. Catatan Penting

Prototype ini **bukan pengganti** mockup Figma yang wajib untuk submission lomba — statusnya alat bantu validasi & demo internal. Kalau ada perbedaan antara apa yang "terasa benar" di prototype ini dengan keputusan final PRD/CLAUDE.md, PRD/CLAUDE.md yang menang, bukan sebaliknya.

**Sebelum dipakai demo:** lakukan satu putaran klik-klik manual sungguhan di link live — terutama jalur Scan AI → Triase → Barang Besar penuh, dan coba toggle Mode Gelap di Profil — karena seluruh Fase 3-5 di atas divalidasi lewat pembacaan kode + syntax check, bukan interaksi visual langsung (browser automation terputus sepanjang sesi ini).

**Di luar cakupan sesi ini (belum dikerjakan sama sekali):**
- Awetin Mitra (app sisi tukang) — masih 0%, cuma ada spec doc
- Pengukuran kontras warna dark-mode sungguhan pakai contrast checker
- Draft Scan AI yang bisa dilanjutkan kapan saja (saat ini "Belum Yakin" langsung kembali ke Home tanpa menyimpan progres)
