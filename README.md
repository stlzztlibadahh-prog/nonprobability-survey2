## NAMA : SITI LIZATUL IBADAH
## NIM : G1F02410035
## PRODI : STATISTIKA
---
# nonprobability-survey1
# ANALISIS KEPUASAN MAHASISWA STATISTIKA TERHADAP FASILITAS DI FMIPA UNIVERSITAS MATARAM

## Deskripsi
Penelitian ini bertujuan untuk menganalisis tingkat kepuasan mahasiswa Program Studi Statistika FMIPA Universitas Mataram terhadap fasilitas kampus menggunakan metode survei. Analisis dilakukan dengan pendekatan statistik deskriptif serta membandingkan hasil *naïve estimation* dan *weighted estimation*.

---

## Latar Belakang
Fasilitas merupakan salah satu faktor penting yang mendukung kenyamanan dan kelancaran aktivitas mahasiswa di lingkungan perguruan tinggi. Ketersediaan fasilitas yang memadai, seperti ruang kelas, laboratorium, perpustakaan, akses internet, serta sarana pendukung lainnya, dapat membantu mahasiswa dalam menjalani proses perkuliahan dengan lebih baik. Sebaliknya, fasilitas yang kurang memadai dapat memengaruhi tingkat kepuasan mahasiswa dan menghambat efektivitas kegiatan akademik. Oleh karena itu, kepuasan mahasiswa terhadap fasilitas yang tersedia menjadi salah satu indikator penting dalam evaluasi kualitas pelayanan di lingkungan kampus.
Mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram sebagai pengguna langsung fasilitas kampus memiliki penilaian yang berbeda-beda terhadap kualitas fasilitas yang tersedia. Penilaian tersebut penting untuk diketahui karena dapat memberikan gambaran mengenai fasilitas yang sudah baik maupun fasilitas yang masih perlu ditingkatkan. Dengan mengetahui tingkat kepuasan mahasiswa, pihak fakultas dapat melakukan evaluasi dan menentukan langkah yang tepat dalam meningkatkan kualitas sarana dan prasarana guna mendukung proses pembelajaran yang lebih optimal. 

## Rumusan Masalah
- Bagaimana tingkat kepuasan mahasiswa Statistika terhadap fasilitas belajar di Fakultas MIPA Universitas Mataram? 
- Bagaimana hasil estimasi kepuasan mahasiswa menggunakan *naïve estimation*? 
- Bagaimana perbandingan hasil *naïve estimation* dan *weighted estimation* pada data survei kepuasan mahasiswa?

## Tujuan Penelitian
- Mengetahui tingkat kepuasan mahasiswa terhadap fasilitas di FMIPA Universitas Mataram.
- Menghitung estimasi kepuasan menggunakan *naïve estimation*.
- Membandingkan hasil *naïve estimation* dan *weighted estimation*.

---

## Metode Penelitian

### Jenis Penelitian
Penelitian kuantitatif dengan metode survei menggunakan kuesioner skala Likert.

### Populasi dan Sampel
- Populasi: Mahasiswa Program Studi Statistika FMIPA Universitas Mataram.
- Sampel: 28 responden.
- Teknik sampling: *Non-probability sampling*.

### Instrumen Penelitian
Kuesioner menggunakan skala Likert:

| Skor | Keterangan |
|------|-------------|
| 1 | Sangat Tidak Puas |
| 2 | Tidak Puas |
| 3 | Netral |
| 4 | Puas |
| 5 | Sangat Puas |

---

# Teknik Analisis Data

## 1. Penentuan Variabel
Tahap awal dilakukan penentuan variabel penelitian yang terdiri dari variabel demografis dan variabel utama.  
Variabel demografis meliputi jenis kelamin, angkatan, dan program studi responden, sedangkan variabel utama berkaitan dengan pertanyaan inti dalam kuesioner penelitian.

