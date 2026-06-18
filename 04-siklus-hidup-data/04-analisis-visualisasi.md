# Analisis dan Visualisasi Data

Puncak dari tata kelola data yang baik adalah kemampuannya untuk dianalisis dan divisualisasikan guna mendukung *Data-Driven Decision Making* bagi para pimpinan di IAIN Pontianak.

## Standardisasi Dashboard dan Pelaporan:
1. **Executive Dashboard Terpusat:** PTID memfasilitasi pembuatan *Dashboard Eksekutif* yang merangkum indikator kinerja utama (*Key Performance Indicators* / KPI) institut, seperti persentase kelulusan tepat waktu, serapan anggaran, dan sebaran jabatan fungsional dosen.
2. **Kesesuaian Sumber Data:** Seluruh laporan statistik dan visualisasi grafik yang ditampilkan pada presentasi resmi institut wajib bersumber dari tarikan data (query) langsung dari *Master Data*, bukan dari kompilasi *spreadsheet* manual yang berpotensi memiliki bias atau *human error*.
3. **Analitik Lanjut (Advanced Analytics):** Untuk keperluan akreditasi atau pemeringkatan institusi, PTID bersama Pusat Jaminan Mutu (LPM) dapat mengolah data mentah menjadi data tren prediktif (misal: memprediksi potensi mahasiswa *Drop Out* berdasarkan tren nilai akademik dan keaktifan).

## Siklus Kerja Pengolahan Data Proyek (Ad-Hoc / Bulanan)

Selain otomasi melalui sistem *dashboard* terpusat, unit kerja atau tim spesialis data sering kali dihadapkan pada permintaan analisis tak terstruktur (proyek ad-hoc bulanan). Untuk menjaga standar kualitas, siklus kerja proyek data ad-hoc harus mengikuti alur berikut:

1. **Perencanaan dan Pembahasan Proyek:** Pada awal periode (awal bulan), tim melakukan evaluasi terkait permasalahan data yang ada atau menentukan target proyek kerja pendataan yang akan dieksekusi selama satu bulan ke depan berdasarkan arahan pimpinan.
2. **Pengumpulan Data Mentah:** Mulai melakukan ekstraksi dan kompilasi data (*data gathering*) dari berbagai sumber yang relevan untuk proyek tersebut, memastikan sumber data akurat dan sesuai dengan instruksi.
3. **Pembersihan Data Dasar (*Data Cleansing*):** Mengolah data awal dengan melakukan pemilahan yang ketat. Tim wajib mengidentifikasi dan menghapus data ganda (*duplicate data*), serta menindaklanjuti atau memfilter data yang kosong (*missing values*) agar tidak merusak perhitungan statistik.
4. **Standardisasi Format Data:** Merapikan bentuk dan format data (misalnya menyeragamkan penulisan tanggal, memperbaiki kapitalisasi teks, dan memastikan kolom identitas NIK/NIM berformat teks yang seragam) sesuai standar arahan yang berlaku.
5. **Analisis Deskriptif (Pengolahan Rumus Excel/Spreadsheet):** Melakukan komputasi dan analisis menggunakan rumus-rumus bawaan pengolah angka (seperti Excel/Google Sheets) untuk mencari nilai rata-rata (*average*), jumlah agregat (*sum*), tren, atau perhitungan lain yang diinstruksikan oleh pimpinan. Hal ini diperkenankan khusus untuk analisis proyek terisolasi di luar *dashboard* utama.
6. **Perancangan Keluaran (Output Design):** Membuat rancangan konseptual mengenai peruntukan akhir dari data yang telah diolah tersebut. Tim harus memperjelas kepada siapa hasil data ini akan dilaporkan, apakah akan divisualisasikan dalam bentuk grafik presentasi, dicetak menjadi laporan kebijakan, atau didistribusikan ke unit kerja lain.

## Panduan Analitik Lanjutan (Bagi Data Expert / Peneliti)

