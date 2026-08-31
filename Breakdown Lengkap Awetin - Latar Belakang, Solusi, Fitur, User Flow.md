# Breakdown Lengkap Konsep Awetin

> **Catatan (31 Agustus 2026):** Nama produk di dokumen ini diperbarui dari nama kerja sebelumnya menjadi **Awetin**, menyusul temuan bahwa nama sebelumnya sudah dipakai aplikasi/skripsi lain. Isi & analisis substantif dokumen ini tidak berubah.
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Disusun:** 26 Agustus 2026
**Konteks:** Eksekusi Poin 3 dari dokumen sebelumnya — breakdown lengkap latar belakang masalah, solusi, adaptasi fitur, dan user flow untuk konsep Awetin (Repair Economy Network) yang telah disepakati tim

---

## Ringkasan Eksekutif

Dokumen ini menjawab satu pertanyaan yang selama ini belum benar-benar dijawab tuntas: **kenapa Awetin, dan kenapa sekarang?** Bukan cuma "budaya buang-beli baru sudah mengakar" — itu terlalu umum, dan juri kompetisi desain sudah pasti pernah dengar kalimat itu berkali-kali dari peserta lain.

Riset mendalam di dokumen ini menemukan sesuatu yang lebih tajam: masalahnya bukan cuma masyarakat "malas" memperbaiki barang. Datanya menunjukkan **krisis dua sisi yang saling mengunci** — di sisi permintaan, kesadaran lingkungan masyarakat Indonesia sebenarnya sudah tinggi (62,9% pernah beli produk ramah lingkungan), tapi niat itu tidak nyambung ke perilaku reparasi karena hambatannya bukan soal nilai/kepedulian, melainkan soal **akses dan visibilitas** (45% masyarakat masih kurang paham konsep produk berkelanjutan, dan untuk soal tukang reparasi spesifik, masalahnya adalah "susah dicari", bukan "tidak mau"). Di sisi lain — dan ini yang jarang dibahas kompetitor manapun — **pasokan tukang reparasi informal sendiri sedang menyusut dan makin tidak terlihat**, sebagaimana ditunjukkan oleh kondisi nyata tukang sol sepatu di Bandung yang bisnisnya menurun drastis pasca-pandemi dan nyaris tidak terdokumentasi di dunia digital sama sekali.

Awetin, dengan kerangka ini, bukan sekadar "aplikasi cari tukang" — ia menjawab **kegagalan pencocokan (matching failure)** antara permintaan yang sebenarnya sudah berniat baik dan pasokan yang sebenarnya masih ada tapi terkubur dan makin rapuh. Framing ini yang akan dipakai konsisten di seluruh dokumen ini: latar belakang, solusi, fitur, hingga user flow.

---

## 1. Latar Belakang Masalah

### 1.1 Krisis Sampah yang Terus Tumbuh — Bukan Cuma Soal Elektronik

Data resmi KLHK (dikutip ulang oleh berbagai media 2022–2026) menunjukkan Indonesia menghasilkan **1,9–2 juta ton limbah elektronik (e-waste) per tahun** — angka terbesar di Asia Tenggara. Yang lebih mengkhawatirkan bukan angka totalnya, tapi tren dan tata kelolanya:

- Secara global, volume e-waste naik **82% dari 2010 ke 2022**, dan diproyeksikan naik lagi 32% menjadi 82 juta ton pada 2030 — artinya ini bukan masalah statis, tapi kurva yang terus menanjak.
- Dari total e-waste Indonesia, **hanya 17,4% yang mendapat penanganan/daur ulang yang layak** — sisanya disimpan begitu saja di rumah atau tercampur dengan sampah rumah tangga biasa.
- Secara geografis, e-waste terkonsentrasi di **Jawa (56%) dan Sumatra (22%)** — relevan untuk menentukan wilayah pilot yang realistis kalau tim ingin cerita geografis yang konkret di presentasi.

Tapi masalahnya tidak berhenti di elektronik. Riset ini juga menemukan data yang selama ini luput dari diskusi tim: **limbah tekstil/pakaian** ternyata setara besarnya, bahkan lebih personal karena menyentuh kebiasaan sehari-hari semua orang:

