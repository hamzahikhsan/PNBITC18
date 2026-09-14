# Konteks Proyek — Awetin (PNBITC#18, Anonymous Team)

> **Baca file ini dulu sebelum melakukan apa pun.** Dokumen ini adalah briefing hand-off dari sesi-sesi Cowork/Claude Code sebelumnya. Tujuannya supaya kamu (Claude Code) langsung punya konteks penuh dan **tidak perlu riset ulang, tidak perlu menganalisa ulang dari nol, dan tidak keluar dari cakupan proyek ini.** Semua riset besar sudah selesai dan didokumentasikan di file-file yang dirujuk di bawah — tugasmu melanjutkan dari sini, bukan mengulang. Update terakhir dokumen ini: **14 September 2026**, ditulis selengkap mungkin secara sengaja supaya bisa jadi memory penuh untuk sesi baru — jangan diringkas ulang jadi lebih pendek tanpa alasan.

---

## 0. Ringkasan dalam 1 Paragraf

Tim "Anonymous Team" sedang menyiapkan submission untuk **PNB IT Competition #18 (PNBITC#18)**, cabang lomba **Desain UI/UX**, sub-tema wajib **"Tech for Nature by Crafting Sustainable Digital Solutions"**. Konsep produk yang sudah difinalkan (setelah eksplorasi & pembandingan dengan konsep alternatif) adalah **"Awetin"** — marketplace/direktori yang mempertemukan pemilik barang rusak dengan tukang reparasi informal lokal (elektronik kecil, jahit/sol sepatu, las, dll), dengan jalur alternatif jual/donasi/daur-ulang-resmi untuk barang yang tidak ingin diperbaiki. Semua riset, PRD, dan sintesis Design Thinking sudah selesai. FigJam board tim sudah diisi lengkap. **Prototype interaktif (React/Artifact) sudah selesai 5 fase penuh.** **Mockup Figma submission sudah mulai dibangun: 16 dari 16 layar MVP wajib sudah selesai.** Deadline karya **14–16 September 2026** — sangat dekat, jadi sesi baru harus langsung produktif, bukan riset ulang.

---

## 1. Fakta Kompetisi (Jangan Diubah/Diasumsikan Ulang)

| Aspek | Detail |
|---|---|
| Event | PNB IT Competition #18 (PNBITC#18), Politeknik Negeri Bali |
| Cabang | Desain UI/UX |
| Sub-tema wajib | "Tech for Nature by Crafting Sustainable Digital Solutions" |
| Tools wajib | **Figma** (tidak ada alternatif) |
| Format karya | Desain UI/UX aplikasi **mobile**, frame iPhone 16 (393×852px) |
| Deadline karya | 14–16 September 2026, 23.59 WITA |
| Babak final | 2 Oktober 2026, offline di Politeknik Negeri Bali (presentasi 10 menit + tanya jawab 15 menit) |
| ⚠️ Perlu dicek | **Daftar sub-tema resmi turunan** dari tema besar tadinya belum dikonfirmasi ke panitia, wajib ditanyakan tim di Technical Meeting (5 September 2026). File `NOTULENSI DESAIN UIUX PNBITC#18.pdf` (masuk ke repo 14 September 2026) **kemungkinan besar berisi hasil meeting ini — baca file itu duluan di sesi baru**, belum ada sesi yang membacanya. |

Detail lengkap juklak ada di `Context Brief - PNBITC18 UIUX Tech for Nature.md` dan `PETUNJUK PELAKSANAAN DESAIN UI UX PNBITC#18.pdf`.

---

## 2. Status Nama Produk — PENTING

Nama kerja sebelumnya **"TukangIn" sudah tidak dipakai** karena ditemukan konflik dengan produk/skripsi/aplikasi lain yang sudah ada (Google Play, skripsi Telkom University, dll — melanggar syarat orisinalitas juklak). **Nama kerja saat ini: "Awetin"** (dari kata "awet" = tahan lama). Ini **usulan sementara, belum diverifikasi resmi** (baru dicek cepat via web search, bukan penelusuran merek dagang PDKI/Google Play/App Store). Tim wajib memutuskan & memverifikasi nama final sendiri. **Jangan mengganti nama ini secara sepihak** — kalau ingin mengubah, itu keputusan tim, bukan keputusan AI.

---

## 3. Dokumen yang Berlaku (Baca Ini untuk Detail — Jangan Riset Ulang)

Semua ada di direktori ini, sudah lengkap dan saling terhubung. **Urutan baca yang disarankan kalau perlu konteks detail:**

