### NAMA : SITI LIZATUL IBADAH
### NIM : G1F02410035
### PROGRAM STUDI : STATISTIKA
---
# ANALISIS KEPUASAN MAHASISWA STATISTIKA TERHADAP FASILITAS FAKULTAS MIPA UNIVERSITAS MATARAM

## Deskripsi
Penelitian ini bertujuan untuk menganalisis tingkat kepuasan mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram terhadap fasilitas yang tersedia di lingkungan kampus. Analisis dilakukan menggunakan pendekatan statistik deskriptif dengan bantuan software RStudio melalui penyebaran kuesioner kepada responden.

---

## Latar Belakang
Fasilitas kampus merupakan salah satu faktor penting yang mendukung kenyamanan, efektivitas, dan kelancaran proses pembelajaran mahasiswa di perguruan tinggi. Ketersediaan fasilitas yang memadai seperti ruang kelas, laboratorium, perpustakaan, akses internet, serta sarana pendukung lainnya dapat membantu mahasiswa dalam melaksanakan kegiatan akademik secara optimal. Selain itu, kualitas fasilitas yang baik juga dapat meningkatkan motivasi belajar, kenyamanan mahasiswa, serta mendukung terciptanya lingkungan akademik yang kondusif. Sebagai salah satu fakultas yang memiliki berbagai program studi di bidang sains, Fakultas MIPA Universitas Mataram perlu memastikan bahwa fasilitas yang tersedia mampu menunjang kebutuhan mahasiswa dalam proses pembelajaran maupun kegiatan praktikum. Namun, dalam pelaksanaannya masih terdapat berbagai persepsi mahasiswa terkait kualitas fasilitas yang tersedia, baik dari segi kenyamanan ruang kelas, kelayakan sarana belajar, akses internet, maupun kebersihan lingkungan kampus. Mahasiswa Program Studi Statistika sebagai pengguna langsung fasilitas kampus memiliki pengalaman dan penilaian yang berbeda-beda terhadap kualitas fasilitas yang tersedia. Penilaian tersebut penting untuk diketahui karena dapat menjadi bahan evaluasi bagi pihak fakultas dalam meningkatkan kualitas pelayanan dan sarana prasarana kampus. Oleh karena itu, penelitian mengenai tingkat kepuasan mahasiswa terhadap fasilitas di Fakultas MIPA Universitas Mataram perlu dilakukan agar dapat memberikan gambaran mengenai kondisi fasilitas yang sudah baik maupun fasilitas yang masih perlu ditingkatkan.

---

## Rumusan Masalah
1. Bagaimana tingkat kepuasan mahasiswa Program Studi Statistika terhadap fasilitas di Fakultas MIPA Universitas Mataram?
2. Apakah instrumen penelitian yang digunakan telah memenuhi uji validitas dan reliabilitas?
3. Bagaimana distribusi jawaban responden terhadap fasilitas yang tersedia di Fakultas MIPA Universitas Mataram?

---

## Tujuan Penelitian
1. Mengetahui tingkat kepuasan mahasiswa Program Studi Statistika terhadap fasilitas di Fakultas MIPA Universitas Mataram.
2. Mengetahui validitas dan reliabilitas instrumen penelitian yang digunakan.
3. Mendeskripsikan distribusi jawaban responden terhadap fasilitas yang tersedia di Fakultas MIPA Universitas Mataram.

---

# Metode Penelitian

## Jenis Penelitian
Penelitian ini menggunakan pendekatan kuantitatif dengan metode survei menggunakan kuesioner skala Likert.

---

## Populasi dan Sampel
- Populasi: Mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram sebanyak 157 mahasiswa.
- Sampel: 70 responden.

---

## Teknik Sampling
Teknik sampling yang digunakan dalam penelitian ini adalah non-probability sampling.

---

## Penentuan Ukuran Sampel (Rumus Slovin)

Penentuan ukuran sampel dilakukan menggunakan rumus Slovin dengan tingkat kesalahan sebesar 10%.

Rumus Slovin:

n = N / (1 + N × e²)

Keterangan:
- n = ukuran sampel
- N = jumlah populasi
- e = tingkat kesalahan

Diketahui:
- N = 157
- e = 0.10

