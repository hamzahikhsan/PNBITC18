# Sintesis Riset — Kompilasi 6 Dokumen Tim PNBITC#18

**Metode:** Analisa dokumen (desk research synthesis) — bukan riset primer dengan partisipan
**Sumber:** 6 dokumen hasil riset AI agent lain + ideation tim, diunggah 21 Agustus 2026
**Disusun:** 23 Agustus 2026

---

## Ringkasan Eksekutif

Enam dokumen yang kalian kumpulkan sebenarnya berisi **3 kelompok konten**, bukan 6 topik terpisah — dan salah satu kelompok tumpang tindih cukup besar sehingga sebagian bisa dianggap arsip pendukung, bukan bacaan wajib. Kelompok pertama adalah fondasi psikologi perilaku (kenapa orang tidak konsisten berbuat ramah lingkungan). Kelompok kedua adalah riset domain sampah/food waste Indonesia yang sudah dikembangkan sampai satu konsep aplikasi utuh bernama **"Duluan"**. Kelompok ketiga adalah dua ide brainstorming tim kalian sendiri (**AI Waste Scanner** dan **Smart Community Waste Pickup**) yang levelnya masih konsep awal.

Temuan paling penting dari analisa ini: **konsep "Duluan" jauh lebih konsisten dengan riset psikologi yang kalian kumpulkan sendiri** dibanding dua ide brainstorming tim. Ada juga satu ketidaksesuaian yang perlu diklarifikasi — dokumen ide tim menyebut tema lomba melibatkan "dukungan teknologi AI", padahal subtema resmi di juklak tidak menyebut AI sama sekali. Detail lengkap ada di Bagian 5.

---

## 1. Peta Dokumen — Mana yang Perlu Dibaca, Mana yang Cukup Jadi Arsip

| No. | Nama Dokumen | Isi Inti | Status |
|---|---|---|---|
| 1 | *ok dari semua hasil riset dan tesis kamu...* | Riset domain sampah & food waste Indonesia + konsep aplikasi **"Duluan"** lengkap (data, kompetitor, fitur, user flow, 13 layar, design rationale) | **Wajib dibaca penuh** — dokumen paling matang dan actionable |
| 2 | *Kompilasi Riset Lengkap PNBITC18* | Gabungan dari dokumen #4, #5, #6 di bawah + tambahan framework Theory of Planned Behavior | **Wajib dibaca** — ini adalah versi ringkas/index dari 3 dokumen lain |
| 3 | *UIUX Competition Environmental Solution Ideas* | 2 ide brainstorming tim: AI Waste Scanner & Smart Community Waste Pickup | **Wajib dibaca** — tapi lihat catatan kritis di Bagian 5 |
| 4 | *Strategi Mengatasi Dragon Limited Cognition* | Sudah termuat di dalam dokumen #2, bagian 6 | Arsip — simpan untuk kutipan detail saja |
| 5 | *Riset Pola Habit-Forming Aplikasi Lingkungan* | Sudah termuat di dalam dokumen #2, bagian 1 (versi dokumen ini lebih detail: ada angka retensi spesifik & daftar studi kasus lebih lengkap) | Arsip — simpan untuk kutipan angka/sumber |
| 6 | *Riset Psikologi Perilaku Perubahan Iklim* | Sudah termuat di dalam dokumen #2, bagian 2–5 (versi dokumen ini lebih detail: ada data spesifik Indonesia seperti korelasi r=0.588 di studi mahasiswa Bandung) | Arsip — simpan untuk kutipan angka/sumber |

**Cara pakai peta ini:** kalau ada anggota tim yang cuma sempat baca 3 dokumen, baca #1, #2, #3. Dokumen #4–#6 tetap berguna disimpan karena memuat detail statistik dan sitasi sumber yang dipangkas di versi kompilasi (#2) — berguna saat menulis proposal atau menyiapkan jawaban tanya jawab yang butuh angka presisi.

