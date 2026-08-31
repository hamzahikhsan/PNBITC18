# Deep Research: Ekosistem Menyeluruh TukangIn
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Disusun:** 31 Agustus 2026
**Konteks:** Konsolidasi seluruh riset sesi ini (lingkungan, masyarakat, kompetitor, model bisnis, regulasi, teknologi, UX) menjadi satu dokumen referensi tunggal — dasar penyusunan PRD lengkap TukangIn

---

## Ringkasan Eksekutif

Dokumen ini menggabungkan seluruh riset yang sudah dilakukan sepanjang proses (mulai dari breakdown juklak, riset ideation awal, hingga pendalaman TukangIn) ditambah lima area baru yang sebelumnya belum tersentuh: teknologi AI untuk deteksi kerusakan barang, regulasi platform digital Indonesia (PSE & UU PDP), standar pembayaran digital (QRIS), status hukum mitra/tukang sebagai pekerja gig economy, dan konvensi UX aplikasi super-app Indonesia. Tujuannya satu: memastikan tidak ada aspek dari lingkup tema "Tech for Nature by Crafting Sustainable Digital Solutions" — baik dari sisi lingkungan, sosial, bisnis, teknologi, maupun regulasi — yang luput sebelum tim menyusun blueprint produk (PRD) final.

Temuan paling penting dari babak riset baru ini: TukangIn punya kewajiban kepatuhan yang lebih luas dari sekadar "desain bagus" — status tukang sebagai "mitra" (bukan karyawan) punya kekosongan hukum nyata di Indonesia yang perlu disikapi jujur dalam narasi produk; data KTP yang dikumpulkan untuk verifikasi tukang termasuk data pribadi yang dilindungi UU PDP dengan sanksi pidana kalau disalahgunakan; dan platform digital pada umumnya wajib terdaftar PSE di Kominfo. Ini semua bukan detail teknis yang bisa diabaikan karena "cuma prototype lomba" — justru sebaliknya, kemampuan tim menunjukkan kesadaran atas kewajiban-kewajiban ini adalah bukti nyata "kedalaman logika" yang dicari tema besar kompetisi ("Beyond the Prompt: Build the Logic, Own the Fundamental").

---

## Bagian 1 — Konteks Kompetisi (Ringkasan Wajib Diingat)

PNBITC#18 cabang Desain UI/UX menilai berdasarkan struktur bobot: Penyisihan (UX & Accessibility 30%, Interface & Design 30%, Kreativitas & Inovasi 25%, Kesesuaian tema 15%) dan Final (Tanya jawab 60%, Presentasi 40%), dengan Nilai Akhir Final berbobot 60% dari total. Implikasinya konsisten di seluruh dokumen sesi ini: **kemampuan menjelaskan alasan di balik keputusan desain lebih menentukan daripada kecantikan visual semata.** Tema besar event ("Beyond the Prompt: Build the Logic, Own the Fundamental") tidak secara literal mewajibkan fitur AI dalam produk — tapi menuntut tim mampu mengartikulasikan *reasoning* di balik setiap keputusan, termasuk kalau memilih menyertakan fitur AI (seperti "Scan AI" yang diusulkan tim), tim harus siap menjelaskan cara kerjanya, keterbatasannya, dan kenapa itu pilihan yang tepat — bukan sekadar tempelan kata "AI" karena terdengar canggih.

---

## Bagian 2 — Lingkungan: Krisis Sampah yang Terus Tumbuh (Ringkasan dari Riset Sebelumnya)

Indonesia menghasilkan **1,9–2 juta ton limbah elektronik per tahun** (terbesar di Asia Tenggara, hanya 17,4% tertangani layak) dan **2,3 juta ton limbah tekstil per tahun** (hanya 13% didaur ulang). Geografis e-waste terkonsentrasi di Jawa (56%) dan Sumatra (22%). Perilaku konsumen mendukung tren ini: 66% orang dewasa Indonesia membuang minimal satu pakaian setahun, 30% pernah membuang pakaian setelah sekali pakai. *(Detail lengkap ada di dokumen "Breakdown Lengkap TukangIn - Latar Belakang, Solusi, Fitur, User Flow.md", Bagian 1.1.)*

---

## Bagian 3 — Masyarakat: Kesenjangan Sikap-Perilaku & Ekonomi Reparasi Informal (Ringkasan)