- KLHK (2021) mencatat Indonesia menghasilkan **2,3 juta ton limbah pakaian per tahun**, setara 12% dari total sampah rumah tangga nasional.
- Dari jumlah itu, **hanya 0,3 juta ton (13%) yang didaur ulang** — sisanya berakhir di TPA.
- Perilaku konsumen mendukung tren ini: **66% orang dewasa Indonesia membuang setidaknya satu pakaian dalam setahun**, dan **30% populasi pernah membuang pakaian setelah hanya dipakai satu kali**.

**Insight untuk latar belakang:** ini memperkuat argumen bahwa Awetin tidak perlu membatasi diri hanya ke elektronik — kategori jahit/vermak pakaian punya dasar data yang sama kuatnya, bahkan mungkin lebih relevan secara emosional karena hampir semua orang punya pengalaman "baju bagus tapi robek dikit terus nggak kepake lagi."

### 1.2 Kesenjangan Sikap-Perilaku (Attitude-Behavior Gap) — Bukan Soal Tidak Peduli

Ini bagian yang membedakan latar belakang Awetin dari narasi generik "masyarakat konsumtif." Data survei Katadata Insight Center (n=3.631 responden, 17–60 tahun) menunjukkan masyarakat Indonesia **sudah punya niat baik terhadap lingkungan**:

- **62,9%** responden pernah membeli produk ramah lingkungan setidaknya sekali.
- Alasan utama membeli produk berkelanjutan: **60,5% karena ingin melestarikan bumi**, 51,1% karena puas dengan produknya, 41,3% karena membangun citra diri positif.

Tapi ada jurang antara niat dan tindakan. Survei GoodStats/Katadata soal *alasan tidak* membeli produk ramah lingkungan menemukan hambatan utamanya **bukan soal tidak peduli**, melainkan soal akses dan informasi:

- **45%** mengaku kurang paham konsep produk ramah lingkungan (masalah edukasi/visibilitas, bukan nilai).
- **22%** karena harga lebih mahal 15–20% dari produk konvensional.
- **20%** karena produk ramah lingkungan lebih sulit ditemukan (masalah distribusi/akses).
- Hanya **13%** yang murni lebih memilih produk konvensional karena preferensi.

Pola yang sama secara logis berlaku untuk keputusan reparasi vs. beli baru: orang tidak selalu memilih "beli baru" karena tidak peduli lingkungan, tapi karena **jasa reparasi yang tepercaya susah ditemukan saat dibutuhkan** — persis titik masalah yang tim sudah identifikasi sejak awal ("tukang servis lokal susah dicari"), sekarang didukung pola data yang lebih luas soal bagaimana masyarakat Indonesia sebenarnya mengambil keputusan terkait produk berkelanjutan.

**Ini kerangka psikologis yang jauh lebih kuat daripada "budaya buang-beli baru sudah mengakar"** — karena ini menempatkan masalah pada *hambatan akses*, sesuatu yang bisa dijawab langsung oleh produk digital (yang memang fungsinya menjembatani akses), bukan pada *perubahan nilai/karakter masyarakat* yang jauh lebih sulit diklaim bisa diselesaikan lewat satu aplikasi.

### 1.3 Krisis di Sisi Pasokan — Ekonomi Reparasi Informal yang Menyusut dan Tak Terlihat

Ini bagian paling penting dan paling jarang dibahas kompetitor: masalahnya bukan cuma "orang tidak tahu ke mana harus memperbaiki barang" — tapi **jaringan tukang reparasi informal itu sendiri sedang dalam tekanan nyata**.

Data makro dari kategori UMKM Indonesia (SIDT-UMKM, per 31 Desember 2025) menunjukkan skala ekonomi informal yang relevan:

- Indonesia punya **30,2 juta unit UMKM non-pertanian**, dengan **99,7%-nya adalah usaha mikro** — skala yang persis sama dengan profil tukang informal yang disasar Awetin (tukang sol sepatu, penjahit rumahan, tukang servis kecil).
- Sektor "Jasa Lainnya" — kategori tempat tukang reparasi informal biasanya berada — tercatat **1,91 juta unit**, jauh lebih kecil dari sektor dagang (14,44 juta) atau makanan (6,41 juta), mengindikasikan sektor jasa reparasi memang under-represented dan under-served dibanding sektor UMKM lain yang sudah punya banyak platform pendukung (misalnya UMKM kuliner sudah punya GoFood/GrabFood/ShopeeFood).
- **Hanya 3,51% UMKM yang punya catatan keuangan formal** — menunjukkan betapa besar bagian ekonomi ini yang benar-benar informal, tidak terdaftar di sistem manapun, dan karena itu juga tidak terdaftar di platform digital manapun.

