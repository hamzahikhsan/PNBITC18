# Konteks Proyek — Awetin (PNBITC#18, Anonymous Team)

> **Baca file ini dulu sebelum melakukan apa pun.** Dokumen ini adalah briefing hand-off dari sesi Cowork sebelumnya. Tujuannya supaya kamu (Claude Code) langsung punya konteks penuh dan **tidak perlu riset ulang, tidak perlu menganalisa ulang dari nol, dan tidak keluar dari cakupan proyek ini.** Semua riset besar sudah selesai dan didokumentasikan di file-file yang dirujuk di bawah — tugasmu melanjutkan dari sini, bukan mengulang.

---

## 0. Ringkasan dalam 1 Paragraf

Tim "Anonymous Team" sedang menyiapkan submission untuk **PNB IT Competition #18 (PNBITC#18)**, cabang lomba **Desain UI/UX**, sub-tema wajib **"Tech for Nature by Crafting Sustainable Digital Solutions"**. Konsep produk yang sudah difinalkan (setelah eksplorasi & pembandingan dengan konsep alternatif) adalah **"Awetin"** — marketplace/direktori yang mempertemukan pemilik barang rusak dengan tukang reparasi informal lokal (elektronik kecil, jahit/sol sepatu, las, dll), dengan jalur alternatif jual/donasi/daur-ulang-resmi untuk barang yang tidak ingin diperbaiki. Semua riset, PRD, dan sintesis Design Thinking sudah selesai dibuat. FigJam board tim juga sudah diisi dengan chart hasil riset. **Langkah berikutnya yang paling mungkin diminta: membangun mockup UI/UX aktual di Figma (bukan FigJam) berdasarkan PRD** — tapi konfirmasikan ke user dulu apa fokus sesi ini sebelum mulai, jangan asumsikan.

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
| ⚠️ Belum dikonfirmasi | **Daftar sub-tema resmi turunan** dari tema besar belum dikonfirmasi ke panitia — WAJIB ditanyakan tim di Technical Meeting (5 September 2026) sebelum konsep dikunci total. Ini satu-satunya hal yang bisa mengubah validitas seluruh kerangka Awetin. |

Detail lengkap juklak ada di `Context Brief - PNBITC18 UIUX Tech for Nature.md`.

---

## 2. Status Nama Produk — PENTING

Nama kerja sebelumnya **"TukangIn" sudah tidak dipakai** karena ditemukan konflik dengan produk/skripsi/aplikasi lain yang sudah ada (Google Play, skripsi Telkom University, dll — melanggar syarat orisinalitas juklak). **Nama kerja saat ini: "Awetin"** (dari kata "awet" = tahan lama). Ini **usulan sementara, belum diverifikasi resmi** (baru dicek cepat via web search, bukan penelusuran merek dagang PDKI/Google Play/App Store). Tim wajib memutuskan & memverifikasi nama final sendiri. **Jangan mengganti nama ini secara sepihak** — kalau ingin mengubah, itu keputusan tim, bukan keputusan AI.

---

## 3. Dokumen yang Berlaku (Baca Ini untuk Detail — Jangan Riset Ulang)

Semua ada di direktori ini, sudah lengkap dan saling terhubung. **Urutan baca yang disarankan kalau perlu konteks detail:**

1. **`PRD Lengkap - Awetin.md`** ⭐ — **Dokumen paling penting.** Blueprint lengkap: persona, prinsip desain, informasi arsitektur & navbar, 6 modul fitur, 12 user flow end-to-end (tanpa jalan buntu), daftar 39 layar Figma yang perlu dibuat, microcopy, kepatuhan regulasi, aksesibilitas, ruang lingkup MVP, risiko & mitigasi, **7 pertanyaan terbuka untuk tim** (lihat Bagian 14 dokumen ini).
2. **`Deep Research - Ekosistem Menyeluruh Awetin.md`** — Riset menyeluruh: lingkungan (e-waste, tekstil), masyarakat, kompetitor, regulasi (PSE, UU PDP, e-waste B3), QRIS, status hukum "mitra" gig economy, AI computer vision damage assessment, konvensi UX Gojek, aksesibilitas, tabel sintesis temuan→keputusan produk, dan temuan audit soal konflik nama.
3. **`Breakdown Lengkap Awetin - Latar Belakang, Solusi, Fitur, User Flow.md`** — Versi awal breakdown solusi (latar belakang, fitur, flow) — sudah sebagian besar tercakup ulang di PRD, tapi berguna untuk detail data mentah latar belakang.
4. **`Pendalaman Awetin - Mekanisme Harga, Jalur Non-Servis, dan Analisa Celah.md`** — Riset spesifik soal mekanisme harga (Estimasi Berjenjang) dan jalur non-servis (jual/donasi/daur ulang).
5. **`Riset Kompetitor Awetin dan Pembedahan Poin 6.md`** — Analisis kompetitor (Sejasa, Kanggo, lakuKan) yang mengonfirmasi tidak ada yang menyasar reparasi informal super-lokal dengan identitas anti-sampah.
6. **`Perbandingan Konsep - Kampung Iklim Digital vs Awetin.md`** — Alasan kenapa arah Awetin dipilih dibanding konsep alternatif "Kampung Iklim Digital".
7. **`Context Brief - PNBITC18 UIUX Tech for Nature.md`** — Ringkasan juklak resmi kompetisi.