Survei Katadata Insight Center menunjukkan 62,9% masyarakat Indonesia pernah membeli produk ramah lingkungan, dengan hambatan utama bukan ketidakpedulian tapi akses/visibilitas (45% kurang paham, 20% sulit menemukan). Di sisi pasokan, 30,2 juta UMKM mikro Indonesia (99,7% dari total UMKM) mencakup sektor jasa reparasi yang under-served, didukung narasi lapangan nyata tukang sol sepatu Gang Kote Bandung yang bisnisnya menyusut bukan karena kebutuhan reparasi hilang, tapi karena kehilangan visibilitas di era digital. *(Detail lengkap di dokumen yang sama, Bagian 1.2–1.3.)*

---

## Bagian 4 — Preseden Global & Kompetitor (Ringkasan)

French Repairability Index (skor 0–10 kelayakan reparasi produk elektronik, wajib sejak 2021) dan gerakan Repair Café global (60.000 event/tahun, 1,5 juta pengunjung) jadi referensi desain, dengan catatan model bisnisnya berbeda dari TukangIn (regulasi produsen vs. komunitas relawan vs. marketplace TukangIn). Kompetitor lokal (Sejasa, Kanggo, lakuKan) dikonfirmasi bermain di jasa rumah tangga umum/konstruksi dengan mitra formal skala menengah — tidak ada yang menjadikan "reparasi anti-sampah" sebagai identitas inti atau menyasar tukang informal super-lokal. *(Detail lengkap di "Riset Kompetitor TukangIn dan Pembedahan Poin 6.md".)*

---

## Bagian 5 — Model Bisnis: Harga & Bootstrap (Ringkasan)

TaskRabbit memakai tiga model harga (self-set hourly, task-based fixed, pre-set hourly) tergantung kategori; Sejasa memakai daftar harga referensi dengan disclaimer kondisi lapangan. Rekomendasi TukangIn: "Estimasi Berjenjang dengan Persetujuan Wajib" — platform beri jangkar harga, tukang beri penawaran dengan alasan wajib kalau menyimpang, pengguna approve sebelum kerja dimulai. Strategi bootstrap dua sisi: fokus geografis sempit, onboarding manual awal, insentif mitra pertama, kemitraan dengan struktur yang sudah ada. *(Detail lengkap di "Pendalaman TukangIn..." dan "Riset Kompetitor...".)*

---

## Bagian 6 — Regulasi Barang Bekas & E-Waste (Ringkasan)

Larangan "thrifting" di Indonesia hanya berlaku untuk pakaian bekas **impor**, bukan jual-beli/donasi barang bekas domestik (yang sepenuhnya legal). Elektronik rusak masuk kategori limbah B3 (PP 101/2014) dan wajib disalurkan lewat jalur resmi (dropbox e-waste), bukan dibuang sembarangan atau didonasikan begitu saja. Ekosistem donasi/daur ulang sudah ada tapi terfragmentasi per kategori (Waste4Change, Komunitas Saya Pilih Bumi, Ewasterj, dll) — TukangIn diposisikan sebagai hub triase yang mengarahkan, bukan membangun ulang infrastruktur ini. *(Detail lengkap di "Pendalaman TukangIn...", Bagian 2.)*

---

## Bagian 7 — BARU: Regulasi Platform Digital Indonesia — PSE & UU PDP

### 7.1 Kewajiban Pendaftaran PSE (Penyelenggara Sistem Elektronik)

Setiap entitas yang mengoperasikan sistem elektronik yang diakses publik di Indonesia — termasuk marketplace, aplikasi jasa, dan platform sejenis — pada dasarnya wajib terdaftar sebagai PSE Lingkup Privat di Kominfo (Komdigi), melalui sistem OSS (Online Single Submission) dengan NIB dan kode KBLI yang sesuai. Konsekuensi tidak terdaftar padahal wajib: **pemutusan akses (pemblokiran) langsung tanpa peringatan bertahap** — pernah diterapkan ke platform besar seperti eBay dan KLM di masa lalu.

**Implikasi untuk TukangIn:** ini murni catatan kepatuhan bisnis nyata (di luar cakupan Figma prototype), tapi penting disebut di narasi presentasi sebagai bukti tim memahami bahwa produk digital yang serius punya kewajiban legal, bukan cuma soal visual. Kalau juri bertanya "kalau ini benar-benar diluncurkan, apa yang perlu disiapkan secara legal?" — jawaban soal PSE menunjukkan pemahaman menyeluruh, bukan cuma di level desain.

### 7.2 UU Perlindungan Data Pribadi (UU PDP, UU No. 27/2022) — Relevansi Langsung ke Fitur Verifikasi