Data makro ini didukung oleh narasi lapangan yang jauh lebih konkret dan manusiawi: kisah **Anung Solihin dan anaknya Tedi**, tukang sol sepatu di Gang Kote, Bandung (diliput Detik.com). Poin-poin kunci dari kisah ini yang relevan untuk latar belakang:

- Bisnis tukang sol sepatu di kawasan ini **menurun drastis pasca-pandemi** — bukan karena permintaan reparasi sepatu hilang, tapi karena pelanggan makin sulit menemukan mereka dan kebiasaan belanja bergeser ke online.
- Ironisnya, **kualitas bahan modern (lem) justru terkadang lebih cepat rusak** dibanding metode lama — artinya kebutuhan reparasi sebenarnya tidak berkurang, mungkin malah bertambah, tapi tidak dibarengi peningkatan visibilitas jasa reparasi.
- Ada harapan eksplisit dari pelaku usaha ini sendiri: *"jangan sampai punah tukang sol"* — sebuah kekhawatiran nyata bahwa keahlian ini akan hilang bukan karena tidak dibutuhkan, tapi karena tidak ada jembatan yang menghubungkan mereka ke pelanggan baru di era digital.

**Insight kunci untuk latar belakang:** Ini mengubah framing Awetin dari "aplikasi yang mendorong orang memperbaiki barang" (asumsi masalah ada di sisi permintaan/kesadaran) menjadi **"aplikasi yang menyelamatkan infrastruktur ekonomi reparasi yang sudah ada tapi sekarat karena tidak terlihat"** (masalah struktural di sisi pasokan). Ini juga selaras dengan kerangka kausal dari riset budaya sekali-pakai (BPM UMA): produksi massal, *planned obsolescence*, dan persepsi "barang baru selalu lebih baik" tidak cuma menciptakan sampah — tapi juga **menghilangkan profesi dan keahlian reparasi** serta mendorong ekonomi linear (ambil-pakai-buang) menggantikan ekonomi sirkular yang dulu jadi kebiasaan alami masyarakat (budaya "diperbaiki dulu" sebelum "beli baru").

### 1.4 Preseden Global — Bukan untuk Ditiru Mentah, Tapi untuk Diadaptasi

Dua preseden internasional relevan sebagai referensi desain, dengan catatan bahwa keduanya punya model berbeda dari Awetin dan tidak boleh disamakan begitu saja:

**French Repairability Index (Indice de Réparabilité)** — sistem wajib pemerintah Prancis sejak Januari 2021 yang mewajibkan produk elektronik diberi skor reparabilitas 0–10 berdasarkan 5 kriteria: ketersediaan dokumentasi servis, kemudahan pembongkaran, ketersediaan suku cadang, harga suku cadang, dan faktor spesifik produk. Catatan penting: sistem ini berbasis **self-scoring oleh produsen** dan baru punya sanksi resmi sejak 2022 — jadi bukan sistem sempurna, tapi konsepnya (skor transparan yang membantu konsumen menilai "seberapa layak diperbaiki barang ini") bisa diadaptasi jadi fitur di Awetin, bukan untuk barang baru, tapi untuk **menilai kelayakan reparasi barang yang sudah dimiliki pengguna**.

**Gerakan Repair Café global** — jaringan komunitas reparasi sukarela yang kini ada di puluhan negara. Skala globalnya: sekitar **60.000 event per tahun**, menarik **1,5 juta pengunjung**, dengan sekitar **1,6 juta barang dibawa untuk diperbaiki** dan **89.000 relawan** terlibat. Catatan penting: model Repair Café berbasis **relawan/gratis di ruang komunitas fisik terjadwal**, sangat berbeda dari model marketplace Awetin yang berbasis transaksi dengan tukang profesional/semi-profesional yang mengandalkan reparasi sebagai sumber penghasilan. Yang layak diadaptasi bukan model bisnisnya, tapi **elemen komunitas dan dampak kolektifnya** — misalnya penghitung dampak agregat ("X barang diselamatkan minggu ini di wilayahmu") yang membuat aksi individu terasa jadi bagian gerakan yang lebih besar.

