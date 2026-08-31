# Pendalaman Awetin: Mekanisme Harga, Jalur Non-Servis, dan Analisa Celah

> **Catatan (31 Agustus 2026):** Nama produk di dokumen ini diperbarui dari nama kerja sebelumnya menjadi **Awetin**, menyusul temuan bahwa nama sebelumnya sudah dipakai aplikasi/skripsi lain. Isi & analisis substantif dokumen ini tidak berubah.
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Disusun:** 26 Agustus 2026
**Konteks:** Menjawab dua pertanyaan kritis tim sebelum lanjut ke desain visual — mekanisme harga jasa, dan skenario ketika pengguna tidak ingin memperbaiki barangnya — sekaligus analisa celah menyeluruh dari solusi & flow yang sudah dirumuskan sebelumnya

---

## Ringkasan Eksekutif

Dua pertanyaan tim ini bukan detail kecil — keduanya menyentuh **fondasi kelayakan desain** yang kalau tidak dijawab tegas, akan jadi titik lemah paling gampang diserang saat sesi tanya jawab (bobot 60% dari nilai final). Riset di dokumen ini menemukan bahwa kedua platform acuan industri (Sejasa dan TaskRabbit) sama-sama **tidak memakai satu model harga tunggal**, melainkan model berjenjang — dan pola itu yang paling masuk akal diadaptasi untuk Awetin: **estimasi referensi dari platform sebagai jangkar, tukang tetap punya ruang menyesuaikan dengan wajib alasan tertulis, pengguna approve sebelum kerja dimulai.** Ini langsung menutup dua risiko sekaligus: nego merugikan di tempat (sudah diidentifikasi di riset kepercayaan sebelumnya) dan kekakuan harga fixed yang tidak realistis untuk jasa reparasi yang variatif kerusakannya.

Untuk pertanyaan kedua, ditemukan sesuatu yang penting: **regulasi Indonesia sebenarnya tidak melarang jual-beli atau donasi barang bekas domestik** — yang dilarang cuma impor pakaian bekas dari luar negeri (isu berbeda sama sekali dari fitur yang akan dibangun tim). Tapi ada nuansa regulasi lain yang harus disikapi hati-hati: elektronik yang sudah tidak berfungsi masuk kategori limbah B3 (bahan berbahaya beracun) dan tidak boleh dibuang sembarangan atau bahkan dijual-donasikan tanpa penanganan yang tepat. Temuan ini mengarahkan tim untuk menambahkan **cabang keputusan (decision branch)** di awal flow Awetin — bukan cuma "perbaiki", tapi triase tiga arah: perbaiki, jual/donasi (kalau masih layak pakai), atau arahkan ke saluran daur ulang resmi (kalau sudah benar-benar rusak) — yang sekaligus membuat Awetin selaras penuh dengan hierarki pengelolaan sampah resmi (reduce-reuse-repair-recycle), bukan cuma platform reparasi satu dimensi.

---

## 1. Pertanyaan 1 — Mekanisme Harga: Bagaimana Harga Jasa Dicocokkan?

### 1.1 Riset Pembanding

**TaskRabbit** (marketplace jasa global) ternyata tidak memakai satu model, tapi tiga model sekaligus tergantung jenis tugas:

- **Self-set hourly** — tukang/tasker menetapkan sendiri tarif per jam untuk kategori yang fleksibel (misal bersih-bersih, rakit furnitur) — mereka dapat 100% dari tarif yang mereka tetapkan sendiri.
- **Task-based fixed** — harga tetap per tugas untuk pekerjaan yang sudah terstandardisasi (misal rakit produk IKEA) — tukang dibayar penuh berapapun lama pengerjaannya.
- **Pre-set hourly** — untuk direct-hire, platform yang menentukan tarif.

Yang penting: **harga selalu terlihat jelas di depan sebelum pengguna booking** — setiap penawaran ditandai jenis skema harganya, jadi tidak ada kejutan di lapangan.