KTP (termasuk NIK, nama, alamat, dll) secara eksplisit dikategorikan sebagai data pribadi yang dilindungi negara. Platform yang mengumpulkan foto KTP (seperti fitur verifikasi tukang yang sudah dirancang di dokumen sebelumnya) berkedudukan sebagai **pengendali data (data controller)** dengan kewajiban: menerapkan sistem keamanan elektronik yang andal, memastikan akses data sesuai tujuan yang sah, mencegah akses tidak sah, dan menghormati hak-hak subjek data (Pasal 5–15 UU PDP). Pelanggaran (akses/penyebaran data pribadi tanpa hak) diancam pidana **hingga 2 tahun penjara dan/atau denda Rp25 juta**.

**Implikasi untuk desain TukangIn:** flow verifikasi KTP tukang (dari dokumen sebelumnya) perlu ditambah elemen desain eksplisit yang menunjukkan kesadaran ini — misalnya layar persetujuan (consent) sebelum unggah KTP yang menjelaskan untuk apa data dipakai dan bagaimana dilindungi, bukan sekadar form upload polos. Ini juga poin kuat untuk kriteria "UX dan Accessibility" karena transparansi data adalah bagian dari UX yang bertanggung jawab, dan jadi jawaban solid kalau juri bertanya soal keamanan data pengguna.

---

## Bagian 8 — BARU: Pembayaran Digital — QRIS

QRIS (QR Code Indonesian Standard) adalah standar pembayaran digital nasional yang diwajibkan Bank Indonesia untuk transaksi QR code lintas penyedia (bank maupun e-wallet seperti GoPay, OVO, DANA) — volume transaksinya mencapai **12,55 miliar transaksi pada semester I 2026**, menunjukkan adopsi yang sudah sangat luas dan jadi metode pembayaran default yang dikenali hampir semua lapisan masyarakat Indonesia, termasuk pedagang kecil/informal.

**Implikasi untuk desain TukangIn:** QRIS adalah pilihan pembayaran paling realistis dan familiar untuk konteks transaksi dengan tukang informal (dibanding memaksa integrasi kartu kredit atau dompet digital tunggal) — karena kemungkinan besar tukang informal skala kecil sudah punya QRIS statis sendiri (banyak pedagang kecil Indonesia sudah pakai ini) atau bisa dengan mudah dibuatkan lewat program onboarding. Ini juga jadi jawaban konkret untuk fitur "pembayaran terlindungi hanya kalau lewat aplikasi" yang direkomendasikan sebagai insentif retensi di brainstorming sebelumnya — QRIS in-app adalah cara realistis mewujudkannya tanpa membangun sistem pembayaran custom dari nol.

---

## Bagian 9 — BARU: Status Hukum Tukang sebagai "Mitra" — Realita Gig Economy Indonesia

Ini temuan paling penting dan paling perlu disikapi jujur oleh tim. Indonesia punya **kekosongan hukum nyata** untuk hubungan kemitraan gig economy — UU Ketenagakerjaan 2003 tidak mengatur model ini, dan UU UMKM 2008 mengatur kemitraan dalam konteks berbeda. Akibatnya, pekerja yang berstatus "mitra" (seperti driver ojol, dan berpotensi sama untuk tukang mitra TukangIn) kehilangan proteksi signifikan: tidak ada standar upah minimum (kompensasi per-pekerjaan), tidak ada pesangon/tunjangan, tidak ada jaminan BPJS Ketenagakerjaan otomatis, dan tidak ada batas jam kerja resmi. Ini "persoalan struktural", bukan pilihan individu — dengan lebih dari 2,5 juta pekerja gig roda dua di Indonesia yang mengalami kondisi ini.

**Implikasi kritis untuk TukangIn:** karena konsep TukangIn secara eksplisit memberdayakan tukang informal sebagai "mitra" (bukan karyawan), tim **tidak boleh mengklaim TukangIn otomatis "memberdayakan" tukang tanpa mengakui keterbatasan model kemitraan ini**. Ini justru kesempatan untuk menunjukkan kedalaman berpikir yang dicari kompetisi — tim bisa secara eksplisit menyatakan di presentasi bahwa mereka sadar model kemitraan punya keterbatasan proteksi hukum, dan sebagai respons desain, TukangIn bisa mempertimbangkan elemen yang meringankan (bukan menyelesaikan penuh, karena itu di luar cakupan desain UI/UX) — misalnya transparansi penuh soal potongan platform/komisi (kalau ada), tidak ada praktik "algoritma tersembunyi" yang menyulitkan tukang (sistem penurunan visibilitas dari riset sebelumnya harus punya alasan yang bisa dilihat tukang, bukan kotak hitam), dan fitur riwayat pendapatan yang transparan untuk tukang. Ini jauh lebih kredibel daripada narasi "pemberdayaan ekonomi" yang naif tanpa mengakui realita ini — dan bisa jadi jawaban kuat kalau juri (yang mungkin sudah familiar isu ojol) bertanya "apa bedanya tukang mitra TukangIn dengan driver ojol yang sering dikritik minim perlindungan?"

