# Kampung Iklim Digital — Breakdown & Analisa Konsep Lengkap
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Status:** Konsep siap didiskusikan tim
**Disusun:** 24 Agustus 2026

---

## 1. Ringkasan Eksekutif

**Kampung Iklim Digital** adalah aplikasi mobile pendamping untuk RT/RW yang mengubah partisipasi dalam Program Kampung Iklim (ProKlim) — program resmi nasional dari Kementerian Lingkungan Hidup — dari sesuatu yang terasa administratif dan tidak terasa dampaknya, menjadi pengalaman komunitas yang konkret, terlihat progresnya, dan mudah diikuti warga sehari-hari. Berdasarkan verifikasi lapangan (Bagian 2), gap sebenarnya bukan "belum ada sistem digital sama sekali", tapi sistem digital resmi yang ada (SRN-PPI) bersifat sistem pelaporan institusional yang rumit — bukan alat yang dipakai warga RT/RW untuk terlibat sehari-hari. Konsep ini juga menjawab permintaan tambahan untuk memasukkan isu kebakaran hutan dan lahan (karhutla) yang sedang parah terjadi di 2026, lewat modul kesiapsiagaan yang terhubung ke kelompok resmi **Masyarakat Peduli Api (MPA)**.

---

## 2. Verifikasi Lapangan — Koreksi Terhadap Asumsi Sebelumnya

Di dokumen riset sebelumnya, saya menandai sebagai asumsi bahwa proses ProKlim "kemungkinan masih manual/paper-based". Setelah verifikasi, **asumsi ini perlu dikoreksi** — dan koreksi ini justru memperkuat, bukan melemahkan, konsep ini.

### 2.1 Apa yang sebenarnya sudah ada

Pemerintah punya sistem bernama **SRN-PPI (Sistem Registri Nasional Pengendalian Perubahan Iklim)**, diakses lewat `srn.menlhk.go.id`, tempat skema ProKlim didaftarkan secara digital. Tapi dari dokumentasi panduan pengisiannya, sistem ini:

- Ditujukan untuk **"Pemrakarsa"** (pengusul/penyelenggara — kemungkinan besar kader RT/RW, DLH, atau pendamping teknis), bukan warga biasa secara langsung.
- Prosesnya berlapis: input data umum & lokasi → unggah dokumen pendukung (Word/Excel/PDF) → direview Sekretariat → status "Perlu Perbaikan" atau "Disetujui" → input data teknis lewat form Excel dan aplikasi Android terpisah bernama **SPECTRUM Mitigasi**.
- Ini jelas dirancang sebagai **sistem pelaporan/registrasi resmi**, bukan alat keterlibatan warga sehari-hari. Butuh keahlian administratif untuk mengisinya (dokumen teknis, form Excel).

### 2.2 Kendala nyata di lapangan (dari kajian akademik)

Tinjauan implementasi ProKlim di Indonesia (jurnal akademik, lihat sumber) menemukan kendala berulang: **partisipasi masyarakat rendah** karena "persepsi bahwa manfaat adaptasi dan mitigasi perubahan iklim tidak dapat dirasakan secara langsung", ditambah warga lebih memprioritaskan pekerjaan/ekonomi; **kelembagaan lemah** karena pembinaan kader pelaksana belum optimal; **minim sosialisasi dan dukungan teknis-finansial**; serta **keterbatasan sarana-prasarana**.

**Ini penting:** kendala "manfaat tidak dirasakan langsung" ini **persis** dengan Dragon "Limited Cognition" yang sudah dibahas di riset psikologi tim sebelumnya (dampak abstrak dan jauh). Artinya bukan cuma teori psikologi yang bilang begitu — kajian lapangan soal ProKlim secara spesifik mengonfirmasi masalah yang sama persis. Ini bukti silang yang kuat untuk proposal.

### 2.3 Gap yang sebenarnya disasar (revisi dari dokumen sebelumnya)