### 1.5 Simpulan Latar Belakang — Rumusan Masalah yang Dipakai untuk Solusi

Menggabungkan seluruh temuan di atas, rumusan masalah Awetin yang lebih presisi (dan akan dipakai sebagai dasar seluruh bagian solusi & fitur di bawah) adalah:

> Indonesia menghadapi krisis sampah elektronik dan tekstil yang terus tumbuh (1,9–2,3 juta ton/tahun masing-masing, dengan tingkat daur ulang/penanganan layak di bawah 20%), sementara masyarakat sebenarnya sudah punya kepedulian lingkungan yang cukup tinggi (62,9% pernah membeli produk ramah lingkungan) namun terhambat mewujudkannya dalam bentuk reparasi karena masalah akses dan visibilitas, bukan karena tidak peduli. Di saat bersamaan, jaringan tukang reparasi informal — bagian dari 30,2 juta UMKM mikro Indonesia — sedang mengalami tekanan nyata (menyusutnya pelanggan pasca-pandemi, minim jejak digital) yang berisiko membuat keahlian reparasi tradisional perlahan hilang, bukan karena tidak dibutuhkan, tapi karena tidak ada jembatan yang menghubungkan mereka ke pelanggan baru di era digital.

Rumusan ini punya dua keunggulan dibanding narasi awal ("budaya buang-beli baru sudah mengakar"):

1. **Lebih spesifik dan bisa diverifikasi** — didukung angka konkret, bukan klaim budaya yang sulit diukur.
2. **Menempatkan solusi digital sebagai jawaban yang logis**, bukan tempelan — karena masalah intinya adalah kegagalan pencocokan informasi (matching/visibility problem), yang memang persis jenis masalah yang bisa dijawab platform digital, bukan masalah nilai/budaya yang butuh perubahan generasi.

---

## 2. Solusi yang Ditawarkan

### 2.1 Reposisi Value Proposition

Berdasarkan rumusan masalah di atas, value proposition Awetin diperjelas menjadi dua sisi yang eksplisit — bukan cuma "platform cari tukang", tapi **jembatan dua arah**:

- **Untuk pengguna/pemilik barang:** kemudahan menemukan tukang reparasi tepercaya terdekat tanpa harus tahu ke mana harus mencari — cukup foto barang rusak, sistem mencocokkan ke kategori dan tukang terdekat.
- **Untuk tukang informal:** visibilitas digital yang selama ini tidak mereka miliki — cara baru mendapatkan pelanggan tanpa harus mengandalkan lokasi fisik atau dari mulut ke mulut yang semakin melemah di era belanja online.

**Tagline yang diperkuat:** *"Rusak? Jangan dibuang. Perbaiki — dan bantu tukang lokal tetap ada."* — dua manfaat sekaligus dalam satu kalimat: lingkungan (jangan dibuang) dan sosial (tukang lokal tetap ada), sesuai dua sisi krisis yang ditemukan di riset latar belakang.

### 2.2 Cakupan Kategori — Diperluas Berdasarkan Data

Berdasarkan temuan 1.1, kategori Awetin diperluas secara sengaja (bukan cuma elektronik) menjadi empat klaster utama, masing-masing didukung data:

| Klaster | Contoh Barang | Dasar Data |
|---|---|---|
| Elektronik kecil | HP, charger, kipas angin, setrika, blender | 1,9–2 juta ton e-waste/tahun, hanya 17,4% tertangani layak |
| Pakaian & tekstil (jahit/vermak) | Baju robek, ritsleting rusak, celana kekecilan | 2,3 juta ton limbah pakaian/tahun, hanya 13% didaur ulang |
| Alas kaki | Sepatu, sandal (sol, jahit ulang) | Kisah nyata tukang sol Bandung — kategori dengan tukang informal paling rentan hilang |
| Logam & las | Pagar, teralis, perkakas rumah tangga | Kategori yang sudah ada di ide awal tim, dipertahankan sebagai pelengkap |

### 2.3 Mekanisme Inti (Tetap Dipertahankan, Diperkuat Kepercayaannya)