## 2. Mengumpulkan Data
Data diperoleh melalui penyebaran kuesioner kepada responden.  
Seluruh hasil pengisian kuesioner kemudian diunduh dalam bentuk file CSV atau Excel untuk dilakukan proses pengolahan lebih lanjut.

## 3. Uji Validitas
Uji validitas dilakukan untuk mengetahui apakah setiap item pernyataan dalam kuesioner mampu mengukur variabel penelitian dengan tepat.  
Suatu item dinyatakan valid apabila nilai r hitung > r tabel dan nilai signifikansi (Sig.) < 0,05.  
Sebaliknya, jika r hitung < r tabel dan Sig. > 0,05, maka item dinyatakan tidak valid dan tidak digunakan dalam analisis selanjutnya.

## 4. Uji Reliabilitas
Uji reliabilitas dilakukan untuk mengetahui tingkat konsistensi instrumen penelitian sehingga data yang dihasilkan dapat dipercaya.  
Metode yang digunakan adalah Cronbach’s Alpha.  
Instrumen dinyatakan reliabel jika nilai Cronbach’s Alpha > 0,70.

## 5. Analisis Deskriptif
Analisis deskriptif dilakukan menggunakan SPSS untuk menghitung distribusi frekuensi, persentase, serta menyajikan grafik data responden dan variabel penelitian.

## 6. Naïve Estimation
Estimasi dilakukan tanpa penyesuaian (koreksi), yaitu dengan menghitung proporsi responden yang menjawab “setuju” terhadap total responden.

Rumus:
`P̂ = Jumlah Setuju / Total Responden`

## 7. Weighted (Weighting Sederhana)
Dilakukan pembobotan sederhana untuk menyesuaikan distribusi sampel dengan populasi.

Rumus bobot:
`wᵢ = Proporsi Populasi / Proporsi Sampel`

## 8. Perbandingan Estimasi
Hasil naïve estimation dan weighted estimation dibandingkan untuk melihat perbedaan antara estimasi tanpa pembobotan dan yang sudah disesuaikan dengan struktur populasi.

## 9. Visualisasi Data
Tahap akhir dilakukan visualisasi data dalam bentuk grafik, minimal dua grafik:
- Grafik distribusi responden  
- Grafik perbandingan hasil estimasi  

Visualisasi bertujuan agar hasil analisis lebih mudah dipahami dan diinterpretasikan.

--- 
# HASIL DAN PEMBAHASAN  

## Uji Validitas
Berikut adalah hasil uji validitas menggunakan software SPSS:

**Tabel 1. Item-Total Statistics**

| Pertanyaan | r hitung | r tabel | Nilai Sig. | Keputusan     |
|-----------|----------|---------|------------|---------------|
| 1         | 0.600    | 0.374   | 0.001      | Valid         |
| 2         | 0.563    | 0.374   | 0.002      | Valid         |
| 3         | 0.475    | 0.374   | 0.011      | Valid         |
| 4         | 0.583    | 0.374   | 0.001      | Valid         |
| 5         | 0.435    | 0.374   | 0.021      | Valid         |
| 6         | 0.665    | 0.374   | 0.000      | Valid         |
| 7         | 0.501    | 0.374   | 0.007      | Valid         |
| 8         | 0.711    | 0.374   | 0.000      | Valid         |
| 9         | 0.390    | 0.374   | 0.040      | Valid         |
| 10        | 0.228    | 0.374   | 0.244      | Tidak Valid   |
| 11        | 0.499    | 0.374   | 0.007      | Valid         |
| 12        | 0.699    | 0.374   | 0.000      | Valid         |

