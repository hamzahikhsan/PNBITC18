# Audit: Kesesuaian Handoff Saif vs PRD Lengkap - Awetin

**Disusun:** 6 September 2026
**Status:** Temuan audit — bukan keputusan final, perlu ditinjau tim sebelum dipakai sebagai dasar lanjutan
**Objek audit:** `Dokumen Handofff saif/AWETIN MITRA FULL BUILD + WEB RESEARCH + E2E AUDIT HANDOFF.md` (spec) dan `Dokumen Handofff saif/blom_merged (awetin).html` (hasil build aktual)
**Dibandingkan terhadap:** `PRD Lengkap - Awetin.md` (Revisi 2, 31 Agustus 2026) dan `CLAUDE.md` (keputusan final tim)

---

## 0. Ringkasan Eksekutif

Sebagian besar isi spec handoff **valid dan bersumber dari PRD** — terutama flow Onboarding Tukang, segmentasi Barang Besar/Kecil, invoice, payment, dan sistem reputasi. Tapi ditemukan **dua penyimpangan dari keputusan yang sudah dikunci tim** (bukan sekadar elaborasi), beberapa fitur baru tanpa dasar riset PRD, dan gap antara apa yang diminta spec vs apa yang benar-benar ada di file HTML hasil build.

**Temuan paling kritis:**
1. Spec ini meminta app **"Awetin Mitra"** (sisi tukang) dibangun — tapi `blom_merged (awetin).html` yang dibundel di folder yang sama justru berisi app **sisi konsumen (Awetin)**. App Awetin Mitra yang diminta spec **belum dibangun sama sekali**, baik di HTML maupun Figma.
2. Spec mengubah **navbar tukang dari 4 tab (final, PRD 5.3) menjadi 5 tab** tanpa disebut sebagai revisi sadar.
3. Spec mengasumsikan **Awetin dan Awetin Mitra adalah dua aplikasi terpisah total** (download terpisah), padahal PRD memutuskan **dua mode dalam satu konsep app**, dipilih saat onboarding.
4. Build HTML konsumen yang ada kehilangan 3-4 layar wajib dari daftar 39 layar PRD (Daur Ulang Resmi, Direktori Partner Donasi, Klaim Garansi, Riwayat Penyaluran Non-Servis).

---

## 1. Metodologi

Setiap section dari spec handoff (48 section) dibandingkan manual terhadap:
- PRD Bagian 5 (Navigasi), 6 (Fitur per Modul), 7 (User Flow), 8 (Daftar 39 Layar), 9 (Microcopy)
- CLAUDE.md Bagian 4 (Keputusan Kunci Final) dan Bagian 6 (Pertanyaan Terbuka)

Lalu setiap elemen spec diklasifikasi ke salah satu dari 4 kategori (A-D) di bawah. Build HTML aktual (`blom_merged (awetin).html`, 3080 baris) juga dibaca langsung (bukan cuma nama filenya) untuk verifikasi apa yang benar-benar terimplementasi, bukan cuma apa yang diklaim spec.

---

## 2. Kategori A — Sesuai & Bersumber Langsung dari PRD

Bagian spec ini terverifikasi selaras dengan PRD, termasuk beberapa yang copy-nya diambil hampir verbatim:

| Elemen Spec (Section) | Sumber PRD |
|---|---|
| Onboarding Usaha 8-step (kategori → data dasar → consent KTP → consent lokasi → upload → kisaran harga → menunggu verifikasi → hasil) | Flow 7.9, Screen #30-34 |
| Segmentasi Barang Besar vs Barang Kecil, jalur berbeda | Flow 7.2 poin 3, Flow 7.3, 7.4 |
| Invoice & persetujuan wajib sebelum kerja dimulai | Flow 7.3 poin 4-5, Modul 6.2 |
| Terima/Tolak pesanan dengan alasan + reroute ke tukang lain di radius sama | Flow 7.10 poin 1-2 |
| Payment (QRIS/tunai) **hanya berlaku untuk Barang Besar**, Barang Kecil dibayar di luar aplikasi | Flow 7.8, Modul 6.5 |
| Copy alert reputasi — *"Visibilitas profilmu diturunkan sementara karena beberapa laporan harga di luar rata-rata wilayahmu..."* — **disalin persis kata-katanya** | PRD Bagian 9 (Microcopy) |
| Sistem reputasi dipicu oleh harga di luar rata-rata **lokal**, bukan ambang nasional | Flow 7.11 poin 2 |
| Profil Usaha (edit kategori/harga, portofolio before/after, badge verifikasi) | Modul 6.3, Screen #37 |
| Rincian pendapatan dengan komisi platform (~5-10%, tunai = Rp0 komisi) | Modul 6.5, Screen #38 |
| Prinsip aksesibilitas umum (kontras, label, status bukan cuma warna) | PRD Bagian 11 |
| Persona tukang: literasi digital terbatas, butuh UI sederhana tanpa jargon | Persona B ("Pak Anung") |