Mekanisme dasar tidak berubah dari konsep awal karena memang sudah tervalidasi sebagai pola familiar (mirip Gojek/Grab untuk jasa): **foto barang rusak → pilih/dicocokkan kategori → sistem menampilkan tukang terdekat sesuai kategori → transaksi → bukti hasil reparasi**. Yang diperkuat adalah lapisan kepercayaan dan cerita dampaknya (lihat Bagian 3).

### 2.4 Diferensiasi (Diwarisi dari Riset Kompetitor Sebelumnya, Diringkas)

Sejasa, Kanggo, dan lakuKan semua bermain di jasa rumah tangga umum atau konstruksi/renovasi dengan mitra yang cenderung lebih formal/menengah. Tidak satupun menjadikan "reparasi untuk mengurangi sampah" sebagai identitas inti, dan tidak ada yang secara spesifik menyasar tukang informal super-lokal (sol sepatu keliling, penjahit rumahan). Awetin mengisi celah ini secara sengaja di tiga lapis: kategori jasa (barang kecil sehari-hari, bukan AC/renovasi), segmen mitra (tukang informal super-lokal, bukan teknisi bersertifikat), dan narasi produk (penyelamatan barang + pemberdayaan tukang lokal, bukan sekadar "cari jasa cepat").

---

## 3. Adaptasi Solusi Menjadi Fitur

Setiap fitur di bawah ini secara eksplisit ditelusuri balik ke temuan riset spesifik — bukan daftar fitur generik aplikasi jasa pada umumnya.

### 3.1 Fitur Inti — Permintaan Reparasi via Foto

**Apa:** Pengguna memfoto barang rusak, sistem/AI membantu menyarankan kategori (elektronik/jahit/sepatu/las), lalu menampilkan daftar tukang terdekat yang sesuai kategori tersebut lengkap dengan estimasi harga dan jarak.

**Kenapa (traceability ke riset):** Menjawab temuan 1.2 — hambatan utama bukan soal kepedulian (45% masalahnya "kurang paham"/"susah menemukan", bukan "tidak mau"). Foto-langsung-cocok menghilangkan friksi "harus tahu ke mana mencari tukang yang tepat", persis titik hambatan akses yang ditemukan di data.

### 3.2 Fitur Skor Kelayakan Reparasi (terinspirasi French Repairability Index)

**Apa:** Setiap kategori barang diberi indikator sederhana "layak diperbaiki" berdasarkan jenis kerusakan yang difoto/dijelaskan pengguna — bukan skor 0–10 rumit ala Prancis, tapi versi disederhanakan yang cocok untuk konteks aplikasi konsumen (misal label "Sangat layak diperbaiki" / "Cek dulu ke tukang" / "Mungkin lebih baik diganti") — dengan estimasi kasar biaya reparasi vs. beli baru, agar pengguna bisa mengambil keputusan informasional, bukan cuma diarahkan otomatis ke transaksi.

**Kenapa (traceability ke riset):** Diadaptasi langsung dari temuan 1.4 (French Repairability Index) tapi disederhanakan untuk konteks konsumen sehari-hari, bukan regulasi produsen. Fitur ini juga menjawab bagian dari temuan 1.2 soal barrier harga (22% orang menganggap produk berkelanjutan lebih mahal) — dengan menunjukkan estimasi biaya reparasi di depan, pengguna bisa melihat sendiri kalau reparasi seringkali jauh lebih murah daripada beli baru, bukan sekadar diklaim oleh aplikasi.

### 3.3 Fitur Kepercayaan — Verifikasi, Rating, Bukti Before/After, Garansi Sederhana

**Apa:** Verifikasi identitas dasar tukang saat mendaftar (foto KTP + foto lokasi/tempat usaha), rating & ulasan per transaksi, foto before/after hasil reparasi, dan garansi sederhana (servis ulang gratis jika rusak lagi dalam periode singkat).

**Kenapa (traceability ke riset):** Menjawab temuan 1.3 langsung — karena tukang yang disasar adalah tukang informal yang tidak terverifikasi lembaga manapun (berbeda dari mitra Sejasa/Kanggo yang lebih formal), kepercayaan harus dibangun eksplisit di desain, bukan diasumsikan. Foto before/after juga berguna ganda: selain membangun kepercayaan, jadi sumber data untuk fitur dampak di bawah.

### 3.4 Fitur Penghitung Dampak Komunitas (terinspirasi Repair Café)