### Dokumen historis/superseded (JANGAN dipakai sebagai rujukan aktif — hanya arsip proses berpikir sebelumnya)

- `Konsep Kampung Iklim Digital - Breakdown Lengkap.md` dan `Klarifikasi Konsep - Verifikasi, Ide Saif, dan Analogi.md` — konsep **alternatif yang TIDAK dipilih** (soal iklim/karhutla via RT/RW). Jangan campur dengan konsep Awetin.
- `Riset & Analisa - PNBITC18 Desain UIUX.md`, `Sintesis Riset - 6 Dokumen Tim PNBITC18.md`, `Riset Ideation Baru - Arah Konsep Fresh PNBITC18.md` — riset tahap eksplorasi awal sebelum konsep Awetin difinalkan. Sudah diserap ke dalam dokumen-dokumen di atas.

**Jangan menulis ulang atau meriset ulang apa yang sudah ada di dokumen-dokumen "berlaku" di atas.** Kalau user minta sesuatu yang jawabannya sudah ada di sana, rujuk/kutip dari situ dulu sebelum mengarang analisis baru.

---

## 4. Keputusan Kunci yang Sudah Final (Jangan Dipertanyakan Ulang Tanpa Alasan Baru)

- **Navbar final:** Home / Pesanan / Perbaiki (tombol tengah, menonjol) / Tukang (+ sub-section "Jual-Beli") / Profil. Ini revisi dari ide awal tim (Home/My Reparasi+Scan AI/Aktifitas/Profile) — lihat PRD Bagian 5.
- **Model harga:** "Estimasi Berjenjang" digabung dengan sistem "Anti-Tembak" dari mentor tim — Barang Besar (AI estimasi → Biaya Jasa Tetap dibayar di muka via QRIS-hold → cek fisik → invoice → persetujuan) vs Barang Kecil (AI estimasi → nego chat → antar sendiri). Lihat PRD Bagian 6.1 & 7.3–7.4.
- **Sistem reputasi tukang:** "Filter Tukang Nakal" — deteksi otomatis kalau harga tukang menyimpang dari **rata-rata LOKAL** (bukan ambang nasional flat — ini revisi dari usulan awal mentor).
- **Jalur non-servis:** Triase 3 arah — Servis / Jual-Donasi (dengan sisi pembeli di tab Tukang→Jual-Beli) / Daur Ulang Resmi (e-waste = limbah B3, wajib dropbox resmi).
- **Prinsip retensi:** "Retensi etis, bukan retensi paksa" — user boleh saja lepas dari app setelah cocok dengan 1 tukang; app hanya perlu kasih alasan organik untuk kembali (riwayat, garansi, Tukang Favorit, dampak komunitas), bukan mengunci secara artifisial. Ini jawaban resmi untuk pertanyaan disintermediasi dari Zikru.
- **MVP demo backbone:** Flow **Barang Besar** (bukan Barang Kecil) — karena lebih linear dan tidak butuh simulasi chat yang rawan terlihat "skrip" di depan juri. Lihat PRD Bagian 12.
- **Fitur "Tukang Keliling"** (ide Zikru, model ala ojol) sudah masuk ke Modul Tukang.
- **Asumsi komisi platform:** 5–10% (working assumption, belum final — perlu dikonfirmasi tim, lihat Pertanyaan Terbuka #6).

---

## 5. Status FigJam — Sudah Dikerjakan

Board tim: `https://www.figma.com/board/bU0Ymy1GpY5vdkK5EWi0A2/Anonymous-brainstorming`

Page **"Anonymous"** (node-id `67:6411`) sudah diisi penuh dengan **sintesis Design Thinking** (Empathize → Define → Ideate → Prototype → Test) berisi 45 kartu warna-kode + 4 panah penghubung fase, semua ditarik langsung dari Deep Research & PRD di atas — termasuk insight dari diskusi Discord tim (Zikru, Saif, mentor) yang sudah di-cross-reference ke keputusan produk. **Sudah diverifikasi rapi oleh user** (sempat ada bug layout Section FigJam yang tidak stabil untuk board lebar — sudah diperbaiki dengan rebuild tanpa Section node, kartu ditempel langsung ke page).

**Catatan teknis kalau lanjut edit FigJam/Figma dari sini:** kalau environment ini (Claude Code) punya akses ke Figma MCP tools (`use_figma`, dll), WAJIB load skill `figma-use` dulu sebelum panggil `use_figma` — dan untuk board FigJam lebar, **hindari membuat/mengedit banyak node secara paralel (concurrent) di page yang sama** — itu penyebab bug kemarin (Section bergeser sendiri, beberapa kartu "kabur"). Lebih aman satu panggilan sequential per kelompok konten, lalu verifikasi posisi node secara langsung (baca `x`/`y` tiap child) — jangan cuma percaya `get_screenshot`, karena tool screenshot itu sendiri sempat menampilkan render yang salah/glitch untuk board yang sangat lebar meski datanya sebenarnya benar.

**Belum dikerjakan:** mockup UI/UX aktual di **Figma design file** (bukan FigJam) — 39 layar sesuai daftar di PRD Bagian 8, frame iPhone 16 (393×852px) sesuai syarat lomba. Ini kemungkinan besar tugas berikutnya, tapi **konfirmasi dulu ke user** apa fokus sesi Claude Code ini sebelum mulai membangun apa pun.

---

## 6. Pertanyaan Terbuka untuk Tim (Belum Terjawab — Jangan Coba Jawab Sendiri)

Dari PRD Bagian 14 — ini keputusan yang harus diambil TIM, bukan diasumsikan AI:

1. Konfirmasi nama produk final (Awetin masih usulan).
2. Fitur "Jual" barang — full prototype Figma atau cukup konsep ringan saja?
3. Satu akun bisa dual-role (user + tukang) atau dipisah total? (PRD mengasumsikan dipisah untuk kesederhanaan, tapi ini keputusan tim.)
4. Kategori mana yang jadi fokus demo Figma (disarankan 1–2 dari 4: elektronik/jahit/sepatu/las)?
5. Nama/istilah final untuk fitur Scan AI, Skor Kelayakan, tab "Tukang".
6. Konfirmasi angka komisi platform (asumsi kerja: 5–10%).
7. **Paling kritis:** konfirmasi sub-tema resmi PNBITC#18 ke panitia (Technical Meeting 5 September 2026).

---

## 7. Cara Kerja yang Diharapkan dari Kamu (Claude Code)

- **Jangan mulai riset dari nol.** Kalau butuh data/fakta, cek dulu di dokumen-dokumen "berlaku" pada Bagian 3 — kemungkinan besar sudah ada di sana dengan sumbernya.
- **Jangan mengulang proses ideation/brainstorming besar yang sudah selesai** (navbar, model harga, triase, dsb) kecuali user secara eksplisit minta merevisi salah satu keputusan di Bagian 4.
- **User (Hamzah) suka advisor yang tegas dan verifikatif** — jangan langsung meng-iyakan, cek dulu faktanya, sampaikan temuan apa adanya (termasuk kalau ternyata ada yang salah/kurang), baru lanjut.
- Kalau diminta lanjut ke desain UI Figma: rujuk PRD Bagian 8 (daftar 39 layar) dan Bagian 12 (ruang lingkup MVP) sebagai acuan prioritas, jangan mendesain ulang struktur fitur dari nol.
- Kalau ada revisi konten dokumen, edit dokumen yang sudah ada (jangan bikin dokumen duplikat baru dengan nama mirip) — kecuali memang deliverable baru yang belum ada.
- Selalu **tanyakan ke user dulu** kalau scope permintaan ambigu, alih-alih menebak dan langsung mengerjakan sesuatu yang besar.
