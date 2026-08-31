# Riset Ideation Ulang — Mencari Arah Konsep yang Fresh
## PNBITC#18 — Desain UI/UX — Tech for Nature by Crafting Sustainable Digital Solutions

**Konteks:** Disusun ulang berdasarkan koreksi target pengguna dari tim (berbagai latar belakang, mencakup struktur RT/RW) dan permintaan eksplisit untuk mencari arah yang lebih segar dari tiga ide sebelumnya (Duluan, AI Waste Scanner, Smart Community Pickup).

---

## 0. Realitas yang Perlu Disadari Dulu

Sebelum masuk ke ide baru, ada satu fakta pasar yang jujur harus disampaikan: **ranah "aplikasi sampah/daur ulang" di Indonesia sudah sangat padat kompetitor.** Dari riset, ada minimal 8 pemain aktif dengan model serupa — Octopus (beroperasi di 6 kota), Duitin, EMPOWER, Rekosistem, Plastic Bank Indonesia, AKSI, BankIn, plus belasan aplikasi sejenis lain yang muncul di listicle media Indonesia. Bahkan artikel independen soal pemulung digital menyimpulkan gap terbesar di sektor ini **bukan soal inovasi teknologi/UX, tapi soal kebijakan dan integrasi sistemik** (dukungan pemerintah, formalisasi status pemulung, skema pendanaan) — sesuatu yang tidak bisa diselesaikan lewat desain aplikasi saja.

Ini bukan berarti domain sampah/pemulung harus ditinggalkan sama sekali, tapi kalau tim tetap ke sana, standar "fresh"-nya jadi tinggi — harus benar-benar beda dari 8+ pemain yang sudah ada, bukan variasi kecil dari fitur yang sudah umum (jadwal pickup, poin, marketplace jual-beli sampah — itu semua sudah jadi fitur standar di pasar).

Karena itu riset kali ini saya arahkan ke domain-domain yang **masih kosong** dari kompetitor dan dari brainstorming tim sebelumnya.

---

## 1. Temuan Kunci: Program Kampung Iklim (ProKlim) — Ranah yang Belum Tersentuh Sama Sekali

Ini temuan paling penting dari riset ulang ini. **ProKlim** adalah program resmi nasional dari Kementerian Lingkungan Hidup yang secara eksplisit beroperasi di level **RT/RW/kampung** — persis target pengguna yang baru saja tim tetapkan.

### Cara Kerja ProKlim (fakta, bukan asumsi)

Ada sistem jenjang resmi: **ProKlim Pratama** (komunitas pemula) → **ProKlim Madya** (sudah menjalankan aksi adaptasi-mitigasi) → **ProKlim Utama** (punya sistem kelembagaan & keberlanjutan) → **Trofi ProKlim Nasional** (praktik terbaik untuk direplikasi).

Aksi yang dinilai terbagi dua kategori:

- **Adaptasi:** pengelolaan air (sumur resapan, panen hujan), ketahanan pangan (pertanian organik, vertical garden), pencegahan penyakit terkait iklim, pengurangan risiko bencana.
- **Mitigasi:** pengelolaan sampah terpadu & komposting, energi terbarukan/efisiensi energi, penghijauan & konservasi lahan.

RT/RW dan kelompok masyarakat berperan sebagai **pelaksana utama** — mereka yang mengusulkan wilayah, menjalankan kegiatan, dan membangun keberlanjutan program, dengan fasilitasi pemerintah.

### Kenapa ini fresh

Tidak ada satu pun dokumen riset atau ide brainstorming tim sebelumnya yang menyentuh ProKlim. Program ini sudah berjalan secara resmi dan berkembang (KLHK melaporkan partisipasi kampung meningkat 128% di tahun 2023), tapi dari yang saya temukan, prosesnya masih sangat bergantung pada dokumentasi manual/laporan fisik untuk pengajuan dan penilaian jenjang. **Ini gap digital yang nyata dan belum digarap kompetitor manapun** yang saya temukan di riset sampah/eco-app manapun sejauh ini.

---

## 2. Lima Arah Konsep

### Arah A — "Kampung Iklim Digital": Companion App untuk RT/RW Menuju Sertifikasi ProKlim