---

## Bagian 10 — BARU: Teknologi AI — Computer Vision untuk Deteksi Kerusakan Barang

Riset industri asuransi (yang sudah lama memakai AI damage assessment dari foto) memberi kerangka realistis untuk fitur "Scan AI" yang diusulkan tim:

**Alur kerja pengguna:** pengguna memfoto barang lewat aplikasi mobile — kualitas panduan foto ("app yang membimbing pengguna mengambil foto yang bisa dipakai adalah setengah dari keberhasilan sistem") jadi elemen UX penting, bukan detail sepele.

**Output AI yang realistis ditampilkan:** (1) klasifikasi jenis kerusakan (retak, penyok, robek, dsb), (2) estimasi biaya berdasarkan data harga yang terintegrasi, dan — ini yang paling penting untuk desain — (3) **skor keyakinan (confidence score)**: kasus dengan keyakinan rendah diarahkan ke penilaian manual/manusia, bukan dipaksakan otomatis.

**Keterbatasan yang harus diakui jujur:** akurasi model sangat bergantung pada data latih, performanya baik untuk kerusakan umum tapi lemah untuk kasus langka/ambigu, dan butuh pembaruan berkelanjutan seiring pola kerusakan baru muncul.

**Implikasi untuk desain fitur "Scan AI" TukangIn:** fitur ini harus didesain dengan **jalur keluar yang jujur** ketika AI tidak yakin — bukan memaksakan hasil deteksi yang mungkin salah. Desain yang direkomendasikan: setelah scan, tampilkan hasil deteksi dengan level keyakinan (misal "Kemungkinan besar: ritsleting rusak" vs "Kurang yakin, coba jelaskan manual atau chat tukang langsung"), sehingga kalau AI gagal mendeteksi dengan baik, pengguna tetap punya jalur lanjutan (bukan flow buntu). Ini juga menjawab kekhawatiran soal AI-washing (fitur AI yang cuma tempelan) — karena desainnya menunjukkan pemahaman nyata soal keterbatasan teknologi ini, persis semangat "Build the Logic" dari tema besar kompetisi.

---

## Bagian 11 — BARU: Konvensi UX Super-App Indonesia (Referensi Gojek)

Studi kasus UX Gojek (via riset pengguna n=5, SUS score 75,5) menunjukkan tiga prinsip organisasi utama yang terbukti bekerja untuk konteks Indonesia: **promosi personal** (konten/penawaran disesuaikan kebutuhan pengguna), **akses cepat ke fitur yang sering dipakai** (tombol pintasan untuk layanan favorit/berlangganan), dan **arsitektur informasi hierarkis yang jelas** (alur, konten, dan komponen didokumentasikan sistematis sebelum masuk wireframe).

**Implikasi untuk IA TukangIn:** pola "akses cepat ke fitur yang sering dipakai" ini relevan langsung dengan solusi yang sudah dibahas untuk pertanyaan disintermediasi Zikru (tombol "Tukang Favorit" untuk booking ulang cepat) — ini bukan ide baru dari kosong, tapi konsisten dengan pola yang sudah terbukti bekerja di konteks pengguna Indonesia lewat Gojek. Ini poin bagus untuk disebut di presentasi sebagai bukti keputusan desain berbasis preseden lokal yang relevan, bukan asumsi sendiri.

---

## Bagian 12 — Aksesibilitas (Ringkasan dari Riset Awal)

Standar konkret dari riset awal: target sentuh minimal 44×44pt (Apple)/48×48dp (Google), kontras teks-latar minimal 4,5:1 (teks biasa)/3:1 (teks besar), label deskriptif (bukan "klik di sini"), teks bisa di-resize, urutan fokus logis untuk screen reader. Ini berbobot sama besar dengan Interface & Design (30%:30%) di rubrik penyisihan — checklist ini wajib jadi acuan literal saat desain di Figma, bukan formalitas.

---

## Bagian 13 — Sintesis: Peta Keterkaitan Temuan ke Keputusan Produk