Untuk kebutuhan analitik data berskala besar (*Big Data*), penelitian akademis mendalam, atau otomatisasi laporan kompleks yang melampaui batas kemampuan *spreadsheet* biasa, para *Data Analyst*, Ahli IT, dan Peneliti di lingkungan institusi sangat dianjurkan untuk memanfaatkan perkakas analitik modern:

### 1. Pemanfaatan Bahasa Pemrograman Python
- **Automasi Pembersihan Data:** Alih-alih merapikan data secara manual, gunakan pustaka (*library*) Python seperti `pandas` dan `NumPy` untuk melakukan *data cleansing* (membuang data ganda, mengisi nilai kosong) secara massal dan otomatis.
- **Analisis Prediktif:** Gunakan Python untuk menjalankan algoritma *Machine Learning* (melalui pustaka `scikit-learn` atau `TensorFlow`) guna mencari korelasi data yang tersembunyi, seperti memprediksi tren kelulusan mahasiswa atau mengelompokkan karakteristik kinerja pegawai.

### 2. Penggunaan Google Colab (Colaboratory)
- **Komputasi Berbasis Cloud:** Peneliti tidak perlu memiliki komputer berspesifikasi tinggi. Gunakan *Google Colab* sebagai *Jupyter Notebook* virtual yang berjalan di server Google secara gratis untuk memproses kumpulan data kampus yang sangat besar.
- **Kolaborasi Aman:** Script Python di Colab dapat dibagikan dengan mudah ke sesama rekan peneliti atau dosen. **Peringatan Keamanan:** Saat mengunggah data institusi ke *Google Colab*, pastikan data tersebut telah di-anonimisasi (menghapus NIK, nama lengkap, atau informasi sensitif lainnya) untuk menjaga kepatuhan terhadap UU Pelindungan Data Pribadi (PDP).

### 3. Teknik *Lookup* dan Visualisasi Lanjutan (Google Looker Studio)
- **Integrasi *Lookup* Multi-Sumber:** Jika Anda menggunakan Google Sheets sebagai basis data proyek ad-hoc, manfaatkan fitur *Advanced Lookup* (seperti `VLOOKUP`, `INDEX MATCH`, atau `XLOOKUP`) untuk menggabungkan beberapa tabel secara presisi (misal: menyatukan tabel daftar hadir kegiatan dengan tabel master profil peserta).
- **Pembuatan *Dashboard* Interaktif:** Untuk perancangan keluaran (*Output Design*) yang profesional, sambungkan hasil olahan data (dari Python, API, atau Google Sheets) ke **Google Looker Studio (Data Studio)**. Aplikasi ini memungkinkan tim *expert* membuat *dashboard* visual interaktif yang dapat diperbarui secara *real-time* dan dibagikan melalui sebuah tautan (link) ke unsur pimpinan, tanpa harus mengirim ulang lampiran file secara berulang-ulang.

---

## Lampiran Teknis: Panduan Kerja "Statistisi Ahli Pertama" (Python, Scraping, & Integrasi AI)

Bagi aparatur dengan Jabatan Fungsional **Statistisi Ahli Pertama**, tuntutan kerja tidak lagi sebatas rekapitulasi manual, melainkan harus mampu menerapkan otomasi analitik, teknik pengumpulan data eksternal, dan adopsi Kecerdasan Buatan (AI) ke dalam alur kerja (*workflow*).

### 1. Integrasi AI ke dalam *Workflow* Statistisi
Sebagai Statistisi Ahli Pertama, AI (seperti ChatGPT, Google Gemini, atau GitHub Copilot) bukan difungsikan untuk menggantikan analisis, melainkan sebagai **Kopilot (Asisten Analitik)**:
- **AI untuk *Code Generation*:** Menulis *prompt* kepada AI untuk membuatkan *template script* Python/R yang kompleks, menulis ekspresi *Regex* (*Regular Expression*) untuk pembersihan teks, atau formula kueri *SQL* tingkat lanjut.
- **AI untuk Interpretasi Awal:** Memberikan ringkasan statistik deskriptif kepada AI untuk membantu membuat draf narasi kesimpulan atau tren sebelum diperhalus menjadi Laporan Kebijakan resmi pimpinan institusi.
- **Keamanan Data dengan AI:** **DILARANG KERAS** menyalin dan menempel (*copy-paste*) data mentah kampus yang mengandung informasi pribadi (NIK, nama mahasiswa, data finansial) ke dalam *prompt* aplikasi AI publik. Data harus di-anonimisasi terlebih dahulu.