**Masalah:** RT/RW yang ingin ikut ProKlim kesulitan mendokumentasikan aksi mereka secara terstruktur sesuai kriteria resmi, warga tidak tahu aktivitas mana yang "terhitung", proses naik jenjang (Pratama→Madya→Utama) tidak transparan, dan koordinasi antar warga untuk kegiatan kolektif (kerja bakti, panen hujan bersama, dst.) masih manual lewat grup WhatsApp yang mudah tenggelam.

**Fitur inti:** checklist aksi resmi ProKlim per kategori (air, pangan, sampah, energi, penghijauan, bencana) yang bisa dicentang dengan bukti foto; tracker progres jenjang sertifikasi; kalender & koordinasi kegiatan kolektif RT; dashboard kelurahan/kecamatan untuk melihat kampung mana yang aktif; profil kampung yang menampilkan pencapaian (bisa jadi kebanggaan komunitas — relevan dengan riset *identity & ownership* dari analisa psikologi sebelumnya).

**Kesesuaian target:** sangat pas — ini secara harfiah aplikasi untuk RT/RW, bukan individu.

**Catatan jujur:** perlu diverifikasi apakah pendaftaran ProKlim memang masih manual (asumsi berdasarkan tidak ditemukannya platform digital resmi saat riset — bukan konfirmasi definitif). Juga admin RT/RW belum tentu melek teknologi — desain onboarding harus sangat sederhana.

---

### Arah B — Kesiapsiagaan Bencana Berbasis Komunitas (Early Warning & Respons RT/RW)

**Masalah:** Indonesia rawan banjir, longsor, dan kekeringan, dan riset akademik menunjukkan sistem peringatan dini yang efektif justru butuh integrasi antara sensor sederhana, aplikasi mobile, dan **mekanisme respons komunitas** — bukan cuma notifikasi dari BMKG/BNPB yang sifatnya satu arah. Studi kasus di desa NTT dan riset "desa berliterasi teknologi rendah" menunjukkan pendekatan berbasis komunitas lebih efektif dibanding sistem top-down murni.

**Fitur inti:** pelaporan kondisi warga secara real-time (ketinggian air, kondisi jalan) yang teragregasi jadi peta risiko RT; sistem rantai peringatan berjenjang (RT → warga) dengan peran jelas siapa yang harus bertindak apa; titik kumpul & jalur evakuasi yang bisa diperbarui warga; mode kesiapsiagaan pra-musim (checklist persiapan sebelum musim hujan/kemarau) — ini juga masuk kategori "adaptasi" resmi ProKlim.

**Kesesuaian target:** kuat untuk RT/RW, terutama daerah rawan bencana.

**Catatan jujur:** ini domain sensitif (nyawa manusia) — kalau dipilih, jangan overclaim kemampuan aplikasi ("sistem peringatan dini akurat") tanpa dasar teknis nyata; framing sebagai *alat koordinasi komunitas*, bukan pengganti sistem resmi BMKG/BNPB, akan lebih realistis dan lebih mudah dipertahankan di sesi tanya jawab.

---

### Arah C — Ketahanan Pangan Komunal: Koordinasi Kebun/Pertanian Bersama RT/RW

**Beda dari "Duluan":** kalau "Duluan" fokus mencegah food waste di level individu/rumah tangga, arah ini fokus ke **produksi pangan bersama** di level komunitas — vertical garden RW, kebun kolektif, atau lahan kosong yang dikelola bareng. Ini juga masuk kategori resmi "ketahanan pangan" di ProKlim.

**Fitur inti:** koordinasi jadwal piket kebun komunal, pencatatan hasil panen & pembagian ke warga, marketplace kecil hasil kebun antarwarga, panduan menanam sederhana untuk lahan sempit perkotaan, integrasi dengan komposting dari sampah organik warga (menyambungkan ke domain "Duluan" kalau tim mau menggabungkan dua arah).

**Kesesuaian target:** kuat untuk RT/RW, terutama sangat relevan untuk konteks perkotaan padat yang lahan terbatas.

**Catatan jujur:** butuh riset lanjutan seberapa banyak RT/RW di kota besar yang benar-benar sudah punya lahan kebun komunal — kalau jarang, konsep berisiko terasa idealis dan tidak grounded.