| Temuan Riset | Keputusan Produk yang Dihasilkan |
|---|---|
| Attitude-behavior gap (masalah akses, bukan niat) | Foto-langsung-cocok sebagai titik masuk utama, bukan form kategori manual |
| Ekonomi reparasi informal menyusut & tak terlihat | Direktori tukang dengan profil spesialisasi + visibilitas digital |
| Tukang informal tidak terverifikasi lembaga manapun | Verifikasi ringan (KTP + lokasi usaha), bukan verifikasi rumit ala kontraktor |
| Model harga TaskRabbit/Sejasa (berjenjang) + insight tim (barang besar vs kecil) | Flow "Estimasi Berjenjang" tersegmentasi ukuran barang, dengan biaya jasa tetap untuk kunjungan fisik |
| Regulasi barang bekas domestik legal, tapi e-waste = limbah B3 | Flow triase 3 arah (servis/jual-donasi/daur ulang resmi) dengan disclaimer domestik & rujukan dropbox resmi |
| UU PDP — KTP adalah data pribadi dilindungi | Layar consent eksplisit sebelum upload KTP tukang |
| Status "mitra" tukang minim proteksi hukum | Transparansi penuh sistem visibilitas/komisi, bukan algoritma tersembunyi |
| AI damage assessment butuh confidence score & fallback | Fitur Scan AI dengan jalur keluar manual saat AI tidak yakin |
| Pola UX Gojek — akses cepat fitur favorit | Fitur "Tukang Favorit" untuk booking ulang cepat, menjawab risiko disintermediasi |
| QRIS sebagai standar pembayaran nasional | Pembayaran in-app via QRIS sebagai mekanisme utama + syarat perlindungan garansi |
| Repair Café — dampak kolektif komunitas | Dashboard dampak komunitas wilayah |
| French Repairability Index | Skor kelayakan reparasi sederhana sebelum transaksi |

---

## Bagian 14 — Sumber Baru (Selain yang Sudah Tercantum di Dokumen Sebelumnya)

- [AI-Powered Damage Assessment: Computer Vision Guide — Acquaintsoft](https://acquaintsoft.com/blog/ai-damage-assessment-for-insurance-claims)
- [Cara Mendaftarkan Platform Digital sebagai PSE di Komdigi — IZIN.co.id](https://izin.co.id/blog/apa-itu-pse-kominfo/)
- [Apakah KTP Merupakan Data Pribadi yang Dilindungi? — Klinik Hukumonline](https://www.hukumonline.com/klinik/a/apakah-ktp-merupakan-data-pribadi-yang-dilindungi-lt5c8b573e224de/)
- [UU No. 27 Tahun 2022 tentang Perlindungan Data Pribadi — Peraturan BPK](https://peraturan.bpk.go.id/Details/229798/uu-no-27-tahun-2022)
- [BI: Transaksi QRIS Capai 12,55 Miliar pada Semester I 2026 — Antara News](https://www.antaranews.com/berita/5682285/bi-transaksi-qris-capai-1255-miliar-pada-semester-i-2026)
- [Disebut "Mitra" tapi Tak Ada Payung Hukumnya: Pekerja Gig Economy Tidak Terproteksi — The Conversation](https://theconversation.com/disebut-mitra-tapi-tak-ada-payung-hukumnya-pekerja-gig-economy-tidak-terproteksi-190464)
- [4 Juta Mitra Ojol, Nol Perlindungan — FounderPlus](https://founderplus.id/blog/gig-economy-indonesia-pelajaran-founder-model-mitra/)
- [UX Study Case: Mengoptimalkan Pengalaman Pengguna Melalui Halaman Beranda Gojek — Medium](https://medium.com/@chaerulimam22/ux-study-case-mengoptimalkan-pengalaman-pengguna-melalui-halaman-beranda-gojek-7386aae9e993)

*(Sumber untuk Bagian 2–8 sudah tercantum lengkap di dokumen-dokumen riset sebelumnya yang dirujuk di masing-masing bagian.)*

---

## Catatan Penutup

Dengan dokumen ini, seluruh aspek lingkup tema — lingkungan, masyarakat, kompetitor, model bisnis, regulasi barang bekas, regulasi platform digital, regulasi data pribadi, status hukum mitra, teknologi AI, standar pembayaran, dan konvensi UX lokal — sudah dipetakan dan ditautkan langsung ke keputusan produk. Langkah selanjutnya adalah menyusun PRD (Product Requirements Document) lengkap yang menerjemahkan seluruh peta keterkaitan di Bagian 13 menjadi blueprint flow dan fitur yang runtut dari awal sampai akhir — dokumen terpisah yang menyusul dokumen ini.
