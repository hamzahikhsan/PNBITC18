# Perbandingan Konsep: Kampung Iklim Digital vs TukangIn
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Disusun:** 24 Agustus 2026
**Konteks:** Analisa pembanding setelah tim menyampaikan konsep alternatif "TukangIn" dan mempertanyakan ambiguitas konsep "Kampung Iklim Digital"

---

## Ringkasan Eksekutif

Setelah verifikasi pasar dan analisa lintas beberapa dimensi (kejelasan masalah, kejelasan solusi, dampak lingkungan, dampak sosial, kesesuaian brief, dan risiko presentasi), kesimpulannya: **TukangIn lebih kuat sebagai pilihan untuk format lomba ini secara spesifik** — bukan karena idenya "lebih baik" secara absolut, tapi karena ceritanya jauh lebih mudah disampaikan meyakinkan dalam waktu presentasi yang terbatas, dan risikonya lebih mudah dijawab dibanding risiko Kampung Iklim Digital. Keluhan tim bahwa ProKlim "masih ambigu" juga terbukti valid — bukan karena kurang dijelaskan, tapi karena memang sifat dasar topiknya berlapis (program pemerintah + sistem pelaporan institusional yang detail teknisnya sendiri belum bisa dipastikan 100% dari riset).

---

## 1. Breakdown Konsep TukangIn

**Tagline:** *Rusak? Jangan dibuang. Perbaiki.*

**Problem:** Budaya buang-beli baru sudah mengakar, padahal ribuan tukang servis lokal (elektronik, jahit, sol sepatu, las) susah dicari. Barang yang sebenarnya masih layak pakai akhirnya berakhir di TPA.

**Solution:** Platform matchmaking — foto barang rusak, langsung terhubung ke tukang servis terdekat sesuai kategori (elektronik, jahit, sol sepatu, las, dll).

**Unique:** Menggabungkan aksi lingkungan dengan pemberdayaan ekonomi informal. Repair = kurangi sampah + tambah penghasilan tukang.

**Impact:** 1 barang diperbaiki = 1 barang tidak masuk TPA.

### Verifikasi Pasar

Indonesia sudah punya beberapa aplikasi pencarian jasa tukang — Sejasa, Kanggo, Panggil Tukang, lakuKan, Tukang.com — tapi dari penelusuran, mayoritas didominasi **jasa tukang bangunan/rumah** (renovasi, AC, listrik, pipa), bukan jaringan reparasi barang kecil informal (sol sepatu, jahit, servis elektronik kecil) yang dibingkai eksplisit sebagai solusi anti-sampah.

**Kesimpulan verifikasi:** mekanisme dasar (foto → dicocokkan ke penyedia jasa terdekat) bukan hal baru, tapi **domain dan framing-nya** — reparasi barang kecil + pemberdayaan ekonomi informal + pengurangan sampah — adalah celah yang belum digarap kompetitor yang ditemukan. Inovasinya ada di sudut pandang dan segmen, bukan di mekanisme interaksinya.

---

## 2. Perbandingan Head-to-Head

