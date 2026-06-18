# Panduan Akses dan Instalasi Perangkat Lunak Praktikum

Untuk menunjang kelancaran praktikum Manajemen Data, asisten laboratorium atau mahasiswa secara mandiri perlu menyiapkan lingkungan kerja (*environment*) pada komputer masing-masing. 

Berikut adalah panduan resmi berisi sumber unduhan resmi (*official link*) dan instruksi penyiapan aplikasi yang digunakan dalam kurikulum silabus.

---

## 1. Google Colab (*Python Cloud Environment*)
Google Colab (*Colaboratory*) adalah *Jupyter Notebook* gratis dari Google yang berjalan di *cloud*. **Aplikasi ini tidak perlu diunduh/diinstal.**
*   **Persyaratan:** *Web Browser* modern (Chrome/Edge) dan Akun Google (sangat disarankan menggunakan *email* institusi berakhiran `@iainptk.ac.id`).
*   **Tata Cara Akses:**
    1. Buka tautan resmi: [https://colab.research.google.com/](https://colab.research.google.com/)
    2. *Login* menggunakan Akun Google.
    3. Klik menu **File > New Notebook** untuk membuka lembar kerja Python kosong.
    4. Seluruh *library* utama untuk data (seperti `pandas`, `numpy`, `scikit-learn`) umumnya sudah terinstal (Pre-installed) di server Google Colab.

---

## 2. R dan RStudio (Analitik Statistik Offline)
Jika kelas praktikum (*Advanced Analytics*) diarahkan untuk dijalankan secara luring (*offline*) di lab komputer kampus, teknisi lab atau mahasiswa wajib menginstal **R** (mesin pengolah statistik) terlebih dahulu, baru disusul menginstal **RStudio** (antarmuka visualnya).

*   **Langkah 1: Instalasi Core R**
    1. Kunjungi situs resmi CRAN (*The Comprehensive R Archive Network*): [https://cran.r-project.org/](https://cran.r-project.org/)
    2. Klik tautan *Download* sesuai OS (Windows / macOS / Linux).
    3. Pilih tautan *"install R for the first time"* (versi *base*).
    4. Unduh dan jalankan *installer*, tekan *Next* hingga selesai dengan setelan *default*.
*   **Langkah 2: Instalasi IDE RStudio Desktop**
    1. Setelah R terinstal, kunjungi situs web Posit (Developer RStudio): [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)
    2. Unduh versi **RStudio Desktop (Free)**.
    3. Jalankan *installer* hingga selesai.
    4. Buka aplikasi RStudio dari menu program. Ia akan secara otomatis mendeteksi bahasa R yang diinstal di Langkah 1.

---

## 3. Spreadsheet Apps (Fungsi *Lookup* & *Data Cleansing*)
Digunakan secara ekstensif pada Modul II untuk pembersihan data mentah manual.
*   **Microsoft Excel:** Biasanya telah menjadi bawaan sistem (*Pre-installed*) pada sistem operasi Windows. Jika harus menggunakan Excel, pastikan menggunakan minimal **Excel 2016** atau Office 365 agar formula seperti `XLOOKUP` bisa berjalan tanpa gangguan.
*   **Google Sheets (Alternatif Cloud Gratis):** Tidak perlu instalasi. 
    1. Buka portal [https://sheets.google.com/](https://sheets.google.com/).
    2. Pilih *Blank Spreadsheet*.
    3. Semua formula standar seperti `VLOOKUP`, `INDEX`, dan `MATCH` tersedia penuh.

---

## 4. Google Looker Studio (Visualisasi & *Dashboard*)
Sebuah alat intelijen bisnis (*Business Intelligence Tool*) dari Google untuk mendesain grafik interaktif. **Aplikasi ini tidak perlu diinstal.**
*   **Tata Cara Akses:**
    1. Kunjungi portal web: [https://lookerstudio.google.com/](https://lookerstudio.google.com/)
    2. Masuk dengan Akun Google. **Sangat Penting:** Gunakan akun yang sama dengan akun yang digunakan untuk menyimpan dataset mahasiswa di *Google Drive/Sheets* agar izin sinkronisasi lebih mudah dilakukan.
    3. Klik **Create > Report** untuk memulai merancang *Dashboard*.

---

## 5. Postman (Pengujian Integrasi *API Gateway*)
Digunakan pada Modul IV untuk menyimulasikan diri sebagai vendor pihak ketiga yang mencoba menarik data dari *API Gateway* kampus.
*   **Sumber Unduhan:**
    1. Kunjungi situs web resmi: [https://www.postman.com/downloads/](https://www.postman.com/downloads/)
    2. Unduh versi *Desktop App* (Windows/Mac).
*   **Tata Cara Instalasi:**
    1. Klik ganda pada *file setup* `Postman-Setup.exe`.
    2. Instalasi berjalan otomatis. Saat muncul layar registrasi, mahasiswa diizinkan untuk melewati proses tersebut (*Skip and go to the app*) jika ingin langsung menggunakan antarmuka pemanggilan JSON tanpa membuat akun.