1. **`PRD Lengkap - Awetin.md`** ⭐ — **Dokumen paling penting.** Blueprint lengkap: persona, prinsip desain, informasi arsitektur & navbar (Bagian 5), 6 modul fitur (Bagian 6), 12 user flow end-to-end tanpa jalan buntu (Bagian 7), daftar 39 layar Figma (Bagian 8), microcopy (Bagian 9), kepatuhan regulasi (Bagian 10), aksesibilitas (Bagian 11), ruang lingkup MVP (Bagian 12), risiko & mitigasi (Bagian 13), **7 pertanyaan terbuka untuk tim** (Bagian 14).
2. **`Deep Research - Ekosistem Menyeluruh Awetin.md`** — Riset menyeluruh: lingkungan (e-waste, tekstil), masyarakat, kompetitor, regulasi (PSE, UU PDP, e-waste B3), QRIS, status hukum "mitra" gig economy, AI computer vision damage assessment, konvensi UX Gojek, aksesibilitas, tabel sintesis temuan→keputusan produk, dan temuan audit soal konflik nama.
3. **`Breakdown Lengkap Awetin - Latar Belakang, Solusi, Fitur, User Flow.md`** — Versi awal breakdown solusi — sudah sebagian besar tercakup ulang di PRD, berguna untuk detail data mentah latar belakang.
4. **`Pendalaman Awetin - Mekanisme Harga, Jalur Non-Servis, dan Analisa Celah.md`** — Riset spesifik soal mekanisme harga (Estimasi Berjenjang) dan jalur non-servis (jual/donasi/daur ulang).
5. **`Riset Kompetitor Awetin dan Pembedahan Poin 6.md`** — Analisis kompetitor (Sejasa, Kanggo, lakuKan) yang mengonfirmasi tidak ada yang menyasar reparasi informal super-lokal dengan identitas anti-sampah.
6. **`Perbandingan Konsep - Kampung Iklim Digital vs Awetin.md`** — Alasan kenapa arah Awetin dipilih dibanding konsep alternatif "Kampung Iklim Digital".
7. **`Context Brief - PNBITC18 UIUX Tech for Nature.md`** — Ringkasan juklak resmi kompetisi.
8. **`Audit - Kesesuaian Handoff Saif vs PRD.md`** — Audit lengkap temuan penyimpangan handoff Saif vs PRD, lihat Bagian 5.1 dokumen ini untuk ringkasannya.
9. **`Design System/DESIGN-awetin.md`** — Design system tunggal (warna 3-lapis, tipografi, spacing, komponen, dark mode, aksesibilitas) — sumber token untuk prototype HTML **dan** file Figma.
10. **`Rencana Regenerasi Prototype Awetin.md`** — Laporan lengkap regenerasi prototype interaktif, lihat Bagian 5.2 dokumen ini untuk ringkasannya.

### Dokumen historis/superseded (JANGAN dipakai sebagai rujukan aktif — hanya arsip proses berpikir sebelumnya)

- Semua file berjudul mengandung **"TukangIn"** — duplikat lama dari dokumen Awetin sebelum ganti nama konsep. Jangan dipakai.
- `Konsep Kampung Iklim Digital - Breakdown Lengkap.md` dan `Klarifikasi Konsep - Verifikasi, Ide Saif, dan Analogi.md` — konsep **alternatif yang TIDAK dipilih** (soal iklim/karhutla via RT/RW). Jangan campur dengan konsep Awetin.
- `Riset & Analisa - PNBITC18 Desain UIUX.md`, `Sintesis Riset - 6 Dokumen Tim PNBITC18.md`, `Riset Ideation Baru - Arah Konsep Fresh PNBITC18.md`, `Kompilasi_Riset_Lengkap_PNBITC18_UIUX_Tech_for_Nature.md`, `Prediksi_Lanskap_Konsep_Kompetitor_PNBITC18.md`, `Riset_Pola_Habit_Forming_Aplikasi_Lingkungan.md`, `Riset_Psikologi_Perilaku_Perubahan_Iklim.md`, `Strategi_Mengatasi_Dragon_Limited_Cognition.md`, `UIUX_Competition_Environmental_Solution_Ideas.md`, `ok dari semua hasil riset dan tesis kamu ini dari.md` — riset tahap eksplorasi awal sebelum konsep Awetin difinalkan, sudah diserap ke dokumen-dokumen di atas.
- `Dokumen Handofff saif/awetin-onboarding.html` (kalau masih ada) — dikonfirmasi superseded oleh `blom_merged (awetin).html`, cuma 1005 baris dan berhenti di Home + StubScreen.

**Jangan menulis ulang atau meriset ulang apa yang sudah ada di dokumen-dokumen "berlaku" di atas.** Kalau user minta sesuatu yang jawabannya sudah ada di sana, rujuk/kutip dari situ dulu sebelum mengarang analisis baru.

---

## 4. Keputusan Kunci yang Sudah Final (Jangan Dipertanyakan Ulang Tanpa Alasan Baru)