---

## 2. Kelompok 1 — Fondasi Psikologi Perilaku

### Tema A: Kesadaran bukan masalahnya, konsistensi yang jadi masalah

Attitude-Behavior Gap: mayoritas orang sudah peduli lingkungan (di beberapa survei global sampai 89% mendukung aksi iklim), tapi hanya sebagian kecil yang benar-benar bertindak konsisten. Penyebabnya dipetakan jadi tiga: intrapersonal (bias kognitif, kebiasaan lama), sosial (norma yang lemah/salah dipersepsikan), struktural (biaya, kenyamanan, akses).

**Implikasi:** aplikasi yang cuma mengedukasi/mengingatkan tidak akan cukup. Harus aktif menutup jarak antara niat dan tindakan nyata.

### Tema B: Tujuh hambatan psikologis spesifik (Dragons of Inaction, Gifford 2011)

| Dragon | Inti masalah | Paling relevan untuk domain kalian? |
|---|---|---|
| Limited Cognition | Dampak lingkungan terasa abstrak & jauh | **Sangat relevan** — dibahas paling detail di seluruh dokumen |
| Ideologies | Percaya teknologi/pihak lain yang akan selesaikan | Relevan sedang |
| Comparisons with Others | Norma sosial lemah ("orang lain juga tidak melakukan") | Relevan — bisa dijawab dengan social proof |
| Sunk Costs | Kebiasaan lama terasa sayang ditinggalkan | Relevan rendah-sedang |
| Discredence | Tidak percaya data/otoritas | Relevan rendah |
| Perceived Risks | Takut rugi waktu/uang/kenyamanan | Relevan sedang |
| Limited Behavior/Tokenism | Merasa sudah cukup setelah aksi kecil | Relevan sedang |

**Implikasi:** setiap fitur idealnya bisa dijelaskan sedang "melawan dragon yang mana" — ini kerangka paling kuat untuk justifikasi di sesi tanya jawab juri (bobot 60% di final).

### Tema C: Pola desain yang terbukti membangun kebiasaan jangka panjang

Dari studi kasus (Ant Forest, Ecosia, Too Good To Go, Folium, JouleBug) dan riset retensi (mayoritas aplikasi wellness/habit kehilangan >70% pengguna dalam 30 hari, drop-off eco-app tipikal di minggu 1–2):

- **Yang terbukti bekerja:** micro-action di awal (bukan daftar panjang kebiasaan), automasi/low-friction logging, visual ownership (metafora tumbuh seperti pohon/ekosistem), feedback konkret & emosional (bukan angka abstrak), flexible streak (bukan streak kaku yang menghukum), social layer yang tidak menggurui, reward ekonomi nyata, habit stacking ke rutinitas yang sudah ada, tone positif.
- **Yang terbukti gagal:** manual logging panjang, guilt-based messaging, streak kaku, 10+ kebiasaan di hari pertama, leaderboard global yang intimidatif, poin/badge sebagai satu-satunya motivator.

### Tema D: Konteks Indonesia yang berulang muncul di semua dokumen

Bank sampah informal sudah mapan (solusi digital sebaiknya berintegrasi, bukan menggantikan), insentif ekonomi langsung sangat kuat dibanding gamifikasi murni, budaya kolektif/gotong royong bisa dimanfaatkan untuk challenge komunitas, dan ada data awal dari studi mahasiswa Bandung bahwa *climate anxiety* justru berkorelasi positif dengan perilaku pro-lingkungan (asal disertai rasa mampu bertindak/self-efficacy).

---

## 3. Kelompok 2 — Riset Domain Sampah & Konsep "Duluan"

### Data kunci

- Timbulan sampah Indonesia: **±24,8 juta ton/tahun**, **65,45% belum terkelola** (data SIPSN 2025).
- Rumah tangga menyumbang **56,7%** dari total timbulan sampah.
- Komposisi sampah nasional: **sisa makanan 40,8%**, plastik hanya **20%** — food waste adalah masalah yang secara volume lebih besar dari plastik, tapi mayoritas solusi digital yang ada justru fokus ke sampah anorganik bernilai jual.