---

### Arah D — Konservasi Air Tingkat Kampung (Sumur Resapan & Panen Hujan)

**Masalah:** krisis air bersih dan banjir sering terjadi berdampingan di kota-kota Indonesia — daerah yang kebanjiran saat hujan justru sering kekurangan air bersih saat kemarau, karena air hujan tidak diserap/ditampung dengan baik. Ini juga kategori resmi "adaptasi" ProKlim (sumur resapan, panen hujan).

**Fitur inti:** peta titik sumur resapan/tandon air komunal RT, panduan teknis sederhana membuat sumur resapan skala rumah, pelacakan kontribusi kolektif RT terhadap target konservasi air, edukasi kontekstual (nudge saat musim kemarau mendekat).

**Kesesuaian target:** kuat untuk RT/RW.

**Catatan jujur:** domain paling teknis/infrastruktur di antara lima arah ini — perlu hati-hati supaya tetap terasa sebagai aplikasi (bukan justru terasa seperti brosur infrastruktur).

---

### Arah E — Pemulung, Direvisi: Dari "Logistik Sampah" ke "Identitas & Perlindungan Sosial"

Kalau tim masih tertarik ke isu pemulung, saya sarankan **pivot sudut pandangnya**, bukan menambah pemain ke-9 di pasar logistik sampah yang sudah padat. Riset menunjukkan gap sebenarnya bukan soal jadwal pickup (itu sudah solved oleh 8+ kompetitor), tapi soal **pemulung tidak punya rekam jejak/identitas formal** yang bisa membuka akses ke perlindungan sosial (BPJS, pengakuan pemerintah daerah), dan pekerjaan mereka masih sering tidak diakui secara layak.

**Fitur inti (kalau dipilih):** profil digital terverifikasi berbasis riwayat transaksi nyata (bukan sekadar rating), badge kepercayaan yang terakumulasi dari waktu ke waktu, panduan/tautan ke program perlindungan sosial yang bisa diakses, laporan agregat (anonim) yang bisa dipakai advokasi ke pemerintah daerah soal kontribusi ekonomi pemulung.

**Kesesuaian target:** sedang — ini lebih ke arah individu pemulung + masyarakat luas sebagai mitra, bukan RT/RW sebagai institusi.

**Catatan jujur — paling penting:** riset independen bilang gap terbesar di ranah ini **bukan UX, tapi kebijakan**. Sebuah aplikasi UI/UX kompetisi tidak bisa "menyelesaikan" masalah formalisasi status pemulung — paling realistis, aplikasi hanya bisa jadi *satu titik masuk* menuju penyelesaian yang lebih besar. Kalau dipilih, penting untuk jujur soal batasan ini di proposal, bukan overclaim.

---

## 3. Perbandingan Kelima Arah

| Arah | Freshness (vs kompetitor+ide lama) | Dampak Lingkungan+Sosial | Kesesuaian Target RT/RW | Kelayakan Prototype Figma | Risiko Utama |
|---|---|---|---|---|---|
| A — Kampung Iklim Digital | Sangat tinggi (belum ada yang menggarap) | Tinggi (mencakup 6 kategori resmi sekaligus) | Sangat tinggi | Tinggi | Perlu verifikasi asumsi digitalisasi ProKlim saat ini |
| B — Kesiapsiagaan Bencana | Tinggi | Tinggi (langsung menyangkut keselamatan) | Tinggi | Sedang | Domain sensitif, jangan overclaim akurasi |
| C — Ketahanan Pangan Komunal | Tinggi | Sedang–Tinggi | Tinggi | Tinggi | Perlu validasi keberadaan lahan komunal |
| D — Konservasi Air Kampung | Sedang–Tinggi | Sedang | Sedang–Tinggi | Sedang | Risiko terasa terlalu teknis/infrastruktur |
| E — Pemulung (revisi) | Sedang (masih berdekatan dgn pasar padat) | Sedang (sosial kuat, lingkungan tidak langsung) | Sedang | Tinggi | Gap sebenarnya adalah kebijakan, bukan UX — perlu jujur soal batasan |