**Sejasa** (pembanding lokal paling relevan) memakai **daftar harga referensi yang ditetapkan platform** per jenis servis (misal: pemeriksaan instalasi listrik Rp85.000, pemasangan MCB per titik Rp80.000), tapi dengan disclaimer eksplisit: *"Estimasi harga di atas bisa berbeda sesuai kondisi lapangan dan material/sparepart tambahan."* Providernya tetap menginformasikan biaya aktual sebelum mulai kerja, supaya tidak ada biaya tersembunyi.

**Insight kunci:** Tidak ada satupun dari dua platform ini yang murni membiarkan tukang bebas mematok harga tanpa acuan, dan tidak ada juga yang murni fixed-price kaku tanpa ruang penyesuaian kondisi lapangan. Keduanya memakai **harga referensi/jangkar + ruang penyesuaian yang transparan**.

### 1.2 Kenapa Awetin Tidak Bisa Pakai Fixed Price Murni

Reparasi barang secara sifat sangat variatif — dua HP dengan kerusakan "layar retak" bisa butuh biaya sangat berbeda tergantung tingkat keparahan, model HP, dan ketersediaan spare part. Kalau platform memaksakan satu harga fixed per kategori, dua risiko muncul: (1) tukang menolak kerja yang sebenarnya lebih rumit dari perkiraan karena harga tidak sepadan, atau (2) tukang menerima tapi mengakali dengan kualitas kerja/spare part lebih rendah dari seharusnya. Kedua risiko ini justru bertentangan dengan mekanisme kepercayaan yang sudah dibangun tim di dokumen sebelumnya (garansi sederhana, bukti before/after).

### 1.3 Kenapa Awetin Juga Tidak Bisa Pakai "Tukang Bebas Pasang Harga" Murni

Ini justru mengembalikan masalah yang sudah diidentifikasi sejak riset mekanisme kepercayaan sebelumnya: **nego harga di tempat berpotensi merugikan konsumen**, apalagi dalam konteks tukang informal yang belum tentu terbiasa dengan transparansi harga digital. Ini juga bertentangan langsung dengan temuan riset perilaku konsumen (Bagian 1.2 dokumen sebelumnya) — 22% orang menghindari opsi berkelanjutan karena menganggapnya lebih mahal; kalau harga servis di Awetin terasa tidak transparan/bisa berubah-ubah sewaktu-waktu, ini memperkuat persepsi negatif itu, bukan menjawabnya.

### 1.4 Rekomendasi Flow Harga — "Estimasi Berjenjang dengan Persetujuan Wajib"

Menggabungkan kekuatan kedua model referensi (bukan menyalin mentah salah satu), berikut flow yang direkomendasikan:

**Langkah 1 — Estimasi Awal dari Platform (Jangkar Harga).**
Begitu pengguna mengunggah foto barang rusak dan sistem mendeteksi kategori + tingkat kerusakan (fitur Skor Kelayakan Reparasi yang sudah dirancang sebelumnya), sistem langsung menampilkan **rentang estimasi harga** berdasarkan data historis kategori tersebut (contoh: "Servis ritsleting jaket: estimasi Rp25.000–Rp45.000"). Ini bukan harga final, tapi jangkar referensi supaya pengguna sudah punya ekspektasi wajar sebelum bicara dengan tukang manapun.

**Langkah 2 — Daftar Tukang dengan Penawaran Masing-Masing.**
Tukang yang muncul di daftar bisa menampilkan harga mereka sendiri untuk kategori tersebut — tapi jika harga yang mereka pasang menyimpang jauh dari rentang estimasi platform (baik lebih tinggi atau anehnya lebih rendah dari wajar), sistem memberi label kecil seperti "Di atas estimasi rata-rata" supaya pengguna sadar dan bisa bertanya alasannya, bukan melarang, hanya memberi transparansi.