- **Navbar user final:** Home / Pesanan / Perbaiki (tombol tengah FAB, menonjol) / Tukang (+ sub-section "Jual-Beli") / Profil — **5 tab**. Ini revisi dari ide awal tim (Home/My Reparasi+Scan AI/Aktifitas/Profile) — lihat PRD Bagian 5.2.
- **Navbar tukang final:** Pesanan Masuk (tab utama, home-like) / Profil Usaha / Pendapatan / Notifikasi — **4 tab**, BUKAN 5. PRD sengaja jadikan "Pesanan Masuk" sebagai tab utama supaya navbar tetap sederhana untuk Persona B (literasi digital terbatas). ⚠️ Spec handoff Saif pernah diam-diam mengubah ini jadi 5 tab (nambah "Beranda") — itu **bukan keputusan tim**, lihat Bagian 5.1.
- **Model harga:** "Estimasi Berjenjang" digabung dengan sistem "Anti-Tembak" dari mentor tim — Barang Besar (AI estimasi → Biaya Jasa Tetap dibayar di muka via QRIS-hold → cek fisik → invoice → persetujuan) vs Barang Kecil (AI estimasi → nego chat → antar sendiri). Lihat PRD Bagian 6.1 & 7.3–7.4.
- **Sistem reputasi tukang:** "Filter Tukang Nakal" — deteksi otomatis kalau harga tukang menyimpang dari **rata-rata LOKAL** (bukan ambang nasional flat — ini revisi dari usulan awal mentor).
- **Jalur non-servis:** Triase 3 arah — Servis / Jual-Donasi (dengan sisi pembeli di tab Tukang→Jual-Beli) / Daur Ulang Resmi (e-waste = limbah B3, wajib dropbox resmi).
- **Prinsip retensi:** "Retensi etis, bukan retensi paksa" — user boleh saja lepas dari app setelah cocok dengan 1 tukang; app hanya perlu kasih alasan organik untuk kembali (riwayat, garansi, Tukang Favorit, dampak komunitas), bukan mengunci secara artifisial. Ini jawaban resmi untuk pertanyaan disintermediasi dari Zikru.
- **MVP demo backbone:** Flow **Barang Besar** (bukan Barang Kecil) — karena lebih linear dan tidak butuh simulasi chat yang rawan terlihat "skrip" di depan juri. Lihat PRD Bagian 12.
- **Guest browsing:** Boleh jelajah tanpa akun (Flow 7.1) — gerbang login baru muncul di titik komitmen transaksi nyata (booking, chat, flow Barang Besar, form jual-beli, klaim garansi), bukan dipaksa di awal.
- **Fitur "Tukang Keliling"** (ide Zikru, model ala ojol) sudah masuk ke Modul Tukang.
- **Asumsi komisi platform:** 5–10% (working assumption, belum final — perlu dikonfirmasi tim, lihat Pertanyaan Terbuka #6).
- **Arsitektur user vs tukang (⚠️ masih pertanyaan terbuka #3, JANGAN dianggap final):** PRD berasumsi "dua mode dalam satu konsep app, dipilih di layar Onboarding awal" (bukan toggle di satu akun, bukan juga dua aplikasi terpisah total) — tapi ini eksplisit belum diputuskan tim. Spec handoff Saif pernah menjawabnya sepihak jadi "dua aplikasi terpisah total" — itu juga bukan keputusan tim yang sah, lihat Bagian 5.1.

---

## 5. Status Pengerjaan per Area — DETAIL LENGKAP

### 5.1 Audit Handoff Saif vs PRD — Selesai (`Audit - Kesesuaian Handoff Saif vs PRD.md`, 6 Sept 2026)

Membandingkan spec `Dokumen Handofff saif/AWETIN MITRA FULL BUILD + WEB RESEARCH + E2E AUDIT HANDOFF.md` (48 section) dan build `Dokumen Handofff saif/blom_merged (awetin).html` (3080 baris/27 layar) terhadap PRD dan keputusan final tim.

**Temuan paling kritis:** Spec berjudul/berisi permintaan membangun **"Awetin Mitra"** (sisi tukang), tapi file HTML yang dibundel di folder yang sama ternyata isinya **sisi konsumen (Awetin)** — file itu sendiri bilang eksplisit (baris 333) "Awetin Mitra adalah aplikasi terpisah... Aplikasi ini (Awetin) khusus untuk mencari jasa." Nol dari 14 komponen reusable yang diminta spec untuk sisi Mitra ditemukan di file itu. **Kesimpulan lama: Awetin Mitra = 0% dibangun, cuma ada spec tertulis.** ⚠️ **Update terbaru:** ada file baru `Dokumen Handofff saif/Saif Baru/awetin_mitra.html` (masuk 12 Sept 2026) yang kemungkinan besar ini jawabannya — **belum diaudit sama sekali**, cek dulu isinya sebelum asumsi Mitra masih 0%.

**Kategori A (sesuai PRD, sebagian copy verbatim):** Onboarding Usaha 8-step, segmentasi Barang Besar/Kecil, invoice wajib disetujui sebelum kerja, terima/tolak pesanan + reroute ke tukang lain, payment QRIS/tunai cuma untuk Barang Besar, copy alert reputasi disalin persis dari PRD Bagian 9, reputasi dari rata-rata lokal, Profil Usaha, rincian pendapatan dgn komisi, prinsip aksesibilitas umum, Persona B.

**Kategori B (elaborasi masuk akal, TAPI tidak berdasar riset PRD — jangan diklaim ke juri sebagai "hasil riset"):** Auth OTP-only + flow Pemulihan Akun, Kode Verifikasi 4-digit wajib sebelum Cek Fisik, Live Tracking Map, rating dua arah (tukang menilai pelanggan), fitur Tip terpisah dari komisi, pembatalan tukang memicu alert reputasi, onboarding "Ditolak" dengan CTA perbaikan, App Lock/PIN, halaman legal statis, reschedule pesanan umum.

**Kategori C 🚩 (bertentangan dengan keputusan final tim, tanpa disebut sebagai revisi sadar):**
1. Navbar tukang 4 tab (final PRD 5.3) diam-diam diubah spec jadi 5 tab (nambah "Beranda").
2. "Dua mode dalam satu konsep app" (PRD, belum final) diam-diam dijawab spec sebagai "dua aplikasi terpisah total" — ini menjawab sepihak salah satu dari 7 Pertanyaan Terbuka PRD yang CLAUDE.md eksplisit larang diasumsikan.

**Kategori D — 4 layar wajib PRD yang hilang dari build `blom_merged`:** #20 Form Klaim Garansi, #24 Direktori Partner Donasi, #25 Direktori Dropbox Daur Ulang Resmi, #26 Riwayat Penyaluran Non-Servis. **✅ Semua 4 ini sudah dibangun ulang** saat regenerasi prototype Fase 3 (lihat 5.2 di bawah).

**Rekomendasi yang masih menunggu keputusan tim:** konfirmasi arsitektur 1-app-2-mode vs 2-app-terpisah (menentukan apakah Figma perlu 2×39 layar atau 1 app + percabangan mode), konfirmasi navbar tukang 4 vs 5 tab, putuskan fitur Kategori B mana yang dipakai (framing sebagai "keputusan desain praktis", bukan "hasil riset").

### 5.2 Prototype Interaktif React/Artifact — SELESAI 5 Fase (`Rencana Regenerasi Prototype Awetin.md`, selesai 9 Sept, update 11 Sept 2026)

File: `Prototype/awetin-prototype.html` — single-file React 18 (UMD, cdnjs) + Babel Standalone (JSX in-browser) + Tailwind CDN. Fork dari `Dokumen Handofff saif/blom_merged (awetin).html`. **Bukan pengganti submission Figma** — murni alat validasi flow & demo internal. Live URL Artifact: `https://claude.ai/code/artifact/6c1004e4-4a99-45dd-a5f8-f24ebbf3c172` (mungkin sudah expired/butuh re-publish di sesi baru — cek dulu).

**Fase 1 (Fondasi):** CDN unpkg→cdnjs (React 18.3.1, ReactDOM 18.3.1, Babel Standalone 7.29.8, semua di-pin). Hapus tag `<!DOCTYPE>/<html>/<head>/<body>` (syarat Artifact). Token Tailwind Saif dipertahankan+diperluas.

**Fase 2 (Navigasi & Kategori):** Bottom nav user diaudit — sudah sesuai PRD 5.2, tidak perlu perbaikan. Warna kategori disatukan ke satu `CATEGORY_STYLE` constant (sebelumnya 3 definisi ad-hoc beda-beda, Elektronik sempat pakai hijau primary yang sama dgn CTA — ambigu, sudah dipisah).

**Fase 3 (Gap Flow, paling besar):** Temuan kritis baru: ScanAI cuma py 1 skenario ter-script (Kulkas) yang salah rute ke chat Barang Kecil, padahal kulkas = Barang Besar (PRD Flow 7.2). **Diperbaiki total:** Triase 3-arah ditambahkan ke `ScanAIScreen`, dan seluruh **flow Barang Besar dibangun dari nol** (MVP backbone wajib PRD Bagian 12, sebelumnya 0%): `PilihTukangBesarScreen` → `MJadwalBiayaStep` (jadwal+Biaya Jasa Tetap QRIS) → `MMenujuLokasiStep` → `MVerifikasiKodeStep` (gate 4-digit wajib) → `MCekFisikStep` → `MInvoiceStep` (Setuju/Tolak, konsekuensi Biaya Jasa Tetap tetap milik tukang kalau ditolak) → `MMengerjakanStep` → `MBeforeAfterStep`, semua diorkestrasi `BarangBesarFlow` (state machine `step`). 4 gap kecil dari Audit 5.1 juga ditutup: Klaim Garansi, Jual atau Donasi (pilihan eksplisit), Direktori Partner Donasi, Direktori Daur Ulang Resmi (B3 vs bank sampah), Riwayat Penyaluran Non-Servis.

**Fase 4 (Dark Mode & Aksesibilitas):** 572+ class Tailwind raw hex disatukan ke token semantik di seluruh file (3 script Node.js sekali-pakai, sudah dihapus). Token warna jadi CSS variable dengan pola 3-state resmi Artifact (`:root` light → `@media(prefers-color-scheme:dark):not([data-theme="light"])` → `:root[data-theme="dark"]`). Toggle Mode Gelap sungguhan di Profil→Aksesibilitas, tersimpan `localStorage`, independen dari tema browser. `aria-label` ditambahkan ke tombol ikon-saja kritis. **Keterbatasan yang diakui terbuka:** icon `color="#HEX"` literal JS tidak ikut re-theme otomatis (tetap terbaca, kontras berkurang); beberapa warna dekoratif satu-off sengaja tidak disentuh (ScanAI memang gelap by design); hue kategori default sengaja sama di kedua tema.

**Fase 5 (QA E2E):** `claude-in-chrome` terputus sepanjang sesi Fase 3-5, gagal disambung ulang. Playwright dicoba dan **terbukti tidak valid** (browser baru tanpa sesi login, artifact private mental ke halaman login). QA dilakukan dengan **membaca kode baris-per-baris**, divalidasi `@babel/core` (compiler JSX sungguhan) di tiap checkpoint — bukan klik-klik interaktif.

**Post-Fase-5 (gap login-skip, commit "Update status: gap login-skip sudah ditutup"):** Cross-check ke FigJam yang sudah dikoreksi (lihat 5.3) menemukan prototype maksa login di depan, padahal PRD Flow 7.1 bolehkan jelajah tanpa akun. **Diperbaiki:** `OBWelcomeScreen` dapat link "Jelajahi Dulu, Nanti Saja", `OnboardingFlow`/`App` dapat jalur `onBrowseGuest`/`isGuest` langsung ke `AppShell` mode tamu, `AppShell` dapat `requireAuth()` guard + `GUARDED_ROUTES` (`booking`,`chat`,`barang_besar_flow`,`jual_beli_form`,`klaim_garansi`) yang munculkan login-gate bottom sheet kalau tamu coba aksi transaksi nyata.

**Verdict Requirement Matrix: PASS dengan catatan.** Semua flow & logika lengkap, tervalidasi statis tanpa bug ditemukan. **Yang belum:** dark mode belum 100% (partial, lihat keterbatasan di atas), kontras warna belum diukur alat sungguhan, draft ScanAI belum auto-save saat "Belum Yakin", dan **verifikasi visual live click-through browser sungguhan BELUM PERNAH dilakukan** — ini satu-satunya langkah wajib terakhir sebelum prototype dipakai demo ke juri/tim.

### 5.3 FigJam Boards — 3 board berbeda, jangan tertukar

**a) Board brainstorming** `https://www.figma.com/board/bU0Ymy1GpY5vdkK5EWi0A2/Anonymous-brainstorming`, page "Anonymous" (`67:6411`) — 45 kartu sintesis Design Thinking + 4 panah fase, sudah diverifikasi user. Bug lama Section-drift di board lebar sudah diperbaiki (rebuild tanpa Section node).

**b) Board "AWETIN — User Flow Lengkap"** (fileKey `BjvULfjvYprFQQOi8Z1x8V`) — dibaca penuh (75 shape+92 connector), **DIMODIFIKASI tapi originalnya TIDAK PERNAH disentuh** sesuai instruksi eksplisit user ("jangan merubah flow chart yang ada, tapi coba kamu duplikat dan modifikasi"). Cara: seluruh flowchart di-clone offset +6000 x-axis (idMap 75 shape lama→baru, 92 connector direkonstruksi ulang), lalu HANYA klonanya yang diedit: (1) branch Jual/Donasi Triase yang tadinya terpisah digabung jadi satu diamond baru "Pilih: Jual atau Donasi?" (`6:854`, connector `6:858/862/866/870`), (2) node Klaim Garansi diperluas jadi flow form→notify→confirm (`7:854` klaimForm → `7:858` notifTukang → `7:862` confirmDiamond → `7:866` ditinjau, connector `7:870-886`), (3) header text `7:890`. Original (`1:54`,`1:60`,`1:63`,`1:222`,`1:225`) diverifikasi tetap utuh setelah edit. Koreksi ini dibuat karena kode prototype (5.2) sudah lebih benar duluan — FigJam yang dikejar menyamai kode, bukan sebaliknya.

