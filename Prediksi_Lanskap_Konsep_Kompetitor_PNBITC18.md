# Sintesis Riset: Prediksi Lanskap Konsep Kompetitor — PNBITC#18 Desain UI/UX

**Metode:** Analisa pola (desk research + pattern forecasting) — **bukan** data observasi karya kompetitor sungguhan, karena karya belum ada yang dikumpulkan (deadline 14–16 September 2026).
**Cakupan riset:** Kompilasi 6+ dokumen riset/brainstorming internal tim (arsip project ini) + pencarian web lanjutan soal pola ide kompetisi UI/UX sustainability di Indonesia & global.
**Disusun:** 26 Agustus 2026

---

## Executive Summary

Pertanyaannya bukan "ide apa yang paling bagus", tapi "ide apa yang paling *mungkin dipikirkan tim lain juga*" — dan dua pertanyaan itu punya jawaban berbeda. Berdasarkan tiga sumber bukti (data saturasi pasar aplikasi sampah Indonesia yang sudah tim kumpulkan sendiri, pola ide di studi kasus UI/UX mahasiswa Indonesia yang bisa dicek publik, dan struktur insentif kompetisi ini — peserta pelajar/mahasiswa, Figma-only, waktu persiapan pendek dari Technical Meeting 5 September ke deadline 14–16 September), kesimpulannya jelas: **kompetitor lain kemungkinan besar akan berkerumun di sekitar 3 domain yang sama** — pengelolaan sampah/bank sampah, jejak karbon personal, dan food waste/kulkas pintar — karena ini domain yang paling gampang di-Google, paling banyak template studi kasusnya di Behance/Dribbble, dan paling sering muncul di daftar "ide proyek sustainability untuk mahasiswa" versi kampus.

Ini punya implikasi langsung dan tidak menyenangkan untuk salah satu dari tiga konsep yang baru dipresentasikan Saif: **"Sebelum Basi" berada tepat di domain yang diprediksi paling padat kompetitor**, dan justru menariknya, ini domain yang sama dengan yang sudah tim kembangkan jauh lebih matang sebelumnya lewat konsep "Duluan" — sementara "Sebelum Basi" versi terbaru malah kembali memakai pola (leaderboard RT kompetitif) yang riset psikologi tim sendiri sudah simpulkan lemah untuk retensi. Sebaliknya, **TukangIn dan ImpactPool berada di domain yang diprediksi jarang dipilih kompetitor** — tapi untuk alasan berbeda, dan dengan beban pembuktian di sesi tanya jawab yang juga berbeda. Detail lengkap dan bukti pendukung ada di bawah.

---

## Bagian 1 — Kluster Konsep yang Diprediksi Ramai Dipilih Kompetitor

### Kluster 1: Bank Sampah / Pengelolaan Sampah & Daur Ulang — Prevalensi Diprediksi **Sangat Tinggi**

Ini domain paling "default" untuk tugas atau lomba bertema lingkungan di Indonesia. Buktinya bukan cuma dugaan:

- Pencarian cepat menemukan banyak **skripsi/tugas akhir desain UI/UX bank sampah** dari kampus Indonesia (Telkom University, Universitas Negeri Makassar) dan studi kasus publik di Dribbble ("Bank Sampah MOLEN") serta Medium ("Gredz — Aplikasi Pengelola Daur Ulang Sampah") — pola ini sudah jadi semacam "tugas wajib" tersendiri di kalangan mahasiswa desain Indonesia.
- Artikel resmi kampus (UMN) yang menyarankan ide proyek sustainability untuk mahasiswa secara eksplisit menyebut "**intelligent waste management systems**" sebagai salah satu dari hanya empat kategori ide yang mereka rekomendasikan — ini sinyal kuat bahwa ide ini ada di "starter list" yang kemungkinan juga dibaca tim-tim lain.
- Riset internal tim sendiri (dokumen *Riset Ideation Baru*) sudah memetakan minimal **8 pemain aktif** di pasar riil Indonesia (Octopus, Duitin, EMPOWER, Rekosistem, Plastic Bank Indonesia, AKSI, BankIn, Ngupahan) — pasar sudah sangat padat bahkan di luar konteks lomba.

