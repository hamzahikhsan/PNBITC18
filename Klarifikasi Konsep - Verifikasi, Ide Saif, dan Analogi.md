# Klarifikasi Konsep Kampung Iklim Digital
## Breakdown Pertanyaan Verifikasi, Analisa Ide Tambahan, dan Penjelasan dengan Analogi

**Disusun:** 24 Agustus 2026
**Konteks:** Lanjutan dari dokumen "Konsep Kampung Iklim Digital — Breakdown Lengkap"

---

## 1. Breakdown Poin 10 — Kenapa Pertanyaan Verifikasi Itu Penting

Tiga pertanyaan di bagian penutup dokumen sebelumnya bukan basa-basi — masing-masing punya konsekuensi nyata terhadap konsep kalau tidak dijawab.

### 1.1 "Apakah karhutla benar-benar masuk kriteria resmi ProKlim?"

Kalau ternyata tidak masuk kriteria resmi, itu **tidak menggagalkan konsepnya** — karhutla tetap isu lingkungan yang sah untuk diangkat. Tapi ini mengubah cara menjualnya ke juri:

- Kalau masuk kriteria resmi → tim bisa bilang "ini bagian dari program pemerintah yang sudah ada."
- Kalau tidak → tim harus bilang "ini perluasan yang kami tambahkan karena relevan dengan kondisi 2026," yang merupakan klaim berbeda dan bisa diuji juri saat tanya jawab.

### 1.2 "Siapa sebenarnya 'Pemrakarsa' di SRN-PPI — kader RT/RW langsung atau selalu lewat DLH?"

Ini penentu apakah Modul 5 (ekspor laporan) realistis atau tidak. Kalau yang mengisi SRN-PPI selalu petugas DLH kabupaten (bukan kader RT langsung), aplikasi tidak bisa "menyambung" langsung ke sistem itu — paling jauh hanya bisa membantu DLH, bukan warga RT/RW secara langsung. Ini mengubah siapa target pengguna utama.

### 1.3 "Apakah tim/kenalan tim punya akses ke RT/RW yang sudah ikut ProKlim?"

Bukan syarat wajib, tapi kalau ada, ini validasi tercepat dan termurah sebelum submit proposal — tanya langsung ke ketua RT: "kalau ada aplikasi begini, kepakai tidak?" Kalau tidak ada akses, konsep tetap berbasis riset sekunder (bukan tervalidasi langsung) — ini perlu disebut jujur sebagai batasan di proposal.

---

## 2. Analisa Ide Tambahan dari Tim (Saif) — Early Warning & Lapor Karhutla Berbasis Komunitas

### 2.1 Isi Ide Asli

**Masalah:** El Nino, karhutla naik, warga telat info, lapor bingung, ISPU terpencar, sinyal jelek.

**Solusi:** Early Warning & Lapor Karhutla Berbasis Komunitas.

**Fitur:**
- Dashboard: status Aman/Waspada/Siaga/Bahaya + ISPU + saran
- Peta: titik api, arah angin, posko evakuasi
- Lapor cepat: foto → auto-lokasi → kirim (anonim + verifikasi warga)
- Mode darurat: rute evakuasi, nomor darurat, info posko
- Mode hemat: peta ringan, offline, kompres foto
- Share WA: auto-template laporan

**Flow:**
- Lapor: Home → Lapor → Foto → Lokasi → Kirim → Share WA
- Darurat: Status Bahaya → Rute → Posko
- Verifikasi: Notifikasi → Lihat → "Saya juga lihat"

**Layar:** Onboarding, Home Aman, Home Bahaya, Peta, Detail Api, Lapor (3 step), Posko, Setting.

### 2.2 Kekuatan Ide Ini

Yang paling menonjol: **"Mode Hemat" (peta ringan, offline, kompres foto)** dan penyebutan eksplisit "sinyal jelek" sebagai bagian dari masalah. Ini detail yang sering dilewatkan tim lomba desain — daerah rawan karhutla (Kalimantan, Sumatra pedalaman) memang sering punya sinyal internet buruk, jadi mendesain aplikasi yang tetap berfungsi dalam kondisi jaringan lemah adalah keputusan UX yang matang dan realistis, bukan sekadar pemanis.

Dashboard status Aman/Waspada/Siaga/Bahaya plus data ISPU (indeks standar pencemar udara) dan **arah angin** juga jauh lebih detail teknis dibanding modul karhutla di konsep sebelumnya — arah angin penting karena menentukan ke mana asap/api akan menyebar, bukan fitur dekoratif.

