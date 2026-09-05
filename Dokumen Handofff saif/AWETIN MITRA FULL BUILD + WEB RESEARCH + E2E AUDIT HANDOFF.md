## FULL BUILD + WEB SEARCH + END-TO-END VALIDATION

Kamu bertindak sebagai **Lead Product Designer, UX/UI Designer, Product Engineer, UX Researcher, dan QA Engineer** untuk membangun aplikasi **Awetin Mitra** sampai benar-benar utuh, terhubung, interaktif, konsisten, dan dapat digunakan dari awal sampai akhir.

## ATURAN UTAMA

Kerjakan seluruh spesifikasi di bawah ini sebagai **SATU MASTER SPECIFICATION**.

Jangan mengerjakannya sebagai beberapa tugas terpisah.

Jangan menunggu instruksi lanjutan.

Jangan meminta saya memberikan prompt berikutnya.

Jangan berhenti setelah menyelesaikan sebagian fitur.

Target akhirnya adalah:

> **SATU APLIKASI AWETIN MITRA YANG UTUH, TERHUBUNG, INTERAKTIF, KONSISTEN, DAN LULUS END-TO-END TEST.**

Gunakan proses kerja internal:

> PLAN → WEB SEARCH → BUILD → CONNECT → TEST → AUDIT → FIX → FINALIZE

Jika menemukan bug, dead-end, inkonsistensi, atau requirement yang belum tersambung dan masih berada dalam scope spesifikasi ini, **perbaiki langsung**.

---

# 1. WEB SEARCH

Gunakan Web Search untuk melakukan riset ketika informasi eksternal dapat membantu keputusan.

Riset terutama mengenai:

- UX aplikasi partner/merchant;
- aplikasi jasa/on-demand;
- onboarding mitra;
- OTP authentication;
- order management;
- order acceptance/rejection;
- service workflow;
- partner dashboard;
- rating dua arah;
- reputation system;
- invoice;
- QRIS/payment UX;
- privacy dan consent;
- KTP verification;
- location consent;
- warranty claim;
- notification UX;
- mobile navigation;
- accessibility;
- mobile form UX;
- status stepper;
- aplikasi reparasi/service marketplace.

Prioritaskan:

1. sumber resmi;
2. dokumentasi resmi;
3. pemerintah/regulator;
4. standar accessibility/UX;
5. sumber kredibel;
6. komunitas sebagai referensi tambahan.

Untuk informasi yang dapat berubah, gunakan sumber terbaru.

Jangan mengarang fakta.

Gunakan hasil Web Search untuk:

- validasi;
- benchmarking;
- UX best practice;
- keputusan desain;
- keputusan produk;
- regulasi;
- accessibility.

Jika requirement sudah ditentukan dalam spesifikasi ini, jangan menggantinya hanya karena aplikasi lain menggunakan pendekatan berbeda.

Gunakan aplikasi lain hanya sebagai referensi pola pengalaman, **bukan untuk cloning**.

---

# 2. BRAND & VISUAL

## BRAND UTAMA

> **AWETIN = HIJAU**

Hijau adalah warna identitas utama Awetin.

Gunakan hijau sebagai brand anchor di seluruh aplikasi.

Selain arahan bahwa brand menggunakan hijau, **AI bebas menentukan seluruh keputusan visual lainnya.**

AI menentukan sendiri:

- shade hijau;
- warna background;
- warna surface;
- warna teks;
- warna secondary;
- accent;
- success;
- warning;
- error;
- info;
- typography;
- font;
- font weight;
- font size;
- spacing;
- grid;
- card;
- button;
- input;
- radius;
- shadow;
- elevation;
- icon;
- illustration;
- modal;
- bottom sheet;
- navigation;
- animation;
- transition;
- layout.

Dasarkan keputusan tersebut pada:

- Web Search;
- usability;
- accessibility;
- mobile UX;
- karakter persona;
- konteks aplikasi jasa;
- konsistensi brand.

### PENTING

Jangan membuat semua elemen menjadi hijau.

Gunakan hijau secara strategis untuk:

- primary CTA;
- active navigation;
- brand element;
- selected state;
- elemen penting lainnya.

Background dan surface boleh menggunakan warna netral.

Setelah visual system ditentukan:

> gunakan secara konsisten di seluruh aplikasi.

Jangan mengubah style secara acak antar-screen.

---

# 3. ACCESSIBILITY

Pastikan seluruh UI memperhatikan accessibility.

Perhatikan:

- contrast;
- ukuran teks;
- touch target;
- readability;
- label form;
- error feedback;
- navigation;
- status;
- hierarchy.

Jangan menyampaikan informasi hanya menggunakan warna.

Status harus tetap dapat dipahami melalui:

- text;
- icon;
- label;
- shape;
- position;
- atau kombinasi beberapa indikator.

Gunakan standar accessibility modern sebagai referensi.

---

# 4. PERSONA

Persona utama:

> **Tukang reparasi / Mitra**

UI harus:

- sederhana;
- praktis;
- jelas;
- tidak menggunakan jargon;
- tidak terlalu banyak keputusan dalam satu layar;
- memiliki CTA yang mudah ditemukan.

Microcopy menggunakan Bahasa Indonesia natural dan sederhana.

Aplikasi harus terasa seperti:

> **alat kerja harian profesional untuk tukang.**

Bukan sekadar dashboard kosong.

---

# 5. AUTHENTICATION

## TIDAK ADA PASSWORD

Authentication hanya:

> **Nomor HP → OTP**

Jangan membuat authentication menggunakan password.

Jangan membuat:

- password;
- confirm password;
- forgot password;
- reset password.

PIN/biometrik hanya boleh digunakan sebagai:

> **Kunci Aplikasi lokal pada perangkat.**

Itu bukan metode login.

---

# 6. SPLASH SCREEN

Tampilkan:

> Awetin

Label:

> Mitra

Tagline:

> Kerjaan reparasi, langsung dari HP-mu

Jika nomor HP pada perangkat:

- sudah pernah login;
- profil usaha berstatus Aktif;

langsung:

> Beranda.

Lewati onboarding.

---

# 7. INTERSTITIAL PERAN

Hanya pada pembukaan pertama.

Judul:

> Awetin Mitra ini untuk kamu yang menerima pekerjaan reparasi

CTA:

> Lanjutkan

Link:

> Mau perbaiki barangmu sendiri? Unduh Awetin

Tap link:

`ConfirmationModal`

Tombol:

- Buka Store
- Batal

Ini adalah:

> link keluar ke aplikasi Awetin konsumen.

Bukan mode switch.

Tidak mengubah shell aplikasi Mitra.

---

# 8. MASUK / DAFTAR

Satu layar.

Tidak ada tab Login dan Daftar.

Field:

> Nomor HP

Checkbox:

> Saya menyetujui Syarat & Ketentuan Mitra dan Kebijakan Privasi

CTA:

> Lanjutkan

CTA aktif hanya ketika:

- nomor valid;
- checkbox dicentang.

Link:

> Nomor HP lama hilang atau ganti?

→ Pemulihan Akun.

State:

- idle;
- loading;
- error.

Error:

> Nomor HP tidak valid

Tap Lanjutkan:

> Mock OTP → Verifikasi OTP.

---

# 9. VERIFIKASI OTP

Gunakan:

`OTPInputField`

Kode:

> 4–6 digit

CTA:

> Verifikasi

Link:

> Kirim ulang kode

Countdown:

> 60 detik

State:

- benar;
- salah;
- kedaluwarsa.

Setelah OTP benar:

### Nomor belum terdaftar

→ Onboarding Usaha.

### Nomor sudah terdaftar + Aktif

→ Beranda.

### Nomor terdaftar + onboarding belum selesai

→ lanjutkan dari langkah terakhir.

### Nomor terdaftar + Ditolak

→ kembali ke bagian yang harus diperbaiki.

Jangan mengulang dari awal.

---

# 10. PEMULIHAN AKUN

Flow:

1. Nomor HP lama
2. OTP nomor lama
3. Nomor HP baru
4. OTP nomor baru
5. akun berhasil dipindahkan

Reuse:

`OTPInputField`

---

# 11. ONBOARDING PROFIL USAHA

## STEP 1 — Kategori

Grid:

- Elektronik
- Jahit/Pakaian
- Sepatu
- Las

Multi-select.

---

## STEP 2 — Data Dasar

Input:

- nama;
- wilayah operasi.

Pilihan layanan:

- Menerima drop-off;
- Bisa keliling/jemput;
- Menerima kunjungan ke rumah user.

Pilihan ini menentukan kelayakan menerima order Barang Besar.

---

## STEP 3 — Consent Data Pribadi

Jelaskan penggunaan KTP dengan bahasa sederhana.

Gunakan referensi regulasi yang relevan jika diperlukan.

CTA:

