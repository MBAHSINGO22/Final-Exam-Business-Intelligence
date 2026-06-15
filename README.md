# Data Cleaning dan Preprocessing Dataset Kemiskinan & Bantuan Sosial Jawa Timur

## Deskripsi Proyek

Proyek ini berfokus pada proses **Data Cleaning**, **Quality Assessment**, dan **Data Preprocessing** terhadap dataset indikator kemiskinan dan bantuan sosial di Provinsi Jawa Timur.

Dataset yang digunakan mencakup berbagai indikator sosial-ekonomi seperti Indeks Pembangunan Manusia (IPM), Tingkat Pengangguran Terbuka (TPT), jumlah penduduk miskin, garis kemiskinan, serta realisasi bantuan sosial pada berbagai kabupaten dan kota di Jawa Timur.

Tujuan utama proyek ini adalah menghasilkan dataset yang bersih, konsisten, dan siap digunakan untuk analisis data, visualisasi, Business Intelligence, maupun Machine Learning.

---

## Dataset

Dataset terdiri dari **234 observasi** dengan **14 atribut**, meliputi:

| Kolom                          | Deskripsi                          |
| ------------------------------ | ---------------------------------- |
| Kabupaten_Kota                 | Nama Kabupaten/Kota di Jawa Timur  |
| Tipe                           | Kategori wilayah                   |
| Tahun                          | Tahun pengamatan                   |
| IPM                            | Indeks Pembangunan Manusia         |
| Jumlah_Penduduk_Miskin_Ribu    | Jumlah penduduk miskin (ribu jiwa) |
| Rata_Rata_Lama_Sekolah         | Rata-rata lama sekolah             |
| TPT_Persen                     | Tingkat Pengangguran Terbuka (%)   |
| Garis_Kemiskinan_Maret_Rp      | Garis kemiskinan (Rp)              |
| Jml_Penduduk_Miskin_Maret_Ribu | Jumlah penduduk miskin bulan Maret |
| Persen_Penduduk_Miskin_Maret   | Persentase penduduk miskin         |
| Bansos_KPM_Rencana             | Rencana penerima bantuan sosial    |
| Bansos_KPM_Realisasi           | Realisasi penerima bantuan sosial  |
| Bansos_Anggaran_Rencana_Rp     | Rencana anggaran bantuan sosial    |
| Bansos_Anggaran_Realisasi_Rp   | Realisasi anggaran bantuan sosial  |

---

## Tujuan Proyek

* Melakukan audit kualitas data.
* Mengidentifikasi missing values.
* Mengidentifikasi outlier menggunakan metode IQR.
* Mendeteksi inkonsistensi data.
* Melakukan imputasi data yang hilang.
* Menangani outlier menggunakan Winsorization.
* Melakukan normalisasi data menggunakan Min-Max Scaling.
* Menghasilkan dataset siap analisis.

---

## Teknologi yang Digunakan

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* OpenPyXL
* Jupyter Notebook

---

## Tahapan Data Cleaning

### 1. Audit Kualitas Data

Pada tahap awal dilakukan pemeriksaan kualitas data untuk mengidentifikasi:

* Missing values
* Outlier
* Data duplikat
* Nilai yang tidak logis
* Inkonsistensi format

### 2. Penanganan Missing Values

Nilai yang hilang ditangani menggunakan metode:

**Median Imputation per Kabupaten/Kota**

Pendekatan ini dipilih untuk mempertahankan karakteristik masing-masing wilayah dan mengurangi bias akibat nilai ekstrem.

### 3. Penanganan Outlier

Outlier diidentifikasi menggunakan:

* Interquartile Range (IQR)

Kemudian dilakukan penanganan menggunakan:

* Winsorization (P5–P95)

Metode ini mempertahankan jumlah data tanpa menghapus observasi.

### 4. Normalisasi Data

Normalisasi dilakukan menggunakan:

**Min-Max Scaling**

Sehingga seluruh fitur numerik berada pada rentang 0–1.

### 5. Validasi Dataset

Setelah proses cleaning selesai dilakukan:

* Verifikasi missing values
* Pemeriksaan statistik deskriptif
* Validasi struktur dataset
* Ekspor dataset hasil cleaning

---

## Struktur Proyek

```text
Data_Cleaning_JawaTimur/
│
├── Data_Cleaning_JawaTimur.ipynb
├── Dataset_Jawa_Timur.xlsx
├── dataset_jawatimur_CLEANED.xlsx
├── dataset_jawatimur_NORMALIZED.xlsx
└── README.md
```

---

## Cara Menjalankan

### Clone Repository

```bash
git clone https://github.com/username/Data_Cleaning_JawaTimur.git
```

### Masuk ke Direktori

```bash
cd Data_Cleaning_JawaTimur
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy openpyxl
```

### Jalankan Notebook

```bash
jupyter notebook Data_Cleaning_JawaTimur.ipynb
```

atau menggunakan Google Colab.

---

## Output

Proyek menghasilkan dua dataset utama:

### Dataset Cleaning

```text
dataset_jawatimur_CLEANED.xlsx
```

Berisi data yang telah:

* Diimputasi
* Diperbaiki kualitasnya
* Ditangani outliernya

### Dataset Normalisasi

```text
dataset_jawatimur_NORMALIZED.xlsx
```

Berisi data yang telah melalui proses:

* Data Cleaning
* Min-Max Scaling

dan siap digunakan untuk:

* Machine Learning
* Clustering
* Classification
* Regression
* Business Intelligence

---

## Hasil yang Diharapkan

* Kualitas data meningkat.
* Tidak terdapat missing values.
* Outlier lebih terkendali.
* Data konsisten dan siap dianalisis.
* Dataset siap digunakan untuk penelitian dan pengembangan model Machine Learning.

---

## Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dilakukan:

* Dashboard Business Intelligence menggunakan Power BI
* Analisis tren kemiskinan Jawa Timur
* Clustering Kabupaten/Kota
* Prediksi tingkat kemiskinan
* Analisis efektivitas bantuan sosial
* Integrasi Machine Learning dan Data Mining

---

## Author

**Eugenius Kriswinar Adi Cahya**

Program Studi Informatika