Berdasarkan tabel Item-Total Statistics diperoleh nilai Total Correlation (r hitung) berkisar antara 0,228 hingga 0,711. Nilai tersebut menunjukkan tingkat hubungan antara masing-masing item pertanyaan dengan skor total kuesioner. Adapun nilai r tabel yang digunakan sebesar 0,374, diperoleh dari taraf signifikansi (α = 0,05) dengan derajat kebebasan (df) = N − 2 = 28 − 2 = 26.  Berdasarkan perbandingan antara r hitung dan r tabel, terdapat 11 item pertanyaan yang dinyatakan valid karena memiliki nilai r hitung lebih besar daripada r tabel, yaitu pertanyaan nomor 1, 2, 3, 4, 5, 6, 7, 8, 9, 11, dan 12. Sementara itu, pertanyaan nomor 10 dinyatakan tidak valid karena memiliki nilai r hitung sebesar 0,228, yang lebih kecil dibandingkan r tabel sebesar 0,374. Selain itu, jika ditinjau dari nilai signifikansi (Sig.), seluruh item yang valid memiliki nilai Sig. < 0,05. Contohnya, pertanyaan nomor 1 (0,001), nomor 6 (0,000), dan nomor 9 (0,040), yang menunjukkan bahwa item tersebut signifikan. Sebaliknya, pertanyaan nomor 10 memiliki nilai Sig. sebesar 0,244 (> 0,05), sehingga tidak signifikan dan tidak valid. Dengan demikian, dari total 12 item pertanyaan, terdapat 11 item valid dan 1 item tidak valid (pertanyaan nomor 10). Item tidak valid tersebut tidak digunakan dalam analisis selanjutnya, sedangkan item valid dilanjutkan ke uji reliabilitas.

## Uji Reliabilitas

**Tabel 2. Uji Reliabilitas**

| Cronbach’s Alpha | N of Items |
|------------------|------------|
| 0.772            | 11         |

Berdasarkan output *Reliability Statistics* dari SPSS, uji reliabilitas dilakukan menggunakan metode Cronbach’s Alpha terhadap 11 item pertanyaan. Diperoleh nilai Cronbach’s Alpha sebesar **0,772**. Nilai ini lebih besar dari 0,70 (0,772 > 0,70), sehingga instrumen penelitian dinyatakan **reliabel**. Hal ini menunjukkan bahwa setiap item pertanyaan memiliki konsistensi internal yang baik dan saling berkorelasi dalam mengukur variabel penelitian. Dengan demikian, kuesioner yang digunakan telah memenuhi kriteria reliabilitas dan layak digunakan untuk analisis lebih lanjut.

## Analisis Deskriptif
### a. Tabel Frekuensi

| Item | Distribusi Frekuensi (Skor 1–5) |
|------|---------------------------------|
| 1. Ruang kelas nyaman | 1:1, 2:1, 3:9, 4:14, 5:3 |
| 2. Meja & kursi layak | 3:9, 4:15, 5:4 |
| 3. AC/Kipas berfungsi | 1:1, 2:9, 3:12, 4:5, 5:1 |
| 4. Pencahayaan memadai | 3:12, 4:11, 5:5 |
| 5. TV/LCD mendukung | 1:2, 2:2, 3:9, 4:11, 5:4 |
| 6. Laboratorium memadai | 2:3, 3:4, 4:16, 5:5 |
| 7. Akses WiFi lancar | 3:11, 4:13, 5:4 |
| 8. Kebersihan kelas | 2:1, 3:8, 4:10, 5:9 |
| 9. Kebersihan toilet | 2:1, 3:13, 4:9, 5:5 |
| 10. Perpustakaan nyaman | 2:1, 3:5, 4:15, 5:7 |
| 11. Area parkir aman | 3:5, 4:14, 5:9 |
| 12. Kepuasan fasilitas FMIPA | 3:7, 4:17, 5:4 |

---

### b. Tabel Persentase

