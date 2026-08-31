<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# ok dari semua hasil riset dan tesis kamu ini dari awal sampai sekarang (didalam chat ini)

aku mau kamu membuatnya menjadi markdown (.MD)

```md
# PNBITC#18 — Riset Domain Pengelolaan Sampah & Food Waste Indonesia

> **Konteks kompetisi:** PNBITC#18 — Desain UI/UX  
> **Subtema:** *Tech for Nature by Crafting Sustainable Digital Solutions*  
> **Deliverable:** Desain aplikasi mobile di Figma, iPhone 16 (393 × 852 px)  
> **Fokus dokumen:** Riset pengelolaan sampah Indonesia, gap aplikasi eksisting, dan arah konsep aplikasi untuk mengurangi sampah sisa makanan (*food waste*).

---

## 1. Batasan Konsep

### In scope

- Solusi berbentuk aplikasi mobile.
- Fokus pada keberlanjutan lingkungan, khususnya pengelolaan sampah dan sisa makanan rumah tangga.
- Memperkuat infrastruktur yang sudah ada: bank sampah, pengepul, TPS3R, komposter komunal, serta mitra pengolahan.
- Berbasis konteks Indonesia.
- Dapat divisualisasikan sebagai user flow, wireframe, UI system, dan prototype Figma.

### Out of scope

- Menggantikan seluruh sistem pengelolaan sampah pemerintah.
- Mengandalkan teknologi yang tidak bisa dibuktikan dalam pengalaman UI/UX.
- Mengasumsikan semua pengguna memiliki halaman rumah, komposter pribadi, kendaraan, atau akses bank sampah.
- Menawarkan klaim pengurangan karbon tanpa metode perhitungan yang transparan.
- Menjadikan poin dan leaderboard sebagai solusi utama tanpa menyelesaikan hambatan perilaku pengguna.

---

# 2. Masalah Sampah di Indonesia

## 2.1 Ringkasan data

- Berdasarkan data SIPSN 2025 yang dikutip dalam pemberitaan KLH, timbulan sampah Indonesia mencapai sekitar **24,8 juta ton per tahun**.
- Sekitar **65,45% atau 16,3 juta ton per tahun** dilaporkan masih belum terkelola.
- Rumah tangga adalah salah satu sumber sampah paling penting untuk ditangani, dengan kontribusi sekitar **56,7%** dari timbulan sampah.
- Komposisi sampah nasional didominasi oleh:
  - Sisa makanan: sekitar **40,8%**
  - Plastik: sekitar **20%**
- Sampah organik/sisa makanan merupakan masalah yang lebih besar secara volume dibanding plastik, tetapi banyak solusi digital lebih fokus pada sampah anorganik bernilai ekonomi.
- Pada awal 2026, pemerintah melaporkan tingkat sampah yang tertangani sekitar **24,95%**, menandakan masih ada kesenjangan besar antara jumlah sampah yang dihasilkan dan yang berhasil dikelola.

> **Catatan penting untuk proposal:** Angka SIPSN dapat berubah berdasarkan jumlah kabupaten/kota yang melaporkan data. Saat digunakan pada slide, cantumkan tahun, sumber, dan konteks cakupan data.

## 2.2 Hambatan perilaku pengguna

Masalah utama bukan hanya kurangnya edukasi tentang sampah.

Pengguna sering kali sudah mengetahui bahwa sampah harus dipilah, tetapi sulit melakukannya secara konsisten karena:

- Tidak punya cukup ruang untuk menyimpan sampah terpilah.
- Tidak punya waktu untuk membersihkan, memilah, dan menyetor sampah.
- Tidak tahu material tertentu harus masuk kategori apa.
- Tidak tahu lokasi penyaluran yang menerima jenis sampah tertentu.
- Tidak yakin apakah sampah yang sudah disetor benar-benar diproses.
- Menganggap proses bank sampah tidak praktis.
- Tidak mendapat manfaat langsung yang terasa dari kebiasaan memilah.

Penelitian terhadap warga perkotaan di Indonesia menunjukkan bahwa keterbatasan **waktu dan ruang** merupakan hambatan besar dalam pemilahan sampah dari rumah. Akses terhadap bank sampah tidak otomatis menghasilkan partisipasi apabila alurnya terasa merepotkan.

---

# 3. Lanskap Aplikasi dan Platform Eksisting

| Aplikasi/platform | Model layanan | Nilai utama | Kekuatan | Gap/peluang UX |
|---|---|---|---|---|
| Rekosistem | Pickup dan drop-off sampah bernilai | Pickup terjadwal, waste station, reward, penyaluran daur ulang | Menghubungkan pengguna dengan pengumpulan dan insentif | Lebih kuat untuk material anorganik bernilai; pengguna tetap perlu memilah, menyimpan, dan memahami aturan material |
| Octopus | Circular economy berbasis produsen | Pelacakan produk pascakonsumsi dan reward ekosistem | Mendukung transparansi material dan keterlibatan brand | Lebih berorientasi pada ekosistem produsen/pengumpul daripada rutinitas rumah tangga |
| AKSI / Aplikasi Data Sampah Indonesia | Digitalisasi bank sampah | Catatan setoran, saldo, transaksi, monitoring data | Mengurangi administrasi manual bank sampah | Fokus pada operasional bank sampah; belum tentu membantu keputusan pemilahan harian pengguna |
| BankIn | Bank sampah digital berbasis insentif | Setor sampah untuk uang, poin, pulsa, voucher | Insentif konkret mudah dipahami | Bergantung pada material bernilai jual; belum menjawab sampah organik |
| Aplikasi bank sampah lokal | Administrasi komunitas | Catat nasabah dan transaksi setoran | Dekat dengan kebutuhan komunitas lokal | Pengalaman pengguna dan data terfragmentasi antarwilayah |
| Ngupahan | Berbagi surplus pangan | Menyalurkan makanan berlebih agar tidak menjadi sampah | Fokus langsung pada food waste rumah tangga urban | Memerlukan manajemen kualitas makanan, waktu, keamanan, dan ketersediaan penerima |

---

# 4. Gap Utama yang Belum Terselesaikan

## 4.1 Friksi sebelum sampah disetor

Pengguna tidak hanya perlu tahu lokasi bank sampah. Mereka perlu menyelesaikan pertanyaan kecil setiap hari:

- Ini sampah apa?
- Bisa didaur ulang atau tidak?
- Harus dicuci atau tidak?
- Harus dikeringkan atau tidak?
- Disimpan di mana?
- Kapan harus disetor?
- Tempat mana yang menerima sampah ini?

### Peluang UX

- Panduan pemilahan berdasarkan foto, scan, atau kategori visual.
- Instruksi sederhana: bilas, keringkan, lipat, pisahkan, atau buang sebagai residu.
- Pengingat ketika tempat penyimpanan sudah penuh.
- Rekomendasi titik penyaluran berdasarkan jenis sampah.
- Mode khusus hunian sempit: kos, apartemen, rumah kecil.

---

## 4.2 Sampah organik kurang terlayani

Sisa makanan merupakan komponen terbesar sampah nasional. Namun banyak layanan digital berfokus pada plastik, kardus, botol, minyak jelantah, atau material lain yang memiliki harga jual.

### Peluang UX

- Jalur pemilahan dua kategori utama:
  - Sampah anorganik bernilai/setor
  - Sampah organik/olah
- Rekomendasi pengolahan organik sesuai kondisi pengguna:
  - Kompos mandiri
  - Komposter komunal
  - Setor ke mitra organik
  - Pengurangan sisa makanan sejak sebelum dibuang
- Panduan sederhana untuk sisa nasi, kulit buah, sayuran, tulang, ampas kopi, dan minyak jelantah.
- Peta fasilitas pengolahan organik yang tersedia di area pengguna.

> Jangan mengasumsikan semua pengguna dapat membuat kompos sendiri. Pengguna kos atau apartemen mungkin tidak memiliki ruang, alat, maupun waktu.

---

## 4.3 Insentif ekonomi belum cukup

Poin dan uang dapat mendorong pengguna untuk menyetor sampah bernilai. Namun, model ini memiliki keterbatasan:

- Harga material sampah dapat berubah.
- Sampah organik dan residu sering tidak bernilai secara ekonomi.
- Reward kecil tidak selalu sebanding dengan usaha memilah dan menyimpan sampah.
- Pengguna bisa berhenti saat insentif terasa tidak menarik.

### Peluang UX

- Transparansi estimasi harga material sebelum pengguna menyetor.
- Insentif komunitas, misalnya target RT, potongan iuran lingkungan, atau kontribusi kegiatan warga.
- Penghargaan untuk perilaku yang tidak punya nilai jual langsung, seperti mengurangi food waste.
- Bukti manfaat praktis: uang yang dihemat karena makanan tidak terbuang.

---

## 4.4 Kesenjangan antara aksi dan dampak

Pengguna dapat menyetor sampah, tetapi tidak selalu tahu apa yang terjadi setelah itu.

### Peluang UX

- Riwayat perjalanan setoran:
  - Dikumpulkan
  - Diverifikasi
  - Diteruskan ke mitra
  - Diolah/didaur ulang
- Bukti setoran dan status penyaluran.
- Dashboard komunitas yang membedakan:
  - Sampah terkumpul
  - Sampah terverifikasi
  - Sampah benar-benar tersalurkan
- Hindari klaim seperti “Anda menyelamatkan bumi” tanpa data atau metode yang jelas.

---

## 4.5 Infrastruktur lokal yang terfragmentasi

Bank sampah tersebar di banyak wilayah, tetapi setiap lokasi dapat memiliki:

- Jadwal yang berbeda.
- Jenis material yang berbeda.
- Harga beli yang berbeda.
- Sistem pencatatan yang berbeda.
- Kapasitas layanan yang berbeda.

### Peluang UX

- Aplikasi sebagai penghubung, bukan pengganti bank sampah.
- Peta fasilitas lokal dengan informasi:
  - Jam operasional
  - Jenis sampah yang diterima
  - Syarat kebersihan material
  - Harga estimasi
  - Status aktif/nonaktif
  - Jadwal pickup
- Mode admin ringan untuk bank sampah:
  - Input timbang
  - Update harga
  - Konfirmasi pickup
  - Verifikasi setoran

---

# 5. Fokus Khusus: Sampah Sisa Makanan

## 5.1 Mengapa food waste penting

Sisa makanan menyumbang sekitar **40,8%** dari total komposisi sampah nasional. Artinya, solusi sampah yang hanya berfokus pada plastik belum menangani sumber sampah terbesar dari rumah tangga.

Food waste dapat terjadi karena:

- Membeli bahan makanan terlalu banyak.
- Lupa bahan makanan yang tersimpan di kulkas.
- Tidak memahami tanggal kedaluwarsa dan *best before*.
- Memasak dalam porsi terlalu besar.
- Tidak tahu cara menggunakan bahan hampir rusak.
- Tidak tahu cara menyimpan bahan dengan benar.
- Sisa makanan matang langsung dibuang.
- Tidak ada fasilitas pengolahan organik yang mudah dijangkau.

## 5.2 Prinsip desain untuk food waste

Aplikasi sebaiknya mengikuti hierarki berikut:

1. **Mencegah:** jangan beli atau masak berlebihan.
2. **Menggunakan kembali:** masak bahan yang hampir habis atau olah sisa makanan.
3. **Membagikan:** salurkan makanan yang masih layak konsumsi.
4. **Mengolah:** kompos atau salurkan sisa organik.
5. **Membuang dengan benar:** pisahkan residu yang tidak dapat diolah.

Prioritas utama adalah mencegah makanan menjadi sampah, bukan hanya mengelola sampah setelah makanan rusak.

---

# 6. Daftar Fitur Aplikasi Food Waste

| Fitur | Masalah yang diselesaikan | Bentuk UI/UX |
|---|---|---|
| Stok Dapur Cepat | Pengguna lupa bahan makanan yang dimiliki | Scan struk, foto bahan, atau input cepat |
| Duluan Habis | Bahan mendekati rusak terlupakan | Kartu prioritas “gunakan hari ini” |
| Pengingat adaptif | Notifikasi generik sering diabaikan | Reminder berdasarkan tanggal beli, jenis bahan, dan kebiasaan pengguna |
| Resep dari bahan tersisa | Pengguna bingung mengolah bahan | Pilih bahan tersisa lalu tampilkan resep sederhana |
| Meal planner | Pengguna memasak atau membeli berlebihan | Rencana menu mingguan dan daftar belanja otomatis |
| Pengatur porsi | Sisa makanan matang terlalu banyak | Pilihan porsi 1–5 orang dan estimasi bahan |
| Label kesegaran | Pengguna bingung dengan tanggal makanan | Status: gunakan segera, cek kondisi, tidak layak konsumsi |
| Mode sisa makanan | Sisa makanan matang langsung dibuang | Pilihan: simpan ulang, olah jadi menu baru, bagikan, atau olah organik |
| Berbagi surplus | Makanan layak konsumsi tidak habis | Post surplus makanan, waktu ambil, jumlah porsi |
| Panduan organik | Sisa makanan tercampur residu | Kategori sisa makanan dan instruksi pemilahan |
| Peta fasilitas organik | Pengguna tidak punya tempat kompos | Lokasi komposter komunal, TPS3R, atau mitra pengolahan |
| Ringkasan penghematan | Dampak kebiasaan terasa abstrak | Bahan terselamatkan, porsi terselamatkan, estimasi uang belanja yang dihemat |

---

# 7. Konsep Rekomendasi: “Duluan”

## 7.1 Deskripsi konsep

**Duluan** adalah aplikasi mobile asisten dapur yang membantu pengguna mencegah makanan menjadi sampah.

Aplikasi memprioritaskan bahan makanan yang harus segera digunakan, memberikan ide resep dari stok yang tersisa, membantu pengguna merencanakan porsi, dan mengarahkan sisa makanan yang tidak dapat dikonsumsi ke pengolahan organik yang tepat.

## 7.2 Target pengguna

> **Asumsi desain — bukan fakta dari juklak:**  
> Target pengguna utama adalah mahasiswa, pekerja muda, pasangan muda, atau penghuni kos/apartemen di kota besar Indonesia yang memiliki akses kulkas tetapi ruang penyimpanan dan waktu terbatas.

### Karakteristik target pengguna

- Berbelanja bahan makanan mingguan atau beberapa kali seminggu.
- Sering lupa bahan yang tersimpan di kulkas.
- Ingin hidup lebih hemat dan ramah lingkungan.
- Tidak ingin melakukan input data panjang setiap hari.
- Tidak selalu memiliki akses ke komposter pribadi.
- Membutuhkan solusi cepat dan praktis.

---

# 8. Fitur Inti Konsep “Duluan”

## 8.1 Stok Dapur Cepat

Pengguna memasukkan bahan makanan melalui:

- Scan struk.
- Foto bahan.
- Pilihan bahan umum.
- Input manual singkat.

### Tujuan

Mengurangi beban pengguna saat mencatat bahan makanan.

### Prinsip UX

- Jangan meminta detail terlalu banyak.
- Gunakan preset seperti: “telur”, “nasi”, “ayam”, “bayam”, “pisang”, “roti”.
- Tawarkan estimasi tanggal penggunaan berdasarkan jenis bahan, tetapi pengguna dapat mengubahnya.

---

## 8.2 Kartu “Pakai Dulu”

Beranda menampilkan maksimal tiga bahan prioritas.

Contoh:

- Gunakan hari ini: ayam fillet
- Gunakan besok: pisang
- Masih aman disimpan: wortel

### Tujuan

Mengurangi kebingungan pengguna saat melihat banyak stok bahan.

### Prinsip UX

- Satu tindakan utama per kartu.
- Gunakan bahasa praktis, bukan bahasa menghakimi.
- Hindari notifikasi berlebihan.
- Tampilkan alasan prioritas: “dibeli 4 hari lalu” atau “mendekati batas konsumsi yang kamu atur”.

---

## 8.3 Resep dari Bahan Tersisa

Pengguna memilih bahan yang tersedia lalu aplikasi menampilkan resep yang sesuai.

Contoh:

- Nasi + telur + sayur sisa → nasi goreng sayur.
- Pisang + roti → roti pisang panggang.
- Ayam + sayur → tumis ayam sederhana.

### Tujuan

Membantu pengguna mengubah bahan tersisa menjadi makanan, bukan sampah.

### Prinsip UX

- Tampilkan resep sederhana.
- Gunakan bahan yang realistis untuk dapur Indonesia.
- Sediakan filter:
  - Waktu memasak
  - Jumlah porsi
  - Tingkat kesulitan
  - Bahan tambahan minimum
- Jangan membuat resep terlalu aspiratif atau membutuhkan bahan mahal.

---

## 8.4 Meal Planner dan Pengatur Porsi

Fitur ini membantu pengguna merencanakan makan dan belanja secukupnya.

### Elemen UI

- Kalender menu mingguan.
- Pilihan jumlah penghuni rumah.
- Pengatur porsi.
- Daftar belanja otomatis.
- Indikator bahan yang sudah tersedia di stok.

### Tujuan

Mencegah pembelian bahan berlebihan dan memasak dalam porsi terlalu besar.

---

## 8.5 Mode Sisa Makanan

Saat pengguna memiliki sisa makanan matang, aplikasi menawarkan tindakan berikut:

- Simpan dengan cara yang benar.
- Ubah menjadi resep baru.
- Bagikan ke orang sekitar jika masih layak konsumsi.
- Olah menjadi kompos atau salurkan sebagai sampah organik.
- Buang sebagai residu jika tidak dapat dimanfaatkan.

### Tujuan

Mencegah alur default “sisa makanan = langsung dibuang”.

---

## 8.6 Panduan Sampah Organik

Jika makanan tidak lagi layak dikonsumsi, aplikasi memberi panduan:

| Jenis sisa | Rekomendasi |
|---|---|
| Kulit buah dan sayur | Kompos atau pengolahan organik |
| Sisa nasi | Kompos/pengolahan organik jika fasilitas tersedia |
| Ampas kopi/teh | Kompos dalam jumlah terbatas |
| Tulang | Residu atau fasilitas khusus |
| Minyak jelantah | Jangan dibuang ke saluran air; salurkan ke titik pengumpulan |
| Makanan berkuah/berminyak | Pisahkan cairan dan padatan bila memungkinkan, lalu ikuti panduan fasilitas lokal |

> Catatan: Informasi keamanan dan pengolahan makanan harus dibuat hati-hati. Aplikasi tidak boleh menggantikan saran ahli kesehatan atau layanan pengelolaan sampah lokal.

---

# 9. User Flow Utama

## 9.1 Alur mencegah food waste

```text
Onboarding
→ Pilih tipe hunian
→ Pilih jumlah penghuni
→ Tambah stok dapur
→ Beranda “Pakai Dulu”
→ Pilih bahan prioritas
→ Pilih resep / simpan / bagikan
→ Tandai bahan berhasil digunakan
→ Lihat ringkasan penghematan
```


## 9.2 Alur menangani sisa makanan

```text
Pengguna memiliki sisa makanan
→ Buka Mode Sisa Makanan
→ Pilih kondisi makanan:
   masih layak / hampir tidak layak / tidak layak