Maka:

n = 157 / (1 + 157 × (0.1)²)

n = 157 / (1 + 157 × 0.01)

n = 157 / 2.57

n = 61.08949

Hasil perhitungan menunjukkan bahwa jumlah sampel minimum yang diperlukan adalah 62 responden. Dalam penelitian ini digunakan sebanyak 70 responden sehingga jumlah sampel telah memenuhi kebutuhan penelitian.
Hasil perhitungan menunjukkan bahwa jumlah sampel minimum yang diperlukan adalah 62 responden. Dalam penelitian ini digunakan sebanyak 70 responden sehingga jumlah sampel telah memenuhi kebutuhan penelitian.

---

## Instrumen Penelitian

Instrumen penelitian menggunakan kuesioner dengan skala Likert sebagai berikut:

| Skor | Keterangan |
|------|-------------|
| 1 | Sangat Tidak Puas |
| 2 | Tidak Puas |
| 3 | Netral |
| 4 | Puas |
| 5 | Sangat Puas |

---

## Tahapan Analisis Data

### 1. Load Library
Pada tahap ini digunakan beberapa package yang membantu proses membaca data, analisis statistik, dan pengolahan data.

```r
# =========================
# LOAD LIBRARY
# =========================
library(readxl)
library(psych)
library(tidyverse)
```

---

### 2. Import Data
Data hasil kuesioner kepuasan mahasiswa diimpor dari file Excel agar dapat dianalisis menggunakan RStudio.

```r
# =========================
# MEMBACA DATA
# =========================
data <- read_excel(
  "D:/SEMESTER 4/TEKSAM/DATA KEPUASAN FASILITAS MIPA (3).xlsx"
)

# Melihat data
View(data)
```

---

### 3. Struktur dan Pengolahan Data
Tahap ini dilakukan untuk melihat struktur data serta mengubah seluruh variabel menjadi numerik agar dapat digunakan dalam analisis statistik.

```r
# =========================
# STRUKTUR DATA
# =========================
str(data)

# Mengubah semua variabel menjadi numerik
data <- data %>%
  mutate(across(everything(), as.numeric))
```

---

### 4. Penentuan Ukuran Sampel Menggunakan Rumus Slovin
Rumus Slovin digunakan untuk menentukan jumlah sampel minimum berdasarkan jumlah populasi dan tingkat kesalahan penelitian.

```r
# =========================
# RUMUS SLOVIN
# =========================

# Jumlah populasi
N <- 157

# Tingkat kesalahan
e <- 0.10

# Menghitung ukuran sampel
n <- N / (1 + N * e^2)

# Menampilkan hasil Slovin
n

# Membulatkan hasil
ceiling(n)
```

---

### 5. Memilih Item Pertanyaan
Tahap ini dilakukan untuk mengambil variabel item pertanyaan yang digunakan dalam penelitian.

```r
# =========================
# MEMILIH ITEM PERTANYAAN
# =========================
item <- data[, 1:12]
```

---

### 6. Uji Validitas
Uji validitas dilakukan untuk mengetahui apakah setiap item pertanyaan mampu mengukur variabel penelitian dengan baik. Korelasi item terhadap total skor dihitung menggunakan fungsi `cor()` dan `cor.test()`.

```r
# =========================
# UJI VALIDITAS
# =========================

# Menghitung total skor
total_skor <- rowSums(item)

# Korelasi item dengan total skor
validitas <- data.frame(
  Item = names(item),
  
  r_hitung = sapply(item, function(x)
    cor(x, total_skor)
  ),
  
  p_value = sapply(item, function(x)
    cor.test(x, total_skor)$p.value
  )
)

# Menampilkan hasil validitas
print(validitas)
```

---

### 7. Uji Reliabilitas
Uji reliabilitas dilakukan menggunakan metode Cronbach’s Alpha untuk mengetahui tingkat konsistensi instrumen penelitian.

```r
# =========================
# UJI RELIABILITAS
# =========================

reliabilitas <- psych::alpha(item)

# Menampilkan hasil reliabilitas
reliabilitas

# Nilai Cronbach Alpha
reliabilitas$total$raw_alpha
```

---