**c) Board "AWETIN — Tukang/Partner Flow"** (fileKey `76WpgPl0l4xCFQSMT3YJK8`) — dibaca, sudah sesuai PRD Flow 7.9-7.11 dengan baik, **tidak ada perubahan dibuat**.

**Catatan teknis FigJam:** WAJIB load skill `figma-use` sebelum `use_figma`. Untuk board lebar, hindari edit banyak node paralel di page yang sama (penyebab bug drift lama). Satu panggilan sequential per kelompok konten, verifikasi posisi node lewat `x`/`y` langsung, jangan cuma percaya `get_screenshot` (bisa glitch di board sangat lebar meski data sebenarnya benar).

### 5.4 Figma Design File (Submission) — 16/16 Layar MVP SELESAI

File terpisah dari FigJam, khusus mockup UI: **"Awetin - UI Design"**, fileKey `uamDapxiZkJMGkPZ1INLfE`, https://www.figma.com/design/uamDapxiZkJMGkPZ1INLfE, dibuat di bawah team plan `team::1397404814006645490` ("hamzah .student's team").

**Page "00 — Components" (`3:2`):**
- Variable Collection `VariableCollectionId:1:2` "Awetin Colors" mode "Light" (`1:0`), 34 color variable `VariableID:1:3` s.d. `1:36` (primary/default,hover,pressed,disabled,container,on-primary,on-container → secondary/default,container → neutral/background,surface,surface-variant,border,divider → text/primary,secondary,tertiary,disabled → status/success,warning,error,information (+container masing²) → category/elektronik,jahit,sepatu,las (+container masing²)).
- 12 Text Style `Awetin/Display` s.d. `Awetin/Caption`, font "Plus Jakarta Sans".
- Component set `Button` (frame `3:7`): variant `3:3` Primary, `3:5` Secondary. **Text property key = `Label#3:2`** (bukan cuma `"Label"` — pakai key pendek gagal diam-diam).
- Frame `BottomNav` (`13:7`, 393×88) — BUKAN component/instance sungguhan, sengaja cuma plain frame yang di-`.clone()` per layar biar tab aktif gampang diedit manual. Baru dipakai di 1 layar (Home).