**Apa:** Dashboard/halaman komunitas yang menampilkan akumulasi dampak di level wilayah — "X barang diperbaiki bulan ini di kelurahanmu", "Y tukang lokal terbantu" — bukan klaim 1:1 pasti terhadap pengurangan sampah TPA (klaim ini perlu dilunakkan menjadi "berpotensi mengurangi", sesuai catatan risiko dari dokumen sebelumnya), tapi disajikan sebagai dampak kolektif yang terlihat nyata.

**Kenapa (traceability ke riset):** Diadaptasi dari elemen komunitas gerakan Repair Café global (temuan 1.4) yang berhasil membuat 1,5 juta orang/tahun merasa jadi bagian gerakan kolektif — meski model transaksinya beda (marketplace vs. volunteer), elemen "melihat dampak bersama" ini yang diadaptasi ke Awetin.

### 3.5 Fitur Direktori Tukang per Kategori & Wilayah (Onboarding & Visibilitas Tukang)

**Apa:** Profil tukang yang menonjolkan spesialisasi (bukan cuma "tukang servis umum" tapi "spesialis jahit ritsleting", "spesialis sol sepatu kulit"), lokasi/wilayah operasi, dan jam ketersediaan — dirancang agar tukang informal yang biasanya cuma dikenal lewat mulut ke mulut di sekitar rumahnya bisa punya representasi digital yang jelas.

**Kenapa (traceability ke riset):** Menjawab langsung inti masalah dari kisah Anung & Tedi di Bandung (temuan 1.3) — masalah mereka bukan kehilangan keahlian atau kehilangan permintaan, tapi kehilangan visibilitas di tengah pergeseran kebiasaan belanja ke digital. Fitur ini secara harfiah adalah jembatan visibilitas yang hilang tersebut.

### 3.6 Fitur Pendukung Bootstrap (Naratif, Sebagian Bisa Jadi Fitur Ringan di Prototype)

Mewarisi strategi dari dokumen sebelumnya (fokus geografis sempit, onboarding manual awal, insentif mitra pertama, kemitraan dengan struktur yang sudah ada seperti pasar tradisional/kelurahan) — di level fitur Figma, ini bisa dimanifestasikan sebagai halaman "Wilayah yang sudah tersedia" yang jujur menunjukkan cakupan awal terbatas (misalnya mulai dari satu kecamatan), bukan berpura-pura sudah nasional — konsisten dengan narasi kelayakan bisnis yang akan dipertahankan saat tanya jawab.

---

## 4. User Flow

### 4.1 Flow Utama — Pengguna Meminta Reparasi

1. Buka aplikasi → halaman utama menampilkan tombol "Perbaiki Barang" + penghitung dampak komunitas wilayah pengguna.
2. Tap "Perbaiki Barang" → ambil/unggah foto barang rusak.
3. Sistem menyarankan kategori otomatis (bisa dikoreksi manual) + menampilkan skor kelayakan reparasi (Fitur 3.2) dengan estimasi biaya reparasi vs. kisaran harga beli baru.
4. Jika pengguna lanjut → tampil daftar tukang terdekat sesuai kategori, masing-masing dengan rating, jarak, estimasi harga, dan contoh foto before/after hasil kerja sebelumnya.
5. Pengguna pilih tukang → lihat detail profil tukang (spesialisasi, verifikasi, garansi yang ditawarkan) → konfirmasi permintaan.
6. Status pesanan berjalan (diterima tukang → proses → selesai).
7. Setelah selesai, pengguna diminta unggah foto hasil (before/after) + rating + ulasan.
8. Konfirmasi dampak: "Barangmu berhasil diselamatkan! Kontribusimu menambah penghitung dampak wilayah."

### 4.2 Flow Onboarding Tukang/Mitra

1. Tukang mendaftar mandiri (atau didata petugas lapangan di fase awal peluncuran, sesuai strategi bootstrap) → isi data dasar (nama, kategori keahlian, wilayah operasi).
2. Unggah foto KTP + foto lokasi/tempat usaha untuk verifikasi dasar.
3. Isi kisaran harga per jenis servis dalam kategorinya.
4. Menunggu verifikasi (proses sederhana, bukan birokrasi rumit — sesuai prinsip "cukup untuk akuntabilitas minimal" dari riset kepercayaan sebelumnya).
5. Setelah terverifikasi, profil tukang aktif dan mulai muncul di pencarian pengguna pada radius wilayahnya.
6. Menerima notifikasi permintaan baru → terima/tolak → update status pekerjaan → unggah bukti selesai.