### 8. Analisis Deskriptif
Analisis deskriptif digunakan untuk melihat gambaran umum data seperti nilai minimum, maksimum, rata-rata, dan standar deviasi.

```r
# =========================
# ANALISIS DESKRIPTIF
# =========================

# Statistik deskriptif sederhana
summary(item)

# Statistik deskriptif lengkap
describe(item)
```

---

### 9. Tabel Frekuensi dan Persentase
Tahap ini bertujuan untuk mengetahui jumlah jawaban responden dan persentase pada setiap kategori skala Likert untuk seluruh item pertanyaan.

```r
# =========================
# FREKUENSI DAN PERSENTASE
# =========================

for(i in names(item)){

  cat("\n====================\n")
  cat("Frekuensi", i, "\n")
  cat("====================\n")

  print(table(item[[i]]))

  cat("\nPersentase", i, "\n")

  print(
    round(
      prop.table(table(item[[i]])) * 100,
      2
    )
  )

}
```

---

### 10. Visualisasi Data
Histogram digunakan untuk melihat distribusi total skor kepuasan responden secara keseluruhan.

```r
# =========================
# VISUALISASI DATA
# =========================

hist(
  total_skor,

  main = "Distribusi Skor Kepuasan Responden",

  xlab = "Total Skor Kepuasan",
  ylab = "Frekuensi Responden",

  col = "lightblue",
  border = "black"
)
```

---

# Hasil dan Pembahasan

## Uji Validitas

| No | Item Pertanyaan | r hitung | p-value | Keterangan |
|---|---|---|---|---|
| 1 | Ruang kelas nyaman untuk proses pembelajaran | 0.663 | 0.000 | Valid |
| 2 | Meja dan kursi layak digunakan | 0.627 | 0.000 | Valid |
| 3 | AC atau kipas angin berfungsi baik | 0.655 | 0.000 | Valid |
| 4 | Pencahayaan ruang kelas memadai | 0.634 | 0.000 | Valid |
| 5 | TV/LCD mendukung perkuliahan | 0.433 | 0.000 | Valid |
| 6 | Laboratorium memadai | 0.588 | 0.000 | Valid |
| 7 | Akses internet/WiFi membantu pembelajaran | 0.639 | 0.000 | Valid |
| 8 | Kebersihan ruang kelas terjaga | 0.746 | 0.000 | Valid |
| 9 | Kebersihan toilet terjaga | 0.541 | 0.000 | Valid |
| 10 | Perpustakaan nyaman untuk belajar | 0.595 | 0.000 | Valid |
| 11 | Area parkir aman dan memadai | 0.530 | 0.000 | Valid |
| 12 | Kepuasan keseluruhan terhadap fasilitas FMIPA | 0.862 | 0.000 | Valid |

Berdasarkan hasil uji validitas diperoleh seluruh item memiliki nilai \(r_{hitung} > 0.30\) dan nilai signifikansi \(< 0.05\), sehingga seluruh item pertanyaan dinyatakan valid dan layak digunakan dalam penelitian. Nilai validitas tertinggi terdapat pada item kepuasan keseluruhan terhadap fasilitas FMIPA dengan nilai \(r_{hitung} = 0.862\), sedangkan nilai validitas terendah terdapat pada item fasilitas TV/LCD dengan nilai \(r_{hitung} = 0.433\). Meskipun demikian, seluruh item tetap memenuhi kriteria validitas.

---

## Uji Reliabilitas

| Cronbach’s Alpha | Jumlah Item |
|---|---|
| 0.848 | 12 |

Berdasarkan hasil uji reliabilitas diperoleh nilai Cronbach’s Alpha sebesar 0.848. Nilai tersebut lebih besar dari 0.70 sehingga instrumen penelitian dinyatakan reliabel. Hal ini menunjukkan bahwa seluruh item pertanyaan memiliki tingkat konsistensi internal yang baik dan dapat digunakan untuk analisis lebih lanjut.

---

## Analisis Deskriptif

### Tabel Frekuensi