### 2.3 Referensi "Safety Tips" (Aplikasi Jepang) — Verifikasi

Aplikasi yang direferensikan adalah **"Safety tips"** dari Japan Tourism Agency/JNTO — isinya notifikasi bencana multibahasa (gempa, tsunami, cuaca ekstrem) untuk turis asing dan warga di Jepang, dengan mode offline dan panduan evakuasi.

**Catatan penting:** aplikasi ini **bukan aplikasi khusus kebakaran hutan** — Jepang tidak punya masalah karhutla besar seperti Indonesia, jadi fungsinya lebih ke gempa/tsunami/cuaca. Yang bisa dicontoh dari sana adalah **pola UX**-nya (dashboard status, notifikasi darurat berjenjang, mode offline), bukan konten/datanya.

### 2.4 Perbandingan dengan Konsep "Kampung Iklim Digital"

| Aspek | Ide Saif (karhutla-only) | Kampung Iklim Digital |
|---|---|---|
| Cakupan | Fokus sempit, dalam — hanya karhutla | Luas — 6 kategori aksi iklim, karhutla salah satu modul |
| Kedalaman fitur karhutla | Sangat detail (ISPU, arah angin, mode hemat, rute evakuasi) | Masih dasar (baru: foto + lokasi + status) |
| Keterkaitan ke ProKlim/pemerintah | Tidak ada | Terhubung ke program resmi (SRN-PPI, MPA) |
| Risiko | Domain sempit — perlu jawaban kuat kalau juri tanya "kenapa cuma karhutla, subtema kan luas soal sustainability" | Domain luas berisiko terasa kurang dalam di satu isu spesifik kalau tidak difokuskan saat presentasi |

### 2.5 Rekomendasi

**Jangan pilih salah satu secara membuang yang lain — gabungkan.** Pakai kerangka besar "Kampung Iklim Digital" (supaya tetap punya jangkar ke program resmi pemerintah dan cakupan sustainability yang luas sesuai subtema), tapi **ganti isi Modul 3 (Kesiapsiagaan Karhutla) yang masih dangkal dengan detail fitur dari ide Saif** — dashboard status, ISPU, arah angin, mode hemat, share WA.

Hasilnya: kerangka besar yang kredibel + satu modul unggulan yang benar-benar dalam dan matang. Ini memperkuat kriteria "kreativitas & inovasi" karena tim menunjukkan satu isu digarap serius, bukan enam isu yang semuanya dangkal.

*(Status: usulan ini belum dieksekusi ke dokumen breakdown utama — menunggu konfirmasi tim sebelum Modul 3 direvisi penuh.)*

---

## 3. Apakah ProKlim Benar-Benar Berfungsi untuk Lingkungan dan Masyarakat, dan Sesuai Brief?

**Jawaban singkat: ya, secara kerangka sangat sesuai — dengan satu batasan penting yang wajib dipahami dan disebutkan jujur.**

### 3.1 Untuk Lingkungan

ProKlim bukan konsep buatan tim, tapi kerangka resmi mitigasi (sampah, energi, penghijauan) dan adaptasi (air, pangan, kesehatan, bencana) perubahan iklim yang sudah diakui dan diukur pemerintah sendiri lewat SRN-PPI. Dampak lingkungannya bukan klaim yang harus dibuktikan tim dari nol — kerangkanya sudah tervalidasi negara.

### 3.2 Untuk Masyarakat

Unit dasarnya RT/RW, bukan individu — dampaknya otomatis kolektif/komunitas, bukan cuma satu orang memakai aplikasi sendirian. Ini juga selaras dengan budaya gotong royong yang sudah dibahas di riset psikologi sebelumnya.

### 3.3 Untuk Kesesuaian Brief

Cocok dengan "Tech for Nature by Crafting Sustainable Digital Solutions": ini teknologi (aplikasi) untuk alam (aksi iklim nyata) yang sifatnya berkelanjutan — bukan alat sekali pakai, tapi pendamping jangka panjang mengikuti siklus program pemerintah yang terus berjalan.

### 3.4 Batasan yang Harus Disampaikan Jujur