---

## 3. Kategori B — Elaborasi yang Mengisi Celah PRD (Tidak Bertentangan, Tapi Tidak Tertelusuri)

PRD memang tidak mendetailkan sampai level ini, jadi bagian-bagian berikut adalah "karangan lanjutan" yang masuk akal secara UX, tapi **tidak bisa dirujuk balik ke riset atau keputusan tim manapun** — kalau juri tanya dasarnya, jawabannya "praktik umum aplikasi sejenis", bukan "ada di riset kami":

| Elemen Spec | Catatan |
|---|---|
| Auth OTP-only tanpa password sama sekali + flow Pemulihan Akun (ganti nomor HP) | PRD cuma sebut "nomor HP/email" secara umum (Flow 7.1), tidak pernah spesifik OTP-only, dan flow Pemulihan Akun tidak ada di 39 layar PRD sama sekali |
| **Kode Verifikasi 4-digit** wajib saat tukang tiba di lokasi, gate sebelum Cek Fisik | Tidak ada di Flow 7.3 PRD |
| **Live Tracking Map** (rute mock sisi tukang) | Tidak disebut PRD sama sekali, tidak ada di 39 layar |
| Rating **tukang menilai pelanggan** (privat, dua arah) | Flow 7.11 PRD cuma satu arah (pelanggan → tukang, untuk filter tukang nakal). Tidak ada mekanisme sebaliknya di PRD manapun |
| **Fitur Tip** (terpisah dari komisi, 100% ke tukang) | Tidak disebut di PRD sama sekali |
| Pembatalan oleh tukang memicu `ReputationAlertCard` | PRD Flow 7.11 cuma kaitkan reputasi ke "pola harga di luar wajar", bukan ke pembatalan |
| Onboarding "Ditolak" dengan alasan spesifik + CTA "Perbaiki" langsung ke bagian error | PRD Flow 7.9 cuma sampai "terverifikasi → aktif", tidak detail jalur ditolak (walau konsisten dengan Prinsip Desain #3 "tanpa jalan buntu") |
| App Lock (PIN/biometrik lokal), halaman legal statis, info versi app | Tidak dibahas PRD, tapi wajar sebagai boilerplate standar |
| Jadwal Ulang pesanan (reschedule umum) | Beda dari jadwal ulang garansi (Flow 7.12) yang memang ada di PRD |

---

## 4. Kategori C — Bertentangan dengan Keputusan yang Sudah Final 🚩

Dua temuan ini **mengubah keputusan yang sudah dikunci** (CLAUDE.md Bagian 4: *"jangan dipertanyakan ulang tanpa alasan baru"*) tanpa disebut sebagai revisi sadar:

### 4.1 Navbar Tukang: 4 tab (final) → jadi 5 tab (spec)

| | PRD Bagian 5.3 (final) | Spec Handoff |
|---|---|---|
| Jumlah tab | 4 | 5 |
| Isi | Pesanan Masuk (utama) — Profil Usaha — Pendapatan — Notifikasi | **Beranda** — Pesanan Masuk — Pendapatan — Notifikasi — Profil Usaha |

PRD sengaja membuat "Pesanan Masuk" sebagai tab utama/home-like (biar navbar tukang tetap sederhana, sesuai kebutuhan Persona B literasi digital terbatas). Spec menambah "Beranda" sebagai dashboard terpisah (kartu performa, banner tips, dsb.) — secara fungsi masuk akal, tapi ini perubahan struktural terhadap keputusan final, bukan detail tambahan.

### 4.2 Arsitektur: "Dua mode dalam satu konsep" → jadi "Dua aplikasi terpisah total"

| | PRD Bagian 5.3 (final) | Spec Handoff |
|---|---|---|
| Model | "Dua mode antarmuka terpisah, dipilih di layar Onboarding awal — bukan toggle di satu akun" | "Awetin Mitra adalah **aplikasi terpisah**... Bukan mode switch. Tidak mengubah shell aplikasi Mitra." |
| Dual-role akun (Pertanyaan Terbuka #3 PRD) | Eksplisit ditandai sebagai **keputusan tim, belum diputuskan** | Diam-diam dijawab "terpisah total" oleh spec, tanpa konfirmasi tim |

Ini bukan cuma beda framing — spec ini **menjawab sepihak salah satu dari 7 Pertanyaan Terbuka PRD** yang CLAUDE.md eksplisit bilang tidak boleh diasumsikan AI.

---

## 5. Kategori D — Build HTML Aktual vs Spec vs PRD

Ini bagian paling penting: **apa yang diminta ≠ apa yang dibangun**.

- Spec (`AWETIN MITRA FULL BUILD...HANDOFF.md`) meminta app **Awetin Mitra** (sisi tukang) dibangun end-to-end.
- File HTML yang dibundel di folder yang sama, `blom_merged (awetin).html` (3080 baris, 27 layar), ternyata adalah **sisi konsumen (Awetin)** — bukan Mitra. File itu sendiri secara eksplisit bilang (baris 333): *"Awetin Mitra adalah aplikasi terpisah... Aplikasi ini (Awetin) khusus untuk mencari jasa."*
- **Nol** dari 14 komponen reusable yang diminta spec untuk Mitra (`OrderRequestCard`, `StatusStepper`, `InvoiceEditor`, `EarningsCard`, dll.) ditemukan di file ini.
- **Kesimpulan: app Awetin Mitra yang diminta spec = 0% dibangun.** Yang ada baru spec tertulisnya.

### 5.1 Kelengkapan build konsumen (`blom_merged`) vs 29 layar "Sisi Pengguna" PRD Bagian 8

Layar wajib PRD yang **tidak ditemukan** di build:

| Layar PRD (Bagian 8) | Status di `blom_merged` |
|---|---|
| #20 Form Klaim Garansi | ❌ Tidak ada |
| #24 Direktori Partner Donasi | ❌ Tidak ada — "Donasi" cuma jadi checkbox di form Jual, bukan flow redirect ke partner sesuai Flow 7.6 poin 4 |
| #25 Direktori Dropbox Daur Ulang Resmi | ❌ Tidak ada — Flow 7.7 (Daur Ulang Resmi) sama sekali tidak terimplementasi |
| #26 Riwayat Penyaluran Non-Servis | ❌ Tidak ditemukan sebagai layar terpisah |

File `awetin-onboarding.html` (di root folder) sudah dikonfirmasi **superseded** oleh `blom_merged` — screen-nya identik (WelcomeScreen, PhoneEntry, OTP, dst., minus prefix "OB") tapi cuma 1005 baris dan berhenti di Home + `StubScreen` untuk sisanya. Tidak perlu dipakai lagi sebagai rujukan aktif.

---

## 6. Rekomendasi

1. **Konfirmasi ke tim (bukan asumsi sepihak):** apakah "Awetin Mitra sebagai aplikasi terpisah total" ini keputusan sadar tim yang meng-override PRD 5.3, atau perlu diluruskan balik ke "satu app, dua mode". Ini menentukan arah seluruh kerja selanjutnya (termasuk apakah perlu 2x39 layar Figma atau tetap 1 app dengan percabangan mode).
2. **Kalau arsitektur 2-app dipertahankan:** update PRD Bagian 5.3 dan CLAUDE.md secara eksplisit sebagai revisi sadar (bukan dibiarkan menggantung sebagai kontradiksi diam-diam), dan jawab Pertanyaan Terbuka #3 secara resmi.
3. **Navbar tukang 5-tab vs 4-tab final:** putuskan salah satu, catat sebagai revisi resmi kalau memang berubah ke 5 tab.
4. **Fitur baru tanpa dasar PRD** (Tip, rating dua arah, kode verifikasi, live tracking) — boleh dipakai kalau tim setuju sebagai UX enhancement, tapi jangan dipresentasikan ke juri seolah-olah hasil riset; sebutkan sebagai keputusan desain praktis.
5. **Kalau melanjutkan `blom_merged.html` sebagai basis:** lengkapi dulu 4 layar yang hilang (Klaim Garansi, Donasi, Daur Ulang Resmi, Riwayat Penyaluran) sebelum dipakai sebagai rujukan untuk mockup Figma — supaya tidak ada celah yang ikut terbawa ke Figma.
6. **Ingat:** HTML/React ini valid sebagai *prototype fungsional internal* untuk validasi flow, tapi **tidak bisa jadi bagian dari submission lomba** — deliverable wajib tetap Figma, frame iPhone 16 (393×852px).

---

## 7. Referensi

- `PRD Lengkap - Awetin.md` (Revisi 2, 31 Agustus 2026)
- `CLAUDE.md` (briefing konteks & keputusan final tim)
- `Dokumen Handofff saif/AWETIN MITRA FULL BUILD + WEB RESEARCH + E2E AUDIT HANDOFF.md`
- `Dokumen Handofff saif/blom_merged (awetin).html`
- `awetin-onboarding.html` (superseded, hanya arsip)