Bukan "menciptakan sistem digital yang belum ada", tapi: **menjembatani antara sistem pelaporan resmi pemerintah (SRN-PPI, institusional & rumit) dengan pengalaman warga sehari-hari (kasual, terlihat progresnya, terasa manfaatnya)** — dan menjadikan warga bagian aktif dari proses, bukan cuma objek yang datanya diinput orang lain.

---

## 3. Latar Belakang: Kenapa Ini Masalah yang Layak Diselesaikan

### 3.1 Skala program

KLHK melaporkan partisipasi kampung dalam ProKlim meningkat 128% di tahun 2023 — programnya tumbuh, tapi kajian akademik menunjukkan kualitas partisipasi warga di lapangan masih jadi masalah struktural, bukan cuma soal jumlah kampung yang terdaftar.

### 3.2 Konteks krisis yang sedang terjadi (karhutla 2026)

Ini bagian yang menjawab pertanyaan kalian soal kebakaran hutan. Datanya nyata dan sedang berlangsung saat dokumen ini ditulis:

- Per akhir Juli 2026, sekitar **202.011 hektare** lahan dan hutan Indonesia sudah terbakar, dengan **454 kejadian kebakaran** tercatat BNPB — lonjakan tajam terjadi di Juli sendiri (94.545 ha).
- **54% kejadian di kawasan hutan, 46% di luar kawasan hutan** — artinya bukan cuma soal hutan lindung jauh dari pemukiman, tapi juga menyentuh lahan yang berdekatan dengan wilayah masyarakat.
- Kalimantan dan Papua jadi titik konsentrasi hotspot tertinggi pertengahan Agustus 2026; asap dari Kalimantan sudah mencapai Malaysia.
- Penyebab dominan: kondisi El Niño yang diproyeksikan bertahan sampai awal 2027.
- Dampak sosial nyata: krisis 2015 (skala serupa) menyebabkan sekitar 504.000 kasus kesehatan dan kerugian ekonomi sekitar Rp220 triliun — pola dampak yang sama berpotensi terulang.

### 3.3 Kaitan karhutla dengan struktur komunitas yang sudah ada

Pemerintah (lewat KLHK) sudah membentuk kelompok resmi bernama **Masyarakat Peduli Api (MPA)** di banyak desa/wilayah rawan kebakaran — semacam "satgas kebakaran" tingkat komunitas yang dilatih untuk deteksi dini dan respons awal. Ini kelompok yang nyata dan sudah eksis, bukan konsep karangan.

**Catatan jujur:** saya tidak menemukan bukti definitif bahwa "pengendalian karhutla" tercantum sebagai kategori resmi terpisah dalam kriteria ProKlim (halaman resmi hanya menyebut kategori umum: air, pangan, kesehatan, pengurangan risiko bencana untuk adaptasi; sampah, energi, penghijauan untuk mitigasi). Tapi karhutla secara logis masuk kategori **"pengurangan risiko bencana"** dalam adaptasi ProKlim, dan MPA sendiri adalah program resmi terpisah dari KLHK yang bisa diintegrasikan sebagai modul tanpa perlu bergantung pada apakah ProKlim secara eksplisit menyebutnya.

---

## 4. Konsep Solusi

### 4.1 Filosofi Inti

Bukan aplikasi pelaporan birokrasi, tapi **aplikasi kebanggaan komunitas** — warga RT/RW melihat kampung mereka "tumbuh" (secara visual dan status) seiring aksi iklim yang mereka lakukan bersama, sambil di baliknya data yang terkumpul bisa membantu kader RT/RW menyusun laporan untuk SRN-PPI dengan jauh lebih mudah dibanding proses manual sekarang.

### 4.2 Dua Sisi Pengguna (Multi-Role)

| Peran | Siapa | Kebutuhan Utama |
|---|---|---|
| Warga | Siapa saja anggota RT/RW, berbagai latar belakang | Ikut aksi mudah, lihat progres kampung, dapat notifikasi relevan |
| Kader/Admin RT-RW | Pengurus RT/RW yang jadi penanggung jawab | Kelola data aksi, susun laporan, koordinasi kegiatan |
| Anggota MPA | Warga yang terdaftar di kelompok Masyarakat Peduli Api | Modul khusus kesiapsiagaan & pelaporan titik api |