---

## 4. Insight Tambahan: Arah A Bisa Jadi "Payung" untuk Arah Lain

Karena ProKlim secara resmi mencakup kategori air, pangan, sampah, energi, penghijauan, dan bencana sekaligus, **Arah B, C, dan D sebenarnya bisa didesain sebagai modul di dalam Arah A**, bukan harus jadi aplikasi terpisah. Ini memberi tim fleksibilitas: mulai dari kerangka besar "Kampung Iklim Digital", lalu pilih 1-2 modul untuk didalami sebagai fitur unggulan di prototype (karena waktu terbatas, tidak mungkin membangun keenam kategori sekaligus secara mendalam untuk lomba).

---

## 5. Rekomendasi Langkah Selanjutnya

1. **Verifikasi paling penting:** cari tahu apakah ProKlim benar-benar masih manual/paper-based di level pendaftaran dan pelaporan RT/RW (bisa lewat pencarian lebih lanjut, atau tanya langsung ke pengurus RT/kelurahan setempat kalau memungkinkan). Ini asumsi kunci yang menentukan apakah Arah A valid.
2. Diskusikan internal tim: dari lima arah ini, mana yang paling terasa "menarik" secara personal buat tim — ingat pertanyaan saya soal kedekatan personal tadi, ini saat yang tepat untuk mempertimbangkannya.
3. Setelah pilih 1 arah dasar (kemungkinan besar A, dengan 1-2 modul dari B/C/D sebagai fitur unggulan), saya bisa bantu susun user flow, daftar layar, dan design rationale seperti yang sudah dibuat untuk "Duluan" — supaya levelnya setara dan siap dipakai untuk proposal.
4. Kalau tim tetap penasaran ke arah pemulung (Arah E), saya sarankan itu jadi opsi cadangan, bukan opsi utama — kecuali ada anggota tim dengan kedekatan personal yang kuat ke isu tersebut.

---

## 6. Sumber

- [Program Kampung Iklim (ProKlim) — Kementerian Lingkungan Hidup](https://kemenlh.go.id/contents/16/Program-Kampung-Iklim-Proklim)
- [Program Kampung Iklim meningkat 128% di tahun 2023 — DJPPI KLHK](https://www.ditjenppi.org/indonesia/berita2/program-kampung-iklim-meningkat-128-di-tahun-2023)
- [Roadmap Program Kampung Iklim — Kecamatan Sindangkasih](https://kecamatan-sindangkasih.ciamiskab.go.id/wp-content/uploads/2023/12/Roadmap-Program-Kampung-Iklim-Proklim.pdf)
- [12 innovators improving the lives of Indonesia's informal sector workers — World Economic Forum](https://www.weforum.org/stories/2021/06/innovators-indonesia-waste-informal-sector/)
- [The apps helping Indonesia's waste collectors — Dialogue Earth](https://dialogue.earth/en/pollution/the-apps-helping-indonesias-waste-collectors/)
- [Formalizing 'pemulung' toward humane waste system — The Jakarta Post](https://www.thejakartapost.com/paper/2021/06/16/formalizing-pemulung-toward-humane-waste-system)
- [Integrasi Sensor Low-Cost, Aplikasi Mobile, dan Mekanisme Respons Komunitas — Jurnal Pengabdian Masyarakat](https://ejournal.lib-institute.com/dharmabakti/article/view/74)
- [Sistem Peringatan Dini Berbasis Masyarakat di NTT — ResearchGate](https://www.researchgate.net/publication/388120224_Sistem_Peringatan_Dini_berbasis_Masyarakat_di_Daerah_Rawan_Bencana_Studi_di_Tiga_Desa_di_Provinsi_Nusa_Tenggara_Timur_Indonesia)
- [10+ Climate Tech Startup Ideas to Launch in 2026 — Appinventiv](https://appinventiv.com/blog/climate-tech-startup-ideas/)
- [Octopus Indonesia — Global Solutions Initiative](https://www.global-solutions-initiative.org/article/octopus-indonesia/)
- [14 Aplikasi Daur Ulang Sampah — Hipwee](https://www.hipwee.com/feature/aplikasi-daur-ulang-sampah/)