**Langkah 3 — Konfirmasi Harga Final Setelah Tukang Melihat Detail.**
Setelah pengguna memilih tukang dan mengirim detail kerusakan (foto + deskripsi), tukang wajib mengonfirmasi **harga final** sebelum mulai kerja. Jika harga final berbeda dari penawaran awal (misal ternyata butuh spare part tambahan), tukang **wajib mengisi alasan singkat** (field wajib, bukan opsional) — dan pengguna harus menyetujui secara eksplisit sebelum pekerjaan dimulai. Tidak ada revisi harga sepihak setelah kerja dimulai tanpa persetujuan ulang pengguna.

**Langkah 4 — Harga Aktual Memperkaya Data Estimasi (Feedback Loop).**
Setiap transaksi yang selesai menyumbang data ke sistem estimasi kategori — sehingga rentang estimasi di Langkah 1 makin akurat dari waktu ke waktu, bukan angka statis yang ditetapkan sekali di awal. Ini elemen desain yang bagus untuk ditunjukkan ke juri sebagai bukti pemikiran jangka panjang, meski di prototype Figma cukup direpresentasikan sebagai konsep, bukan sistem backend yang benar-benar berjalan.

**Kenapa flow ini defensible saat tanya jawab:** jawaban singkatnya adalah *"harga bukan dipatok sepihak oleh tukang atau oleh platform, tapi platform memberi jangkar referensi dari data historis, tukang punya ruang wajar untuk menyesuaikan dengan kondisi nyata, dan pengguna selalu jadi pihak yang menyetujui sebelum kerja dimulai — sehingga tidak ada kejutan harga di tempat."* Ini jauh lebih kuat daripada memilih salah satu ekstrem (fixed price kaku atau bebas nego).

---

## 2. Pertanyaan 2 — Bagaimana Jika Pengguna Tidak Ingin Menservis Barangnya?

### 2.1 Kenapa Ini Celah Nyata di Flow Sebelumnya

Benar seperti yang tim amati: seluruh flow yang dirumuskan sebelumnya berasumsi pengguna **selalu** ingin memperbaiki barangnya begitu masuk aplikasi. Padahal secara realistis, tidak semua orang yang punya barang tidak terpakai ingin memperbaikinya — sebagian mungkin sudah bosan, ukurannya tidak muat lagi (pakaian), modelnya ketinggalan zaman, atau kerusakannya memang sudah terlalu parah untuk diperbaiki secara ekonomis. Kalau Awetin hanya menyediakan satu jalur (servis), pengguna dengan kebutuhan ini akan keluar aplikasi dan tetap membuang barangnya — persis skenario yang ingin dihindari, dan sebuah celah besar mengingat brief lomba secara eksplisit soal solusi keberlanjutan menyeluruh, bukan cuma satu skenario sempit.

### 2.2 Riset Regulasi — Apakah Fitur Jual/Donasi Legal di Indonesia?

Ini pertanyaan yang wajib dijawab tuntas sebelum desain dibuat, karena kalau salah, bisa jadi bahan serangan juri yang justru fatal.

**Temuan penting:** Larangan yang ramai dibahas media soal "thrifting" di Indonesia **hanya berlaku untuk pakaian bekas impor dari luar negeri** — alasan pemerintah melarangnya adalah kesehatan (barang tidak disterilkan, berpotensi mengandung bakteri/kimia berbahaya) dan perlindungan industri tekstil domestik dari banjir barang impor murah, bukan soal "menjual barang bekas" itu sendiri.

**Yang sepenuhnya legal:** jual-beli atau donasi barang bekas **yang berasal dari dalam negeri** (barang milik pengguna sendiri yang dibeli/dipakai di Indonesia) — ini dikategorikan sebagai perdagangan barang bekas domestik biasa, bukan impor barang bekas. Untuk berjualan secara formal/skala usaha memang perlu NIB dengan kode KBLI yang sesuai, tapi untuk individu yang menjual/mendonasikan barang miliknya sendiri lewat platform (seperti marketplace preloved pada umumnya: Facebook Marketplace, OLX, Carousell), ini praktik yang sudah lazim dan legal di Indonesia.