**Implikasi:** kalau banyak tim lain mendarat di sini, fitur standar (jadwal pickup, poin, marketplace jual-beli sampah, peta bank sampah) sudah jadi ekspektasi dasar juri, bukan lagi nilai pembeda. Tim yang tetap ke domain ini butuh sudut yang benar-benar berbeda dari delapan pemain yang sudah ada.

### Kluster 2: Jejak Karbon Personal (Carbon Tracker) — Prevalensi Diprediksi **Tinggi**

Ini pola case-study paling umum di Behance/Dribbble untuk topik "sustainability app" secara global — mudah ditemukan sebagai template "UX/UI Case Study" siap tiru strukturnya (log aktivitas → hitung jejak karbon → dashboard → tips). Artikel UMN yang sama juga menyebut "carbon footprint monitoring applications" sebagai ide default. Masalahnya, brief kompetisi sendiri (dan riset tim) sudah mengidentifikasi kelemahan klasik pola ini: angka karbon terasa abstrak dan tidak actionable — jadi meski kategori ini diprediksi ramai, kemungkinan besar eksekusinya dangkal di banyak tim lain (peluang untuk tim yang menyelesaikan masalah abstraksi ini secara serius, tapi kategorinya sendiri tetap diprediksi padat).

### Kluster 3: Food Waste / Kulkas Pintar — Prevalensi Diprediksi **Tinggi** (dan ini yang paling relevan untuk konsep "Sebelum Basi")

Domain ini juga masuk daftar rekomendasi UMN, dan pola "smart fridge / expiry tracker / resep dari sisa bahan" adalah hasil pencarian yang sangat umum di studi kasus desain global. Yang membuat prediksi ini makin kuat secara spesifik untuk konteks Indonesia: statistik "sisa makanan = 40,8% komposisi sampah nasional (data SIPSN)" adalah angka yang **sangat mudah ditemukan** di halaman pertama pencarian manapun soal sampah Indonesia — riset tim sendiri menemukannya, dan kemungkinan besar tim lain yang meriset topik sampah Indonesia (bukan cuma food waste) juga akan menemukan angka yang sama, lalu tergoda mengarah ke konsep serupa: pelacak stok dapur, alert kedaluwarsa, resep dari sisa bahan.

**Titik kritis untuk tim:** "Sebelum Basi" (dari screenshot brainstorming Saif) persis berada di pola ini — auto-alert sebelum basi, saran resep, hitung kg makanan terselamatkan, plus leaderboard RT. Tim sendiri sebenarnya **sudah membangun versi yang jauh lebih matang dari domain yang sama** lewat konsep "Duluan" (13 layar, user flow lengkap, design rationale, tabel risiko) — dan salah satu keputusan desain paling ditekankan di "Duluan" adalah **secara sengaja menghindari gamifikasi/poin sebagai inti solusi**, karena riset habit-forming tim sendiri menyimpulkan pola leaderboard kompetitif justru berisiko memicu churn (rasa bersalah, perbandingan sosial yang mengintimidasi). "Sebelum Basi" versi terbaru justru menaruh "Leaderboard RT: adu siapa paling banyak menyelamatkan makanan" sebagai fitur gamifikasi utama — ini bukan cuma berisiko tumpang tindih dengan kompetitor lain, tapi juga **berlawanan dengan kesimpulan riset psikologi tim sendiri**. Kalau juri sempat membaca konsistensi argumen tim (dan sesi tanya jawab 60% dirancang untuk menguji itu), ini titik lemah yang bisa dipertanyakan langsung.

### Kluster 4: Gamifikasi Habit-Tracking (bukan domain tersendiri, tapi lapisan yang diprediksi hampir universal)

Poin, badge, dan leaderboard adalah "gerakan default" yang diajarkan di hampir semua kelas/bootcamp UI/UX sebagai cara menunjukkan "inovasi". Prediksi: mayoritas kompetitor, apa pun domainnya, kemungkinan besar akan menempelkan mekanik ini tanpa justifikasi psikologis yang dalam. Ini justru celah: tim yang **secara eksplisit menjelaskan kenapa TIDAK memakai leaderboard kompetitif murni** (seperti rationale "Duluan") akan terdengar lebih matang secara "logic" di sesi tanya jawab dibanding kompetitor yang menaruh leaderboard begitu saja sebagai hiasan "inovasi".

### Kluster 5: Marketplace Barang Bekas / Ekonomi Sirkular — Prevalensi Diprediksi **Sedang**