### Gap yang teridentifikasi di lanskap aplikasi eksisting

Enam layanan dibandingkan (Rekosistem, Octopus, AKSI, BankIn, aplikasi bank sampah lokal, Ngupahan) — pola yang konsisten: semuanya kuat di sisi transaksi sampah bernilai ekonomi, tapi lemah di lima area: friksi harian sebelum sampah disetor (bingung kategori, cara cuci/simpan), sampah organik yang kurang terlayani, insentif ekonomi yang terbatas untuk sampah tak bernilai jual, minim transparansi soal apa yang terjadi setelah sampah disetor, dan infrastruktur bank sampah yang terfragmentasi antarwilayah.

### Konsep "Duluan"

Aplikasi asisten dapur yang **mencegah** makanan menjadi sampah — bukan sekadar mencatat sampah setelah terjadi. Mengikuti hierarki: mencegah → menggunakan kembali → membagikan → mengolah → membuang dengan benar.

**Fitur inti:** Stok Dapur Cepat (input ringan lewat scan struk/foto/preset), kartu "Pakai Dulu" (maksimal 3 prioritas di beranda), resep dari bahan tersisa, meal planner & pengatur porsi, mode sisa makanan (simpan/olah/bagikan/kompos/residu), panduan sampah organik, dan ringkasan penghematan.

**Target pengguna (asumsi desain, bukan fakta juklak):** mahasiswa, pekerja muda, pasangan muda, penghuni kos/apartemen kota besar — akses kulkas ada, tapi ruang penyimpanan dan waktu terbatas.

**Yang membuat konsep ini kuat:** sudah punya user flow lengkap, 13 layar prototype yang disarankan, design rationale untuk tiap keputusan (termasuk alasan eksplisit *menghindari* gamifikasi sebagai inti — selaras dengan Tema C di atas), tabel risiko & mitigasi, dan daftar metrik dampak yang realistis (plus daftar klaim yang harus dihindari karena tidak bisa dibuktikan, seperti "menyelamatkan bumi" atau angka pengurangan karbon tanpa metodologi).

---

## 4. Kelompok 3 — Ide Brainstorming Tim

### Idea 1 — AI Waste Scanner & Recycling Assistant

Pengguna memfoto barang/sampah → AI mengenali jenis & material → sistem merekomendasikan tindakan (daur ulang / berbahaya / tidak bisa didaur ulang / masih bernilai jual) → jika bernilai, bisa langsung dijual lewat marketplace bawaan aplikasi dengan estimasi harga dari AI.

### Idea 2 — Smart Community Waste Pickup

Platform pengambilan sampah terjadwal untuk komplek perumahan/cluster, menghubungkan warga, pengelola lingkungan, dan pemulung/collector. Ada AI prediksi volume sampah, penjadwalan otomatis, pencarian collector berbasis lokasi, dashboard komunitas, dan sistem reward berbasis poin untuk warga yang aktif memilah/mengikuti jadwal.

Menurut perbandingan yang dibuat tim sendiri di dokumen ini, Idea 2 dinilai lebih unggul dari sisi social impact dan scalability, sementara Idea 1 lebih unggul dari sisi kekuatan peran AI.

---

## 5. Titik Kritis yang Perlu Diperhatikan Tim

Ini bagian yang saya rasa penting disampaikan apa adanya, bukan cuma dirangkum rapi.

### 5.1 Idea 2 berisiko bertentangan dengan riset psikologi kalian sendiri