**Implikasi untuk desain Awetin:** fitur jual/donasi barang milik pengguna sendiri **tidak melanggar regulasi apapun** yang ditemukan — selama jelas bahwa ini fasilitas peer-to-peer untuk barang domestik milik pengguna, bukan platform impor barang bekas dari luar negeri. Ini penting untuk **ditegaskan eksplisit dalam materi presentasi** (misal lewat teks kecil di layar "khusus barang milik sendiri, bukan barang impor") — bukan karena teknis dibutuhkan di prototype, tapi supaya tim punya jawaban tegas kalau juri sempat mengasosiasikan fitur ini dengan isu thrifting impor yang lagi ramai dibahas publik.

### 2.3 Nuansa Regulasi Kedua — Elektronik yang Sudah Rusak Total Berbeda dari yang Masih Berfungsi

Ini bagian yang perlu disikapi lebih hati-hati. Regulasi Indonesia (PP 101/2014 tentang Pengelolaan Limbah B3, diperkuat PP 27/2020) mengklasifikasikan limbah elektronik (baterai, kabel, lampu, kipas, komputer, TV, mesin cuci, dll) sebagai **limbah B3 (bahan berbahaya beracun)** yang wajib dikelola sesuai standar khusus, terpisah dari sampah biasa.

**Catatan kejujuran riset:** sumber-sumber yang ditemukan **tidak secara eksplisit membedakan** antara elektronik yang sudah benar-benar rusak/dibuang dengan elektronik bekas yang masih berfungsi dan hendak dijual/didonasikan apa adanya. Ini area abu-abu yang sebaiknya **tidak diklaim pasti oleh tim** tanpa konsultasi lebih lanjut ke ahli regulasi lingkungan. Namun, interpretasi yang paling masuk akal dan konsisten dengan praktik yang sudah berjalan (banyak marketplace preloved elektronik seperti Facebook Marketplace/Carousell beroperasi legal di Indonesia untuk barang elektronik bekas yang masih berfungsi) adalah:

- **Elektronik yang masih berfungsi dan dijual/didonasikan apa adanya** → ranahnya perdagangan barang bekas biasa, bukan pengelolaan limbah B3.
- **Elektronik yang sudah tidak berfungsi/rusak total dan pengguna ingin membuangnya** → wajib masuk jalur pengelolaan limbah B3 resmi (dropbox e-waste seperti program Erafone "Jaga Bumi" atau Waste4Change), **tidak boleh** dibuang ke TPS/tempat sampah biasa atau "didonasikan" begitu saja tanpa penanganan yang tepat.

### 2.4 Ekosistem Donasi/Daur Ulang yang Sudah Ada — Awetin Tidak Perlu Membangun dari Nol

Riset menemukan ekosistem donasi/daur ulang barang bekas di Indonesia sudah ada, meski terfragmentasi per kategori — masing-masing organisasi/program hanya menangani satu jenis barang:

| Organisasi/Program | Kategori Barang | Model |
|---|---|---|
| Waste4Change | Sampah daur ulang umum (kertas, plastik, kaca, logam) | Dropbox + jemput, poin ditukar pulsa/bayar listrik |
| Komunitas Saya Pilih Bumi | Sepatu bekas layak pakai | Donasi via Instagram, disalurkan ke yang membutuhkan |
| Ewasterj | Elektronik kecil (komputer, kamera, perangkat kecil) | Dropbox, wajib isi form online dulu |
| Rubah Kertas | Kertas bekas (HVS, folio, kardus) | Kirim ke workshop, diolah jadi produk kertas daur ulang |
| Erafone "Jaga Bumi" | E-waste umum | Dropbox fisik, target ekspansi 25–50 titik di 5 kota besar |