Terkait tren thrifting Gen Z Indonesia, cukup umum tapi tidak sepadat kluster 1–3. Berbeda dari TukangIn (yang fokus jasa reparasi, bukan jual-beli barang bekas) — kalau kompetitor lain masuk ke "reduce-reuse-recycle" secara umum, kemungkinan mereka mendarat di marketplace resale, bukan matchmaking tukang servis.

### Kluster 6: Peringatan Dini Bencana / Kualitas Udara / Karhutla — Prevalensi Diprediksi **Sedang, dan Sedang Naik karena Faktor Waktu**

Ini poin koreksi penting terhadap asumsi di salah satu dokumen riset internal sebelumnya ("Kampung Iklim Digital — Breakdown Lengkap") yang menyimpulkan modul karhutla "belum tersentuh kompetitor manapun". Klaim itu benar untuk **aplikasi/startup yang sudah eksis di pasar riil** — tapi ini bukan pertanyaan yang diajukan sekarang. Pertanyaannya adalah soal **tim kompetitor lain di PNBITC#18**, dan karhutla 2026 adalah **berita nasional yang sedang berlangsung** (202.011 hektare terbakar per akhir Juli 2026, asap sampai Malaysia, liputan aktif di CNBC Indonesia dan Mongabay sepanjang Agustus 2026). Tim lain yang mencari "isu lingkungan Indonesia terkini" untuk riset lomba **sangat mungkin menemukan berita yang sama persis** dalam rentang waktu persiapan yang sama (Agustus–September 2026). Jadi freshness topik ini terhadap kompetitor lomba **tidak seyakin** freshness-nya terhadap startup/app yang sudah eksis — dua populasi pembanding yang berbeda dan tidak boleh disamakan.

---

## Bagian 2 — Kluster yang Diprediksi Jarang Dipilih Kompetitor

### TukangIn (Repair Economy Network) — Prevalensi Diprediksi **Rendah**

Ada dua lapis alasan kenapa domain ini diprediksi jarang dipilih kompetitor lain, bukan cuma satu:

1. **Terhadap pasar riil** (sudah diverifikasi tim lewat riset kompetitor langsung): Sejasa, Kanggo, dan lakuKan semuanya bermain di jasa umum/renovasi skala menengah, bukan reparasi barang kecil (sol sepatu, jahit, elektronik kecil) yang dibingkai eksplisit sebagai solusi anti-sampah.
2. **Terhadap pola ideation kompetitor lomba**: "matchmaking jasa reparasi informal" bukan pola yang muncul di daftar "ide proyek sustainability" manapun yang saya temukan (baik UMN, Behance, maupun listicle Indonesia) — mayoritas materi yang jadi rujukan cepat mahasiswa mengarah ke sampah/karbon/food waste, bukan ke ekonomi jasa informal. Ini butuh sudut pandang yang sedikit lebih tidak biasa (memikirkan tukang servis sebagai subjek, bukan cuma sampah sebagai objek).

Ini alasan objektif kenapa dokumen perbandingan internal tim ("Perbandingan Konsep — Kampung Iklim Digital vs TukangIn") sebelumnya menyimpulkan TukangIn lebih unggul untuk format lomba ini — kesimpulan itu tetap konsisten dengan prediksi lanskap kompetitor yang lebih luas ini, bukan cuma klaim internal tim semata.

### ImpactPool (Micro-Investment Lingkungan) — Prevalensi Diprediksi **Paling Rendah**, tapi dengan Catatan Penting

Ini konsep yang paling baru muncul (baru di screenshot Saif, belum ada riset pendukung sama sekali di dokumen tim manapun sebelumnya) — jadi analisa berikut murni baru, bukan rujukan ke dokumen lama.

Kenapa diprediksi paling jarang dipilih kompetitor: menggabungkan mekanisme fintech (investasi, bagi hasil, carbon credit) dengan isu lingkungan adalah lompatan domain yang tidak biasa untuk mahasiswa/pelajar jalur desain — ini butuh pemahaman soal skema pendanaan dan literasi finansial yang tidak lazim diajarkan di kelas UI/UX biasa. Precedent riil di Indonesia memang ada, tapi terbatas dan sempit: platform seperti **Mangrove Tag** (carbon offset berbasis data untuk mangrove) atau securities crowdfunding umum yang sudah berizin OJK (contoh: eku.id, Visiku, Vestora) — tapi belum ditemukan platform yang secara eksplisit menyasar micro-investment ritel untuk proyek lingkungan lokal kecil (bank sampah, urban farming, biogas) dengan model bagi-hasil/panen seperti yang dideskripsikan ImpactPool.

