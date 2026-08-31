# Product Requirements Document (PRD) Lengkap: Awetin
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Disusun:** 31 Agustus 2026 (Revisi 2 — pasca-audit)
**Status:** Blueprint final untuk tahap wireframe/hi-fi Figma
**Konteks:** Menerjemahkan seluruh riset ("Deep Research - Ekosistem Menyeluruh Awetin.md" dan dokumen-dokumen sebelumnya) menjadi satu dokumen produk tunggal — tidak ada flow yang buntu dari awal sampai akhir

---

## Catatan Revisi 2 (Pasca-Audit)

Dokumen ini direvisi setelah audit mandiri menemukan beberapa masalah di versi pertama. Perubahan utama:

1. **Nama produk diganti dari "TukangIn" menjadi "Awetin"** — nama sebelumnya ternyata sudah dipakai beberapa aplikasi dan skripsi lain di domain yang sama persis (jasa tukang online), berisiko terhadap syarat "orisinalitas mutlak" di juklak lomba. **"Awetin" adalah usulan kerja, bukan keputusan final** — tim tetap perlu memverifikasi sendiri (cek Google Play, App Store, PDKI/merek terdaftar) sebelum benar-benar dipakai di proposal, karena riset saya juga tidak bisa memastikan 100% nama ini bebas konflik.
2. **Lima celah struktural ditutup:** mekanisme segmentasi barang besar/kecil dijelaskan eksplisit, timing Biaya Jasa Tetap diperbaiki supaya benar-benar melindungi tukang, hubungan antara dua estimasi harga diperjelas, Flow Jual ditambah sisi pembeli, dan model komisi dijadikan asumsi eksplisit (bukan menggantung).
3. **Celah minor ditutup:** fallback "tidak ada tukang di radius" di flow servis, fallback negosiasi chat gagal sepakat, izin lokasi (GPS), fitur pencarian teks, consent data lokasi (selain KTP), dan koreksi rekomendasi MVP.

---

## 0. Cara Membaca Dokumen Ini

Dokumen ini dirancang sebagai rujukan tunggal yang bisa dibuka tim kapan pun butuh jawaban "kenapa fitur ini ada" atau "apa langkah selanjutnya kalau user melakukan X". Setiap keputusan di dokumen ini ditelusuri balik ke temuan riset spesifik (bukan asumsi bebas), sesuai prinsip yang sudah dipegang sepanjang sesi ini. Kalau ada bagian yang masih berupa keputusan terbuka untuk tim, ditandai eksplisit di Bagian 14.

---

## 1. Ringkasan Eksekutif

**Awetin** adalah platform yang mempertemukan pemilik barang rusak dengan tukang reparasi informal terdekat (elektronik kecil, jahit/pakaian, sepatu, las), dengan tiga pilar nilai: mengurangi barang yang berakhir di TPA lewat reparasi, memberi visibilitas digital ke tukang informal yang selama ini sulit ditemukan generasi baru pengguna belanja online, dan — kalau reparasi memang bukan pilihan tepat — mengarahkan pengguna ke jalur jual, donasi, atau daur ulang resmi, bukan sekadar dibuang.

**Value proposition:** *"Rusak? Jangan dibuang. Perbaiki — dan bantu tukang lokal tetap ada."*

**Target pengguna:** dua sisi — (1) pemilik barang dari berbagai kalangan usia & latar belakang di kawasan urban/sub-urban Indonesia, dan (2) tukang reparasi informal (tukang servis elektronik kecil, penjahit rumahan/keliling, tukang sol sepatu, tukang las) yang ingin mendapat pelanggan baru lewat visibilitas digital.

---

## 2. Tujuan Produk & Metrik Keberhasilan (untuk Narasi Presentasi)

Karena ini produk kompetisi (bukan aplikasi yang benar-benar dioperasikan), metrik di bawah berfungsi sebagai **kerangka argumen** saat presentasi/tanya jawab — bukti bahwa tim merancang dengan tujuan terukur, bukan asal menambah fitur.

| Tujuan | Indikator Keberhasilan (Konseptual) |
|---|---|
| Mengurangi barang masuk TPA lewat reparasi | Jumlah barang diperbaiki per wilayah per bulan (ditampilkan di dashboard komunitas) |
| Memberi visibilitas ke tukang informal | Jumlah tukang aktif per kategori/wilayah, pertumbuhan pesanan per tukang |
| Menjawab kebutuhan barang yang tidak ingin diperbaiki | Jumlah barang tersalur lewat jalur jual/donasi/daur ulang resmi (bukan cuma servis) |
| Membangun kepercayaan transaksi | Rating rata-rata tukang, tingkat penyelesaian pesanan tanpa komplain |
| Retensi yang etis (bukan retensi paksa) | Persentase pengguna yang memakai fitur riwayat/garansi/dampak, bukan cuma transaksi sekali pakai |

---

## 3. Persona Pengguna

### 3.1 Persona A — "Bu Rina", Pemilik Barang (Pengguna Utama)

Perempuan 30–45 tahun, tinggal di kawasan urban/sub-urban, punya barang rusak (setrika mati, baju robek, sepatu anak jebol) tapi tidak tahu ke mana harus mencari tukang tepercaya sejak kebiasaan belanja bergeser ke online. Peduli lingkungan tapi bukan aktivis — kepeduliannya butuh jalan yang mudah, bukan effort besar. *(Berdasarkan temuan attitude-behavior gap: 62,9% pernah beli produk ramah lingkungan, tapi terhambat akses.)*

### 3.2 Persona B — "Pak Anung", Tukang Reparasi Informal (Mitra)

Laki-laki 40–60 tahun, tukang sol sepatu/servis elektronik kecil/penjahit, sudah puluhan tahun berjualan di lokasi tetap atau keliling, pelanggan menyusut pasca-pandemi bukan karena kehilangan keahlian tapi kehilangan visibilitas. Literasi digital terbatas — butuh onboarding yang sangat sederhana, bukan form rumit ala pendaftaran mitra korporat. *(Berdasarkan kisah nyata tukang Gang Kote, Bandung.)*