Aplikasi ini **tidak menciptakan** dampak lingkungan itu sendiri — ia hanya mempermudah dan mendorong warga melakukan aksi nyata (menanam, mengelola sampah, melapor titik api). Dampak sebenarnya tetap ada di tindakan fisik warga; aplikasinya adalah fasilitator/pendorong, bukan pelaku langsung.

Ini bukan kelemahan — hampir semua aplikasi lomba UI/UX memang bersifat begitu — tapi proposal tidak boleh ditulis seolah aplikasi ini "menyelamatkan lingkungan" secara langsung. Itu klaim berlebihan yang bisa dipatahkan juri di sesi tanya jawab.

---

## 4. Penjelasan Konsep dengan Analogi

### 4.1 Analogi Utama: Sistem Sabuk Bela Diri

Bayangkan ProKlim seperti **sistem sabuk di bela diri** — ada tingkatan (Pratama, Madya, Utama, sampai Trofi Nasional) yang RT/RW bisa naik kalau berhasil menjalankan "gerakan-gerakan" tertentu (aksi iklim di enam kategori: air, pangan, sampah, energi, penghijauan, bencana). "Penguji sabuk"-nya adalah pemerintah lewat sistem SRN-PPI.

Proses "naik sabuk" ini (SRN-PPI) formatnya seperti **ujian tertulis formal** — dokumen diunggah, form Excel diisi, direview petugas. Masuk akal untuk penilaian resmi, tapi bukan cara warga latihan sehari-hari. Analoginya seperti sekolah bela diri yang punya ujian sabuk resmi, tapi tidak punya "buku catatan latihan harian" yang memudahkan murid dan pelatih melacak progres sebelum hari ujian tiba.

### 4.2 Kampung Iklim Digital = "Buku Catatan Latihan"

Aplikasi yang dipakai warga dan kader RT/RW sehari-hari untuk mencatat "gerakan" apa yang sudah mereka lakukan (checklist aksi + foto bukti), melihat progres kolektif kampung menuju sabuk berikutnya (secara visual, seperti melihat meteran naik), dan saat ujian sabuk tiba, kader tinggal "cetak rekap latihan" itu untuk membantu mengisi ujian resmi (Modul 5 — ekspor laporan) — alih-alih menyusun semuanya dari nol di menit-menit terakhir.

### 4.3 Modul Karhutla = "Gerakan Darurat"

Ada satu "gerakan" khusus yang risikonya tinggi dan butuh alat sendiri: kesiapsiagaan kebakaran hutan dan lahan. Ini seperti **gerakan bela diri untuk situasi darurat** (misalnya teknik menghindar dari serangan mendadak) — bukan latihan rutin biasa, tapi sesuatu yang harus selalu siap dipakai kapan saja, dengan alat khusus.

Modul ini (yang disarankan diperkaya dengan detail dari ide Saif — dashboard status, peta arah angin, mode hemat sinyal) adalah "alat siaga darurat" tersebut, terhubung ke kelompok yang memang sudah dilatih pemerintah untuk menangani situasi ini di lapangan: Masyarakat Peduli Api (MPA).

### 4.4 Alur Pakai, Dianalogikan per Peran

**Warga biasa** = murid biasa di sekolah bela diri. Buka aplikasi → lihat "papan skor" kampung (progres sejauh apa) → pilih satu "gerakan" untuk dilakukan hari ini (misal: kelola sampah organik) → foto bukti → selesai. Kalau melihat tanda bahaya (asap/api), buka menu darurat → foto → tandai lokasi → kirim — seperti memencet alarm.

**Kader RT/RW** = pelatih. Lihat semua catatan latihan murid dalam satu dashboard → verifikasi mana yang valid → saat waktunya ujian sabuk tiba, ambil rekap yang sudah tersusun rapi untuk diserahkan ke "penguji" (SRN-PPI).

**Anggota Masyarakat Peduli Api** = instruktur khusus situasi darurat. Dapat notifikasi prioritas kalau ada laporan titik api, dan koordinasi responsnya tercatat statusnya (dilaporkan → diverifikasi → ditindaklanjuti) supaya pelapor tahu laporannya tidak menghilang begitu saja.

---

## 5. Langkah Selanjutnya (Belum Dieksekusi)

- Merevisi Modul 3 di dokumen breakdown utama dengan detail fitur dari ide Saif (dashboard status, ISPU, arah angin, mode hemat, share WA) — menunggu konfirmasi tim.
- Verifikasi tiga pertanyaan di Bagian 1 sebelum konsep dianggap final.