### 4.3 Modul Aplikasi

**Modul 1 — Checklist Aksi Iklim.** Enam kategori resmi ProKlim (air, pangan, kesehatan, bencana, sampah, energi, penghijauan) ditampilkan sebagai checklist visual dengan bukti foto — bukan formulir teknis, tapi kartu-kartu sederhana yang bisa dicentang warga/kader.

**Modul 2 — Progres & Status Kampung.** Visualisasi progres RT/RW menuju jenjang ProKlim berikutnya (Pratama→Madya→Utama), dengan metafora pertumbuhan (mengacu pola visual ownership yang terbukti efektif dari riset habit-forming sebelumnya) — supaya warga merasa memiliki, bukan cuma menonton.

**Modul 3 — Kesiapsiagaan Karhutla (untuk anggota MPA & warga di wilayah rawan).** Pelaporan cepat titik api/asap oleh warga (foto + lokasi), status kesiapsiagaan musim kemarau, checklist edukasi cara buka lahan tanpa bakar, kontak & koordinasi cepat ke anggota MPA terdekat saat kondisi darurat.

**Modul 4 — Koordinasi Kegiatan Komunitas.** Kalender kegiatan kolektif (kerja bakti, panen hujan bersama, dsb), pengingat kontekstual, bukan sekadar broadcast grup WhatsApp yang gampang tenggelam.

**Modul 5 — Ekspor Laporan (nilai tambah ke kader RT/RW).** Data yang terkumpul dari checklist Modul 1 dirangkum otomatis jadi draf laporan yang memudahkan kader saat harus mengisi SRN-PPI — ini fitur *pembeda* karena secara langsung mengurangi beban administratif nyata yang jadi salah satu kendala di kajian akademik.

> **Catatan penting:** Modul 5 ini adalah *usulan desain saya*, bukan fakta bahwa integrasi semacam ini sudah ada atau pasti akan diterima pemerintah — di prototype, ini cukup digambarkan sebagai fitur "ekspor ringkasan siap pakai", tanpa mengklaim aplikasi ini terintegrasi resmi dengan sistem SRN-PPI pemerintah kecuali itu benar-benar diverifikasi lebih lanjut.

---

## 5. User Flow Utama

### 5.1 Alur warga biasa mengikuti aksi

```text
Onboarding (pilih RT/RW, lihat status kampung saat ini)
→ Beranda (progres kampung + aksi yang sedang berjalan)
→ Pilih kategori aksi (air/pangan/sampah/energi/dst.)
→ Ikuti aksi + unggah bukti (foto)
→ Lihat kontribusi personal terhadap progres kampung
→ Notifikasi saat kampung naik status/jenjang
```

### 5.2 Alur pelaporan karhutla (modul MPA)

```text
Warga melihat/mencium tanda titik api atau asap
→ Buka Modul Kesiapsiagaan Karhutla
→ Foto + tandai lokasi
→ Sistem meneruskan ke anggota MPA terdekat + kader RT
→ Status: dilaporkan → diverifikasi → ditindaklanjuti
→ Update status terlihat oleh pelapor
```

### 5.3 Alur kader RT/RW mengelola data

```text
Login sebagai kader
→ Dashboard aksi RT (semua checklist warga + status verifikasi)
→ Verifikasi bukti aksi warga
→ Lihat ringkasan progres menuju jenjang berikutnya
→ Ekspor ringkasan laporan (Modul 5)
→ Kelola/publikasi kegiatan komunitas mendatang
```

---

## 6. Daftar Layar Figma yang Disarankan