| No | Indikator | Distribusi Frekuensi |
|---|---|---|
| 1 | Ruang kelas nyaman | 1:1, 2:3, 3:22, 4:31, 5:13 |
| 2 | Meja dan kursi layak | 2:2, 3:19, 4:32, 5:17 |
| 3 | AC/kipas berfungsi | 1:6, 2:19, 3:23, 4:16, 5:6 |
| 4 | Pencahayaan memadai | 2:2, 3:29, 4:27, 5:12 |
| 5 | TV/LCD mendukung | 1:6, 2:9, 3:18, 4:28, 5:9 |
| 6 | Laboratorium memadai | 2:3, 3:20, 4:30, 5:17 |
| 7 | Akses internet/WiFi | 2:5, 3:24, 4:25, 5:16 |
| 8 | Kebersihan ruang kelas | 2:1, 3:21, 4:26, 5:22 |
| 9 | Kebersihan toilet | 1:4, 2:10, 3:25, 4:21, 5:10 |
| 10 | Perpustakaan nyaman | 2:1, 3:17, 4:33, 5:19 |
| 11 | Area parkir aman | 1:1, 2:3, 3:18, 4:26, 5:22 |
| 12 | Kepuasan keseluruhan FMIPA | 3:25, 4:28, 5:17 |

---

### Tabel Persentase

| No | Indikator | Distribusi Persentase (%) |
|---|---|---|
| 1 | Ruang kelas nyaman | 1:1.43, 2:4.29, 3:31.43, 4:44.29, 5:18.57 |
| 2 | Meja dan kursi layak | 2:2.86, 3:27.14, 4:45.71, 5:24.29 |
| 3 | AC/kipas berfungsi | 1:8.57, 2:27.14, 3:32.86, 4:22.86, 5:8.57 |
| 4 | Pencahayaan memadai | 2:2.86, 3:41.43, 4:38.57, 5:17.14 |
| 5 | TV/LCD mendukung | 1:8.57, 2:12.86, 3:25.71, 4:40.00, 5:12.86 |
| 6 | Laboratorium memadai | 2:4.29, 3:28.57, 4:42.86, 5:24.29 |
| 7 | Akses internet/WiFi | 2:7.14, 3:34.29, 4:35.71, 5:22.86 |
| 8 | Kebersihan ruang kelas | 2:1.43, 3:30.00, 4:37.14, 5:31.43 |
| 9 | Kebersihan toilet | 1:5.71, 2:14.29, 3:35.71, 4:30.00, 5:14.29 |
| 10 | Perpustakaan nyaman | 2:1.43, 3:24.29, 4:47.14, 5:27.14 |
| 11 | Area parkir aman | 1:1.43, 2:4.29, 3:25.71, 4:37.14, 5:31.43 |
| 12 | Kepuasan keseluruhan FMIPA | 3:35.71, 4:40.00, 5:24.29 |

Berdasarkan hasil analisis deskriptif, mayoritas responden memberikan jawaban pada kategori puas dan sangat puas pada hampir seluruh indikator fasilitas. Hal ini menunjukkan bahwa mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram secara umum merasa puas terhadap fasilitas yang tersedia.

Indikator dengan tingkat kepuasan yang cukup tinggi terlihat pada fasilitas perpustakaan, area parkir, dan kebersihan ruang kelas. Sementara itu, fasilitas AC/kipas angin serta kebersihan toilet masih memperoleh beberapa jawaban kurang puas sehingga fasilitas tersebut masih perlu diperhatikan dan ditingkatkan.

---


## Perbandingan Penelitian 28 Responden dan 70 Responden

Penelitian ini mengalami penambahan jumlah responden dari 28 responden menjadi 70 responden. Perbandingan dilakukan untuk melihat perubahan tingkat kesalahan (error), hasil uji validitas, hasil uji reliabilitas, serta distribusi jawaban responden setelah jumlah sampel ditambah.

---

## Perbandingan Penentuan Sampel Menggunakan Rumus Slovin

### Tabel Perbandingan Slovin

| Keterangan | 28 Responden | 70 Responden |
|---|---|---|
| Populasi | 157 | 157 |
| Jumlah Sampel | 28 | 70 |
| Tingkat Error | 17% | 10% |
| Keterangan | Ketelitian lebih rendah | Ketelitian lebih baik |