**Tapi ini yang harus disampaikan jujur, bukan cuma dirayakan sebagai "paling unik":** karena menyentuh mekanisme investasi dengan pengembalian (return), ImpactPool masuk wilayah yang **secara riil diatur OJK** di Indonesia — securities crowdfunding butuh izin resmi, dan skema "bagi hasil panen/carbon credit" bisa memicu pertanyaan juri soal legalitas, siapa yang menjamin dana tidak disalahgunakan, bagaimana proyek diverifikasi, dan apa yang terjadi kalau proyek gagal. Beban pembuktian di sesi tanya jawab (60% bobot final) untuk konsep ini jauh lebih berat dibanding TukangIn atau food waste — dan berbeda dari TukangIn yang sudah punya dokumen riset kompetitor + mitigasi kepercayaan + strategi bootstrap, **ImpactPool saat ini nol riset pendukung**. Kalau tim serius mempertimbangkan ini, pekerjaan rumahnya jauh lebih banyak, bukan lebih sedikit, dibanding TukangIn.

---

## Bagian 3 — Tabel Ringkasan: Posisi Ketiga Konsep Saif + Konsep Lama Tim terhadap Prediksi Lanskap Kompetitor

| Konsep | Overlap Diprediksi dgn Kompetitor Lain | Kematangan Riset Internal Tim | Beban Pembuktian di Tanya Jawab (60% final) | Catatan Kritis |
|---|---|---|---|---|
| **Sebelum Basi** (food waste) | **Tinggi** — domain paling umum di antara ide "sustainability app" mahasiswa | Domain sudah pernah digarap jauh lebih matang lewat "Duluan" (13 layar, rationale lengkap) | Sedang, tapi ada risiko juri menyoal leaderboard RT sebagai kontradiksi terhadap riset psikologi tim sendiri | Secara desain, versi ini adalah **kemunduran** dari "Duluan", bukan kemajuan — leaderboard kompetitif adalah pola yang riset tim sendiri simpulkan lemah |
| **TukangIn** (repair economy) | **Rendah** — baik vs pasar riil (Sejasa/Kanggo/lakuKan bukan pemain di niche ini) maupun vs pola ideation kompetitor lomba | Paling matang — 2 dokumen riset kompetitor + mitigasi kepercayaan + strategi bootstrap sudah tersusun | Sedang — risiko sudah dipetakan (diferensiasi, trust, bootstrap dua sisi) dan sudah ada jawaban awal | Paling siap untuk dieksekusi ke breakdown fitur/flow lengkap |
| **ImpactPool** (micro-investment) | **Paling rendah** — tapi karena kompleksitas domain, bukan karena idenya "lebih baik" | **Nol** — baru muncul, belum ada riset pendukung sama sekali | **Tinggi** — menyentuh wilayah yang diatur OJK; juri kemungkinan menanyakan legalitas, verifikasi dana, jaminan kegagalan proyek | Paling berisiko untuk timeline lomba yang pendek (TM 5 Sept → deadline 14–16 Sept) karena butuh riset regulasi dari nol |
| **Kampung Iklim Digital** (ProKlim/RT-RW) | Sedang–Rendah, tapi modul karhutlanya berisiko duplikasi krn topik sedang hangat di Agustus 2026 | Matang (2 dokumen breakdown) — tapi sudah dibandingkan tim sendiri dan **kalah** dari TukangIn untuk format lomba spesifik ini | Tinggi — kompleksitas multi-role (warga/kader/MPA) & birokrasi ProKlim/SRN-PPI perlu waktu presentasi lebih panjang | Perlu diingat: ini bukan "dibuang", tapi sudah ada kesimpulan internal tim sendiri bahwa TukangIn lebih kuat *untuk format presentasi 10 menit + tanya jawab 15 menit ini secara spesifik* |

---

## Bagian 4 — Insight → Peluang