| No. | Layar | Modul |
|---|---|---|
| 1 | Splash & pemilihan RT/RW | Onboarding |
| 2 | Onboarding peran (warga/kader/anggota MPA) | Onboarding |
| 3 | Beranda warga (status kampung + aksi berjalan) | Modul 1–2 |
| 4 | Daftar kategori aksi iklim | Modul 1 |
| 5 | Detail aksi + unggah bukti | Modul 1 |
| 6 | Progres jenjang kampung (visual growth) | Modul 2 |
| 7 | Modul Kesiapsiagaan Karhutla — beranda | Modul 3 |
| 8 | Form pelaporan titik api/asap | Modul 3 |
| 9 | Status tindak lanjut laporan | Modul 3 |
| 10 | Kalender kegiatan komunitas | Modul 4 |
| 11 | Dashboard kader RT/RW | Modul 5 |
| 12 | Verifikasi bukti aksi (tampilan kader) | Modul 5 |
| 13 | Ekspor ringkasan laporan | Modul 5 |
| 14 | Profil & pengaturan (termasuk aksesibilitas) | Umum |

---

## 7. Design Rationale (Untuk Sesi Tanya Jawab)

| Keputusan Desain | Alasan | Berbasis Riset |
|---|---|---|
| Checklist visual, bukan formulir teknis | Warga bukan admin — beban input harus minimal | Prinsip habit-forming: low-friction |
| Visualisasi progres kampung (metafora tumbuh) | Bangun identitas & rasa memiliki kolektif | Visual ownership + environmental identity |
| Kontribusi personal terlihat dalam progres kolektif | Jawab langsung kendala "manfaat tidak dirasakan langsung" dari kajian ProKlim | Dragon Limited Cognition — impact konkret & lokal |
| Modul karhutla terhubung ke MPA yang sudah ada | Tidak menciptakan struktur baru dari nol, memperkuat yang sudah eksis | Prinsip integrasi dengan infrastruktur lokal (konsisten dgn riset sampah sebelumnya) |
| Fitur ekspor laporan untuk kader | Jawab kendala administratif nyata di lapangan, bukan cuma engagement warga | Kajian akademik ProKlim: kelembagaan lemah |
| Multi-role (warga/kader/MPA) bukan satu peran generik | Realita di lapangan memang ada pembagian peran berbeda | Verifikasi lapangan Bagian 2 |

---

## 8. Kesesuaian dengan Ketentuan & Rubrik Lomba

- **Kesesuaian tema (15%):** langsung menjawab "Tech for Nature" lewat program iklim resmi pemerintah, bukan interpretasi bebas.
- **UX & Accessibility (30%):** multi-role dengan kompleksitas berbeda per peran perlu didesain hati-hati supaya kader (kemungkinan usia lebih beragam, tidak semua melek teknologi) tetap mudah dipakai — checklist visual dan bahasa sederhana jadi kunci.
- **Kreativitas & Inovasi (25%):** kombinasi checklist iklim + kesiapsiagaan bencana + jembatan ke pelaporan resmi pemerintah adalah kombinasi yang belum ditemukan di aplikasi/ide manapun sejauh riset ini.
- **Tanya jawab final (60% dari nilai final):** karena konsep ini berpijak dari program pemerintah resmi (bisa diverifikasi juri), plus data karhutla 2026 yang aktual, tim punya banyak fakta konkret untuk mempertahankan argumen — bukan klaim yang mengambang.

---

## 9. Risiko & Mitigasi

| Risiko | Mitigasi |
|---|---|
| Klaim "terintegrasi dengan SRN-PPI" bisa dianggap berlebihan kalau tidak diverifikasi | Framing sebagai "ekspor ringkasan siap pakai", bukan integrasi resmi, kecuali diverifikasi lebih lanjut |
| Kompleksitas multi-role bisa membuat scope prototype terlalu besar untuk waktu lomba yang terbatas | Fokuskan prototype ke 1-2 role utama (warga + kader) dengan modul karhutla sebagai fitur unggulan pembeda, bukan mendalami semua modul sama dalam |
| Kader RT/RW riil belum tentu punya waktu/kemauan pakai aplikasi baru | Perlu narasi jelas di presentasi soal bagaimana aplikasi mengurangi beban mereka (Modul 5), bukan menambah pekerjaan baru |
| Data karhutla di modul 3 berisiko disalahartikan sebagai sistem peringatan dini resmi yang mengklaim akurasi tinggi | Framing sebagai alat koordinasi & pelaporan warga-ke-MPA, bukan pengganti sistem resmi BNPB/BMKG |