### 4.3 Flow Komplain/Garansi

1. Pengguna melapor barang rusak lagi dalam periode garansi (lihat Fitur 3.3) → pilih pesanan terkait dari riwayat.
2. Sistem menawarkan opsi sesuai kebijakan garansi sederhana yang sudah disepakati di awal transaksi (servis ulang gratis dalam batas wajar).
3. Notifikasi ke tukang terkait → tukang konfirmasi jadwal servis ulang.
4. Jika tidak ada kesepakatan → eskalasi sederhana ke tim (dalam konteks prototype, cukup ditampilkan sebagai status "Sedang Ditinjau").

### 4.4 Flow Eksplorasi Dampak Komunitas (Opsional, Memperkuat Narasi Lingkungan)

1. Dari halaman utama, pengguna tap penghitung dampak wilayah.
2. Melihat breakdown: jumlah barang diperbaiki per kategori bulan ini di wilayahnya, jumlah tukang lokal yang terbantu, dan highlight cerita tukang (mirip kisah Anung & Tedi) untuk membangun koneksi emosional.

---

## 5. Daftar Layar Figma yang Disarankan

1. Onboarding/Splash — perkenalan value proposition dua sisi.
2. Halaman Utama (dashboard pengguna + penghitung dampak).
3. Ambil/Unggah Foto Barang Rusak.
4. Hasil Deteksi Kategori + Skor Kelayakan Reparasi.
5. Daftar Tukang Terdekat (per kategori).
6. Detail Profil Tukang (rating, verifikasi, before/after, garansi).
7. Konfirmasi Permintaan & Estimasi Harga.
8. Status Pesanan (proses reparasi berjalan).
9. Unggah Bukti Hasil + Rating & Ulasan.
10. Halaman Dampak Komunitas Wilayah.
11. Onboarding Tukang — Form Pendaftaran.
12. Onboarding Tukang — Verifikasi Identitas.
13. Dashboard Tukang (pesanan masuk, riwayat, pendapatan).
14. Halaman Komplain/Garansi.

---

## 6. Design Rationale (Ringkas)

| Keputusan Desain | Alasan |
|---|---|
| Foto sebagai titik masuk utama (bukan form kategori manual dulu) | Mengurangi friksi — sesuai temuan hambatan akses (bukan kepedulian) di 1.2 |
| Skor kelayakan reparasi ditampilkan sebelum transaksi | Transparansi biaya menjawab barrier harga (22%, temuan 1.2) dan mengadaptasi French Repairability Index (1.4) |
| Verifikasi tukang ringan, bukan rumit | Menyesuaikan realita tukang informal super-lokal, bukan kontraktor formal (1.3) |
| Penghitung dampak level wilayah, bukan klaim individu 1:1 | Menghindari overclaiming dampak lingkungan; terinspirasi elemen komunitas Repair Café (1.4) |
| Cakupan wilayah awal ditampilkan jujur terbatas | Mendukung narasi bootstrap yang realistis untuk sesi tanya jawab |

---

## 7. Risiko & Mitigasi (Diperbarui)

| Risiko | Mitigasi |
|---|---|
| Klaim dampak lingkungan berlebihan (1 barang diperbaiki ≠ pasti 1 barang tidak masuk TPA) | Gunakan bahasa "berpotensi mengurangi" di seluruh materi, bukan klaim pasti — sudah diterapkan di seluruh dokumen ini |
| Diferensiasi dipertanyakan juri ("ini kan mirip Sejasa/Kanggo?") | Jawaban sudah disiapkan di Bagian 2.4 — tiga lapis diferensiasi (kategori, segmen mitra, narasi) |
| Kepercayaan ke tukang tidak terverifikasi | Dijawab lewat Fitur 3.3 — tapi tetap perlu diakui di sesi tanya jawab bahwa verifikasi ini "dasar", bukan sekuat verifikasi kontraktor besar |
| Masalah bootstrap dua sisi (ayam-telur marketplace) | Strategi naratif sudah disiapkan (fokus geografis sempit, onboarding manual awal) — lihat Bagian 3.6 |
| Data pendukung sebagian bersumber dari artikel berita/survei pihak ketiga, bukan riset primer tim | Wajar untuk konteks kompetisi desain (bukan tesis akademik), tapi sebaiknya dicantumkan sebagai sumber rujukan di materi presentasi, bukan diklaim sebagai riset primer tim |