| Item | Distribusi Persentase (%) |
|------|--------------------------|
| 1. Ruang kelas nyaman | 1:3.57, 2:3.57, 3:32.14, 4:50.00, 5:10.71 |
| 2. Meja & kursi layak | 3:32.14, 4:53.57, 5:14.29 |
| 3. AC/Kipas berfungsi | 1:3.57, 2:32.14, 3:42.86, 4:17.86, 5:3.57 |
| 4. Pencahayaan memadai | 3:42.86, 4:39.29, 5:17.86 |
| 5. TV/LCD mendukung | 1:7.14, 2:7.14, 3:32.14, 4:39.29, 5:14.29 |
| 6. Laboratorium memadai | 2:10.71, 3:14.29, 4:57.14, 5:17.86 |
| 7. Akses WiFi lancar | 3:39.29, 4:46.43, 5:14.29 |
| 8. Kebersihan kelas | 2:3.57, 3:28.57, 4:35.71, 5:32.14 |
| 9. Kebersihan toilet | 2:3.57, 3:46.43, 4:32.14, 5:17.86 |
| 10. Perpustakaan nyaman | 2:3.57, 3:17.86, 4:53.57, 5:25.00 |
| 11. Area parkir aman | 3:17.86, 4:50.00, 5:32.14 |
| 12. Kepuasan fasilitas FMIPA | 3:25.00, 4:60.71, 5:14.29 |

---

### Ringkasan 
Secara umum, mayoritas responden cenderung memberikan jawaban pada kategori **4 (setuju)** dan **5 (sangat setuju)** pada hampir seluruh item, menunjukkan bahwa persepsi responden terhadap fasilitas FMIPA Universitas Mataram cenderung positif.
---
# Estimasi Kepuasan Fasilitas FMIPA Universitas Mataram

## Naïve Estimation

Naïve estimation digunakan untuk menghitung proporsi responden yang memberikan jawaban **Setuju** dan **Sangat Setuju** terhadap setiap indikator fasilitas.

### Rumus

```math
\hat{P}=\frac{\text{Jumlah (Setuju + Sangat Setuju)}}{\text{Total Responden}}
```

Dengan total responden:

```math
n = 28
```

---

## Hasil Naïve Estimation

| No | Indikator Fasilitas | Perhitungan | Nilai |
| --- | --- | --- | --- |
| 1 | Ruang kelas nyaman untuk pembelajaran | (14 + 3) / 28 | 0.607 |
| 2 | Meja dan kursi layak digunakan | (15 + 4) / 28 | 0.679 |
| 3 | AC/kipas berfungsi dengan baik | (5 + 1) / 28 | 0.214 |
| 4 | Pencahayaan ruang kelas memadai | (11 + 5) / 28 | 0.571 |
| 5 | TV/LCD mendukung perkuliahan | (11 + 4) / 28 | 0.536 |
| 6 | Fasilitas laboratorium memadai | (16 + 5) / 28 | 0.750 |
| 7 | Akses internet/WiFi membantu pembelajaran | (13 + 4) / 28 | 0.607 |
| 8 | Kebersihan ruang kelas terjaga | (10 + 9) / 28 | 0.679 |
| 9 | Kebersihan toilet terjaga | (9 + 5) / 28 | 0.500 |
| 10 | Area parkir aman dan memadai | (14 + 9) / 28 | 0.821 |
| 11 | Kepuasan keseluruhan terhadap fasilitas FMIPA | (17 + 4) / 28 | 0.750 |

---

# Weighting Sederhana

Pembobotan sederhana dilakukan berdasarkan **jenis kelamin responden** agar distribusi sampel menyesuaikan distribusi populasi mahasiswa Program Studi Statistika FMIPA Universitas Mataram.

## Distribusi Populasi

| Jenis Kelamin | Jumlah Populasi |
| --- | --- |
| Laki-laki | 31 |
| Perempuan | 126 |
| **Total** | **157** |

## Distribusi Sampel

| Jenis Kelamin | Jumlah Sampel |
| --- | --- |
| Laki-laki | 9 |
| Perempuan | 19 |
| **Total** | **28** |