> Lanjut

Nonaktif sebelum consent.

---

## STEP 4 — Consent Data Lokasi

Jelaskan penggunaan data lokasi usaha dengan bahasa sederhana.

---

## STEP 5 — Upload

Gunakan dua:

`PhotoUploader`

Slot:

1. KTP
2. Foto lokasi/tempat usaha

Tampilkan:

- preview;
- instruksi;
- error;
- retry.

---

## STEP 6 — Kisaran Harga

Form dinamis berdasarkan kategori yang dipilih.

---

## STEP 7 — Menunggu Verifikasi

Tampilkan:

> Estimasi 1–2 hari kerja

Tambahkan tips melengkapi profil.

---

## STEP 8 — HASIL

### Disetujui

> Profil Aktif! Kamu sekarang bisa menerima pesanan

→ Beranda.

### Ditolak

Tampilkan alasan spesifik.

Contoh:

> Foto KTP buram, coba unggah ulang.

CTA:

> Perbaiki

Langsung menuju bagian form yang perlu diperbaiki.

Jangan mengulang onboarding.

---

# 12. SHELL UTAMA

Setelah profil aktif:

> masuk ke shell utama.

Sediakan navigasi yang jelas untuk:

- Beranda;
- Pesanan Masuk;
- Pendapatan;
- Notifikasi;
- Profil Usaha.

Gunakan bottom navigation dengan struktur paling sederhana dan mudah dipahami.

Jika diperlukan struktur navigasi tambahan, gunakan tanpa menghilangkan fitur.

---

# 13. BERANDA

Beranda adalah pusat kerja harian.

Harus terasa hidup.

## Header

> Selamat pagi, Pak Slamet

Toggle:

> Buka / Tutup

Jika Tutup:

> Kamu sedang tidak menerima pesanan baru

---

## Performa Hari Ini

Tiga kartu:

1. Pendapatan hari ini
2. Pesanan selesai
3. Rating rata-rata terbaru

Pendapatan:

→ Pendapatan.

Pesanan selesai:

→ Pendapatan.

Rating:

→ Profil Usaha → Rating & Ulasan.

Rating tidak diarahkan ke Pendapatan.

---

## Banner Tips

Gunakan:

`BannerTipCard`

Contoh:

> Tips: Balas pesanan dalam 5 menit bikin rating naik

> Info: Cara upload foto before/after yang jelas

> Selesaikan 10 pesanan bulan ini, dapat badge Tukang Rajin

---

## Pesanan Masuk

Gunakan:

`OrderRequestCard`

Tampilkan:

- foto barang;
- kategori;
- estimasi lokasi;
- Terima;
- Tolak.

Jika kosong:

> Belum ada pesanan masuk. Pastikan statusmu 'Buka' supaya bisa menerima pesanan baru.

---

# 14. STATE BERANDA

## Loading

Gunakan:

`SkeletonLoader`

untuk kartu performa dan daftar pesanan.

## Offline

Banner:

> Koneksi terputus, coba lagi

Data mock terakhir tetap tampil.

Jangan mengosongkan layar.

Toggle tetap dapat disentuh.

Toast:

> Perubahan akan tersimpan setelah koneksi kembali

## Tutup

Order baru tidak muncul.

Order aktif tetap terlihat.

---

# 15. PESANAN MASUK

Reuse:

`OrderRequestCard`

CTA:

- Terima;
- Tolak.

## Tolak

Alasan:

- Di luar jangkauan;
- Kategori tidak sesuai;
- Sedang penuh.

Setelah:

> Pesanan diteruskan ke tukang lain.

---

# 16. DETAIL PESANAN — BARANG BESAR

Flow:

> Berangkat\
> ↓\
> Tiba di Lokasi\
> ↓\
> Verifikasi Kode\
> ↓\
> Cek Fisik\
> ↓\
> Input Harga Final + Rincian\
> ↓\
> Invoice Terkirim / Menunggu Respons\
> ↓\
> Disetujui User\
> ↓\
> Mulai Mengerjakan\
> ↓\
> Sedang Diperbaiki\
> ↓\
> Selesai\
> ↓\
> Upload Before/After\
> ↓\
> Serah Terima

Gunakan:

`StatusStepper`

---

# 17. LIVE TRACKING

Gunakan:

`LiveTrackingMap`

Tampilkan rute mock di sisi tukang.

Cerita tracking harus konsisten dengan aplikasi Awetin konsumen.

---

# 18. VERIFICATION CODE

