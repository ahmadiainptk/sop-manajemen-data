# Pedoman Manajemen Data IAIN Pontianak

> Buku pedoman resmi tata kelola data Institut Agama Islam Negeri (IAIN) Pontianak — mulai dari kelembagaan, standar arsitektur, siklus hidup data, hingga integrasi, keamanan, dan privasi.

Repositori ini mendokumentasikan pedoman manajemen data IAIN Pontianak secara terbuka agar dapat dipelajari, direplikasi, dan diaudit oleh sivitas akademika serta pemangku kepentingan. Pusat Teknologi Informasi dan Data (PTID) bertindak sebagai **Walidata Institusi** yang menjamin integritas data melalui prinsip *Satu Sumber Kebenaran* (*Single Source of Truth*).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE) [![Docs](https://img.shields.io/badge/dokumen-29_file-blue.svg)](#-indeks-dokumen) [![Release v1.0](https://img.shields.io/badge/release-v1.0-success.svg)](../../releases/tag/v1.0)

## Daftar Isi

1. [Tentang Pedoman](#-tentang-pedoman)
2. [Prinsip Utama](#-prinsip-utama)
3. [Indeks Dokumen](#-indeks-dokumen)
   - Bab 1 s.d. Bab 8 + Lampiran
4. [Struktur Repositori](#-struktur-repositori)
5. [Berkontribusi](#-berkontribusi)
6. [Lisensi](#-lisensi)

## 📌 Tentang Pedoman

Pedoman ini diterbitkan untuk menjawab tantangan umum tata kelola data perguruan tinggi, antara lain:

- **Silo data** — setiap unit kerja mengelola data sendiri tanpa standar bersama.
- **Redundansi & inkonsistensi** — data yang sama dientri berulang di banyak sistem.
- **Keamanan & privasi** — belum ada klasifikasi dan standar perlindungan data pribadi.
- **Kebutuhan pelaporan nasional** — PDDIKTI, EMIS, dan kebutuhan analitik internal.

Sasaran akhir: ekosistem *Data-Driven Decision Making* yang transparan, akuntabel, dan berbasis kinerja.

## 🎯 Prinsip Utama

| Prinsip | Penjelasan Singkat |
| --- | --- |
| **Satu Sumber Kebenaran** | Setiap entitas data memiliki satu sumber otoritatif yang dikelola Walidata. |
| **Peran Kelembagaan Jelas** | Pembina · Walidata · Produsen · Pengguna — masing-masing punya hak & kewajiban. |
| **Standar & Metadata** | Tipe data, format, kamus data, dan kode referensi mengikuti standar institusional. |
| **Siklus Hidup Data Tertutup** | Perencanaan → Kumpulkan → Validasi → Simpan → Analisis → Diseminasikan. |
| **Integrasi via API** | Interkoneksi aplikasi wajib lewat API Gateway; *direct DB access* dilarang. |
| **Keamanan Berlapis** | Klasifikasi data + SSO + RBAC + kepatuhan UU PDP. |

## 📚 Indeks Dokumen

Seluruh dokumen tersusun dalam **8 bab** ditambah **Lampiran** materi praktikum. Total ada **29 file Markdown** dalam repositori ini.

### Bab 1. Pendahuluan

_Latar belakang, maksud & tujuan, ruang lingkup, dan dasar hukum pedoman manajemen data IAIN Pontianak._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`01-pendahuluan/01-latar-belakang.md`](./01-pendahuluan/01-latar-belakang.md) | Manajemen data yang efektif merupakan fondasi utama dalam penyelenggaraan tata kelola perguruan tinggi yang transparan, akuntabel, dan berbasis kinerja. Di lingkungan Institut Agama Islam Negeri (I... |
| 02 | [`01-pendahuluan/02-maksud-tujuan.md`](./01-pendahuluan/02-maksud-tujuan.md) | Buku Pedoman Manajemen Data ini disusun dengan maksud untuk memberikan acuan baku, terstruktur, dan komprehensif bagi seluruh komponen sivitas akademika dan unit kerja di lingkungan IAIN Pontianak.... |
| 03 | [`01-pendahuluan/03-ruang-lingkup.md`](./01-pendahuluan/03-ruang-lingkup.md) | Buku Pedoman Manajemen Data IAIN Pontianak mencakup seluruh siklus hidup data yang berada di bawah kewenangan institusi, baik data yang bersifat publik maupun yang bersifat rahasia/terbatas. Ruang... |
| 04 | [`01-pendahuluan/04-dasar-hukum.md`](./01-pendahuluan/04-dasar-hukum.md) | Penyelenggaraan tata kelola data di IAIN Pontianak dilandasi oleh peraturan perundang-undangan nasional, kebijakan kementerian, serta peraturan internal institusi. Regulasi yang menjadi dasar penyu... |

### Bab 2. Tata Kelola & Kelembagaan

_Pembagian peran kelembagaan: Pembina Data, Walidata Institusi, Produsen Data, dan Pengguna Data._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`02-tata-kelola-kelembagaan/01-pembina-data.md`](./02-tata-kelola-kelembagaan/01-pembina-data.md) | Struktur tertinggi dalam tata kelola data di IAIN Pontianak berada pada tingkat pimpinan institusi, yang dipegang oleh Rektor beserta jajaran Wakil Rektor. Rektor bertindak sebagai **Pembina Data**. |
| 02 | [`02-tata-kelola-kelembagaan/02-walidata-institusi.md`](./02-tata-kelola-kelembagaan/02-walidata-institusi.md) | Pusat Teknologi Informasi dan Data (PTID) ditetapkan sebagai **Walidata Institusi** di IAIN Pontianak. PTID memiliki otoritas penuh dan tanggung jawab operasional teknis dalam manajemen siklus hidu... |
| 03 | [`02-tata-kelola-kelembagaan/03-produsen-data.md`](./02-tata-kelola-kelembagaan/03-produsen-data.md) | 1. **Pengumpulan Data Valid:** Bertanggung jawab penuh atas akurasi, validitas, dan kebaruan (kemutakhiran) data yang diinput ke dalam sistem operasional masing-masing. |
| 04 | [`02-tata-kelola-kelembagaan/04-pengguna-data.md`](./02-tata-kelola-kelembagaan/04-pengguna-data.md) | 1. **Prinsip *Need-to-Know*:** Hak akses hanya diberikan sejauh yang dibutuhkan oleh pengguna untuk menjalankan tugas fungsi atau kepentingan pendidikannya. |

### Bab 3. Standar & Arsitektur Data

_Prinsip Satu Data, standar data, metadata & kamus data, serta master data & kode referensi._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`03-standar-arsitektur/01-prinsip-satu-data.md`](./03-standar-arsitektur/01-prinsip-satu-data.md) | Mengadopsi semangat regulasi Satu Data Indonesia, IAIN Pontianak menerapkan prinsip **"Satu Sumber Kebenaran" (*Single Source of Truth* / SSOT)** sebagai fondasi utama tata kelola sistem informasinya. |
| 02 | [`03-standar-arsitektur/02-standar-data.md`](./03-standar-arsitektur/02-standar-data.md) | Untuk memastikan seluruh aplikasi di IAIN Pontianak dapat saling bertukar informasi secara lancar tanpa terjadi kesalahan *parsing* atau ketidakcocokan format, PTID wajib menetapkan **Standar Data... |
| 03 | [`03-standar-arsitektur/03-metadata-kamus.md`](./03-standar-arsitektur/03-metadata-kamus.md) | Untuk mempermudah pemahaman antar pengembang sistem serta untuk menghindari ambiguasi arti dari setiap kolom pangkalan data, Walidata (PTID) bertanggung jawab untuk menyusun, menerbitkan, dan memut... |
| 04 | [`03-standar-arsitektur/04-master-data-kode-referensi.md`](./03-standar-arsitektur/04-master-data-kode-referensi.md) | Selain definisi tabel dan kolom, komponen kritis lainnya untuk menjamin keterhubungan (*linkage*) antar sistem adalah penggunaan referensi data yang sama. Walidata wajib mengelola repositori **Kode... |

### Bab 4. Siklus Hidup Data

_Perencanaan & pengumpulan, pemeriksaan & validasi, penyimpanan & pemeliharaan, analisis & visualisasi, diseminasi & publikasi._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`04-siklus-hidup-data/01-perencanaan-pengumpulan.md`](./04-siklus-hidup-data/01-perencanaan-pengumpulan.md) | Siklus hidup data diawali dengan perencanaan kebutuhan dan proses pengumpulan data dari lapangan ke dalam sistem basis data. |
| 02 | [`04-siklus-hidup-data/02-pemeriksaan-validasi.md`](./04-siklus-hidup-data/02-pemeriksaan-validasi.md) | Sebelum data mentah disajikan sebagai Laporan Resmi Institusi atau disinkronisasikan ke Pangkalan Data Eksternal (PDDIKTI/EMIS), proses kontrol kualitas data (*Data Quality Assurance*) mutlak diper... |
| 03 | [`04-siklus-hidup-data/03-penyimpanan-pemeliharaan.md`](./04-siklus-hidup-data/03-penyimpanan-pemeliharaan.md) | Fase pasca-validasi menginstruksikan bagaimana data disimpan, dikelola, dan dipertahankan dalam infrastruktur internal agar keutuhan dan performa layanan tetap terjaga. |
| 04 | [`04-siklus-hidup-data/04-analisis-visualisasi.md`](./04-siklus-hidup-data/04-analisis-visualisasi.md) | Puncak dari tata kelola data yang baik adalah kemampuannya untuk dianalisis dan divisualisasikan guna mendukung *Data-Driven Decision Making* bagi para pimpinan di IAIN Pontianak. |
| 05 | [`04-siklus-hidup-data/05-diseminasi-publikasi.md`](./04-siklus-hidup-data/05-diseminasi-publikasi.md) | Diseminasi data merupakan proses penyebarluasan informasi yang telah divalidasi kepada publik, sivitas akademika, atau pihak ketiga sesuai dengan tingkat klasifikasi keamanannya. |

### Bab 5. Integrasi & Interoperabilitas

_Arsitektur integrasi API, sinkronisasi nasional, dan pedoman pengembang internal._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`05-integrasi-interoperabilitas/01-arsitektur-integrasi-api.md`](./05-integrasi-interoperabilitas/01-arsitektur-integrasi-api.md) | Pilar paling teknis dari perwujudan Satu Data di IAIN Pontianak adalah penghentian praktik integrasi *point-to-point* (akses basis data langsung antar aplikasi) dan beralih sepenuhnya pada arsitekt... |
| 02 | [`05-integrasi-interoperabilitas/02-sinkronisasi-nasional.md`](./05-integrasi-interoperabilitas/02-sinkronisasi-nasional.md) | Perguruan tinggi memiliki kewajiban reguler untuk melaporkan dinamika kegiatan akademik ke pangkalan data eksternal kementerian. Di IAIN Pontianak, kewajiban ini utamanya ditujukan kepada Pangkalan... |
| 03 | [`05-integrasi-interoperabilitas/03-pedoman-pengembang-internal.md`](./05-integrasi-interoperabilitas/03-pedoman-pengembang-internal.md) | Untuk menjaga kesinambungan ekosistem pengembangan perangkat lunak kampus, seluruh staf *programmer* PTID dan tim IT fakultas diikat oleh pedoman standar tata kelola pengembangan sistem. |

### Bab 6. Keamanan, Privasi & Akses

_Klasifikasi keamanan, hak akses & autentikasi, perlindungan data pribadi, mitigasi & disaster recovery._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`06-keamanan-privasi-akses/01-klasifikasi-keamanan.md`](./06-keamanan-privasi-akses/01-klasifikasi-keamanan.md) | Aset informasi IAIN Pontianak perlu diklasifikasikan guna menentukan standar perlindungan dan pembatasan hak akses yang sesuai. |
| 02 | [`06-keamanan-privasi-akses/02-hak-akses-autentikasi.md`](./06-keamanan-privasi-akses/02-hak-akses-autentikasi.md) | Pengelolaan identitas digital merupakan garis pertahanan pertama dalam mengamankan sistem informasi di IAIN Pontianak. |
| 03 | [`06-keamanan-privasi-akses/03-perlindungan-data-pribadi.md`](./06-keamanan-privasi-akses/03-perlindungan-data-pribadi.md) | Dalam mematuhi Undang-Undang Perlindungan Data Pribadi (UU PDP), IAIN Pontianak berkomitmen penuh melindungi privasi data sivitas akademika, alumni, maupun calon pendaftar. |
| 04 | [`06-keamanan-privasi-akses/04-mitigasi-disaster-recovery.md`](./06-keamanan-privasi-akses/04-mitigasi-disaster-recovery.md) | Untuk meminimalkan waktu henti layanan (*downtime*) dan mencegah hilangnya aset informasi akibat bencana alam, kegagalan perangkat keras, atau serangan siber (seperti *ransomware*), PTID diwajibkan... |

### Bab 7. Penutup

_Kesimpulan & pemberlakuan, serta sanksi & ketentuan peralihan._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`07-penutup/01-kesimpulan-pemberlakuan.md`](./07-penutup/01-kesimpulan-pemberlakuan.md) | Buku Pedoman Manajemen Data IAIN Pontianak ini merupakan dokumen normatif tertinggi di tingkat institusi yang mengatur siklus hidup, standar arsitektur, dan perlindungan keamanan data. Kesuksesan p... |
| 02 | [`07-penutup/02-sanksi-ketentuan-peralihan.md`](./07-penutup/02-sanksi-ketentuan-peralihan.md) | Guna menjamin kepastian berjalannya SOP dan Standar Data ini, perlu diatur ketentuan masa transisi untuk sistem-sistem yang sudah ada sebelumnya (*legacy systems*), beserta mekanisme penegakan aturan. |

### Bab 8. Lampiran

_Silabus praktikum, rencana pembelajaran & tugas, serta template tugas praktikum._

| # | Dokumen | Ringkasan |
| ---: | --- | --- |
| 01 | [`08-lampiran/01-silabus-praktikum-manajemen-data.md`](./08-lampiran/01-silabus-praktikum-manajemen-data.md) | Mengingat Buku Pedoman Manajemen Data IAIN Pontianak ini memiliki substansi teoritis dan teknis yang padat, buku ini sangat ideal untuk diadaptasi menjadi bahan ajar (Silabus Praktikum) untuk mata... |
| 02 | [`08-lampiran/02-rencana-pembelajaran-dan-tugas.md`](./08-lampiran/02-rencana-pembelajaran-dan-tugas.md) | Dokumen ini merupakan turunan operasional dari Silabus Praktikum Manajemen Data. Di dalamnya memuat panduan langkah pengajaran (*Lesson Plan*) bagi dosen/instruktur, serta contoh bentuk serahan (*d... |
| 03 | [`08-lampiran/03-template-tugas-praktikum.md`](./08-lampiran/03-template-tugas-praktikum.md) | Dokumen ini berisi standar kerangka kerja (*template*) yang harus diikuti oleh mahasiswa saat mengumpulkan hasil tugas praktikum agar format penyerahan (*deliverables*) menjadi seragam dan mudah di... |

> 📁 Struktur folder lengkap dengan deskripsi tiap file tersedia di [`Struktur.md`](./Strruktur.md).

## 🗂 Struktur Repositori

```
.
├── README.md                # Indeks utama (file ini)
├── Struktur.md              # Pemetaan folder & file + deskripsi detil
├── LICENSE                  # Lisensi MIT
├── .gitignore
├── 01-pendahuluan/          # Bab 1
├── 02-tata-kelola-kelembagaan/   # Bab 2
├── 03-standar-arsitektur/        # Bab 3
├── 04-siklus-hidup-data/          # Bab 4
├── 05-integrasi-interoperabilitas/   # Bab 5
├── 06-keamanan-privasi-akses/    # Bab 6
├── 07-penutup/                   # Bab 7
└── 08-lampiran/                  # Lampiran
```

## 🤝 Berkontribusi

Pedoman ini adalah dokumen hidup. Kontribusi dapat berupa:

- **Laporan koreksi** — buka *Issue* untuk提出 koreksi atau klarifikasi.
- **Perbaikan kecil** — *Pull Request* langsung untuk typo, tautan rusak, atau perbaikan redaksional.
- **Perubahan substansial** — diskusikan dulu via *Issue* agar ada konsensus sebelum di-*merge*.

### Alur Kontribusi Singkat

```bash
# 1. Fork & clone
git clone git@github.com:<user>/sop-manajemen-data.git
cd sop-manajemen-data

# 2. Buat branch
git checkout -b perbaiki/bab-3-standar-data

# 3. Edit & commit
git commit -am "perbaiki(standar-data): jelaskan konvensi penamaan entitas"

# 4. Push & buka PR
git push origin perbaiki/bab-3-standar-data
```

## ⚖ Lisensi

Repositori ini dilisensikan di bawah **MIT License** — lihat [`LICENSE`](./LICENSE) untuk detail lengkap.

---

**Pemilik:** IAIN Pontianak · **Walidata:** Pusat Teknologi Informasi dan Data (PTID) · **Versi Dokumen:** 1.0 · **Terakhir diperbarui:** 2026