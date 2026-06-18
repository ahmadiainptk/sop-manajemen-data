# Rencana Pengajaran dan Contoh Hasil Tugas Praktikum

Dokumen ini merupakan turunan operasional dari Silabus Praktikum Manajemen Data. Di dalamnya memuat panduan langkah pengajaran (*Lesson Plan*) bagi dosen/instruktur, serta contoh bentuk serahan (*deliverables*) atau hasil tugas yang diharapkan dari mahasiswa pada tiap modul.

---

## Modul I: Fondasi Tata Kelola dan Teori
**Langkah Pengajaran:**
1. **Pemaparan Dosen (30 Menit):** Dosen menjelaskan konsep *Single Source of Truth* (SSOT) dan bahaya duplikasi data (Silo Data) di kampus menggunakan diagram arsitektur.
2. **Diskusi Kelompok (40 Menit):** Mahasiswa dibagi dalam kelompok, lalu diminta mengidentifikasi aplikasi apa saja di kampus mereka (misal: SIAKAD, E-Library, SIPEG) dan menduga mana yang datanya terpusat atau terpisah.
3. **Praktik Mandiri (50 Menit):** Mahasiswa menyusun Kamus Data di *spreadsheet*.

**Contoh Hasil Tugas (Deliverables):**
- **Tugas Kelompok:** Makalah 2 halaman berjudul *"Identifikasi Potensi Silo Data pada Sistem Peminjaman Buku Perpustakaan"*.
- **Tugas Individu:** *File Spreadsheet* (`Kamus_Data_Mahasiswa_Nama.xlsx`) yang berisi rancangan minimal 10 kolom tabel lengkap dengan Tipe Data, *Length*, dan Aturan *Nullability*.

---

## Modul II: Pengumpulan & *Data Cleansing*
**Langkah Pengajaran:**
1. **Simulasi Role-Play (30 Menit):** Sebagian mahasiswa menjadi "Responden" dan sebagian menjadi "Pengumpul Data" menggunakan Google Forms.
2. **Injeksi Data Kotor (20 Menit):** Dosen mendistribusikan *file dummy* (`raw_data_akademik.csv`) yang sengaja dirusak (banyak *typo*, huruf kapital acak, dan NIM ganda).
3. **Praktikum Excel/Spreadsheet (70 Menit):** Dosen mendemonstrasikan fungsi `TRIM`, `PROPER`, dan `VLOOKUP` di layar utama. Mahasiswa mengikuti (metode *Code-Along*).

**Contoh Hasil Tugas (Deliverables):**
- **File Output:** `Clean_Data_Akademik_Nama.xlsx`.
- **Kriteria Penilaian:** Mahasiswa mendapat nilai A jika *Sheet 1* berisi *Raw Data*, *Sheet 2* berisi tahapan pembersihan, dan *Sheet 3* berisi *Clean Data* yang sudah 100% bebas dari duplikasi dan sel kosong (*NULL*).

---

## Modul III: Otomatisasi & Integrasi AI di Google Colab
**Langkah Pengajaran:**
1. **Orientasi Cloud (20 Menit):** Dosen memastikan semua mahasiswa memiliki akun Google dan berhasil masuk ke *Google Colab*. Dosen menekankan larangan mengunggah data KTP/NIM asli teman mereka.
2. **Demo *Scraping* & *Pandas* (40 Menit):** Dosen menunjukkan cara men-*scrape* daftar prodi dari situs BAN-PT, lalu memuatnya ke dalam *dataframe Pandas*.
3. **Praktik *Prompting* AI (60 Menit):** Mahasiswa menggunakan ChatGPT/Gemini untuk meminta *script* Python. Contoh *Prompt*: *"Saya punya kolom 'Tanggal Lahir' berformat DD-MM-YYYY, buatkan kode Python pandas untuk mengubahnya menjadi umur (tahun) saat ini."*

**Contoh Hasil Tugas (Deliverables):**
- **Link Google Colab:** Tautan ke *Notebook* Colab mahasiswa (disetel *Anyone with the link can view*).
- **Isi Notebook:** Harus memuat blok kode yang di-*generate* oleh AI, *comment* penjelasan dari mahasiswa, dan visualisasi grafik sederhana (seperti grafik *Bar* jumlah mahasiswa per prodi) menggunakan *Matplotlib*.

---

## Modul IV: Interoperabilitas API & Analitik Lanjutan
**Langkah Pengajaran:**
1. **Teori API (30 Menit):** Dosen menjelaskan analogi API seperti pelayan restoran yang menghubungkan pelanggan (Aplikasi) dan dapur (Database).
2. **Praktik Postman/Python (40 Menit):** Mahasiswa melakukan *GET Request* ke *endpoint dummy* (misal: `https://jsonplaceholder.typicode.com/users`) untuk memahami struktur JSON.
3. **Machine Learning Dasar (50 Menit):** Dosen memandu penggunaan aturan kondisional (*if-else* di *Pandas*) atau regresi logistik sederhana untuk melabeli data *"Aman"* dan *"At-Risk"*.

**Contoh Hasil Tugas (Deliverables):**
- **Tugas API:** *Screenshot* keberhasilan menarik data JSON dan mem-*parsing*-nya ke dalam format *tabel* Excel.
- **Tugas Analitik:** Daftar NIM *dummy* yang masuk ke dalam kategori *At-Risk Student* beserta alasan statistiknya (misal: "Karena IPK < 2.5 dan jumlah absen > 5 kali").

---

## Modul V: Visualisasi & Publikasi Proyek Akhir
**Langkah Pengajaran:**
1. **Workshop Looker Studio (60 Menit):** Dosen mengajarkan cara menyambungkan hasil data *clean* dari modul sebelumnya ke Google Looker Studio. Mengajarkan filter rentang tanggal, *dropdown* pilihan Fakultas, dan pewarnaan grafik.
2. **Bimbingan Publikasi (60 Menit):** Mahasiswa mendaftar akun Medium/GitHub Pages, lalu mulai menulis narasi (*Storytelling with Data*) berdasarkan grafik yang telah mereka buat.

**Contoh Hasil Tugas (Deliverables - Final Project):**
- **Dashboard Publik:** Tautan (*Link*) Google Looker Studio yang interaktif.
- **Artikel Publikasi:** Tulisan publik (*Blog Post* / Medium) setebal 500-800 kata yang berisi tangkapan layar *Dashboard*, interpretasi tren kelulusan/akademik, dan kesimpulan kebijakan (*Policy Recommendation*) layaknya seorang Statistisi ahli. 
