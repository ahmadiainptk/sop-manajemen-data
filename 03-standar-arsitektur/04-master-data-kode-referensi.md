# Master Data dan Kode Referensi

Selain definisi tabel dan kolom, komponen kritis lainnya untuk menjamin keterhubungan (*linkage*) antar sistem adalah penggunaan referensi data yang sama. Walidata wajib mengelola repositori **Kode Referensi Tunggal** untuk digunakan oleh seluruh sistem.

## Standarisasi Pengkodean Esensial:
Semua sistem aplikasi internal di IAIN Pontianak dilarang membuat kode referensi unik versinya sendiri untuk entitas berikut, dan wajib menggunakan kode referensi resmi:
1. **Identitas Sivitas:** Nomor Induk Mahasiswa (NIM) dan Nomor Induk Pegawai (NIP) / Nomor Induk Dosen Nasional (NIDN).
2. **Kode Program Studi:** Mengacu pada kode registrasi resmi prodi di pangkalan data PDDIKTI.
3. **Kode Mata Kuliah:** Disusun secara terpusat oleh bagian akademik Institut/Fakultas untuk memastikan tidak ada duplikasi kode untuk mata kuliah yang sama antar program studi, guna memudahkan proses ekuivalensi dan pelaporan.
4. **Kode Ruangan dan Gedung:** Setiap fasilitas dan ruang kelas harus memiliki kode inventaris tunggal (berdasarkan standar BMN) untuk digunakan secara bersama oleh sistem penjadwalan akademik maupun sistem peminjaman sarana prasarana.