| Dimensi | TukangIn | Kampung Iklim Digital |
|---|---|---|
| Kejelasan masalah | Sangat tinggi — bisa dipahami dalam 1 kalimat, tanpa latar belakang khusus | Sedang — perlu menjelaskan ProKlim & SRN-PPI dulu sebelum masuk ke masalah |
| Kejelasan solusi | Sangat tinggi — alur transaksional familiar (mirip Gojek/Grab untuk jasa) | Sedang — 3 peran berbeda (warga/kader/MPA) dengan alur berbeda-beda |
| Mudah didemonstrasikan di Figma dalam 10 menit | Tinggi — satu flow inti yang jelas | Sedang–Rendah — kompleksitas multi-role butuh lebih banyak waktu jelaskan |
| Dampak lingkungan | Konkret & terukur (tapi perlu dilunakkan klaimnya — lihat Bagian 4) | Luas (6 kategori) tapi sulit ditunjukkan konkret dalam satu prototype |
| Dampak sosial | Sangat kuat — pekerja informal yang nyata & dekat secara emosional | Kuat tapi lebih institusional/abstrak (ketahanan iklim RT/RW) |
| Freshness vs kompetitor | Domain & framing baru, mekanisme umum | Domain sepenuhnya belum tergarap kompetitor manapun |
| Risiko presentasi & tanya jawab (60% bobot final) | Risiko bisa dijawab (diferensiasi, kepercayaan, bootstrap) | Risiko lebih struktural (kompleksitas sistem, ketergantungan ke program pemerintah yang detailnya abu-abu) |
| Kesesuaian brief "Tech for Nature" | Sangat cocok — reduce-reuse-repair inti ekonomi sirkular | Cocok tapi butuh argumen lebih panjang |

---

## 3. Analisis Per Dimensi

### 3.1 Kejelasan Masalah

TukangIn menang telak di sini. "Budaya buang-beli baru, tukang servis susah dicari, barang bagus masuk TPA" bisa dipahami orang awam dalam satu kalimat.

Kampung Iklim Digital butuh menjelaskan dulu apa itu ProKlim, apa itu SRN-PPI, baru masuk ke masalah sebenarnya — dan ini justru menguatkan keluhan tim: **ProKlim memang ambigu bukan karena kurang dijelaskan, tapi karena memang berlapis secara struktural** (program pemerintah + sistem pelaporan institusional). Ini bukan keraguan yang bisa dihilangkan hanya dengan penjelasan yang lebih baik — itu sifat dasar topiknya.

### 3.2 Kejelasan Solusi & Kemudahan Didemonstrasikan

TukangIn unggul karena satu alur transaksional jelas (foto barang rusak → dicocokkan ke tukang terdekat → selesai), mirip pola yang sudah dikenal semua orang. Juri tidak perlu belajar konsep baru untuk mengikuti presentasi.

Kampung Iklim Digital punya tiga peran berbeda dengan alur berbeda-beda — secara desain sah, tapi untuk presentasi 10 menit + tanya jawab 15 menit, kompleksitas ini jadi risiko nyata: waktu habis menjelaskan sistem, bukan mempertahankan keputusan desain.

### 3.3 Dampak Lingkungan

TukangIn punya metrik bersih dan gampang diverifikasi logikanya: "1 barang diperbaiki = 1 barang tidak masuk TPA." Tapi klaim ini perlu dilunakkan — tidak semua barang yang tidak diperbaiki otomatis langsung ke TPA (ada yang dijual, didonasikan, dll). Sebaiknya di proposal ditulis "berpotensi mengurangi", bukan klaim pasti 1:1.

Kampung Iklim Digital cakupannya lebih luas (6 kategori sekaligus) tapi karena itu lebih sulit menunjukkan dampak konkret dan terukur dalam satu prototype.

### 3.4 Dampak Sosial — Titik Kuat TukangIn

Ini yang paling menonjol. TukangIn menyasar tukang servis, penjahit, tukang sol sepatu — pekerja informal yang nyata dan dekat secara emosional dengan hampir semua orang Indonesia (semua orang pernah lihat atau pakai jasa tukang sol keliling). Ini jauh lebih mudah membangun empati juri dibanding narasi "ketahanan iklim tingkat RT/RW" yang lebih institusional dan abstrak.

### 3.5 Kesesuaian dengan Brief

Keduanya sah masuk kategori "Tech for Nature by Crafting Sustainable Digital Solutions" — tapi TukangIn lebih "bersih" fit-nya karena reduce-reuse-repair adalah prinsip inti ekonomi sirkular yang lugas. Kampung Iklim Digital butuh argumen lebih panjang untuk menjelaskan kenapa digitalisasi program pemerintah relevan dengan tema.

---

