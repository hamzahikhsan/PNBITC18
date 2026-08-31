# UI/UX Competition — Environmental Solution Ideas

## Tema

**Aplikasi yang dapat membantu menyelesaikan permasalahan lingkungan dengan dukungan teknologi AI.**

---

# IDEA 1 — AI Waste Scanner & Recycling Assistant

## Konsep

Aplikasi yang membantu pengguna mengenali dan menentukan tindakan yang tepat terhadap suatu barang atau sampah hanya dengan menggunakan kamera.

Pengguna cukup **memotret barang**, kemudian AI akan menganalisis barang tersebut dan memberikan rekomendasi tindakan.

## User Flow

1. User memotret barang/sampah.
2. AI mengenali jenis dan material barang.
3. Sistem memberikan hasil analisis:
   - ♻️ Bisa didaur ulang
   - ⚠️ Berbahaya
   - 🗑️ Tidak dapat didaur ulang
   - 💰 Masih memiliki nilai jual
4. Sistem memberikan rekomendasi tindakan.
5. Jika barang dapat didaur ulang, sistem memberikan panduan cara memilah/mendaur ulang.
6. Jika barang berbahaya, sistem memberikan instruksi pembuangan yang aman.
7. Jika barang masih memiliki nilai, user dapat memilih **Sell This Item**.
8. User mengunggah foto, kondisi barang, spesifikasi, dan deskripsi.
9. AI memberikan rekomendasi harga berdasarkan kondisi dan data harga pasar.
10. User dapat melanjutkan proses penjualan.

## Fitur AI

### 1. AI Image Recognition
Mengenali objek dan material dari foto.

### 2. Waste Classification
Menentukan kategori sampah dan bagaimana barang tersebut seharusnya diproses.

### 3. Smart Disposal Recommendation
Memberikan rekomendasi tindakan berdasarkan jenis barang.

### 4. AI Price Recommendation
Memberikan estimasi harga jual berdasarkan kondisi, jenis barang, spesifikasi, dan data harga pasar.

## Masalah yang Diselesaikan

Banyak orang ingin membuang atau mendaur ulang barang dengan benar tetapi tidak mengetahui:
- barang tersebut termasuk kategori apa,
- apakah barang dapat didaur ulang,
- bagaimana cara membuangnya,
- apakah barang masih memiliki nilai jual.

## Dampak Lingkungan

Membantu mengurangi sampah yang berakhir di landfill dengan mengarahkan barang ke proses yang tepat:

**Reuse → Resell → Recycle → Safe Disposal**

---

# IDEA 2 — Smart Community Waste Pickup

## Konsep

Platform pengambilan sampah rutin untuk perumahan atau cluster yang menghubungkan **warga, pengelola lingkungan, dan waste collector/pemulung**.

Tujuannya adalah membuat proses pengambilan sampah menjadi lebih terjadwal, efisien, dan terorganisir.

## User Flow

### 1. Register Community

Perwakilan warga atau pengurus cluster mendaftarkan lingkungan mereka.

Data yang diperlukan:
- nama cluster,
- jumlah rumah,
- jumlah warga,
- lokasi,
- jenis sampah,
- frekuensi pengambilan.

### 2. Choose Subscription

Sistem menentukan paket berdasarkan:

**Jumlah warga + volume sampah + frekuensi pickup**

Contoh:
- Weekly Pickup
- 2× Weekly Pickup
- Daily Pickup

### 3. AI Waste Prediction

AI mempelajari histori pengambilan untuk memprediksi:
- estimasi volume sampah,
- waktu pickup yang optimal,
- kebutuhan pickup berikutnya.

### 4. Smart Scheduling

Sistem otomatis membuat jadwal pengambilan.

Contoh:

**Every Tuesday & Friday — 08:00–10:00**

### 5. Find Collector

Order diberikan kepada collector yang sesuai berdasarkan:
- lokasi,
- kapasitas,
- jenis sampah,
- jadwal,
- histori performa.

### 6. Pickup

Collector menerima order dan mengambil sampah sesuai jadwal.

**Order → Accepted → On The Way → Picked Up → Completed**

### 7. Waste Processing

Setelah pickup, sampah dapat diarahkan ke:

**Reuse / Recycle / Sell / Proper Disposal**

## Fitur AI

### AI Volume Prediction
Memprediksi jumlah sampah berdasarkan histori.

### AI Pickup Optimization
Menentukan frekuensi pickup yang paling optimal.

### AI Route Optimization
Membantu collector menentukan rute pengambilan yang efisien.

### Smart Recommendation
Memberikan rekomendasi kepada komunitas apabila volume sampah meningkat atau jadwal pickup perlu disesuaikan.

## Fitur Tambahan

### Community Dashboard

Menampilkan:
- Total sampah terkumpul
- Sampah yang berhasil didaur ulang
- Total pickup
- CO₂/environmental impact
- Recycling rate

### Reward System

Warga mendapatkan poin berdasarkan aktivitas seperti:
- memilah sampah,
- mengikuti jadwal pickup,
- mengurangi sampah,
- melakukan recycling.

## Dampak Lingkungan

Membuat pengelolaan sampah menjadi lebih rutin dan terukur sehingga:

**Less Waste → Better Collection → More Recycling → Cleaner Environment**

---

# Perbandingan Ide

| Aspek | Idea 1 | Idea 2 |
|---|---|---|
| Problem | Salah memilah/membuang barang | Pengambilan sampah tidak teratur |
| Main User | Individual/Household | Community/Cluster |
| AI Role | Sangat kuat | Perlu diperkuat |
| UI/UX Potential | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Complexity | Medium | High |
| Social Impact | High | Very High |
| Data Visualization | Medium | High |
| Marketplace Potential | High | Medium |
| Scalability | High | Very High |

---

# Kesimpulan Singkat

## Idea 1 — AI Waste Scanner

**Foto sampah → AI mengenali → AI menentukan tindakan → User melakukan tindakan yang benar.**

Fokus utama:
- Identifikasi barang
- Klasifikasi sampah
- Rekomendasi pembuangan
- Rekomendasi daur ulang
- Rekomendasi harga jual

## Idea 2 — Smart Community Waste Pickup

**Community register → AI memprediksi kebutuhan → sistem membuat jadwal → collector mengambil → sampah diproses → community melihat impact.**

Fokus utama:
- Registrasi komunitas
- Subscription
- Prediksi volume sampah
- Penjadwalan pickup
- Pencarian collector
- Monitoring pickup
- Monitoring environmental impact

---

# Ringkasan untuk Diskusi Kelompok

### IDEA 1

Aplikasi berbasis AI yang memungkinkan pengguna memotret barang atau sampah untuk mengetahui jenis, kondisi, apakah dapat didaur ulang, cara membuangnya dengan benar, serta apakah barang tersebut masih memiliki nilai jual. Jika barang dapat dijual, sistem membantu membuat listing dan memberikan rekomendasi harga.

### IDEA 2

Platform pengambilan sampah rutin untuk perumahan atau cluster yang menghubungkan komunitas dengan waste collector/pemulung. Komunitas dapat mendaftarkan lingkungan, memilih subscription dan jadwal pengambilan. AI membantu memprediksi volume sampah, mengoptimalkan jadwal dan rute, lalu sistem meneruskan order kepada collector. Community dapat memantau aktivitas pickup dan dampak lingkungan yang dihasilkan.

# Arah Utama

**Idea 1** lebih menonjolkan penggunaan **AI secara langsung kepada pengguna**.

**Idea 2** lebih menonjolkan **ekosistem pengelolaan sampah dan pengalaman UI/UX end-to-end**.