**Insight penting untuk desain:** karena ekosistemnya sudah ada tapi terfragmentasi (pengguna harus tahu sendiri ke organisasi mana harus pergi tergantung jenis barangnya), **Awetin punya peluang jadi "hub triase"** — bukan membangun ulang logistik donasi/daur ulang dari nol (di luar skala kompetisi desain), tapi **mengarahkan pengguna ke saluran yang tepat** berdasarkan kategori dan kondisi barangnya. Ini juga argumen kelayakan yang kuat untuk sesi tanya jawab: tim tidak perlu berpura-pura akan membangun infrastruktur logistik donasi sendiri, cukup menjadi lapisan penghubung (aggregator/router) ke infrastruktur yang sudah berjalan.

### 2.5 Rekomendasi Flow — Triase Tiga Arah di Awal Perjalanan Pengguna

Berdasarkan seluruh temuan di atas, flow Awetin diperluas dengan **satu langkah percabangan baru** persis setelah pengguna mengunggah foto barang (sebelum masuk ke flow servis yang sudah dirancang sebelumnya):

**Langkah baru — "Apa yang kamu inginkan untuk barang ini?"**

1. **"Masih ingin dipakai, mau diperbaiki"** → lanjut ke flow reparasi yang sudah dirancang sebelumnya (foto → kategori → skor kelayakan → tukang → estimasi berjenjang, dst).
2. **"Sudah tidak ingin pakai, tapi masih bagus/berfungsi"** → masuk ke sub-flow Jual/Donasi:
   - Pengguna pilih: Jual (harga ditentukan sendiri, listing sederhana dengan foto kondisi barang wajib — meniru pola before/after yang sudah dibangun untuk kepercayaan reparasi) atau Donasi (diarahkan ke direktori partner sesuai kategori, misal sepatu → Komunitas Saya Pilih Bumi, elektronik kecil → Ewasterj).
   - Ada label kecil "Khusus barang milik sendiri dari dalam negeri" untuk menghindari kesan memfasilitasi barang impor bekas ilegal (lihat Bagian 2.2).
3. **"Sudah rusak parah, tidak berfungsi lagi"** → sistem menilai kategori barang:
   - Elektronik → arahkan ke direktori dropbox e-waste resmi terdekat (Erafone/Waste4Change/Ewasterj), dengan pesan eksplisit "Barang elektronik rusak termasuk limbah B3, jangan dibuang ke tempat sampah biasa."
   - Non-elektronik (pakaian/sepatu yang benar-benar tidak layak) → arahkan ke bank sampah/opsi daur ulang tekstil terdekat.

**Kenapa flow ini penting secara strategis:** ini membuat Awetin secara desain benar-benar mengikuti **hierarki pengelolaan sampah** yang jadi dasar kebijakan lingkungan global (reduce → reuse → repair → recycle → dispose sebagai opsi terakhir) — bukan cuma menawarkan satu opsi (servis) dan diam-diam mengasumsikan sisanya "bukan masalah kami." Ini juga memperkuat kesesuaian dengan tema "Tech for Nature by Crafting Sustainable Digital Solutions" karena solusinya sekarang menyeluruh (whole lifecycle), bukan cuma satu skenario sempit.

---

## 3. Analisa Celah Menyeluruh — Solusi & Flow Sebelumnya vs. Brief, Lingkungan, Masyarakat, Regulasi

### 3.1 Celah yang Sudah Ditemukan dan Ditutup di Dokumen Ini

| Celah | Dampak Kalau Dibiarkan | Status |
|---|---|---|
| Tidak ada mekanisme harga eksplisit | Pertanyaan pertama yang hampir pasti muncul di sesi tanya jawab; tanpa jawaban, terlihat seperti detail yang belum dipikirkan | Ditutup di Bagian 1 |
| Tidak ada skenario "tidak ingin servis" | Flow linear seolah semua pengguna punya niat sama; padahal ini realitas mayoritas kasus barang tidak terpakai | Ditutup di Bagian 2 |
| Belum menyentuh regulasi barang bekas & e-waste | Risiko diasosiasikan dengan isu thrifting impor ilegal yang sedang ramai dibahas publik, atau dianggap tidak paham status B3 elektronik | Ditutup di Bagian 2.2–2.3 |