Berdasarkan hasil perhitungan menggunakan rumus Slovin, penelitian awal dengan 28 responden memiliki tingkat kesalahan sekitar 17%. Tingkat error tersebut tergolong cukup besar sehingga tingkat ketelitian penelitian masih rendah. Jumlah responden yang relatif sedikit menyebabkan data yang diperoleh belum sepenuhnya mampu mewakili populasi mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram.

Setelah jumlah responden ditambah menjadi 70 responden, tingkat kesalahan penelitian menurun menjadi 10%. Penurunan tingkat error menunjukkan bahwa data penelitian menjadi lebih representatif dan memiliki tingkat ketelitian yang lebih baik dibandingkan penelitian sebelumnya. Selain itu, jumlah sampel sebanyak 70 responden telah melebihi jumlah minimum hasil perhitungan Slovin yaitu sekitar 61 responden, sehingga data penelitian dinilai lebih layak digunakan untuk analisis lebih lanjut.

---

## Perbandingan Uji Validitas

### Tabel Perbandingan Validitas

| No | Indikator | r Hitung (28 Responden) | r Hitung (70 Responden) | Keterangan |
|---|---|---|---|---|
| 1 | Ruang kelas nyaman | 0.600 | 0.663 | Valid |
| 2 | Meja & kursi layak | 0.563 | 0.627 | Valid |
| 3 | AC/Kipas berfungsi | 0.475 | 0.655 | Valid |
| 4 | Pencahayaan memadai | 0.583 | 0.634 | Valid |
| 5 | TV/LCD mendukung | 0.435 | 0.433 | Valid |
| 6 | Laboratorium memadai | 0.665 | 0.588 | Valid |
| 7 | Akses internet/WiFi | 0.501 | 0.639 | Valid |
| 8 | Kebersihan ruang kelas | 0.711 | 0.746 | Valid |
| 9 | Kebersihan toilet | 0.390 | 0.541 | Valid |
| 10 | Perpustakaan nyaman | 0.228 | 0.595 | Tidak Valid → Valid |
| 11 | Area parkir aman | 0.499 | 0.530 | Valid |
| 12 | Kepuasan fasilitas FMIPA | 0.699 | 0.862 | Valid |

Berdasarkan hasil uji validitas pada 28 responden, terdapat satu item yang tidak valid yaitu item nomor 10 dengan nilai \(r_{hitung} = 0.228\), karena nilainya lebih kecil dibandingkan \(r_{tabel} = 0.374\). Sementara itu, item lainnya telah memenuhi kriteria validitas.

Setelah jumlah responden ditambah menjadi 70 responden, seluruh item pertanyaan dinyatakan valid karena seluruh nilai \(r_{hitung}\) berada di atas 0.30 dan memiliki nilai signifikansi \(< 0.05\). Peningkatan jumlah responden menyebabkan hasil korelasi item menjadi lebih stabil dan lebih kuat dalam mengukur variabel penelitian.

Perubahan paling terlihat terdapat pada item nomor 10 mengenai kenyamanan perpustakaan. Pada data awal item tersebut dinyatakan tidak valid, namun setelah jumlah responden ditambah nilai korelasinya meningkat menjadi 0.595 sehingga item tersebut berubah menjadi valid. Hal ini menunjukkan bahwa penambahan jumlah sampel dapat meningkatkan kualitas instrumen penelitian serta menghasilkan pengukuran yang lebih akurat.

Selain itu, nilai validitas tertinggi pada data 70 responden terdapat pada item kepuasan keseluruhan terhadap fasilitas FMIPA dengan nilai \(r_{hitung} = 0.862\). Hal ini menunjukkan bahwa item tersebut memiliki hubungan yang sangat kuat dengan total skor kepuasan mahasiswa.

---

## Perbandingan Uji Reliabilitas

### Tabel Perbandingan Reliabilitas

| Sampel | Cronbach Alpha | Keterangan |
|---|---|---|
| 28 Responden | 0.772 | Reliabel |
| 70 Responden | 0.848 | Reliabel |

Berdasarkan hasil uji reliabilitas menggunakan metode Cronbach’s Alpha, data dengan 28 responden memperoleh nilai Cronbach Alpha sebesar 0.772. Nilai tersebut telah memenuhi kriteria reliabel karena berada di atas 0.70. Namun, setelah jumlah responden ditambah menjadi 70 responden, nilai Cronbach Alpha meningkat menjadi 0.848.