Setelah:

> Tiba di Lokasi

tampilkan:

> Kode Verifikasi

Field:

> 4 digit

CTA:

> Verifikasi

Jika kosong atau salah:

> tidak boleh lanjut ke Cek Fisik.

Ini adalah gate wajib.

---

# 19. INVOICE

Gunakan:

`InvoiceEditor`

Input:

- harga final;
- rincian.

Setelah dikirim:

> Invoice Terkirim / Menunggu Respons

Hanya setelah user menyetujui:

> Mulai Mengerjakan.

---

# 20. BEFORE / AFTER

Setelah selesai:

`PhotoUploader`

Upload:

- Before;
- After.

→ Serah Terima.

---

# 21. BARANG KECIL

Flow:

> Menunggu Diantar\
> ↓\
> Diterima\
> ↓\
> Sedang Dikerjakan\
> ↓\
> Selesai\
> ↓\
> Before/After\
> ↓\
> Serah Terima

Aturan:

Harga sudah disepakati lewat chat sebelum barang diantar.

Pembayaran:

> langsung tunai/transfer antara tukang dan user.

Aplikasi tidak memproses pembayaran Barang Kecil.

Jangan tampilkan:

- QRIS;
- Konfirmasi Pembayaran;
- Tandai Sudah Diterima Tunai.

Barang Kecil:

> tidak masuk Riwayat Transaksi Pendapatan.

---

# 22. BARANG KECIL — JEMPUT

Jika tukang datang menjemput Barang Kecil:

> gunakan Verifikasi Kode.

Jika user mengantar barang:

> tidak menggunakan Verifikasi Kode.

---

# 23. JADWAL ULANG

Jika user melakukan Jadwalkan Ulang:

Tidak perlu layar baru.

Update:

- tanggal;
- jam;
- notifikasi;
- Detail Pesanan.

---

# 24. NILAI PELANGGAN

Setelah Serah Terima:

> Bagaimana pengalaman kerja sama dengan pelanggan ini?

Input:

- bintang;
- Ramah;
- Jelas soal alamat;
- Bayar tepat waktu.

Jika rating rendah:

- Sulit dihubungi;
- Alamat tidak sesuai.

CTA:

> Lewati

Rating:

- opsional;
- tidak memblokir;
- private;
- tidak ditampilkan publik;
- tidak ditampilkan kepada pelanggan;
- tidak ditampilkan kepada pengguna lain.

Simpan sebagai riwayat internal tukang.

---

# 25. PEMBATALAN OLEH TUKANG

Tersedia selama status belum:

> Sedang Dikerjakan.

CTA:

> Batalkan Pesanan

Gunakan:

`ConfirmationModal`

Alasan:

- Berhalangan mendadak;
- Alat rusak;
- Lainnya.

Setelah confirm:

> Dibatalkan oleh Tukang

Simulasikan sisi konsumen:

> refund penuh.

Pembatalan menjadi poin negatif reputasi.

Tampilkan:

> Pembatalan sepihak yang sering terjadi bisa menurunkan visibilitas profilmu.

Wajib memicu:

`ReputationAlertCard`

---

# 26. PAYMENT

**HANYA BARANG BESAR.**

QRIS:

> Terverifikasi

Tunai:

> Tandai Sudah Diterima Tunai

Barang Kecil tidak memiliki fitur ini.

---

# 27. PROFIL USAHA

Tampilkan:

## Profil

Edit:

- kategori;
- harga.

Reuse form onboarding.

## Portfolio

Gunakan:

`PortfolioGalleryItem`

Fungsi:

- tambah;
- hapus.

## Trust

Tampilkan:

- badge verifikasi;
- rating;
- ulasan.

---

# 28. PENGATURAN AKUN

## Kunci Aplikasi

Opsional:

- PIN;
- biometrik.

Hanya untuk kunci lokal perangkat.

Bukan login.

## Logout

Gunakan:

`ConfirmationModal`

→ Login.

---

# 29. AWETIN KONSUMEN

Kartu:

> Mau Jadi Pencari Jasa Juga?

Copy:

> Punya barang sendiri yang perlu diperbaiki atau dijual? Unduh Awetin.

CTA:

> Pelajari / Unduh

Ini adalah link keluar.

Bukan mode switch.

Tidak mengubah shell aplikasi.

---

# 30. LEGAL

Sediakan:

- Syarat & Ketentuan Mitra;
- Kebijakan Privasi.

Berupa halaman teks statis.

