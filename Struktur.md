# Struktur Dokumen: Pedoman Manajemen Data IAIN Pontianak

Dokumen ini menjelaskan struktur repositori dan tata letak file untuk penyusunan Buku Pedoman Manajemen Data IAIN Pontianak. Setiap bab direpresentasikan oleh folder, dan setiap sub-bab dipecah menjadi file Markdown (`.md`) yang berurutan untuk memudahkan proses penulisan menggunakan AI Agent.


```

```text
File Struktur.md berhasil dibuat.

```text
.
├── Struktur.md (File Ini)
├── 01-pendahuluan/
│   ├── 01-latar-belakang.md
│   ├── 02-maksud-tujuan.md
│   ├── 03-ruang-lingkup.md
│   └── 04-dasar-hukum.md
├── 02-tata-kelola-kelembagaan/
│   ├── 01-pembina-data.md
│   ├── 02-walidata-institusi.md
│   ├── 03-produsen-data.md
│   └── 04-pengguna-data.md
├── 03-standar-arsitektur/
│   ├── 01-prinsip-satu-data.md
│   ├── 02-standar-data.md
│   ├── 03-metadata-kamus.md
│   └── 04-master-data-kode-referensi.md
├── 04-siklus-hidup-data/
│   ├── 01-perencanaan-pengumpulan.md
│   ├── 02-pemeriksaan-validasi.md
│   ├── 03-penyimpanan-pemeliharaan.md
│   ├── 04-analisis-visualisasi.md
│   └── 05-diseminasi-publikasi.md
├── 05-integrasi-interoperabilitas/
│   ├── 01-arsitektur-integrasi-api.md
│   ├── 02-sinkronisasi-nasional.md
│   └── 03-pedoman-pengembang-internal.md
├── 06-keamanan-privasi-akses/
│   ├── 01-klasifikasi-keamanan.md
│   ├── 02-hak-akses-autentikasi.md
│   ├── 03-perlindungan-data-pribadi.md
│   └── 04-mitigasi-disaster-recovery.md
├── 07-penutup/
│   ├── 01-kesimpulan-pemberlakuan.md
│   └── 02-sanksi-ketentuan-peralihan.md
└── 08-lampiran/
    ├── 01-silabus-praktikum-manajemen-data.md
    ├── 02-rencana-pembelajaran-dan-tugas.md
    └── 03-template-tugas-praktikum.md

```

---

## Deskripsi Detil File

### 01-pendahuluan/

* `01-latar-belakang.md`: Urgensi tata kelola data di PTKIN, masalah silo data, redundansi, dan pentingnya pengambilan keputusan berbasis data (Data-Driven Decision Making).
* `02-maksud-tujuan.md`: Menetapkan arah panduan umum bagi seluruh unit kerja di lingkungan IAIN Pontianak.
* `03-ruang-lingkup.md`: Batasan data yang dikelola (Akademik, Kemahasiswaan, Kepegawaian, Keuangan, Aset, Penelitian, Pengabdian Masyarakat).
* `04-dasar-hukum.md`: Kumpulan regulasi makro (UU RI, PMA) hingga mikro (SK Rektor IAIN Pontianak).

### 02-tata-kelola-kelembagaan/

* `01-pembina-data.md`: Peran Rektor dan unsur pimpinan dalam menetapkan kebijakan arah strategis data.
* `02-walidata-institusi.md`: Peran sentral Pusat Teknologi Informasi dan Data (PTID) sebagai pengelola teknis, agregator, verifikator, dan pusat integrasi data.
* `03-produsen-data.md`: Hak dan kewajiban unit kerja penghasil data asli (Fakultas, Pascasarjana, Bagian Administrasi, LP2M, LPM, UPT).
* `04-pengguna-data.md`: Aturan akses bagi sivitas akademika maupun pihak luar yang memerlukan konsumsi data.

### 03-standar-arsitektur/