Peningkatan nilai reliabilitas menunjukkan bahwa konsistensi internal antar item pertanyaan menjadi lebih baik setelah jumlah responden ditambah. Dengan kata lain, item-item pertanyaan pada kuesioner semakin stabil dalam mengukur tingkat kepuasan mahasiswa terhadap fasilitas Fakultas MIPA Universitas Mataram.

Nilai reliabilitas yang lebih tinggi pada data 70 responden juga menunjukkan bahwa hasil penelitian menjadi lebih konsisten dan lebih dapat dipercaya dibandingkan data awal dengan 28 responden.

---

## Perbandingan Analisis Deskriptif

### Tabel Perbandingan Frekuensi

| No | Indikator | 28 Responden | 70 Responden |
|---|---|---|---|
| 1 | Ruang kelas nyaman | 1:1, 2:1, 3:9, 4:14, 5:3 | 1:1, 2:3, 3:22, 4:31, 5:13 |
| 2 | Meja & kursi layak | 3:9, 4:15, 5:4 | 2:2, 3:19, 4:32, 5:17 |
| 3 | AC/Kipas berfungsi | 1:1, 2:9, 3:12, 4:5, 5:1 | 1:6, 2:19, 3:23, 4:16, 5:6 |
| 4 | Pencahayaan memadai | 3:12, 4:11, 5:5 | 2:2, 3:29, 4:27, 5:12 |
| 5 | TV/LCD mendukung | 1:2, 2:2, 3:9, 4:11, 5:4 | 1:6, 2:9, 3:18, 4:28, 5:9 |
| 6 | Laboratorium memadai | 2:3, 3:4, 4:16, 5:5 | 2:3, 3:20, 4:30, 5:17 |
| 7 | Akses internet/WiFi | 3:11, 4:13, 5:4 | 2:5, 3:24, 4:25, 5:16 |
| 8 | Kebersihan ruang kelas | 2:1, 3:8, 4:10, 5:9 | 2:1, 3:21, 4:26, 5:22 |
| 9 | Kebersihan toilet | 2:1, 3:13, 4:9, 5:5 | 1:4, 2:10, 3:25, 4:21, 5:10 |
| 10 | Perpustakaan nyaman | 2:1, 3:5, 4:15, 5:7 | 2:1, 3:17, 4:33, 5:19 |
| 11 | Area parkir aman | 3:5, 4:14, 5:9 | 1:1, 2:3, 3:18, 4:26, 5:22 |
| 12 | Kepuasan fasilitas FMIPA | 3:7, 4:17, 5:4 | 3:25, 4:28, 5:17 |

---

### Tabel Perbandingan Persentase

| No | Indikator | 28 Responden (%) | 70 Responden (%) |
|---|---|---|---|
| 1 | Ruang kelas nyaman | 1:3.57, 2:3.57, 3:32.14, 4:50.00, 5:10.71 | 1:1.43, 2:4.29, 3:31.43, 4:44.29, 5:18.57 |
| 2 | Meja & kursi layak | 3:32.14, 4:53.57, 5:14.29 | 2:2.86, 3:27.14, 4:45.71, 5:24.29 |
| 3 | AC/Kipas berfungsi | 1:3.57, 2:32.14, 3:42.86, 4:17.86, 5:3.57 | 1:8.57, 2:27.14, 3:32.86, 4:22.86, 5:8.57 |
| 4 | Pencahayaan memadai | 3:42.86, 4:39.29, 5:17.86 | 2:2.86, 3:41.43, 4:38.57, 5:17.14 |
| 5 | TV/LCD mendukung | 1:7.14, 2:7.14, 3:32.14, 4:39.29, 5:14.29 | 1:8.57, 2:12.86, 3:25.71, 4:40.00, 5:12.86 |
| 6 | Laboratorium memadai | 2:10.71, 3:14.29, 4:57.14, 5:17.86 | 2:4.29, 3:28.57, 4:42.86, 5:24.29 |
| 7 | Akses internet/WiFi | 3:39.29, 4:46.43, 5:14.29 | 2:7.14, 3:34.29, 4:35.71, 5:22.86 |
| 8 | Kebersihan ruang kelas | 2:3.57, 3:28.57, 4:35.71, 5:32.14 | 2:1.43, 3:30.00, 4:37.14, 5:31.43 |
| 9 | Kebersihan toilet | 2:3.57, 3:46.43, 4:32.14, 5:17.86 | 1:5.71, 2:14.29, 3:35.71, 4:30.00, 5:14.29 |
| 10 | Perpustakaan nyaman | 2:3.57, 3:17.86, 4:53.57, 5:25.00 | 2:1.43, 3:24.29, 4:47.14, 5:27.14 |
| 11 | Area parkir aman | 3:17.86, 4:50.00, 5:32.14 | 1:1.43, 2:4.29, 3:25.71, 4:37.14, 5:31.43 |
| 12 | Kepuasan fasilitas FMIPA | 3:25.00, 4:60.71, 5:14.29 | 3:35.71, 4:40.00, 5:24.29 |