### 3.2 Celah Baru yang Muncul Setelah Perluasan Flow (Perlu Disikapi Tim)

**Kepercayaan di fitur Jual/Donasi belum sekuat fitur servis.** Mekanisme kepercayaan sebelumnya (verifikasi KTP, rating, before/after, garansi) dirancang untuk transaksi jasa dengan tukang. Untuk transaksi jual-beli barang peer-to-peer, risikonya beda (barang tidak sesuai deskripsi, penipuan listing) — perlu minimal foto kondisi barang wajib saat listing (mengadaptasi pola before/after yang sudah ada) dan sebaiknya dibatasi dulu ke fitur "arahkan ke partner donasi" yang lebih aman secara lingkup kompetisi, dibanding membangun marketplace jual-beli penuh dengan sistem pembayaran sendiri yang di luar skala realistis prototype Figma.

**Dampak sosial pada penerima donasi belum tergali.** Sejauh ini narasi dampak sosial Awetin berpusat ke tukang (pemberdayaan ekonomi informal). Fitur donasi membuka dimensi baru: barang yang didonasikan bermanfaat langsung untuk warga yang membutuhkan (contoh: Komunitas Saya Pilih Bumi menyalurkan sepatu layak pakai ke yang membutuhkan). Ini **peluang penguatan narasi dampak sosial**, bukan sekadar celah — layak dimasukkan eksplisit ke fitur penghitung dampak komunitas yang sudah dirancang sebelumnya (bukan cuma "X barang diperbaiki" tapi juga "Y barang berhasil disalurkan ke warga yang membutuhkan").

**Batas kewenangan tim perlu jelas saat tanya jawab.** Karena Awetin sekarang jadi "hub triase" yang mengarahkan ke partner eksternal (Waste4Change, Erafone, komunitas donasi), tim perlu bahasa yang hati-hati saat presentasi: Awetin **tidak mengklaim membangun ulang infrastruktur** organisasi-organisasi ini, hanya menjadi lapisan penghubung/informasi. Ini justru kekuatan (skala realistis, tidak membual), tapi harus disampaikan dengan percaya diri, bukan terkesan seperti kekurangan solusi.

**Elektronik "abu-abu" (masih nyala tapi separuh rusak) belum ada jalur jelas.** Contoh kasus: HP yang layarnya retak tapi masih bisa dipakai — apakah ini masuk kategori "servis" atau "jual apa adanya"? Sebaiknya di UI, opsi triase (Bagian 2.5) tidak dibuat kaku tiga pilihan terpisah, tapi user tetap bisa berpindah jalur kapan saja (misal mulai dari "mau servis" tapi setelah lihat estimasi harga yang lumayan mahal, ada tombol "atau jual apa adanya" sebagai alternatif) — desain non-linear ini justru mencerminkan pengambilan keputusan nyata pengguna dan sebaiknya dicatat sebagai prinsip desain untuk tahap wireframe berikutnya.

### 3.3 Kesesuaian dengan Brief Lomba — Setelah Perluasan

Dengan tambahan flow triase ini, Awetin sekarang menjawab brief "Tech for Nature by Crafting Sustainable Digital Solutions" secara lebih menyeluruh: solusinya tidak berhenti di satu titik keputusan (servis), tapi mengikuti keseluruhan siklus hidup barang layaknya prinsip ekonomi sirkular resmi. Ini jadi pembeda tambahan dari kompetitor (Sejasa/Kanggo/lakuKan) yang bahkan untuk servis pun tidak mempertimbangkan nasib barang yang tidak ingin diperbaiki penggunanya.

---

## 4. Ringkasan Perubahan pada User Flow Sebelumnya

Untuk kejelasan implementasi, berikut ringkasan bagaimana dua flow di dokumen sebelumnya berubah:

- **Flow 4.1 (Permintaan Reparasi)** — ditambah langkah percabangan triase di awal (sebelum langkah 3), dan langkah 3–5 diperjelas dengan mekanisme "Estimasi Berjenjang" dari Bagian 1.4 dokumen ini.
- **Flow baru — Jual/Donasi/Daur Ulang Resmi** — flow tambahan yang bercabang dari triase, dengan tiga sub-jalur (jual, donasi ke partner, arahkan ke dropbox e-waste/bank sampah resmi).
- **Daftar layar Figma** perlu tambahan: (1) Layar Triase Awal, (2) Layar Listing Jual/Donasi + Upload Foto Kondisi, (3) Layar Direktori Partner Donasi/Daur Ulang per Kategori, (4) Layar Estimasi Harga Berjenjang (revisi dari layar estimasi sebelumnya, sekarang eksplisit menampilkan tahap referensi → penawaran tukang → konfirmasi final).

---

## 5. Sumber

- [How Pricing Works on TaskRabbit — TaskRabbit Blog](https://www.taskrabbit.com/blog/how-pricing-works-on-taskrabbit-and-what-it-means-for-your-earnings/)
- [Ini Harga Jasa Tukang Listrik Terbaru — Sejasa](https://www.sejasa.com/blog/harga-jasa-tukang-listrik-terbaru/)
- [Penjualan Barang Bekas (Thrifting): Aturan Impor, Larangan, dan Legalitas Jual Beli di Indonesia — Legazy](https://legazy.co.id/artikel/penjualan-barang-bekas-thrifting-aturan-impor-larangan-dan-legalitas-jual-beli-di-indonesia/)
- [Pengelolaan Sampah Elektronik dan Peraturannya di Indonesia — Waste4Change](https://waste4change.com/blog/pengelolaan-sampah-elektronik-dan-peraturannya-di-indonesia/)
- [Peraturan Pengelolaan Limbah Elektronik — Mutu Certification](https://mutucertification.com/peraturan-pengelolaan-limbah-elektronik/)
- [PP Nomor 101 Tahun 2014 tentang Pengelolaan Limbah Bahan Berbahaya dan Beracun](https://pelayanan.jakarta.go.id/download/regulasi/peraturan-pemerintah-nomor-101-tahun-2014-tentang-pengelolaan-limbah-bahan-berbahaya-dan-beracun.pdf)
- [5 Tempat Donasi Barang Bekas agar Kembali Bermanfaat — Kompas Lifestyle](https://lifestyle.kompas.com/read/2021/03/08/171908420/5-tempat-donasi-barang-bekas-agar-kembali-bermanfaat?page=all)
- [Dropbox E-waste: Upaya Erafone Perluas Akses Kelola Sampah Elektronik — Katadata Green](https://green.katadata.co.id/berita/68078006bad91/dropbox-e-waste-upaya-erafone-perluas-akses-kelola-sampah-elektronik)

---

## 6. Catatan Penutup & Langkah Selanjutnya

Dokumen ini menutup dua pertanyaan kritis tim (mekanisme harga dan jalur non-servis) sekaligus menemukan bahwa penambahan flow triase justru memperkuat, bukan mempersulit, posisi kompetitif Awetin — karena membuat cakupan solusi lebih menyeluruh mengikuti siklus hidup barang, sekaligus menutup celah regulasi yang berpotensi jadi serangan balik di sesi tanya jawab.

Yang perlu didiskusikan/diputuskan tim sebelum lanjut ke wireframe: (1) apakah fitur "Jual" akan benar-benar dibangun sebagai listing peer-to-peer penuh di prototype, atau cukup direpresentasikan sebagai konsep ringan mengingat kompleksitas kepercayaan yang lebih tinggi dari fitur donasi/reparasi; (2) apakah tim ingin memasukkan seluruh empat kategori (elektronik, pakaian, sepatu, logam) ke prototype, atau fokus ke satu-dua kategori dulu supaya demonstrasi Figma dalam waktu presentasi terbatas tetap fokus dan tidak terasa terlalu banyak untuk dijelaskan sekaligus.