**Page "01 — MVP Backbone (Sisi Pengguna)" (`0:1`) — 16/16 layar prioritas PRD Bagian 12, semua sudah dibangun & divalidasi screenshot satu-per-satu:**

| # | Frame ID | Nama | Sumber konten |
|---|---|---|---|
| 1 | `4:5` | Splash & Onboarding | `OBWelcomeScreen` |
| 2 | `9:3` | Onboarding Pilih Peran | `OBInterstitialRoleScreen` |
| 3 | `11:5` | Login Nomor HP | `OBPhoneEntryScreen` + keypad custom |
| 4 | `12:6` | Izin Lokasi (GPS) | `OBLocationPermissionScreen` + link alamat manual (baru, sesuai gap audit PRD) |
| 5 | `14:7` | Home | `HomeScreen`, pakai `BottomNav` clone |
| 6 | `19:17` | Scan AI (Deteksi) | `ScanAIScreen` fase recording, AR box + HUD kritis |
| 7 | `24:7` | Hasil Deteksi & Triase | `ScanAIScreen` result sheet — gabung PRD #6+#7+#8 jadi 1 layar |
| 8 | `29:7` | Direktori Tukang | `PilihTukangBesarScreen` + `ScanWorkerCard` |
| 9 | `31:7` | Detail Profil Tukang | `WorkerDetailScreen` |
| 10 | `35:8` | Konfirmasi Jadwal & Biaya | `MJadwalBiayaStep` |
| 11 | `36:9` | Invoice & Persetujuan | `MInvoiceStep` |
| 12 | `37:11` | Status Pesanan Aktif | `OrderDetailScreen` (stepper) |
| 13 | `38:11` | Pembayaran QRIS | didesain baru (pola QR pseudo-random, bukan kode asli scannable) |
| 14 | `39:12` | Upload Bukti & Rating | `MBeforeAfterStep` + form ulasan `OrderDetailScreen` |
| 15 | `40:13` | Dashboard Dampak Komunitas | `DampakDashboardScreen` |
| 16 | `45:13` | Onboarding Tukang (Pilih Kategori) | **didesain baru**, belum ada padanan di prototype — 1 contoh sisi mitra sesuai PRD Bagian 12 |