---

Berdasarkan hasil perbandingan frekuensi dan persentase pada 28 responden dan 70 responden, mayoritas mahasiswa pada kedua penelitian memberikan jawaban pada kategori puas dan sangat puas terhadap sebagian besar fasilitas Fakultas MIPA Universitas Mataram. Pada indikator ruang kelas nyaman, meja dan kursi layak, laboratorium, perpustakaan, serta area parkir, kedua data menunjukkan dominasi jawaban pada kategori puas. Namun, pada data 70 responden distribusi jawaban terlihat lebih beragam karena jumlah responden yang lebih banyak mampu menggambarkan penilaian mahasiswa secara lebih representatif. Indikator kebersihan ruang kelas memperoleh tingkat kepuasan yang cukup tinggi pada kedua penelitian. Pada data 28 responden, kategori sangat puas sebesar 32.14%, sedangkan pada data 70 responden sebesar 31.43%. Hal ini menunjukkan bahwa mahasiswa menilai kebersihan ruang kelas sudah cukup baik dan konsisten pada kedua penelitian. Sementara itu, indikator AC/kipas angin dan kebersihan toilet masih memperoleh cukup banyak jawaban netral dan tidak puas baik pada data 28 responden maupun 70 responden. Hal ini menunjukkan bahwa kedua fasilitas tersebut masih perlu ditingkatkan agar dapat meningkatkan kenyamanan mahasiswa dalam proses pembelajaran. Secara umum, penambahan jumlah responden dari 28 menjadi 70 responden menghasilkan distribusi data yang lebih stabil, lebih representatif, dan lebih mampu menggambarkan kondisi sebenarnya mengenai tingkat kepuasan mahasiswa terhadap fasilitas Fakultas MIPA Universitas Mataram.

# Kesimpulan

Berdasarkan hasil penelitian, mahasiswa Program Studi Statistika Fakultas MIPA Universitas Mataram secara umum merasa puas terhadap fasilitas yang tersedia. Hal ini terlihat dari mayoritas jawaban responden yang berada pada kategori puas dan sangat puas. Hasil uji validitas menunjukkan seluruh item pertanyaan valid dengan nilai r hitung>0.30 dan nilai signifikansi <0.05. Hasil uji reliabilitas juga menunjukkan bahwa instrumen penelitian reliabel dengan nilai Cronbach’s Alpha sebesar 0.848. Berdasarkan perbandingan antara 28 responden dan 70 responden, penambahan jumlah responden memberikan hasil penelitian yang lebih baik. Tingkat error menurun dari sekitar 17% menjadi 10%, sehingga data penelitian menjadi lebih representatif dan lebih akurat. Selain itu, item yang sebelumnya tidak valid pada data 28 responden menjadi valid pada data 70 responden, serta nilai reliabilitas meningkat dari 0.772 menjadi 0.848. Secara umum, fasilitas FMIPA Universitas Mataram sudah dinilai cukup baik oleh mahasiswa, meskipun fasilitas AC/kipas angin dan kebersihan toilet masih perlu ditingkatkan.


## LINK KUISIONER
https://forms.gle/HpB1WEGRwGU1p47b6