| Insight | Peluang | Dampak | Effort |
|---|---|---|---|
| Domain sampah/karbon/food waste diprediksi jadi 70–80% dari total submission (estimasi kasar, bukan angka pasti) | Kalau tim tetap di food waste, harus ada satu sudut yang benar-benar tidak umum ditemukan di studi kasus manapun yang sudah dicek — bukan sekadar rebranding "Duluan" jadi "Sebelum Basi" dengan leaderboard ditambahkan | Tinggi | Sedang |
| Leaderboard/poin kompetitif adalah pola default yang diprediksi dipakai banyak kompetitor tanpa justifikasi mendalam | Tim yang bisa menjelaskan secara eksplisit *kenapa tidak* memakai leaderboard kompetitif murni (seperti rationale "Duluan") akan terdengar lebih matang dibanding mayoritas kompetitor di sesi tanya jawab | Tinggi | Rendah — rationale-nya sudah ada, tinggal dipakai konsisten |
| TukangIn diprediksi punya overlap rendah baik vs pasar riil maupun vs pola ideation kompetitor lomba | TukangIn adalah kandidat dengan risiko "blend into the crowd" paling rendah di antara semua opsi yang ada, dan risetnya sudah paling siap | Tinggi | Rendah (riset sudah ada, tinggal breakdown fitur/flow) |
| Karhutla adalah topik hangat 2026 yang mungkin juga ditemukan tim lain secara independen | Kalau modul karhutla tetap dipakai (baik di Kampung Iklim Digital atau sebagai ide berdiri sendiri ala Saif), diferensiasi harus datang dari kedalaman eksekusi (mode hemat sinyal, integrasi MPA, arah angin/ISPU) — bukan dari klaim "belum ada yang mengangkat ini" | Sedang | Sedang |
| ImpactPool menyentuh wilayah yang diatur OJK (securities/urun dana) tapi belum ada riset regulasi sama sekali | Kalau tim ingin serius mempertimbangkan ImpactPool, perlu riset susulan setingkat TukangIn (verifikasi model bagi-hasil, kerangka legal minimal, mitigasi kepercayaan) sebelum masuk breakdown fitur | Sedang–Tinggi (kalau berhasil dieksekusi, diferensiasinya tinggi) | Tinggi |

---

## Bagian 5 — Rekomendasi

1. **Kalau prioritas tim adalah meminimalkan risiko "tenggelam di kerumunan kompetitor"**, TukangIn tetap pilihan paling masuk akal berdasarkan analisa ini — bukan cuma karena kesimpulan internal tim sebelumnya, tapi karena prediksi lanskap kompetitor yang lebih luas ini juga mengarah ke kesimpulan yang sama secara independen.
2. **Kalau tim tetap ingin melanjutkan arah food waste**, jangan gunakan "Sebelum Basi" versi screenshot apa adanya — kembalikan ke prinsip "Duluan" (hindari leaderboard kompetitif sebagai inti, fokus ke pencegahan sejak dapur) dan cari satu sudut yang belum muncul di riset manapun sejauh ini (misalnya fokus spesifik ke pengolahan sisa organik rumah tangga kos/apartemen kecil, bukan food waste secara umum).
3. **Kalau ImpactPool ingin tetap dipertimbangkan**, perlakukan sebagai opsi yang butuh riset susulan penuh (regulasi OJK, mekanisme verifikasi proyek, precedent seperti Mangrove Tag) sebelum disandingkan setara dengan TukangIn atau Duluan — saat ini levelnya belum sebanding.
4. **Kalau modul karhutla/ProKlim tetap dipakai** (baik lewat Kampung Iklim Digital atau ide Saif), jangan menjual keunikannya semata dari sisi topik — jual dari kedalaman eksekusi teknis (mode hemat sinyal, integrasi MPA, ISPU + arah angin), karena topiknya sendiri kemungkinan tidak seunik yang diasumsikan terhadap sesama peserta lomba.
5. **Apa pun konsep yang dipilih**, dokumentasikan secara eksplisit kenapa desain TIDAK memakai pola-pola default (leaderboard kompetitif, poin sebagai motivator utama, klaim dampak karbon tanpa metodologi) — ini kemungkinan besar jadi pembeda paling murah untuk dieksekusi karena rationale-nya sudah ada di riset psikologi tim sendiri, tinggal dipakai konsisten di proposal dan sesi tanya jawab.

---

## Bagian 6 — Pertanyaan Terbuka & Batasan