**Belum dibangun (PRD Bagian 12 sebut "nice-to-have", boleh cukup dijelaskan konsepnya di presentasi):** layar Jual-Beli (listing/direktori/detail), Direktori Partner Donasi, Direktori Dropbox Daur Ulang, Riwayat Penyaluran Non-Servis, Tukang Favorit, Profil & Pengaturan, dan sisi dashboard Tukang lengkap (consent, verifikasi, pesanan masuk, pendapatan, notifikasi reputasi) di luar 1 contoh onboarding yang sudah ada.

**Catatan teknis PENTING kalau lanjut isi Figma via `use_figma` (bug paling sering muncul sepanjang build 16 layar ini, hampir semua tanpa error, cuma kepotong diam-diam di screenshot):**
1. Frame auto-layout yang jadi child di parent auto-layout: WAJIB set `layoutSizingHorizontal` **dan** `layoutSizingVertical` ke `'HUG'` (kalau memang mau hug) setelah `appendChild()` — cuma set satu sisi, sisi lainnya diam-diam nyangkut FIXED di ukuran default 100×100 dan bikin teks/badge kepotong.
2. Frame yang PUNYA layout sendiri (HORIZONTAL/VERTICAL): `primaryAxisSizingMode` (axis utama) dan `counterAxisSizingMode` (axis silang) itu independen — set `layoutSizingHorizontal:'FILL'` di parent HORIZONTAL cuma benerin `primaryAxisSizingMode` (jadi FIXED-mengikuti-lebar-parent), tapi `counterAxisSizingMode` (tinggi) tetap nyangkut default kalau tidak di-set terpisah ke `'AUTO'`.
3. Kalau parent-nya `layoutMode:'NONE'` (posisi bebas/absolute, dipakai di layar Scan AI yang sinematik), child SAMA SEKALI tidak dapat bantuan dari `layoutSizingHorizontal/Vertical` — `primaryAxisSizingMode`/`counterAxisSizingMode` harus di-set eksplisit sendiri.
4. `layoutPositioning='ABSOLUTE'` cuma valid **setelah** `appendChild()` ke parent auto-layout — kalau di-set sebelum append, error "parent node has layoutMode !== NONE" karena parent-nya masih page/canvas root.
5. `layoutGrow` harus integer, tidak bisa pecahan — untuk progress bar proporsional, hitung lebar pixel literal (`Math.round(trackWidth * pct/100)`) di rectangle biasa di dalam frame track `layoutMode:'NONE'`, jangan pakai `layoutGrow = pct/100`.
6. `layoutWrap:'WRAP'` cuma jalan kalau frame punya lebar FILL/FIXED (ada batas buat di-wrap) — di frame HUG, WRAP tidak ngefek.
7. Panggilan `use_figma` yang error **rollback penuh secara atomik** — tidak ada node setengah jadi tersisa, aman untuk retry setelah fix.
8. Selalu screenshot tiap section (`get_screenshot` → `curl -sL -o <path>` link hasil ke scratchpad → `Read` file lokal) sebelum lanjut ke section berikutnya — ini yang paling cepat nemuin bug di atas.