### 2. Prinsip *Web Scraping* dan Analisis Otomatis
*Web Scraping* (pengekstrakan data dari *website*) adalah teknik lanjutan untuk memperkaya *dataset* institusi (misalnya membandingkan data akreditasi kampus lain dari portal publik).
- **Etika dan Legalitas:** *Scraping* hanya diperbolehkan pada domain publik (Open Data, web portal pemeringkatan seperti Webometrics/UniRank) yang mengizinkan *crawling*. Dilarang keras melakukan *scraping* pada sistem internal ber-SSO atau web eksternal yang melarang secara hukum di file `robots.txt` mereka.
- **Otomatisasi Pipa Data (*Data Pipeline*):** Script Python yang telah berhasil mengekstrak dan membersihkan data tidak boleh dijalankan manual selamanya. Statistisi harus membungkusnya dalam *cron jobs* (di Linux) atau penjadwal tugas berbasis *cloud* (seperti *Apache Airflow*) agar data analisis selalu *up-to-date* tanpa intervensi manusia.

### 3. Contoh Implementasi Sederhana: Python & Data Dummy
Berikut adalah simulasi *workflow* yang dapat dijalankan di **Google Colab** atau komputer lokal untuk mengidentifikasi rata-rata IPK dan mendeteksi mahasiswa yang berpotensi memiliki masalah akademik (*At-Risk Students*).

**A. Contoh Data Dummy (`mahasiswa_dummy.csv`):**
```csv
NIM,Program_Studi,Semester_Aktif,SKS_Lulus,IPK
10111,Pendidikan Agama Islam,4,80,3.75
10112,Pendidikan Agama Islam,4,45,2.10
10211,Ekonomi Syariah,6,110,3.50
10212,Ekonomi Syariah,6,75,1.95
10311,Hukum Keluarga,2,40,3.80
```

**B. Contoh *Script* Analisis (Python - Library Pandas):**
```python
import pandas as pd

# 1. Membaca data dari CSV
df = pd.read_csv('mahasiswa_dummy.csv')

# 2. Membersihkan Data (Data Cleansing)
# Menghapus baris yang memiliki nilai kosong (NaN) pada kolom esensial
df_clean = df.dropna(subset=['IPK', 'SKS_Lulus'])

# 3. Analisis Agregat (Rata-rata IPK per Program Studi)
print("--- Rata-rata IPK per Program Studi ---")
rata_rata_prodi = df_clean.groupby('Program_Studi')['IPK'].mean().round(2)
print(rata_rata_prodi)
print("\n")

# 4. Deteksi Anomali / Peringatan Dini (At-Risk Students)
# Kriteria: Mahasiswa semester >= 4 dengan IPK di bawah 2.50
kondisi_kritis = (df_clean['Semester_Aktif'] >= 4) & (df_clean['IPK'] < 2.50)
mahasiswa_kritis = df_clean[kondisi_kritis]

print("--- Daftar Mahasiswa Berpotensi Masalah Akademik (At-Risk) ---")
print(mahasiswa_kritis[['NIM', 'Program_Studi', 'IPK']])
```

Skrip di atas merupakan pondasi awal bagi seorang Statistisi Ahli Pertama untuk menggeser paradigma pelaporan kampus; dari sekadar tabel data mentah (*Excel rekap*) menjadi **Peringatan Dini Berbasis Data** (*Data-Driven Early Warning System*).
