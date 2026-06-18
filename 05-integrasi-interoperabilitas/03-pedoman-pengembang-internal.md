# Pedoman Pengembang Internal (In-House Developer)

Untuk menjaga kesinambungan ekosistem pengembangan perangkat lunak kampus, seluruh staf *programmer* PTID dan tim IT fakultas diikat oleh pedoman standar tata kelola pengembangan sistem.

## Aturan Baku Pengembangan Sistem:
1. **Penggunaan Identitas Tersentralisasi:** Setiap aplikasi baru wajib menggunakan layanan otentikasi *Single Sign-On* (SSO) institusi. Dilarang keras membuat tabel `users` beserta penyimpanan *password* yang berdiri sendiri pada masing-masing aplikasi.
2. **Keterikatan Master Data:** Aplikasi baru yang membutuhkan profil pengguna, struktur organisasi, daftar mata kuliah, atau daftar ruangan tidak boleh menyediakan antarmuka (form) untuk menginput data tersebut dari awal, melainkan harus mengambilnya dari *endpoint API* Walidata.
3. **Dokumentasi *Source Code*:** Setiap kode sumber aplikasi yang terintegrasi dengan ekosistem data wajib diunggah pada platform *version control* institusi (misal: *GitLab/GitHub internal*) beserta dengan dokumentasi *README* yang memadai terkait cara instalasi dan arsitektur basis datanya.

## Ringkasan Alur Kerja IT dan Pengelolaan Data (SOP Ringkas PTID)

Sebagai rangkuman dari keseluruhan bab pedoman, berikut adalah ringkasan cara kerja operasional bagi bagian IT/Data:

### 1. Cara Menyimpan Data
- **Sentralisasi:** Semua database utama wajib disimpan di server/cloud yang dikelola terpusat oleh PTID. Fakultas tidak diizinkan memiliki server mandiri untuk operasional inti.
- **Pengarsipan (*Archiving*):** Data transaksi historis dipisahkan ke *Cold Storage* agar kinerja sistem utama tetap ringan, namun data vital (seperti transkrip nilai) disimpan permanen.
- **Backup & Mitigasi Bencana:** Database wajib di-backup otomatis setiap hari dan salinannya harus diletakkan pada lokasi geografis atau cloud yang berbeda (*off-site*) untuk mencegah kehilangan total.

### 2. Cara Mengolah dan Menganalisis Data
- **Pemeriksaan Kualitas (*Data Cleansing*):** Tim IT dan Walidata wajib mengecek data secara berkala untuk anomali, duplikasi, dan kekosongan (NULL). Data cacat akan ditolak dan dikembalikan ke fakultas/prodi terkait.
- **Visualisasi Langsung:** Segala bentuk *Dashboard Eksekutif* wajib ditarik (query) langsung dari *Master Data*, bukan berdasarkan file excel manual yang rentan terhadap modifikasi pihak tak berwenang.

### 3. Cara Mengembangkan Sistem (Tim IT)
- **API First:** Aplikasi tidak boleh saling terhubung dengan menembak langsung ke database masing-masing (no direct DB access). Semua lalu lintas data wajib melewati jalur API Gateway.
- **Identitas Tunggal (SSO):** Developer dilarang keras membuat sistem login (`users table` dan password) milik mereka sendiri. Semua aplikasi harus memanggil layanan *Single Sign-On* institusi.
- **Kepatuhan Standar Data:** Penyusunan kolom tanggal (ISO 8601), NIM/NIP (String), dan referensi data lainnya wajib merujuk secara ketat kepada Kamus Data yang dirilis PTID.