---

## Menghitung Proporsi Populasi

### Laki-laki

```math
p_L=\frac{31}{157}=0.197
```

### Perempuan

```math
p_P=\frac{126}{157}=0.803
```

---

## Menghitung Proporsi Sampel

### Laki-laki

```math
p_L=\frac{9}{28}=0.321
```

### Perempuan

```math
p_P=\frac{19}{28}=0.679
```

---

## Menghitung Bobot

Rumus pembobotan:

```math
w_i=\frac{\text{Proporsi Populasi}}{\text{Proporsi Sampel}}
```

### Bobot Laki-laki

```math
w_L=\frac{0.197}{0.321}=0.614
```

### Bobot Perempuan

```math
w_P=\frac{0.803}{0.679}=1.183
```

Berdasarkan hasil tersebut:

- Bobot laki-laki = **0.614**
- Bobot perempuan = **1.183**

---

# Weighted Estimation

Weighted estimation dihitung menggunakan rumus:

```math
\bar{x}_w=\frac{\sum w_i x_i}{\sum w_i}
```

## Hasil Weighted Estimation

| No | Indikator Fasilitas | Weighted Estimation |
| --- | --- | --- |
| 1 | Ruang kelas nyaman | 0.637 |
| 2 | Meja dan kursi layak | 0.701 |
| 3 | AC/kipas berfungsi | 0.253 |
| 4 | Pencahayaan memadai | 0.574 |
| 5 | TV/LCD mendukung | 0.552 |
| 6 | Fasilitas laboratorium | 0.765 |
| 7 | Akses internet/WiFi | 0.449 |
| 8 | Kebersihan ruang kelas | 0.681 |
| 9 | Kebersihan toilet | 0.767 |
| 10 | Area parkir aman | 0.809 |
| 11 | Kepuasan keseluruhan | 0.765 |

---

# Perbandingan Estimasi

| No | Indikator Fasilitas | Naïve Estimation | Weighted Estimation |
| --- | --- | --- | --- |
| 1 | Ruang kelas nyaman | 0.607 | 0.637 |
| 2 | Meja dan kursi layak | 0.679 | 0.701 |
| 3 | AC/kipas berfungsi | 0.214 | 0.253 |
| 4 | Pencahayaan memadai | 0.571 | 0.574 |
| 5 | TV/LCD mendukung | 0.536 | 0.552 |
| 6 | Fasilitas laboratorium | 0.750 | 0.765 |
| 7 | Akses internet/WiFi | 0.607 | 0.449 |
| 8 | Kebersihan ruang kelas | 0.679 | 0.681 |
| 9 | Kebersihan toilet | 0.500 | 0.767 |
| 10 | Area parkir aman | 0.821 | 0.809 |
| 11 | Kepuasan keseluruhan | 0.750 | 0.765 |

---

# Kesimpulan

Berdasarkan hasil analisis, naïve estimation dan weighted estimation menunjukkan pola yang relatif serupa pada sebagian besar indikator fasilitas. Namun, setelah dilakukan pembobotan berdasarkan jenis kelamin responden, terdapat beberapa perubahan nilai estimasi.

Beberapa indikator mengalami peningkatan nilai setelah pembobotan, seperti:

- AC/kipas berfungsi dengan baik
- Fasilitas laboratorium
- Kepuasan keseluruhan terhadap fasilitas

Sementara itu, beberapa indikator mengalami penurunan nilai, seperti:

- Akses internet/WiFi
- Area parkir

Perubahan tersebut menunjukkan bahwa proses pembobotan dapat memengaruhi hasil estimasi karena telah menyesuaikan distribusi sampel dengan struktur populasi sebenarnya. Secara umum, urutan penilaian fasilitas tidak berubah secara signifikan, namun weighted estimation dianggap lebih representatif dibanding naïve estimation karena mempertimbangkan karakteristik populasi responden.