Link harus benar-benar berfungsi.

---

# 31. VERSI APLIKASI

Tampilkan informasi versi aplikasi.

---

# 32. PENDAPATAN

Gunakan:

`EarningsCard`

Contoh:

> Total Rp100.000\
> Komisi Platform (8%) Rp8.000\
> Diterima Bersih Rp92.000

Untuk tunai:

> Komisi: Rp0

Penjelasan:

> Servis bayar tunai tidak dipotong komisi platform.

---

# 33. TIP

Jika ada tip:

> +Rp10.000 Tip dari Budi

Tip harus:

- baris terpisah;
- 100% untuk tukang;
- tidak dipotong komisi.

---

# 34. BARANG KECIL DI PENDAPATAN

Barang Kecil tidak masuk Riwayat Transaksi.

Tampilkan catatan:

> Pendapatan dari servis Barang Kecil (drop-off) dan pelanggan yang datang langsung tidak tercatat di sini karena transaksinya di luar aplikasi.

---

# 35. RINGKASAN PENDAPATAN

Filter:

- Hari Ini;
- Minggu Ini;
- Bulan Ini.

Tampilkan:

- angka;
- grafik sederhana.

---

# 36. KLAIM GARANSI

Section:

> Klaim Garansi Masuk

Tampilkan:

- foto;
- keterangan;
- status.

CTA:

> Konfirmasi Jadwal Servis Ulang

→ date/time picker

→ Terjadwal.

Harus menjadi counterpart yang masuk akal dari klaim garansi aplikasi konsumen.

---

# 37. NOTIFIKASI

Notifikasi:

- pesanan baru;
- pesanan dibatalkan user;
- pembayaran masuk.

Sediakan toggle per jenis.

---

# 38. REPUTASI

Gunakan:

`ReputationAlertCard`

Contoh:

> Visibilitas profilmu diturunkan sementara karena beberapa laporan harga di luar rata-rata wilayahmu.

atau:

> Visibilitas profilmu diturunkan sementara karena beberapa pembatalan sepihak dalam 30 hari terakhir.

Recovery:

> Selesaikan 3 pesanan berikutnya dengan rating baik untuk memulihkannya.

Pembatalan tukang wajib memicu alert reputasi.

---

# 39. KOMPONEN REUSABLE

Gunakan konsisten:

- `OrderRequestCard`
- `StatusStepper`
- `InvoiceEditor`
- `PhotoUploader`
- `EarningsCard`
- `PortfolioGalleryItem`
- `OTPInputField`
- `ConfirmationModal`
- `ToastSnackbar`
- `BottomSheet`
- `SkeletonLoader`
- `BannerTipCard`
- `ReputationAlertCard`
- `LiveTrackingMap`

---

# 40. UX QUALITY

Pastikan setiap layar memiliki hierarchy yang jelas.

Gunakan:

- skeleton untuk loading;
- empty state untuk data kosong;
- error state untuk error;
- success feedback;
- offline state jika relevan;
- toast/snackbar untuk aksi ringan;
- confirmation untuk destructive action.

Jangan membuat satu layar memiliki terlalu banyak keputusan.

---

# 41. END-TO-END TEST

Setelah seluruh aplikasi selesai dibangun, lakukan audit penuh.

## Authentication

Uji:

- nomor valid;
- nomor invalid;
- checkbox;
- OTP benar;
- OTP salah;
- OTP expired;
- resend;
- akun aktif;
- akun belum selesai;
- akun ditolak;
- recovery.

## Onboarding

Uji:

- multi kategori;
- consent;
- upload;
- harga;
- pending;
- approved;
- rejected;
- revisi sebagian.

## Order

Uji:

- Terima;
- Tolak;
- Batalkan;
- Barang Besar;
- Barang Kecil;
- jemput Barang Kecil;
- jadwal ulang.

## Barang Besar

Pastikan:

> Berangkat → Tiba → Kode → Cek Fisik → Invoice → Approval → Kerjakan → Selesai → Before/After → Serah Terima.

Kode salah/kosong:

> BLOCK.

## Barang Kecil

Pastikan:

- tidak ada payment confirmation;
- tidak ada QRIS;
- tidak ada cash confirmation;
- tidak masuk Pendapatan;
- tetap sampai Serah Terima.

## Rating

Pastikan muncul setelah Serah Terima dan tetap private.

## Reputation

Pastikan pembatalan tukang memicu Reputation Alert.

## Warranty

Pastikan:

> klaim → jadwal ulang → Terjadwal.

---

# 42. CROSS-APP CONSISTENCY

Jika informasi aplikasi Awetin konsumen tersedia, verifikasi:

- status Barang Besar;
- status Barang Kecil;
- tracking;
- verification code;
- warranty claim;
- tip.

Cerita antar-aplikasi harus konsisten walaupun prototype belum terhubung secara teknis.

---

# 43. FILOSOFI JEMBATAN AWAL

Pertahankan konsep:

Barang Kecil:

- drop-off;
- harga lewat chat;
- pembayaran langsung;
- tidak diproses aplikasi;
- tidak masuk Pendapatan.

Jangan menambahkan friction yang bertentangan dengan konsep tersebut.

Jangan membuat layar yang membatasi atau menekan tukang agar tidak berbagi kontak pribadi dengan pelanggan.

---

# 44. NO HIDDEN CHANGE

Jangan menghilangkan atau mengubah secara diam-diam:

- CTA;
- navigation;
- state;
- fitur;
- status;
- flow.

Jika perubahan diperlukan untuk memperbaiki bug:

> lakukan perubahan seminimal mungkin.

---

# 45. FINAL VISUAL AUDIT

Periksa seluruh aplikasi:

- green brand identity;
- consistency;
- typography;
- spacing;
- buttons;
- cards;
- icons;
- navigation;
- hierarchy;
- accessibility;
- contrast;
- touch target;
- loading;
- empty;
- error;
- offline;
- success;
- modal;
- form;
- OTP;
- upload;
- date/time picker.

Jika ada layar yang terasa terlalu:

- generik;
- rumit;
- ramai;
- tidak cocok untuk tukang;

perbaiki hanya layar tersebut.

---

# 46. FINAL REQUIREMENT MATRIX

Buat:

| Requirement | Implemented | Tested | Connected | Status |
| ----------- | ----------- | ------ | --------- | ------ |

Semua requirement harus:

> PASS

Jika ada FAIL:

> perbaiki terlebih dahulu.

---

# 47. JANGAN BERHENTI UNTUK MEMINTA PROMPT LANJUTAN

Seluruh requirement sudah ada dalam master specification ini.

Jangan meminta:

- prompt berikutnya;
- spesifikasi ulang;
- keputusan visual yang sebenarnya dapat kamu tentukan sendiri;
- persetujuan untuk memperbaiki bug yang masih berada dalam scope.

Gunakan judgment profesional.

Jika ada beberapa solusi yang valid:

> pilih solusi yang paling sederhana, usable, accessible, dan sesuai persona tukang.

---

# 48. FINAL OUTPUT

Setelah benar-benar selesai, berikan:

## BUILD STATUS

Status keseluruhan aplikasi.

## END-TO-END STATUS

Konfirmasi apakah seluruh journey berhasil ditelusuri.

## FIXED SCREENS

Sebutkan layar yang benar-benar diperbaiki selama audit.

## CRITICAL VALIDATION

Konfirmasi:

- No Password;
- OTP;
- Account Recovery;
- Onboarding Approved;
- Onboarding Rejected;
- Accept;
- Reject;
- Cancel;
- Barang Besar;
- Barang Kecil;
- Verification Code Gate;
- Payment hanya Barang Besar;
- Barang Kecil tidak masuk Pendapatan;
- Tip tidak dipotong komisi;
- Customer Rating private;
- Reputation Alert;
- Warranty Claim;
- Legal pages;
- Cross-app consistency;
- Green brand identity;
- Accessibility.

## WEB SEARCH

Ringkas sumber penting yang digunakan dan keputusan yang dipengaruhi hasil riset.

Gunakan sitasi yang dapat diverifikasi.

## FINAL VERDICT

Jika semuanya lolos:

> **PASS — Awetin Mitra berhasil dibangun, seluruh flow telah tersambung, dan journey end-to-end telah berhasil ditelusuri.**

Jika masih ada masalah:

> **NOT PASS — masih terdapat requirement yang belum terpenuhi.**

Namun, perbaiki terlebih dahulu semua masalah yang masih dapat diperbaiki dalam scope ini.

---

# FINAL COMMAND

Mulai pekerjaan sekarang.

Perlakukan seluruh isi prompt ini sebagai:

> **SATU MASTER SPECIFICATION AWETIN MITRA.**

Kerjakan sampai:

> **BUILT → CONNECTED → TESTED → AUDITED → FIXED → FINALIZED**