### 3.3 Persona C — "Dimas", Tukang Muda/Semi-Profesional (Mitra Sekunder)

Laki-laki 20–35 tahun, punya keahlian servis elektronik/las, lebih melek digital dibanding Persona B, kemungkinan mengelola profil sendiri tanpa bantuan, bisa jadi pengguna awal yang paling cepat aktif di fase bootstrap.

*(Catatan desain: persona B dan C sama-sama masuk kategori "Tukang/Mitra" di produk, tapi kebutuhan onboarding-nya beda tingkat kerumitan — dijelaskan di Bagian 8.9.)*

---

## 4. Prinsip Desain

1. **Akses sebelum edukasi.** Hambatan pengguna bukan kurang peduli, tapi kurang tahu ke mana harus pergi — desain harus meminimalkan langkah antara "punya masalah" dan "ketemu solusi".
2. **Transparansi di setiap titik keputusan.** Harga, status verifikasi tukang, dan penggunaan data pribadi harus terlihat jelas, tidak disembunyikan di balik proses otomatis yang tidak dijelaskan.
3. **Tidak ada jalan buntu.** Setiap flow harus punya jalur lanjutan yang jelas — termasuk saat AI gagal mendeteksi, tukang tidak tersedia, atau pengguna berubah pikiran di tengah proses.
4. **Retensi yang etis, bukan retensi paksa.** Sesuai jawaban untuk pertanyaan Zikru — pengguna boleh saja lepas dari aplikasi setelah cocok dengan satu tukang; desain hanya perlu memberi alasan organik untuk kembali (riwayat, garansi, dampak), bukan mengunci pengguna secara artifisial.
5. **Aksesibel & ringan sebagai bagian dari "sustainable design", bukan tempelan.** Kontras warna, ukuran target sentuh, dan kesederhanaan visual bukan checklist terpisah dari tema lingkungan — keduanya bagian dari filosofi yang sama.

---

## 5. Informasi Arsitektur & Navigasi

### 5.1 Ide Navbar dari Tim (Referensi Awal)

Tim mengusulkan default user: **Home** (tombol fitur utama, fast action, banner promosi, kategori reparasi, rekomendasi terdekat), **My Reparasi** (berisi Scan — fitur AI untuk scan barang & interaksi AI demi petunjuk detail), **Aktifitas** (riwayat reparasi, penyaluran limbah barang, dll), **Profile** (halaman standar). Tim juga bertanya apakah UI tukang perlu berbeda.

### 5.2 Revisi & Modifikasi yang Diusulkan

Struktur dasar tim sudah tepat dan dipertahankan — perubahan yang diusulkan bersifat penyempurnaan, bukan penggantian:

**Perubahan 1 — "My Reparasi" diperluas jadi "Perbaiki" dan dipindah jadi tombol aksi utama di Home, bukan tab terpisah.** Alasan: fitur Scan adalah titik masuk paling penting (jawaban langsung ke masalah inti — akses, sesuai Prinsip Desain #1), jadi sebaiknya tidak "tersembunyi" di tab kedua. Namun riwayat hasil scan/reparasi yang sedang berjalan tetap butuh rumah — dipindah ke tab **Pesanan** (lihat Perubahan 2).

**Perubahan 2 — "Aktifitas" diganti nama jadi "Pesanan" dan diperluas cakupannya**, supaya lebih jelas fungsinya menampung *status pesanan aktif* (bukan cuma riwayat) — ini penting karena flow servis butuh tempat memantau progres (diterima tukang → proses → selesai) yang sebelumnya belum ada rumahnya di ide navbar awal. Isi tab ini: Pesanan Aktif, Riwayat Servis (dengan status garansi), dan Riwayat Penyaluran Limbah/Donasi.

**Perubahan 3 — Tambah tab "Tukang" sebagai tab kelima**, menjawab dua kebutuhan sekaligus: (a) direktori eksplorasi tukang per kategori/wilayah, dan (b) daftar "Tukang Favorit" untuk booking ulang cepat — ini jawaban desain langsung untuk pertanyaan disintermediasi Zikru (retensi organik, bukan paksa), dan konsisten dengan pola "akses cepat ke fitur yang sering dipakai" yang terbukti bekerja di Gojek.

**Perubahan 4 — Tambah elemen "Dampak Komunitas" sebagai kartu ringkasan di Home (bukan tab terpisah, supaya navbar tidak terlalu padat)**, dengan halaman detail dampak bisa diakses dari kartu ini. Ini menjawab kebutuhan dashboard dampak dari riset sebelumnya tanpa menambah tab keenam yang membuat navbar terlalu ramai.

**Navbar final (5 tab):** **Home** — **Pesanan** — **Perbaiki (tombol tengah, ditonjolkan)** — **Tukang** — **Profil**.

**Catatan tambahan (celah yang ditemukan saat audit):** tab **Tukang** juga menampung sub-bagian **Jual-Beli** — direktori listing barang bekas warga sekitar dari Flow 7.6 (Jual). Ini penting supaya listing yang dibuat pengguna di flow Jual/Donasi punya "rumah" untuk ditemukan pembeli lain — versi pertama dokumen ini menjelaskan cara *membuat* listing tapi tidak pernah menjelaskan di mana listing itu muncul untuk dilihat orang lain, sehingga flow-nya buntu di tengah jalan. Detail lengkap ada di Flow 7.6 yang sudah direvisi.

### 5.3 Menjawab Pertanyaan Tim — Apakah UI Tukang Perlu Beda?

Jawabannya **ya, tegas berbeda** — ini bukan cuma preferensi desain, tapi kebutuhan fungsional nyata. Pengguna (pemilik barang) dan tukang (mitra) punya *job to be done* yang sepenuhnya berbeda: satu mencari & meminta jasa, satu menerima & mengerjakan jasa. Kalau dipaksa dalam satu navbar yang sama, kemungkinan besar akan membingungkan (Persona B, tukang dengan literasi digital terbatas, butuh antarmuka yang sangat sederhana dan fokus, bukan navbar multifungsi yang juga menampung fitur pencarian tukang lain).

**Rekomendasi:** dua mode antarmuka terpisah, dipilih di layar Onboarding awal ("Saya ingin memperbaiki/menjual barang" vs "Saya tukang, ingin menerima pesanan") — bukan toggle di dalam satu akun yang sama (ini mempermudah proses desain di Figma dan lebih realistis, karena mayoritas orang cenderung salah satu peran, meski secara konsep tidak menutup kemungkinan satu akun punya dua peran).

**Navbar Tukang (4 tab, lebih sederhana dari sisi pengguna):** **Pesanan Masuk** (utama, termasuk terima/tolak order) — **Profil Usaha** (kelola kategori, harga, foto before/after) — **Pendapatan** (riwayat transaksi, transparan, jawaban langsung untuk isu status "mitra" minim proteksi dari riset regulasi) — **Notifikasi**.

---

## 6. Daftar Fitur Lengkap per Modul

### 6.1 Modul Perbaiki (Sisi Pengguna)

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Scan AI | Ambil/unggah foto barang, AI mendeteksi kategori & jenis kerusakan dengan skor keyakinan | Bagian 10 Deep Research — AI damage assessment butuh confidence score |
| Skor Kelayakan Reparasi | Estimasi "layak diperbaiki" vs "mungkin lebih baik diganti" + estimasi biaya vs beli baru | French Repairability Index (adaptasi) |
| Triase 3 Arah | Percabangan: Perbaiki / Jual-Donasi / Daur Ulang Resmi | Analisa celah — tidak semua orang ingin servis |
| Estimasi Berjenjang | Jangkar harga dari platform → penawaran tukang → persetujuan wajib pengguna. **Catatan penting:** ini SATU sistem estimasi, bukan dua — angka yang muncul di Skor Kelayakan Reparasi (langkah awal, sebelum triase) dan "Rentang Harga Dasar" di Flow Servis Barang Besar adalah angka yang sama, ditampilkan ulang di titik yang berbeda supaya pengguna tidak perlu mengingat-ingat. Versi pertama dokumen ini tidak menjelaskan ini sehingga terlihat seperti dua estimasi berbeda | Riset TaskRabbit/Sejasa + sistem "anti-tembak" tim |
| Direktori Tukang Terdekat | Daftar tukang per kategori & jarak, dengan rating dan foto before/after | Riset kepercayaan sebelumnya |
| Cari Tukang (Pencarian Teks) | Cari berdasarkan nama tukang atau kata kunci jasa (misal "jahit ritsleting"), pelengkap direktori berbasis kategori | Celah ditemukan saat audit — direktori kategori saja tidak cukup untuk pengguna yang sudah tahu mau cari apa |
| Tukang Favorit | Booking ulang cepat ke tukang yang sudah dikenal | Jawaban pertanyaan disintermediasi Zikru + pola UX Gojek |

### 6.2 Modul Pesanan (Sisi Pengguna)

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Status Pesanan Real-Time (konsep) | Diterima → proses → selesai | Standar flow marketplace jasa |
| Invoice Digital & Persetujuan | Harga final wajib disetujui sebelum kerja dimulai | Sistem "anti-tembak" tim (barang besar) |
| Riwayat & Garansi | Riwayat servis dengan status masa garansi aktif | Mekanisme kepercayaan sebelumnya |
| Bukti Before/After | Foto sebelum-sesudah per transaksi | Mekanisme kepercayaan sebelumnya |
| Rating & Ulasan | Wajib diisi setelah pesanan selesai | Mekanisme kepercayaan + filter tukang nakal |
| Komplain/Klaim Garansi | Ajukan klaim dalam periode garansi | Flow komplain sebelumnya |
| Riwayat Penyaluran Non-Servis | Riwayat listing jual/donasi/rujukan daur ulang | Flow triase Bagian 2.5 dokumen sebelumnya |

### 6.3 Modul Tukang (Direktori & Sosial)

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Direktori & Filter | Cari tukang per kategori, jarak, rating, ketersediaan | IA dasar marketplace jasa |
| Profil Tukang | Spesialisasi, portofolio before/after, verifikasi dasar | Visibilitas digital tukang informal |
| Tukang Keliling (opsi tambahan) | Untuk tukang kecil yang biasa keliling (sol/jahit), opsi "datang ke lokasimu" selain drop-off mandiri | Insight Zikru — tukang sol/jahit keliling bersepeda |

### 6.4 Modul Dampak Komunitas

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Dashboard Dampak Wilayah | Jumlah barang diperbaiki/disalurkan per wilayah | Repair Café — dampak kolektif |
| Cerita Tukang | Highlight kisah tukang lokal (mirip kisah Pak Anung) | Membangun koneksi emosional |

### 6.5 Modul Tukang (Dashboard Mitra)

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Pesanan Masuk | Terima/tolak order baru | Flow onboarding tukang sebelumnya |
| Kelola Profil Usaha | Update kategori, harga, foto | Onboarding tukang |
| Pendapatan Transparan | Riwayat transaksi & komisi platform yang jelas, bukan kotak hitam. **Asumsi kerja (perlu dikonfirmasi tim):** platform mengambil komisi kecil (misal 5–10%) dari transaksi yang dibayar lewat QRIS in-app — bukan dari transaksi tunai langsung — supaya ada insentif wajar bagi tukang tetap pakai fitur pembayaran resmi (yang juga membuka akses garansi/riwayat), tanpa memberatkan transaksi tunai kecil sehari-hari. Sebelumnya poin ini dibiarkan menggantung ("komisi kalau ada") tanpa keputusan | Riset status hukum "mitra" — transparansi sebagai mitigasi |
| Sistem Reputasi | Rating masuk, status visibilitas (aktif/diturunkan/dipulihkan) dengan alasan yang terlihat | Sistem filter tukang nakal (tim) + prinsip anti-algoritma-tersembunyi |

### 6.6 Modul Akun & Kepatuhan

| Fitur | Deskripsi Singkat | Dasar Riset |
|---|---|---|
| Consent Data Pribadi | Layar persetujuan eksplisit sebelum upload KTP | UU PDP — Bagian 7.2 Deep Research |
| Consent Data Lokasi | Layar persetujuan eksplisit sebelum aplikasi mengakses lokasi GPS, menjelaskan lokasi dipakai untuk mencocokkan ke tukang terdekat | UU PDP — data lokasi juga termasuk data pribadi, celah ditemukan saat audit (versi pertama cuma cakup consent KTP) |
| Izin Lokasi (GPS) | Permintaan izin akses lokasi saat pertama kali membuka fitur Perbaiki/Tukang, dengan opsi input alamat manual kalau ditolak | Kebutuhan fungsional dasar untuk fitur "tukang terdekat" — celah ditemukan saat audit, sebelumnya tidak pernah disebut |
| Pembayaran QRIS In-App | Pembayaran terlindungi lewat aplikasi | Bagian 8 Deep Research — QRIS |
| Pengaturan Aksesibilitas | Ukuran teks, kontras, mode gelap | Checklist WCAG dari riset awal |

---

## 7. User Flow Menyeluruh — Tanpa Jalan Buntu

Setiap flow di bawah eksplisit menyebut **jalur keluar/lanjutan** di setiap titik keputusan, supaya tidak ada skenario yang berhenti tanpa arah.

### 7.1 Flow Onboarding & Pemilihan Peran

1. Splash/intro — perkenalan value proposition dua sisi.
2. Pilih peran: "Saya punya barang" atau "Saya tukang/mitra".
3. **Jika "Saya punya barang":** daftar/masuk (nomor HP/email) → izin akses lokasi (GPS) diminta, dengan opsi "Isi alamat manual" kalau ditolak/tidak tersedia *(jalur non-buntu — celah yang ditemukan saat audit, sebelumnya tidak pernah disebut padahal fitur "tukang terdekat" butuh ini)* → langsung ke Home. *(Jalur lanjutan: bisa skip login dulu untuk sekadar menjelajah kategori & estimasi harga — baru diminta login saat mau transaksi nyata, supaya tidak ada friksi di awal. Izin lokasi tetap diminta saat itu, bukan lebih awal, kalau pengguna memilih menjelajah dulu tanpa login.)*
4. **Jika "Saya tukang/mitra":** masuk ke Flow 7.9 (Onboarding Tukang).

### 7.2 Flow Utama — Scan & Triase

1. Dari Home, tap tombol "Perbaiki" → ambil/unggah foto barang.
2. AI memproses foto → tampilkan hasil dengan confidence score.
   - **Kasus A — keyakinan tinggi:** tampilkan kategori & jenis kerusakan terdeteksi otomatis.
   - **Kasus B — keyakinan rendah (jalur non-buntu):** tampilkan pesan jujur ("Kurang yakin dengan deteksi ini") + opsi pilih kategori manual dari daftar, sehingga pengguna tetap bisa lanjut meski AI gagal.
3. Sistem tampilkan Skor Kelayakan Reparasi + estimasi biaya reparasi vs. beli baru. **Mekanisme segmentasi ukuran barang (celah yang ditemukan saat audit — sebelumnya tidak dijelaskan):** ukuran barang ("besar" vs "kecil") ditentukan **otomatis dari kategori yang terdeteksi**, bukan dipilih manual pengguna — daftar kategori "besar" (kulkas, AC, mesin cuci, kompor, dan barang elektronik rumah tangga sejenis yang butuh cek fisik langsung) sudah didefinisikan di awal sebagai daftar tetap yang bisa dikelola tim produk; semua kategori lain (pakaian, sepatu, tas, elektronik kecil/genggam, las) otomatis masuk jalur "kecil". Kalau AI mendeteksi kategori dengan keyakinan rendah (Kasus B di atas) dan pengguna pilih manual, sistem tetap otomatis menandai ukurannya dari kategori yang dipilih — pengguna tidak pernah diminta memilih "besar/kecil" secara terpisah, supaya tidak menambah langkah.
4. **Titik keputusan Triase:** "Apa yang kamu inginkan untuk barang ini?"
   - **Ingin diperbaiki** → lanjut ke Flow 7.3/7.4 (tergantung ukuran barang).
   - **Sudah tidak ingin pakai, masih layak** → lanjut ke Flow 7.6 (Jual/Donasi).
   - **Sudah rusak parah** → lanjut ke Flow 7.7 (Daur Ulang Resmi).
   - **Belum yakin/batal dulu** *(jalur non-buntu penting)* → kembali ke Home, hasil scan tersimpan otomatis di draft "Pesanan" supaya bisa dilanjutkan kapan saja, tidak hilang begitu saja.

### 7.3 Flow Servis — Barang Besar (Kulkas, AC, Mesin Cuci, Kompor)

*(Mengadaptasi sistem "anti-tembak" dari tim, dengan istilah yang diselaraskan ke dokumen ini.)*

1. Sistem tampilkan Rentang Harga Dasar sebagai acuan transparansi (angka yang sama dengan Skor Kelayakan Reparasi di Flow 7.2 langkah 3 — lihat catatan di Bagian 6.1).
2. Pengguna pilih tukang dari direktori (atau Tukang Favorit). *(Jalur non-buntu — tidak ada tukang tersedia di radius:* tampilkan pesan jujur + opsi perluas radius pencarian atau simpan barang untuk dicoba lagi nanti, bukan layar kosong — lihat contoh copy di Bagian 9.)
3. **Perbaikan timing (celah yang ditemukan saat audit):** Biaya Jasa Tetap (ongkos kunjungan + cek fisik) **dibayar/diotorisasi di muka, sebelum tukang berangkat** — bukan setelah kunjungan seperti di versi pertama dokumen ini. Ini penting karena tujuan Biaya Jasa Tetap memang melindungi tukang dari kerugian kalau pelanggan batal; kalau dibayar belakangan, tujuan itu tidak tercapai. Pengguna konfirmasi jadwal kunjungan sekaligus otorisasi pembayaran Biaya Jasa Tetap (lewat QRIS in-app, ditahan/di-hold sampai kunjungan selesai — di prototype Figma cukup direpresentasikan sebagai satu layar konfirmasi "Jadwal & Biaya Kunjungan", tidak perlu sistem hold pembayaran sungguhan).
4. Tukang datang, cek fisik langsung → input harga final + rincian (tingkat kesulitan, kebutuhan sparepart) ke aplikasi → **Invoice Digital** terkirim ke pengguna (Biaya Jasa Tetap yang sudah dibayar di langkah 3 otomatis menjadi bagian dari total, bukan biaya terpisah lagi).
5. **Titik keputusan:** pengguna tap "Setuju" → kerja dimulai. Kalau menolak biaya tambahan yang dianggap tidak wajar *(jalur non-buntu)* → kerja tidak dilanjutkan, Biaya Jasa Tetap yang sudah dibayar di langkah 3 tetap menjadi milik tukang (sesuai tujuan awalnya sebagai jaminan kunjungan), transaksi ditutup dengan status "Selesai — biaya tambahan ditolak", bukan menggantung tanpa status.
6. Kerja selesai → unggah bukti before/after → rating & ulasan → opsi lihat Dampak Komunitas.

### 7.4 Flow Servis — Barang Kecil (Pakaian, Sepatu, Tas)

1. Sistem tampilkan estimasi biaya standar (misal "Jahit sobek: estimasi Rp15.000–Rp25.000"). *(Jalur non-buntu — tidak ada tukang tersedia di radius:* sama seperti Flow 7.3, tampilkan opsi perluas radius atau simpan untuk dicoba lagi.)
2. Chat-First: daftar tukang terdekat ditampilkan, pengguna chat/telepon lewat aplikasi untuk konfirmasi & menyepakati harga final. **Jalur non-buntu — gagal sepakat harga (celah yang ditemukan saat audit, sebelumnya tidak ada):** kalau tukang menolak harga atau pengguna tidak setuju penawaran, pengguna bisa tap "Cari tukang lain" untuk kembali ke daftar tukang terdekat (langkah 1) dengan progres foto & kategori tetap tersimpan, tanpa perlu mengulang dari awal.
3. **Titik keputusan pengiriman barang:**
   - **Drop-off mandiri** (default, lebih murah, tanpa biaya ongkir) → pengguna antar barang ke lokasi tukang.
   - **Tukang keliling datang ke lokasi** *(opsi tambahan sesuai insight Zikru, hanya muncul kalau tukang menandai dirinya sebagai "keliling")* → dijadwalkan lewat chat.
4. Setelah harga disepakati di chat, pengguna konfirmasi kesepakatan di aplikasi (supaya tetap tercatat sebagai transaksi resmi, bukan cuma percakapan yang tidak terlacak — penting untuk Fitur Riwayat & Garansi tetap berfungsi).
5. Barang diperbaiki → serah terima → unggah bukti before/after → rating & ulasan.

### 7.5 Flow Pindah Jalur di Tengah Proses (Jalur Non-Buntu Krusial)

Mengacu ke insight sebelumnya soal kategori "abu-abu" (misal HP retak tapi masih nyala): di layar Skor Kelayakan Reparasi maupun di layar estimasi harga manapun, selalu tersedia tombol sekunder **"Atau, jual/donasi barang ini apa adanya"** — supaya pengguna yang awalnya berniat servis tapi berubah pikiran (misal karena harga ternyata lumayan mahal) tidak harus keluar dari flow, cukup berpindah ke Flow 7.6 tanpa kehilangan progres (foto & kategori yang sudah diisi ikut terbawa).

### 7.6 Flow Jual/Donasi

1. Dari Triase atau dari Flow 7.5, pengguna pilih Jual atau Donasi.
2. **Disclaimer wajib tampil:** "Khusus barang milik sendiri dari dalam negeri" (menghindari kesan memfasilitasi barang impor bekas ilegal — lihat Bagian 6 Deep Research).
3. **Jual:** isi listing sederhana (foto kondisi barang wajib, harga, deskripsi) → dipublikasikan ke direktori jual lokal (skala fitur dibatasi lihat Bagian 12 — MVP scope).
   - **Sisi pembeli (celah yang ditemukan saat audit — versi pertama dokumen ini tidak pernah menjelaskan siapa yang melihat/membeli listing ini, jadi flow-nya buntu di tengah jalan):** listing jual muncul di tab "Tukang" *(direvisi cakupannya jadi juga menampung direktori barang bekas warga sekitar, tidak cuma direktori tukang — atau, kalau tim ingin lebih rapi, sebagai sub-tab terpisah "Jual-Beli" di dalam tab Tukang)* dengan filter kategori & jarak, sama seperti direktori tukang. Pembeli (pengguna lain di aplikasi yang sama) bisa menjelajah, tap listing untuk detail, dan hubungi penjual lewat chat in-app (memakai komponen chat yang sama dengan Flow 7.4) untuk sepakat harga & serah terima — bertemu langsung, bukan pengiriman logistik, supaya tidak menambah kompleksitas di luar cakupan lomba.
   - Setelah transaksi terjadi (disepakati lewat chat, serah terima di luar aplikasi), penjual menandai listing "Terjual" secara manual — status ini yang mencatat ke Riwayat Penyaluran, bukan sistem pembayaran/logistik penuh.
4. **Donasi:** sistem tampilkan direktori partner sesuai kategori (misal sepatu → komunitas donasi sepatu, elektronik kecil → partner e-waste/donasi elektronik) → pengguna diarahkan (redirect informasi, bukan transaksi penuh di dalam aplikasi).
5. Setelah barang tersalur (ditandai manual oleh pengguna "Sudah disalurkan"/"Terjual"), otomatis tercatat di Riwayat Penyaluran & menambah Dashboard Dampak Komunitas.

### 7.7 Flow Daur Ulang Resmi (Barang Rusak Parah)

1. Sistem cek kategori barang:
   - **Elektronik** → tampilkan pesan eksplisit "Barang elektronik rusak termasuk limbah B3, jangan dibuang ke tempat sampah biasa" + direktori dropbox e-waste resmi terdekat.
   - **Non-elektronik** (tekstil dsb.) → arahkan ke bank sampah/opsi daur ulang tekstil terdekat.
2. Pengguna melihat peta/daftar titik terdekat → *(jalur non-buntu)* kalau tidak ada titik terdekat dalam radius wajar, tampilkan opsi alternatif umum (misal kontak Waste4Change untuk penjemputan) daripada layar kosong tanpa solusi.
3. Setelah disalurkan, sama seperti Flow 7.6, tercatat ke Riwayat & Dashboard Dampak.

### 7.8 Flow Pembayaran

1. Setelah Invoice Digital disetujui (barang besar) atau kesepakatan chat dikonfirmasi (barang kecil), pengguna pilih metode bayar: **QRIS in-app** (direkomendasikan, dengan proteksi garansi resmi) atau tunai langsung ke tukang (diizinkan untuk fleksibilitas tukang sangat informal, tapi dengan catatan eksplisit "Garansi & riwayat resmi hanya berlaku penuh untuk pembayaran lewat aplikasi").
2. Pembayaran QRIS berhasil → bukti otomatis tersimpan di Riwayat.
3. **Jalur non-buntu — pembayaran gagal:** tampilkan opsi ulangi pembayaran atau ganti metode, dengan status pesanan tetap "Menunggu Pembayaran" (bukan otomatis batal), supaya pengguna tidak kehilangan slot tukang yang sudah dikonfirmasi.

### 7.9 Flow Onboarding Tukang/Mitra

1. Pilih peran "Saya tukang/mitra" → pilih kategori keahlian (elektronik/jahit/sepatu/las).
2. Isi data dasar (nama, wilayah operasi, apakah menerima drop-off/keliling/kunjungan).
3. **Layar Consent Data Pribadi** *(sesuai UU PDP)* — jelaskan singkat kenapa KTP dibutuhkan, bagaimana data dilindungi, sebelum tombol lanjut aktif.
4. Unggah foto KTP + foto lokasi/tempat usaha.
5. Isi kisaran harga per jenis servis dalam kategorinya.
6. Status "Menunggu Verifikasi" → *(jalur non-buntu)* tampilkan estimasi waktu verifikasi dan tips melengkapi profil (portofolio, jam operasional) supaya tukang tetap produktif menunggu, bukan layar kosong.
7. Setelah terverifikasi → profil aktif, muncul di pencarian pengguna sesuai radius wilayah.

### 7.10 Flow Harian Tukang

1. Notifikasi pesanan baru masuk → terima/tolak.
2. **Jika tolak** *(jalur non-buntu)* → sistem tanya alasan singkat (opsional: "Sedang penuh" / "Di luar kategori" / lainnya) untuk membantu sistem mencocokkan lebih baik ke depan, order otomatis diteruskan ke tukang berikutnya di radius yang sama, bukan hilang begitu saja ke pengguna.
3. Jika terima → update status pekerjaan (barang besar: cek fisik → invoice → dikerjakan → selesai; barang kecil: dikerjakan → selesai) → unggah bukti hasil.
4. Menerima pembayaran (QRIS otomatis masuk / konfirmasi manual untuk tunai) → tercatat di Pendapatan.

### 7.11 Flow Filter Tukang Nakal (Sistem Reputasi)

1. Setiap transaksi selesai → pengguna beri rating & ulasan.
2. Sistem mendeteksi pola harga di luar wajar (dibanding rata-rata tukang sekategori **di wilayah yang sama**, bukan standar nasional kaku — revisi dari catatan risiko sebelumnya) → visibilitas otomatis diturunkan.
3. **Jalur non-buntu — tukang yang terkena penurunan visibilitas** diberi notifikasi eksplisit alasan penurunan (transparansi, sesuai prinsip anti-algoritma-tersembunyi) + langkah pemulihan yang jelas (perbaiki rating dalam periode tertentu → visibilitas dikembalikan otomatis), bukan sanksi permanen tanpa penjelasan.

### 7.12 Flow Komplain/Klaim Garansi

1. Dari Riwayat Servis, pengguna pilih pesanan dalam masa garansi → ajukan klaim (foto kondisi barang + keterangan).
2. Notifikasi ke tukang terkait → tukang konfirmasi jadwal servis ulang.
3. **Jalur non-buntu — tidak ada kesepakatan:** eskalasi ke status "Sedang Ditinjau" dengan estimasi waktu tindak lanjut (di prototype cukup direpresentasikan sebagai status, bukan sistem mediasi penuh yang berfungsi).

---

## 8. Daftar Layar Figma (Master List)

**Sisi Pengguna:**
1. Splash/Onboarding — Pilih Peran
2. Login/Daftar (opsional, bisa dilewati untuk eksplorasi)
3. Izin Lokasi (GPS) + Consent Data Lokasi, dengan opsi input alamat manual *(baru — celah audit)*
4. Home (dengan kartu Dampak Komunitas & tombol Perbaiki)
5. Ambil/Unggah Foto — Scan AI
6. Hasil Deteksi AI (keyakinan tinggi) / Pilih Kategori Manual (keyakinan rendah)
7. Skor Kelayakan Reparasi + Estimasi Biaya
8. Titik Keputusan Triase
9. Direktori & Filter Tukang Terdekat *(satu layar dipakai untuk barang besar maupun kecil — versi pertama dokumen ini punya dua layar terpisah #8 dan #24 yang sebenarnya redundan, sekarang digabung jadi satu dengan filter kategori/jarak/rating)*
10. Pencarian Teks Tukang *(baru — celah audit, pelengkap direktori kategori)*
11. Detail Profil Tukang
12. Konfirmasi Jadwal & Otorisasi Biaya Jasa Tetap (barang besar) *(direvisi — sebelumnya "Konfirmasi Jadwal Kunjungan" tanpa pembayaran di muka; sekarang termasuk otorisasi Biaya Jasa Tetap sesuai perbaikan timing di Flow 7.3)*
13. Invoice Digital & Persetujuan (barang besar)
14. Chat dengan Tukang (barang kecil) — dipakai juga untuk negosiasi listing Jual-Beli antar pengguna
15. Pilih Drop-off Mandiri / Tukang Keliling (barang kecil)
16. Status Pesanan Aktif
17. Pembayaran QRIS
18. Unggah Bukti Hasil + Rating & Ulasan
19. Riwayat Servis & Garansi
20. Form Klaim Garansi
21. Buat Listing Jual Barang
22. Direktori Jual-Beli (browse listing warga sekitar) *(baru — celah audit, sisi pembeli yang sebelumnya tidak ada)*
23. Detail Listing Jual Barang *(baru — celah audit)*
24. Direktori Partner Donasi
25. Direktori Dropbox Daur Ulang Resmi
26. Riwayat Penyaluran Non-Servis
27. Dashboard Dampak Komunitas Wilayah
28. Tukang Favorit
29. Profil & Pengaturan Aksesibilitas

**Sisi Tukang/Mitra:**
30. Onboarding — Pilih Kategori
31. Layar Consent Data Pribadi
32. Layar Consent Data Lokasi *(baru — celah audit)*
33. Form Verifikasi (KTP + Lokasi Usaha)
34. Status Menunggu Verifikasi
35. Dashboard Pesanan Masuk
36. Detail Pesanan & Update Status
37. Profil Usaha & Portofolio
38. Riwayat Pendapatan (termasuk rincian komisi platform — lihat Bagian 6.5)
39. Notifikasi Reputasi (transparansi visibilitas)

---

## 9. Microcopy & Prinsip UX Writing

**Nada suara:** hangat, jujur, membumi — bukan korporat kaku atau terlalu "startup-y". Sapaan menggunakan "kamu", bukan "Anda" (lebih akrab, sesuai target pengguna lintas usia yang luas tapi condong ke pengguna urban muda-menengah).

**Prinsip kejujuran dalam copy** (langsung menerapkan Prinsip Desain #2 & #3):
- Saat AI kurang yakin: *"Kami kurang yakin dengan hasil ini — coba bantu pilih kategorinya, ya."* (bukan berpura-pura yakin)
- Saat tukang tidak tersedia di radius: *"Belum ada tukang kategori ini di sekitarmu. Coba perluas radius pencarian, atau simpan barang ini untuk dicoba lagi nanti."* (bukan layar kosong tanpa arahan)
- Saat visibilitas tukang diturunkan: *"Visibilitas profilmu diturunkan sementara karena beberapa laporan harga di luar rata-rata wilayahmu. Selesaikan 3 pesanan berikutnya dengan rating baik untuk memulihkannya."* (transparan, bukan sanksi tanpa penjelasan)
- Saat konfirmasi dampak: *"Barangmu berhasil diselamatkan! +1 untuk wilayahmu."* (positif, personal, terukur)

---

## 10. Kepatuhan Regulasi & Privasi (Ringkasan Aplikasi ke Desain)

| Area Regulasi | Penerapan di Desain |
|---|---|
| UU PDP — data KTP tukang | Layar consent eksplisit sebelum upload (Layar #28) |
| Barang bekas domestik vs impor | Disclaimer eksplisit di flow Jual/Donasi (Flow 7.6) |
| E-waste sebagai limbah B3 | Pesan eksplisit + rujukan dropbox resmi di Flow 7.7 |
| Status hukum "mitra" tukang | Transparansi pendapatan & sistem reputasi (Layar #34, #35) |
| PSE Kominfo | Disebutkan di narasi presentasi sebagai kesadaran kepatuhan bisnis, di luar cakupan Figma prototype |

---

## 11. Aksesibilitas (Checklist Wajib Diterapkan di Setiap Layar)

Target sentuh minimal 44×44pt, kontras teks-latar minimal 4,5:1, label deskriptif di setiap tombol/ikon (hindari "klik di sini"), teks bisa diperbesar tanpa merusak layout, urutan elemen logis untuk mendukung navigasi non-visual. Mode gelap disediakan sebagai pilihan (bukan cuma estetika — hemat daya di layar OLED, selaras filosofi sustainable digital design dari brief kompetisi).

---

## 12. Ruang Lingkup MVP untuk Prototype Figma vs. Fitur Lanjutan

Mengingat keterbatasan waktu presentasi (10 menit) dan waktu pengerjaan, tidak semua fitur di Bagian 6 perlu di-hi-fi penuh. Rekomendasi prioritas:

**MVP (wajib di-prototype penuh, jadi tulang punggung demo):** Scan AI + Skor Kelayakan → Triase → **Flow Servis Barang Besar** (bukan barang kecil seperti rekomendasi versi pertama dokumen ini) → Konfirmasi Jadwal & Biaya Jasa Tetap → Invoice Digital & Persetujuan → Rating & Bukti → Dashboard Dampak. Ditambah satu contoh Onboarding Tukang untuk menunjukkan sisi mitra tanpa harus mendemokan seluruh dashboard tukang.

**Koreksi rekomendasi (celah yang ditemukan saat audit):** versi pertama dokumen ini menyarankan Flow Barang Kecil sebagai tulang punggung demo karena "paling sederhana" — ini keliru. Flow Barang Kecil justru bergantung pada simulasi chat negosiasi yang lebih sulit dibuat terasa meyakinkan di prototype Figma statis (perlu skenario chat yang sudah "dikanalisasi" polanya, mudah terlihat palsu kalau juri mencoba interaksi di luar skrip). Flow Barang Besar punya langkah-langkah linear yang lebih jelas urutannya (pilih tukang → jadwal → invoice → persetujuan → selesai) dan lebih mudah dijelaskan step-by-step dalam presentasi 10 menit tanpa perlu berimprovisasi dialog chat.

**Nice-to-have (bisa ditampilkan sebagai 1-2 layar representatif, dijelaskan konsepnya di presentasi tanpa perlu flow penuh):** Flow Jual/Donasi lengkap, Flow Servis Barang Besar dengan kunjungan fisik, Dashboard Pendapatan Tukang detail, Sistem Filter Tukang Nakal (cukup satu layar contoh notifikasi).

**Di luar cakupan Figma sama sekali (cukup di narasi/dokumentasi):** integrasi PSE, backend AI sungguhan, sistem pembayaran QRIS nyata — ini cukup direpresentasikan sebagai UI/interaksi, bukan dibangun sungguhan (sesuai batasan lomba: murni desain, bukan pengembangan).

---

## 13. Risiko & Mitigasi (Konsolidasi Akhir)

| Risiko | Mitigasi |
|---|---|
| Klaim dampak lingkungan berlebihan | Bahasa "berpotensi mengurangi", bukan klaim pasti 1:1 |
| Diferensiasi dipertanyakan vs Sejasa/Kanggo/lakuKan | Tiga lapis diferensiasi: kategori, segmen mitra, narasi (lihat Deep Research Bagian 4) |
| Disintermediasi setelah transaksi pertama | Fitur retensi organik (riwayat, garansi, dampak, Tukang Favorit), bukan pengunci paksa |
| Harga dianggap tidak transparan/rawan nego | Estimasi Berjenjang + Invoice Digital + persetujuan wajib |
| Status hukum tukang dipertanyakan | Transparansi pendapatan & reputasi, pengakuan jujur soal keterbatasan model kemitraan |
| Data KTP disalahgunakan | Consent eksplisit sesuai UU PDP |
| AI dianggap tempelan/gimmick | Desain confidence score + fallback manual yang jujur |
| Kompleksitas fitur terlalu banyak untuk didemokan 10 menit | Skema MVP vs nice-to-have di Bagian 12 |
| Nama "Awetin" ternyata juga sudah dipakai pihak lain (belum bisa dipastikan 100% bebas konflik dari riset saya) | Tim wajib cek mandiri (Google Play, App Store, PDKI merek terdaftar) sebelum finalisasi proposal — lihat Catatan Revisi di awal dokumen |
| Flow Jual-Beli antar pengguna berpotensi disalahgunakan (barang palsu, penipuan) kalau benar-benar dibangun penuh | Untuk lingkup lomba, cukup direpresentasikan sebagai konsep ringan (lihat Bagian 12) — bukan sistem transaksi/pembayaran penuh yang butuh mekanisme anti-penipuan matang |

---

## 14. Pertanyaan Terbuka untuk Tim

1. **Konfirmasi nama produk final** — "Awetin" adalah usulan kerja hasil brainstorming cepat pasca-audit, tim perlu memutuskan sendiri (dan memverifikasi ke Google Play/App Store/PDKI) sebelum dipakai di proposal resmi.
2. Apakah fitur "Jual" barang (bukan cuma donasi) benar-benar diprototipekan penuh atau cukup konsep ringan — mengingat kompleksitas kepercayaan peer-to-peer lebih tinggi dari reparasi.
3. Apakah satu akun bisa berperan ganda (pengguna sekaligus tukang) atau dipisah total — dokumen ini mengasumsikan dipisah untuk kesederhanaan desain, tapi ini keputusan tim.
4. Kategori mana yang jadi fokus utama demo Figma (disarankan pilih 1–2 dari 4 kategori: elektronik/jahit/sepatu/las) supaya presentasi 10 menit tetap fokus, bukan mencoba menunjukkan semua kategori sekaligus.
5. Nama & istilah final untuk fitur Scan AI, Skor Kelayakan, dan tab "Tukang" — dokumen ini pakai istilah kerja, tim bebas menyesuaikan dengan bahasa yang paling nyaman dipresentasikan.
6. **Konfirmasi angka komisi platform** — Bagian 6.5 mengusulkan 5–10% sebagai asumsi kerja, tim perlu memutuskan angka final (atau memastikan tetap disebut "asumsi" saat presentasi kalau belum final) supaya siap kalau juri bertanya soal model bisnis.
7. **Belum dikonfirmasi ke panitia:** daftar sub-tema resmi turunan dari "Tech for Nature by Crafting Sustainable Digital Solutions" (lihat Deep Research Bagian 1) — ini sebaiknya ditanyakan di Technical Meeting 5 September sebelum konsep benar-benar dikunci, karena berpotensi memengaruhi validitas seluruh kerangka Awetin kalau sub-tema resmi ternyata lebih sempit/berbeda dari yang diasumsikan.

---

## 15. Sumber

Seluruh sumber riset yang mendasari dokumen ini tercantum lengkap di "Deep Research - Ekosistem Menyeluruh Awetin.md" dan dokumen-dokumen riset sebelumnya dalam sesi ini (breakdown lengkap, pendalaman harga & regulasi, riset kompetitor).