Idea 2 mengandalkan "Reward System" berbasis poin dan "Community Dashboard" yang sifatnya kompetitif antarwarga. Tapi Kelompok 1 (riset psikologi yang kalian kumpulkan sendiri) secara eksplisit menyimpulkan: poin/badge semata bukan motivator jangka panjang yang kuat, dan leaderboard global yang intimidatif termasuk pola yang **harus dihindari**. Ini bukan berarti Idea 2 harus dibuang — tapi kalau dipilih, sistem reward dan dashboard-nya perlu didesain ulang mengikuti prinsip dari Kelompok 1 (misalnya: reward ekonomi nyata dibanding poin abstrak, challenge kolektif dibanding ranking individual yang mempermalukan).

### 5.2 Idea 1 sulit dibuktikan lewat prototype Figma statis

Nilai jual utama Idea 1 adalah kemampuan AI mengenali barang dari foto — tapi Figma tidak benar-benar menjalankan model AI. Kalau dipilih, tim perlu strategi eksplisit untuk mensimulasikan hasil AI di prototype (misalnya lewat skenario/state yang sudah ditentukan) tanpa membuat juri merasa itu janji kosong saat sesi tanya jawab.

### 5.3 Ketidaksesuaian penyebutan tema

Dokumen Kelompok 3 menuliskan tema sebagai *"Aplikasi yang dapat membantu menyelesaikan permasalahan lingkungan dengan dukungan teknologi AI."* Ini berbeda dari subtema resmi di juklak: **"Tech for Nature by Crafting Sustainable Digital Solutions"** — yang sama sekali tidak menyebut kata AI sebagai syarat. Ini perlu diklarifikasi ke sumber aslinya (apakah ini interpretasi bebas dari AI agent yang dipakai, atau memang ada info tambahan dari panitia yang belum sampai ke saya). Kalau ternyata AI bukan syarat wajib, konsep "Duluan" (yang tidak bergantung pada AI classifier) tetap sepenuhnya sah dan tidak dirugikan dari sisi kesesuaian tema.

### 5.4 Konsistensi lintas dokumen

Yang secara jelas paling konsisten dengan seluruh riset psikologi di Kelompok 1 adalah konsep **"Duluan"** — mulai dari penghindaran gamifikasi sebagai inti, penggunaan micro-action (kartu "Pakai Dulu" maksimal 3 item), sampai penghindaran klaim dampak yang tidak bisa dibuktikan. Idea 1 dan Idea 2 masih di tahap konsep awal dan belum "diuji" terhadap prinsip-prinsip di Kelompok 1.

---

## 6. Insight → Peluang

| Insight | Peluang | Dampak | Effort |
|---|---|---|---|
| Sisa makanan (40,8%) lebih besar dari plastik (20%) di komposisi sampah, tapi solusi digital minim di area ini | Fokus ke food waste (seperti "Duluan") adalah ruang yang kurang tergarap kompetitor | Tinggi | Sedang |
| Reward poin/leaderboard terbukti lemah untuk retensi | Ganti/kombinasikan dengan insentif ekonomi nyata + visual ownership | Tinggi | Rendah–Sedang |
| Friksi harian (bingung kategori, cara simpan) adalah hambatan terbesar sebelum sampah disetor | Panduan visual/kategori sederhana bisa jadi fitur pembeda kuat | Sedang–Tinggi | Rendah |
| Pengguna tidak tahu apa yang terjadi setelah sampah disetor (kesenjangan aksi-dampak) | Riwayat status penyaluran (dikumpulkan → diverifikasi → diolah) membangun kepercayaan | Sedang | Sedang |
| Bank sampah informal sudah mapan tapi terfragmentasi | Aplikasi sebagai penghubung/pelengkap, bukan pengganti — dengan peta fasilitas lokal | Tinggi | Tinggi |

---

## 7. Perbandingan Tiga Arah Konsep