→ Aplikasi menawarkan opsi:
   simpan / olah kembali / bagikan / olah organik / residu
→ Pengguna memilih aksi
→ Aplikasi mencatat hasil tindakan
```


## 9.3 Alur organik

```text
Sisa makanan tidak dapat dikonsumsi
→ Pilih jenis sisa
→ Aplikasi memberi instruksi pemilahan
→ Pilih opsi:
   kompos mandiri / titik organik / fasilitas komunal / residu
→ Lihat lokasi atau panduan
→ Konfirmasi tindakan
```


---

# 10. Layar Prototype Figma yang Disarankan

| No. | Nama layar | Tujuan |
| :-- | :-- | :-- |
| 1 | Splash screen | Memperkenalkan identitas aplikasi |
| 2 | Onboarding | Memahami tipe hunian, jumlah penghuni, pola belanja |
| 3 | Izin notifikasi | Menjelaskan manfaat reminder bahan prioritas |
| 4 | Beranda “Pakai Dulu” | Menampilkan bahan yang perlu digunakan |
| 5 | Tambah bahan | Scan/foto/input manual |
| 6 | Detail bahan | Status kesegaran, cara simpan, resep, aksi |
| 7 | Resep dari stok | Menampilkan resep berdasarkan bahan tersedia |
| 8 | Meal planner | Merencanakan menu dan porsi |
| 9 | Mode sisa makanan | Menentukan tindakan terhadap makanan tersisa |
| 10 | Panduan organik | Klasifikasi dan instruksi sisa makanan |
| 11 | Peta penyaluran | Lokasi komposter komunal atau mitra |
| 12 | Ringkasan dampak | Bahan terselamatkan dan penghematan |
| 13 | Profil dan preferensi | Mengatur hunian, notifikasi, serta aksesibilitas |


---

# 11. Design Rationale untuk Presentasi

## Masalah

Pengguna sering membuang makanan bukan karena tidak peduli lingkungan, tetapi karena:

- Lupa bahan yang disimpan.
- Tidak tahu cara memanfaatkan bahan mendekati rusak.
- Tidak merencanakan porsi.
- Tidak memiliki alur mudah untuk menangani sisa makanan.


## Solusi

Aplikasi tidak hanya mencatat makanan. Aplikasi membantu pengguna mengambil keputusan pada saat yang tepat:

- Sebelum berbelanja.
- Saat bahan hampir rusak.
- Saat memasak.
- Saat memiliki sisa makanan.
- Saat sisa makanan sudah tidak layak konsumsi.


## Alasan memilih fitur “Pakai Dulu”

- Mengurangi beban kognitif pengguna.
- Memberikan satu prioritas yang jelas.
- Tidak membuat pengguna mengisi log panjang.
- Mengintervensi sebelum bahan berubah menjadi sampah.
- Mudah dibuktikan melalui prototype UI/UX.


## Alasan tidak menjadikan gamifikasi sebagai inti

Gamifikasi dapat meningkatkan engagement, tetapi tidak selalu menghasilkan perubahan perilaku jangka panjang.

Karena itu, aplikasi memprioritaskan:

- Kemudahan tindakan.
- Informasi yang relevan.
- Pengingat adaptif.
- Penghematan yang terlihat.
- Alur penanganan sisa makanan yang realistis.

Gamifikasi dapat digunakan sebagai fitur pendukung, misalnya badge kebiasaan mingguan, tetapi tidak boleh menjadi fondasi solusi.

---

# 12. Risiko Konsep dan Mitigasi

| Risiko | Dampak | Mitigasi desain |
| :-- | :-- | :-- |
| Pengguna malas mencatat stok | Aplikasi tidak memiliki data bahan | Gunakan input cepat, preset, scan struk, dan pilihan foto |
| Pengingat mengganggu | Pengguna mematikan notifikasi | Gunakan reminder adaptif dan batasi jumlah notifikasi |
| Prediksi kesegaran tidak akurat | Pengguna kehilangan kepercayaan | Gunakan bahasa rekomendasi, beri opsi edit, dan jangan memberi klaim keamanan pangan mutlak |
| Resep terlalu rumit | Pengguna tidak menggunakan fitur | Prioritaskan resep singkat dengan bahan umum Indonesia |
| Tidak ada fasilitas organik terdekat | Pengguna tidak dapat menyalurkan sisa | Tampilkan alternatif sesuai kondisi: pengurangan, kompos sederhana, residu terpisah |
| Fitur berbagi makanan berisiko | Potensi masalah kualitas dan keamanan makanan | Batasi pada makanan layak konsumsi, tampilkan waktu batas ambil, dan gunakan disclaimer kondisi makanan |
| Dampak terlalu abstrak | Pengguna tidak termotivasi | Tampilkan indikator praktis: bahan terselamatkan dan estimasi uang yang tidak terbuang |


---

# 13. Metrik Dampak yang Disarankan

Gunakan metrik yang dapat dipahami dan tidak berlebihan.

### Metrik utama

- Jumlah bahan yang berhasil digunakan sebelum rusak.
- Jumlah porsi makanan yang terselamatkan.
- Estimasi nilai belanja yang tidak terbuang.
- Jumlah sisa makanan yang diarahkan ke pengolahan organik.
- Frekuensi pengguna membuat rencana porsi.
- Frekuensi pengguna memakai resep dari stok tersisa.


### Hindari klaim berikut tanpa metodologi jelas

- “Mengurangi emisi karbon sebesar X kg.”
- “Menyelamatkan bumi.”
- “Mengurangi sampah nasional sebesar X%.”
- “Menjamin makanan tetap aman dikonsumsi.”

---

# 14. Data Siap Pakai untuk Proposal

- “Rumah tangga merupakan sumber penting sampah nasional dan menyumbang sekitar 56,7% dari timbulan sampah.”
- “Sisa makanan merupakan komponen sampah terbesar di Indonesia, sekitar 40,8% dari total komposisi sampah nasional.”
- “Plastik penting untuk ditangani, tetapi porsinya berada di bawah sisa makanan, sekitar 20% dari komposisi sampah.”
- “Berdasarkan data SIPSN yang dikutip pada 2025, sekitar 65,45% sampah masih belum terkelola.”
- “Hambatan pemilahan sampah bukan hanya kurangnya kesadaran. Pengguna juga menghadapi keterbatasan waktu, ruang, dan akses terhadap sistem penyaluran yang praktis.”
- “Karena itu, desain solusi perlu mengurangi friksi perilaku sehari-hari, bukan hanya memberi informasi lingkungan.”

---

# 15. Sumber Rujukan

- Sistem Informasi Pengelolaan Sampah Nasional (SIPSN) — Kementerian Lingkungan Hidup.
- Kementerian Lingkungan Hidup/Badan Pengendalian Lingkungan Hidup, Rakornas Pengelolaan Sampah 2026.
- Katadata Databoks, “Indonesia’s Waste Dominated by Food Waste and Plastic.”
- Studi “Understanding Public Participation in Waste Sorting in Indonesia.”
- Rekosistem.
- Octopus Indonesia.
- AKSI / Aplikasi Data Sampah Indonesia.
- BankIn.
- Ngupahan.
- UNEP Food Waste Index.
- Studi tentang aplikasi self-monitoring bergamifikasi untuk pengurangan food waste rumah tangga.
- Systematic review digital interventions for food waste reduction.

---

# 16. Kesimpulan Arah Konsep

Konsep yang paling kuat untuk dikembangkan adalah aplikasi mobile yang membantu pengguna **mencegah sampah sisa makanan sejak dari dapur**, bukan hanya mencatat sampah setelah makanan dibuang.

Arah konsep utama:

> **Duluan — aplikasi asisten dapur yang membantu pengguna menggunakan bahan makanan sebelum terbuang, merencanakan porsi secara realistis, mengolah sisa makanan, dan menyalurkan sampah organik dengan benar.**

Nilai pembeda konsep:

- Menangani akar food waste: lupa bahan, belanja berlebih, dan porsi berlebih.
- Tidak bergantung penuh pada poin atau hadiah.
- Mengakomodasi pengguna dengan ruang dan waktu terbatas.
- Menggabungkan pencegahan food waste dengan penanganan organik.
- Memiliki user flow yang jelas dan mudah divisualisasikan dalam prototype Figma.
- Relevan dengan masalah sampah rumah tangga di Indonesia.

```
```