---

## 6. Pertanyaan Terbuka untuk Tim (Belum Terjawab — Jangan Coba Jawab Sendiri)

Dari PRD Bagian 14 — ini keputusan yang harus diambil TIM, bukan diasumsikan AI. **Cek `NOTULENSI DESAIN UIUX PNBITC#18.pdf` dulu di sesi baru — kemungkinan besar sebagian sudah terjawab di situ.**

1. Konfirmasi nama produk final (Awetin masih usulan).
2. Fitur "Jual" barang — full prototype Figma atau cukup konsep ringan saja?
3. Satu akun bisa dual-role (user + tukang) atau dipisah total? (PRD mengasumsikan "1 app 2 mode", tapi ini keputusan tim — lihat juga kontradiksi di Bagian 5.1.)
4. Kategori mana yang jadi fokus demo Figma (disarankan 1–2 dari 4: elektronik/jahit/sepatu/las)?
5. Nama/istilah final untuk fitur Scan AI, Skor Kelayakan, tab "Tukang".
6. Konfirmasi angka komisi platform (asumsi kerja: 5–10%).
7. **Paling kritis:** konfirmasi sub-tema resmi PNBITC#18 ke panitia (Technical Meeting 5 September 2026).

---

## 7. File Baru yang Belum Dianalisis Sesi Manapun (per 14 September 2026)