- **Ini prediksi, bukan observasi.** Tidak ada cara memverifikasi submission kompetitor sungguhan sebelum karya benar-benar dikumpulkan (14–16 September 2026) — dan bahkan setelah itu, karya kompetitor kemungkinan tidak dipublikasikan sebelum babak final. Semua yang tertulis di atas adalah forecasting berbasis pola, bukan fakta yang bisa dikutip sebagai kepastian ke juri.
- **Kerumunan konsep internal tim sendiri perlu diselesaikan dulu.** Sejauh arsip riset ini, ada minimal 6 konsep berbeda yang pernah dibahas (AI Waste Scanner, Smart Community Waste Pickup, Duluan, Kampung Iklim Digital, TukangIn, dan sekarang Sebelum Basi + ImpactPool dari Saif) — dokumen ini tidak menggantikan keputusan tim untuk memilih satu arah final, hanya memetakan risiko masing-masing terhadap lanskap kompetitor yang diprediksi.
- **Cek tambahan yang bisa memperkuat prediksi ini:** kalau ada dokumentasi publik dari edisi PNBITC sebelumnya (finalis/pemenang cabang Desain UI/UX tahun lalu), itu akan jadi sinyal jauh lebih kuat dibanding pola global — belum ditemukan di riset ini karena keterbatasan hasil pencarian, dan layak ditanyakan langsung ke panitia atau dicari lewat media sosial HMJTI PNB.

---

## Sumber

- [Perancangan UI/UX pada Aplikasi Sistem Bank Sampah Elektronik — Telkom University](https://openlibrarypublications.telkomuniversity.ac.id/index.php/engineering/article/view/28375)
- [Perancangan UI/UX Aplikasi Bank Sampah Induk Surabaya — UNM](https://ojs.unm.ac.id/tanra/article/view/46264)
- [Desain UI/UX Aplikasi Bank Sampah MOLEN — Dribbble](https://dribbble.com/shots/23809857-Desain-UI-UX-Aplikasi-Bank-Sampah-MOLEN)
- [Gredz — Aplikasi Pengelola Daur Ulang Sampah, UX Case Study — Medium](https://medium.com/studentwork/gredz-aplikasi-pengelola-daur-ulang-sampah-ux-case-study-c05c91f96d50)
- [Inspirasi Proyek Sustainability yang Bisa Kamu Coba — Universitas Multimedia Nusantara](https://www.umn.ac.id/inspirasi-proyek-sustainability-yang-bisa-kamu-coba/)
- [App: Carbon Footprint Tracker — UX/UI Case Study — Behance](https://www.behance.net/gallery/187603299/App-Carbon-Footprint-Tracker-UXUI-Case-Study)
- [Mangrove Tag — Platform Carbon Offset Mangrove Indonesia](https://mangrovetag.com/)
- [Daftar Platform Equity Crowdfunding Berizin OJK](https://ojk.go.id/id/berita-dan-kegiatan/publikasi/Pages/Daftar-Platform-Equity-Crowdfunding-yang-Telah-Mendapatkan-Izin-dari-OJK.aspx)
- [Securities Crowdfunding sebagai Alternatif Pendanaan UMKM — OJK](https://sikapiuangmu.ojk.go.id/FrontEnd/CMS/Article/30676)
- Arsip riset & brainstorming internal tim (folder proyek ini): *Kompilasi Riset Lengkap*, *Sintesis Riset — 6 Dokumen Tim*, *Riset Ideation Baru*, *Perbandingan Konsep — Kampung Iklim Digital vs TukangIn*, *Riset Kompetitor TukangIn*, *Konsep Kampung Iklim Digital — Breakdown Lengkap*, *Klarifikasi Konsep*, dokumen konsep "Duluan" ("ok dari semua hasil riset...")

---

*Catatan metodologi: dokumen ini adalah prediksi berbasis pola (pattern forecasting), bukan hasil riset primer terhadap peserta lomba sungguhan. Semua estimasi prevalensi ("tinggi", "sedang", "rendah") bersifat kualitatif dan diturunkan dari kombinasi data pasar riil, pola studi kasus publik, dan struktur insentif kompetisi — bukan angka statistik yang terverifikasi. Gunakan sebagai bahan pertimbangan strategis internal, bukan sebagai klaim yang dikutip langsung ke juri.*