* `01-prinsip-satu-data.md`: Adopsi semangat Satu Data Indonesia ke dalam tata kelola internal kampus (Satu Sumber Kebenaran / Single Source of Truth).
* `02-standar-data.md`: Aturan penulisan, tipe data, format baku, dan konvensi penamaan entitas data di lingkungan kampus.
* `03-metadata-kamus.md`: Panduan penyusunan kamus data struktur organisasi, variabel, definisi operasional, dan tipe data dari setiap tabel database.
* `04-master-data-kode-referensi.md`: Standarisasi pengkodean esensial (NIM, NIP, Kode Prodi, Kode Mata Kuliah, Kode Ruangan).

### 04-siklus-hidup-data/

* `01-perencanaan-pengumpulan.md`: Prosedur perencanaan kebutuhan data tahunan dan metode pengumpulan data (melalui aplikasi operasional/form resmi).
* `02-pemeriksaan-validasi.md`: Proses pembersihan data (data cleansing), penanganan anomali, serta validasi kualitas data oleh Walidata sebelum dipublikasikan.
* `03-penyimpanan-pemeliharaan.md`: Tata cara penyimpanan data terpusat, manajemen basis data (DBMS), dan masa retensi/pengarsipan data historis.
* `04-analisis-visualisasi.md`: Standardisasi pembuatan dashboard eksekutif, laporan statistik periodik, dan analisis tren perkembangan institusi.
* `05-diseminasi-publikasi.md`: Aturan penyebaran data formal melalui portal data institusi resmi.

### 05-integrasi-interoperabilitas/

* `01-arsitektur-integrasi-api.md`: Standardisasi interkoneksi antaraplikasi menggunakan RESTful API/GraphQL terpusat, melarang direct database access lintas aplikasi pihak ketiga.
* `02-sinkronisasi-nasional.md`: Mekanisme otomatisasi dan penjadwalan sinkronisasi data dengan pangkalan data eksternal (PDDIKTI Kementerian Pendidikan dan EMIS Kementerian Agama).
* `03-pedoman-pengembang-internal.md`: Aturan bagi tim pengembang aplikasi internal (in-house) agar wajib menggunakan Master Data dan API Gateway yang disediakan Walidata.

### 06-keamanan-privasi-akses/

* `01-klasifikasi-keamanan.md`: Pengelompokan data berdasarkan sensitivitasnya: Data Publik (Dapat diakses umum), Data Terbatas (Internal institusi), Data Rahasia (Sangat sensitif/Keuangan/Pribadi).
* `02-hak-akses-autentikasi.md`: Implementasi Single Sign-On (SSO) sebagai pintu gerbang autentikasi tunggal dan Role-Based Access Control (RBAC) pada setiap aplikasi subdomain.
* `03-perlindungan-data-pribadi.md`: Penerapan UU Perlindungan Data Pribadi (UU PDP) terhadap data mahasiswa, dosen, tenaga kependidikan, alumni, dan pendaftar baru.
* `04-mitigasi-disaster-recovery.md`: Kebijakan automated backup (harian/mingguan), penyimpanan cadangan di infrastruktur cloud aman, serta standardisasi pemulihan data pasca-insiden (Disaster Recovery Plan).

### 07-penutup/

* `01-kesimpulan-pemberlakuan.md`: Pernyataan penutup, tanggal mulai berlakunya pedoman, dan sifat keterikatan pedoman bagi seluruh unit kerja.
* `02-sanksi-ketentuan-peralihan.md`: Mekanisme penegakan aturan terhadap pelanggaran prosedur manajemen data dan masa transisi sistem lama ke sistem baru.

### 08-lampiran/

* `01-silabus-praktikum-manajemen-data.md`: Modul implementasi setara 24 pertemuan praktikum (Mencakup Excel, Python, Google Colab, AI, Scraping, API, dan Visualisasi Looker Studio) yang dapat digunakan dosen untuk mata kuliah Manajemen Data.
* `02-rencana-pembelajaran-dan-tugas.md`: Penjelasan langkah demi langkah pedagogi di kelas beserta contoh konkret *deliverables* (hasil tugas) yang harus diselesaikan oleh mahasiswa pada setiap modul.
* `03-template-tugas-praktikum.md`: Kerangka kerja baku (*template*) yang mengatur format penyerahan tugas (seperti kerangka Excel, susunan kode Colab, dan kerangka artikel publikasi).