| Aspek | Duluan (food waste) | Idea 1 (AI Waste Scanner) | Idea 2 (Smart Community Pickup) |
|---|---|---|---|
| Kematangan konsep | Sudah lengkap (flow, 13 layar, rationale, risiko) | Konsep awal | Konsep awal |
| Konsistensi dgn riset psikologi Kelompok 1 | Tinggi | Belum diuji | Berisiko bertentangan (poin/leaderboard) |
| Mudah dibuktikan di prototype Figma statis | Ya | Sulit (bergantung AI) | Ya |
| Diferensiasi vs aplikasi eksisting | Tinggi (fokus organik yang jarang digarap) | Sedang (banyak app scanner serupa secara global) | Sedang–Tinggi |
| Kompleksitas sistem (butuh banyak pihak: warga, pengelola, collector) | Rendah (individual) | Rendah–Sedang | Tinggi |
| Risiko soal "AI wajib" jika ternyata bukan syarat | Tidak berpengaruh | Konsep jadi kurang relevan | Sebagian fitur (prediksi AI) kurang relevan |

---

## 8. Rekomendasi

1. **Prioritas tinggi — klarifikasi tema.** Sebelum melangkah lebih jauh, pastikan ke panitia atau sumber asli apakah "dukungan teknologi AI" memang bagian dari ketentuan resmi atau bukan. Ini memengaruhi bobot ketiga konsep secara berbeda.
2. **Prioritas tinggi — jadikan "Duluan" baseline diskusi**, karena paling matang dan paling konsisten dengan riset yang sudah susah payah kalian kumpulkan. Bukan berarti harus dipilih, tapi jadikan tolok ukur pembanding untuk menilai dua ide lain.
3. **Prioritas sedang — jika Idea 2 tetap menarik**, revisi sistem reward-nya dulu (dari poin/leaderboard kompetitif menjadi insentif ekonomi/kolektif) sebelum dikembangkan lebih jauh, supaya tidak bertentangan dengan riset sendiri.
4. **Prioritas sedang — jika Idea 1 tetap menarik**, siapkan strategi presentasi khusus untuk menjelaskan bagaimana kemampuan AI-nya akan "dibuktikan" meski Figma statis.
5. **Prioritas rendah — gabungkan yang terbaik.** Tidak harus pilih satu secara eksklusif; misalnya elemen "panduan visual pemilahan" dari riset Kelompok 2 bisa memperkuat Idea 1, atau elemen "peta fasilitas organik" bisa melengkapi Idea 2.

---

## 9. Pertanyaan yang Masih Perlu Dijawab

- Apakah "dukungan teknologi AI" benar bagian dari ketentuan resmi lomba, atau salah kutip dari AI agent yang dipakai teman kalian? (Lihat juga poin ini di Context Brief sebelumnya soal daftar sub-tema resmi yang belum terverifikasi.)
- Kalau tim condong ke arah food waste ("Duluan"), apakah target pengguna (kos/apartemen kota besar) ini hasil kesepakatan tim atau masih asumsi satu orang?
- Untuk Idea 2, siapa yang akan memerankan "collector/pemulung" dalam skenario prototype — apakah ini realistis digambarkan dalam 10 menit presentasi?
- Apakah tim sudah punya preferensi personal/kedekatan terhadap salah satu domain (food waste vs sampah umum vs logistik komunitas) yang belum tercermin di dokumen manapun?

---

## 10. Catatan Metodologi

Sintesis ini dibuat dari 6 dokumen hasil riset sekunder (desk research) yang dikumpulkan dari berbagai AI agent dan ideation internal tim — bukan dari wawancara atau pengujian dengan pengguna nyata. Artinya seluruh "insight" di atas masih berupa hipotesis yang perlu divalidasi lewat riset primer ringan (misalnya uji cepat konsep ke 5–8 calon pengguna), sebagaimana sudah disarankan di salah satu dokumen sumber. Belum ada data retensi longitudinal yang spesifik untuk aplikasi eco-app di Indonesia — semua angka retensi/pola habit-forming di atas berbasis studi global yang diasumsikan berlaku serupa di konteks Indonesia.