---

## 10. Pertanyaan yang Masih Perlu Diverifikasi

- Apakah kriteria resmi ProKlim benar-benar memasukkan pengurangan risiko karhutla di bawah kategori "pengurangan risiko bencana", atau ini murni penambahan desain di luar kriteria resmi (perlu dicek ke sumber KLHK lebih detail atau ditanyakan saat Technical Meeting).
- Siapa sebenarnya yang berperan sebagai "Pemrakarsa" di SRN-PPI di lapangan — kader RT/RW langsung, atau selalu lewat DLH kabupaten/kota? Ini memengaruhi seberapa realistis Modul 5 (ekspor laporan) sebagai fitur.
- Apakah tim (atau kenalan tim) punya akses ke RT/RW yang sudah/sedang ikut ProKlim untuk validasi cepat konsep — akan sangat memperkuat proposal kalau ada.

---

## 11. Sumber

- [Program Kampung Iklim (ProKlim) — Kementerian Lingkungan Hidup](https://kemenlh.go.id/contents/16/Program-Kampung-Iklim-Proklim)
- [Sistem Registri Nasional Pengendalian Perubahan Iklim (SRN-PPI) Skema ProKlim](https://dml.or.id/sistem-registri-nasional-pengendalian-perubahan-iklim-srn-ppi-skema-proklim/)
- [Panduan & FAQ SRN — srn.menlhk.go.id](https://srn.menlhk.go.id/index.php?r=home/bantuan)
- [Tinjauan Implementasi Program Kampung Iklim di Indonesia — Jurnal JPAMS](https://journal.umnyarsi.ac.id/index.php/JPAMS/article/download/267/49/840)
- [Program Kampung Iklim meningkat 128% di tahun 2023 — DJPPI KLHK](https://www.ditjenppi.org/indonesia/berita2/program-kampung-iklim-meningkat-128-di-tahun-2023)
- [200.000 Lahan & Hutan RI Terbakar Tahun Ini, Terburuk Sejak Kapan? — CNBC Indonesia](https://www.cnbcindonesia.com/research/20260824093442-128-761828/200000-lahan-hutan-ri-terbakar-tahun-ini-terburuk-sejak-kapan)
- [Ketika Kebakaran Hutan dan Lahan Menggila di Kalimantan — Mongabay Indonesia](https://mongabay.co.id/2026/08/06/ketika-kebakaran-hutan-dan-lahan-menggila-di-kalimantan/)
- [Waspada Karhutla 2026 — Kementerian Lingkungan Hidup](https://kemenlh.go.id/news/detail/waspada-karhutla-2026-menteri-lh-tegaskan-sinergi-pusat-dan-daerah-hadapi-lonjakan-titik-panas)
- [Perkembangan Situasi dan Penanganan Bencana — BNPB, 20 Juli 2026](https://www.bnpb.go.id/berita/perkembangan-situasi-dan-penanganan-bencana-di-tanah-air-20-juli-2026)
- [Masyarakat Peduli Api (MPA) sebagai Garda Terdepan Cegah Karhutla — Sampan Kalimantan](https://sampankalimantan.id/masyarakat-peduli-api-mpa-sebagai-garda-terdepan-cegah-karhutla/)
- [Pembentukan Kelompok Masyarakat Peduli Api — Ditjen PPI KLHK](https://ditjenppi.menlhk.go.id/berita-ppi/3751-pembentukan-kelompok-masyarakat-peduli-api-mpa-di-kecamatan-pulau-moa-kabupaten-maluku-barat-daya-provinsi-maluku.html)
- [Pengembangan Aplikasi Mobile Sistem Peringatan Dini Kebakaran Hutan dan Lahan — Repository IPB](https://repository.ipb.ac.id/handle/123456789/174049)

---

*Dokumen ini siap didiskusikan tim. Kalau sudah ada keputusan awal, saya bisa lanjutkan ke tahap wireframe/struktur komponen Figma.*
