# Lampiran Khusus: Panduan Praktikum Manajemen Data (24 Pertemuan)

Mengingat Buku Pedoman Manajemen Data IAIN Pontianak ini memiliki substansi teoritis dan teknis yang padat, buku ini sangat ideal untuk diadaptasi menjadi bahan ajar (Silabus Praktikum) untuk mata kuliah **Manajemen Data** atau **Sistem Informasi Manajemen**.

Berikut adalah rancangan modul praktikum komprehensif sebanyak 24 kali pertemuan, yang menjembatani teori regulasi dengan praktik pengolahan data riil menggunakan Excel, Python, Google Colab, AI, hingga publikasi *Dashboard*.

---

## Modul I: Fondasi Tata Kelola dan Teori (Pertemuan 1 - 4)
Fokus pada pemahaman masalah institusional dan pencarian literatur regulasi.
* **Pertemuan 1-2: Studi Kasus *Silo Data* di Perguruan Tinggi.**
  - **Aktivitas:** Mahasiswa ditugaskan mencari teori terkait arsitektur *Single Source of Truth* (SSOT) dan mendiskusikan studi kasus kerugian institusi akibat inkonsistensi data antar unit.
* **Pertemuan 3-4: Pembuatan Kamus Data & Standar Data.**
  - **Aktivitas Praktikum:** Dosen memberikan *form* kertas kosong. Mahasiswa merancang **Kamus Data** institusi (menentukan tipe data, *primary key* NIM/NIP, dan format tanggal ISO) di dalam *spreadsheet*.

## Modul II: Pengumpulan & *Data Cleansing* (Pertemuan 5 - 8)
Fokus pada pengolahan data operasional manual menggunakan rumus.
* **Pertemuan 5-6: Simulasi Pengumpulan Data Berbasis Form.**
  - **Aktivitas Praktikum:** Membuat sistem *input* menggunakan Google Forms / Microsoft Forms dengan validasi *regex* (contoh: NIM wajib angka 10 digit).
* **Pertemuan 7-8: Praktikum *Data Cleansing* & *Advanced Lookup*.**
  - **Contoh Data Dummy:** Disediakan *file* Excel berisi 500 baris data mahasiswa yang berantakan (ada spasi ganda, huruf kapital berantakan, NIM duplikat, dan nilai kosong).
  - **Aktivitas Praktikum:** Mahasiswa menggunakan rumus Excel (`TRIM`, `PROPER`, `REMOVE DUPLICATES`, `VLOOKUP`, `INDEX-MATCH`) untuk membersihkan dan menggabungkan tabel profil mahasiswa dengan tabel nilai.

## Modul III: Otomatisasi & Integrasi AI di Google Colab (Pertemuan 9 - 14)
Transisi dari pengolah angka manual menuju otomasi *scripting* dibantu Kecerdasan Buatan.
* **Pertemuan 9-10: Pengenalan Google Colab & *Pandas*.**
  - **Aktivitas Praktikum:** Mahasiswa mengunggah *dataset* CSV (data alumni) ke Google Colab. Menjalankan *script* dasar Python (`import pandas as pd`) untuk membaca dan memfilter data.
* **Pertemuan 11-12: *Web Scraping* Data Publik secara Etis.**
  - **Aktivitas Praktikum:** Menggunakan Python (`BeautifulSoup` atau `requests`) untuk men-*scrape* data akreditasi prodi dari portal publik BAN-PT atau pemeringkatan *Webometrics*. Membahas larangan *scraping* pada sistem internal.
* **Pertemuan 13-14: *AI as a Copilot* (Integrasi Prompting).**
  - **Aktivitas Praktikum:** Mahasiswa menggunakan ChatGPT/Gemini untuk men-*generate* kode Python yang rumit (misal: "Buatkan kode untuk mengelompokkan mahasiswa berdasarkan IPK dan menampilkannya sebagai grafik pie"). Mempraktikkan proses anonimisasi data sebelum menyisipkannya ke *prompt* AI.

## Modul IV: Interoperabilitas API & Analitik Lanjutan (Pertemuan 15 - 20)
Fokus pada pertukaran data antar sistem dan *Machine Learning* tingkat dasar.
* **Pertemuan 15-16: Simulasi Konsumsi *API Gateway*.**
  - **Aktivitas Praktikum:** Mahasiswa bertindak sebagai *vendor*. Mereka menggunakan Python/Postman untuk menembak *endpoint API Dummy* yang disediakan dosen (menggunakan format JSON) untuk menarik profil mahasiswa.
* **Pertemuan 17-18: Analisis Prediktif Sederhana (*At-Risk Students*).**
  - **Contoh Data Dummy:** *Dataset* rekaman akademik (jumlah absen, nilai tugas, keaktifan).
  - **Aktivitas Praktikum:** Menggunakan Python (`scikit-learn` dasar atau logika kondisional `pandas`) untuk memprediksi mahasiswa mana yang kemungkinan besar terkena *Drop Out* (DO), guna menciptakan *Early Warning System*.
* **Pertemuan 19-20: Interpretasi Data oleh Statistisi.**
  - **Aktivitas Praktikum:** Mahasiswa menyusun narasi statistik deskriptif dari hasil prediksi di atas. Meminta bantuan AI untuk memperhalus gaya bahasa interpretasi agar cocok untuk Laporan Kebijakan Pimpinan.

## Modul V: Visualisasi & Publikasi Proyek Akhir (Pertemuan 21 - 24)
Fokus pada diseminasi informasi dan pembuatan *output* siap konsumsi publik/pimpinan.
* **Pertemuan 21-22: Pembuatan *Dashboard* di Google Looker Studio.**
  - **Aktivitas Praktikum:** Menghubungkan *Google Sheets* / hasil ekstraksi CSV dari Python ke Google Looker Studio. Mendesain grafik batang interaktif, diagram tren kelulusan, dan peta sebaran domisili mahasiswa.
* **Pertemuan 23-24: Publikasi dan Presentasi Proyek.**
  - **Aktivitas Praktikum:** Mahasiswa mempublikasikan hasil laporan akhirnya dalam format artikel data (*Data Journalism*) di *platform* publik seperti **Medium**, **GitHub Pages**, atau blog kampus. *Dashboard* di-set menjadi "Publik" agar bisa diakses menggunakan *link*, lalu dipresentasikan layaknya mempresentasikan laporan eksekutif kepada Rektor.

---

> [!NOTE]
> **Ketersediaan Data Dummy:**
> Seluruh kegiatan praktikum ini **dilarang keras** menggunakan pangkalan data asli (SIKAD/SIPEG) kampus guna menghindari kebocoran data (UU PDP). Tim dosen/PTID wajib membuat *dataset dummy* yang strukturnya menyerupai aslinya, namun berisi nama dan angka acak (*randomized*), yang secara khusus didistribusikan kepada mahasiswa di setiap pertemuan.