## 4. Risiko TukangIn yang Perlu Diwaspadai (Supaya Tidak Dianggap Sempurna)

- **Diferensiasi vs kompetitor.** Juri yang jeli bisa bertanya "ini kan mirip Sejasa/Kanggo, bedanya di mana selain kemasan hijau?" — tim perlu jawaban tegas: fokus ke tukang informal skala kecil (sol sepatu, jahit, elektronik kecil), bukan kontraktor/jasa besar seperti kompetitor eksisting.
- **Kepercayaan & jaminan kualitas.** Juri bisa bertanya bagaimana kalau tukang yang dicocokkan tidak becus, atau barang malah rusak lebih parah. Ini perlu dipikirkan sebagai fitur (rating, verifikasi, garansi sederhana), bukan diabaikan.
- **Masalah bootstrap marketplace dua sisi.** Kenapa tukang mau gabung platform baru kalau supply pelanggan belum ada? Perlu strategi awal yang masuk akal untuk dijawab di sesi tanya jawab, meski tidak harus jadi fitur di prototype.
- **Klaim dampak perlu dilunakkan** — lihat Bagian 3.3.

---

## 5. Kesimpulan & Rekomendasi

Untuk format lomba ini secara spesifik — presentasi singkat, tanya jawab berbobot 60% dari nilai final, waktu terbatas — **TukangIn lebih kuat sebagai pilihan.** Ceritanya lebih mudah disampaikan meyakinkan dalam waktu terbatas, dan risikonya jauh lebih mudah dijawab dibanding risiko struktural Kampung Iklim Digital.

Ini bukan berarti Kampung Iklim Digital "gagal" sebagai ide — cakupannya justru lebih ambisius dan komprehensif. Tapi untuk kompetisi dengan format presentasi ketat seperti ini, kejelasan dan kemudahan dipertahankan saat tanya jawab jauh lebih menentukan daripada keluasan cakupan.

---

## 6. Langkah Selanjutnya (Belum Dieksekusi)

Kalau tim memutuskan lanjut ke arah TukangIn, tiga hal berikut perlu diperkuat dulu sebelum masuk ke breakdown fitur & flow lengkap:

1. Diferensiasi eksplisit vs Sejasa/Kanggo/lakuKan.
2. Mekanisme kepercayaan (rating, verifikasi, garansi sederhana).
3. Strategi bootstrap dua sisi (menarik tukang & pelanggan di awal).

Setelah tiga hal ini disepakati arahnya, breakdown lengkap (latar belakang, fitur, user flow, daftar layar Figma, design rationale, risiko & mitigasi) bisa disusun setara levelnya dengan konsep-konsep sebelumnya.

---

## 7. Sumber

- [Tukang Servis AC Terbaik di Indonesia — Sejasa](https://www.sejasa.com/layanan/tukang-servis-ac)
- [Jasa Pertukangan Terbaik Indonesia — Sejasa](https://www.sejasa.com/layanan/jasa-pertukangan)
- [6 Aplikasi Android Terbaik untuk Cari Jasa Tukang — CariSinyal](https://carisinyal.com/aplikasi-cari-jasa-tukang/)
- [20 Aplikasi Pencarian Jasa Serba Guna — Pasangan Tipe Tirta](https://www.pasangantipetir.id/20-aplikasi-pencarian-jasa-serba-guna/)
- [Tukang.com](https://tukang.com/)
- [The Right to Repair — IEEP Policy Brief](https://ieep.eu/wp-content/uploads/2022/12/Policy-brief_The-right-to-repair_IEEP-2022.pdf)
- [Repair, reduce, recycle: Ways to tackle mounting e-waste — World Economic Forum](https://www.weforum.org/stories/2022/01/repair-recycle-waste-circular-economy/)
- [Indonesia's Expanding Electronic Waste Landscape — SUPRA International](https://supra-international.com/insights/indonesia-s-expanding-electronic-waste-landscape)