---

## 8. Sumber

- [Indonesia Hasilkan 1,9 Juta Ton Limbah Elektronik — Komdigi](https://www.komdigi.go.id/berita/berita-komdigi/detail/indonesia-hasilkan-19-juta-ton-limbah-elektronik-pemerintah-siapkan-kebijakan-nasional-e-waste)
- [Langkah Nyata Atasi Krisis E-waste di Indonesia — Katadata Green](https://green.katadata.co.id/berita/67dd13fb1d4e2/langkah-nyata-atasi-krisis-e-waste-di-indonesia)
- [Sampah Pakaian Makin Banyak, Saatnya Sudahi Konsumsi Fast Fashion — GoodStats](https://goodstats.id/article/sampah-pakaian-makin-banyak-saatnya-sudahi-konsumsi-fast-fashion-Bx10s)
- [Industri "Fast Fashion" Hasilkan Limbah Tekstil Tak Terkelola 92 Juta Ton Per Tahun — Kompas](https://lestari.kompas.com/read/2025/04/11/073000286/industri-fast-fashion-hasilkan-limbah-tekstil-tak-terkelola-92-juta-ton-per?page=all)
- [16% Orang Indonesia Belum Pernah Membeli Produk Sustainable, Apa Alasannya? — GoodStats Data](https://data.goodstats.id/statistic/16-orang-indonesia-belum-pernah-membeli-produk-sustainable-apa-alasannya-j8YGd)
- [5 Alasan Konsumen Belanja Produk Ramah Lingkungan — Databoks](https://databoks.katadata.co.id/produk-konsumen/statistik/a7c5e69df2a64c6/5-alasan-konsumen-belanja-produk-ramah-lingkungan)
- [Data UMKM, Jumlah dan Pertumbuhan Usaha Mikro, Kecil, dan Menengah di Indonesia — UKMINDONESIA.ID](https://ukmindonesia.id/baca-deskripsi-posts/data-umkm-jumlah-dan-pertumbuhan-usaha-mikro-kecil-dan-menengah-di-indonesia)
- [Peradaban yang Lupa Memperbaiki: Mengapa Budaya Sekali Pakai Menjadi Ancaman Global? — BPM UMA](https://bpm.uma.ac.id/peradaban-yang-lupa-memperbaiki-mengapa-budaya-sekali-pakai-menjadi-ancaman-global/)
- [The Right to Repair — IEEP Policy Brief (French Repairability Index)](https://ieep.eu/wp-content/uploads/2022/12/Policy-brief_The-right-to-repair_IEEP-2022.pdf)
- [Repair Cafés attract 1.5 million visitors every year — Repaircafe.org](https://www.repaircafe.org/en/repair-cafes-attract-1-5-million-visitors-every-year/)
- Kisah tukang sol sepatu Gang Kote, Bandung — Detik.com (diakses via pencarian web, artikel tentang Anung Solihin & Tedi)

---

## 9. Catatan Penutup

Dokumen ini sudah menuntaskan Poin 3 dari dokumen sebelumnya: latar belakang masalah (dengan data yang jauh lebih spesifik dan dua sisi — permintaan & pasokan), solusi yang ditawarkan (value proposition diperjelas dua arah), adaptasi fitur (enam fitur, masing-masing ditelusuri balik ke temuan riset spesifik, bukan generik), dan user flow (empat alur: permintaan reparasi, onboarding tukang, komplain/garansi, eksplorasi dampak komunitas).

Yang belum dikerjakan dan bisa jadi langkah berikutnya kalau tim sudah siap: (1) wireframe/mockup Figma aktual berdasarkan 14 layar yang disarankan di Bagian 5, (2) copywriting detail per layar (microcopy, nama fitur final), (3) sistem/skala visual (warna, tipografi) yang mencerminkan identitas "lingkungan + pemberdayaan lokal" tanpa jatuh ke klise hijau-daun yang terlalu umum di kompetisi sejenis.