- **`NOTULENSI DESAIN UIUX PNBITC#18.pdf`** (masuk 14 Sept) — kemungkinan notulen meeting tim, mungkin termasuk hasil Technical Meeting 5 Sept yang jawab Pertanyaan Terbuka #7. **Baca ini duluan di sesi baru.**
- **`Dokumen Handofff saif/Saif Baru/awetin.html`** dan **`awetin_mitra.html`** (masuk 12 Sept) — build baru dari Saif, kemungkinan `awetin_mitra.html` ini jawaban atas temuan "Awetin Mitra 0% dibangun" di Bagian 5.1. **Belum diaudit sama sekali** — jalankan metodologi audit yang sama (kategori A/B/C/D vs PRD) kalau ada waktu.
- **`Dokumen Handofff saif/blom_merged (mitra).html`** (masuk ~9 Sept) — belum dianalisis, mungkin versi lain/duplikat dari file di atas, diff dulu sebelum asumsi mana yang otoritatif.
- **`Screenshot 2026-09-09 212748.png`** — untracked, tujuan tidak diketahui, prioritas rendah.

**Prioritas kerja berikutnya yang disarankan (deadline karya 14-16 Sept sudah sangat dekat):**
1. Baca NOTULENSI pdf dulu — bisa mengubah scope/keputusan di bawahnya.
2. Putuskan nasib build Mitra baru dari Saif — audit, dan/atau pakai sebagai basis bikin sisa layar Figma sisi tukang (baru ada 1 dari ~10 layar tukang).
3. Kalau waktu memungkinkan, lanjut layar "nice-to-have" Figma yang belum dibangun (lihat daftar Bagian 5.4).
4. **Kemungkinan besar lebih bernilai daripada nambah scope:** lakukan verifikasi klik-klik manual sungguhan di prototype (Bagian 5.2, belum pernah dilakukan) dan/atau QA visual ulang ke-16 layar Figma yang sudah ada, karena deadline sudah dekat.

---

## 8. Cara Kerja yang Diharapkan dari Kamu (Claude Code)

- **Jangan mulai riset dari nol.** Kalau butuh data/fakta, cek dulu di dokumen-dokumen "berlaku" pada Bagian 3 — kemungkinan besar sudah ada di sana dengan sumbernya.
- **Jangan mengulang proses ideation/brainstorming besar yang sudah selesai** (navbar, model harga, triase, dsb) kecuali user secara eksplisit minta merevisi salah satu keputusan di Bagian 4.
- **User (Hamzah) suka advisor yang tegas dan verifikatif** — jangan langsung meng-iyakan, cek dulu faktanya, sampaikan temuan apa adanya (termasuk kalau ternyata ada yang salah/kurang), baru lanjut. Dia menulis santai/informal (campur Indonesia-Inggris) — balas dengan gaya serupa, bukan kaku formal.
- Kalau diminta lanjut ke desain UI Figma: rujuk PRD Bagian 8 (daftar 39 layar) dan Bagian 12 (ruang lingkup MVP) sebagai acuan prioritas, jangan mendesain ulang struktur fitur dari nol — pakai konten dari `Prototype/awetin-prototype.html` yang sudah divalidasi (Bagian 5.2) sebagai rujukan, bukan mengarang ulang.
- Untuk edit FigJam/flowchart: kalau user minta "duplikat dan modifikasi, jangan ubah yang asli" — ikuti persis, dan verifikasi node aslinya tetap utuh setelah selesai (lihat pola di Bagian 5.3).
- Kalau ada revisi konten dokumen, edit dokumen yang sudah ada (jangan bikin dokumen duplikat baru dengan nama mirip) — kecuali memang deliverable baru yang belum ada.
- Selalu **tanyakan ke user dulu** kalau scope permintaan ambigu, alih-alih menebak dan langsung mengerjakan sesuatu yang besar — tapi begitu scope dikonfirmasi (misal "lanjutin ke fase berikutnya"), lanjutkan otonom tanpa berhenti minta izin di tiap sub-langkah kecil.
- Git commit multi-baris dengan karakter spesial (kurung, dsb.) bisa gagal diam-diam lewat `-m` inline — selalu tulis ke file temp dan `git commit -F <file>`.
- `claude-in-chrome` browser tool berulang kali putus koneksi/drift koordinat di environment ini lintas sesi — jangan terlalu yakin bisa verifikasi visual live, dan Playwright BUKAN pengganti valid (browser baru tanpa login, Artifact private mental ke halaman login).

---

## 9. Memory Tambahan (Claude Code Memory Files)

Selain dokumen ini, ada memory files personal Claude Code (bukan bagian repo, tidak di-commit) di `C:\Users\User\.claude\projects\D--Anonimous-Team---PNBITC\memory\` yang menyimpan detail teknis yang sama plus catatan gaya kerja user — kalau harness memuat memory itu otomatis di awal sesi, anggap sebagai pelengkap dokumen ini, bukan pengganti. Isinya: identitas proyek, riwayat lengkap prototype 5-fase, audit Saif, FigJam boards, detail teknis file Figma (termasuk seluruh bug auto-layout sizing di atas), gaya kerja Hamzah, dan daftar file baru yang belum dianalisis.
