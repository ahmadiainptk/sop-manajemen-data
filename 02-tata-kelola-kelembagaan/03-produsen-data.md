# Produsen Data

**Produsen Data** adalah entitas atau unit kerja yang menghasilkan, mengumpulkan, dan melakukan input data asli ke dalam sistem informasi sesuai dengan tugas pokok dan fungsinya. Entitas ini meliputi Fakultas, Pascasarjana, Bagian Administrasi, LP2M, LPM, dan UPT di lingkungan IAIN Pontianak.

## Hak dan Kewajiban Produsen Data:
1. **Pengumpulan Data Valid:** Bertanggung jawab penuh atas akurasi, validitas, dan kebaruan (kemutakhiran) data yang diinput ke dalam sistem operasional masing-masing.
2. **Kepatuhan Standar:** Wajib mematuhi struktur Kamus Data dan Standar Data yang telah ditetapkan oleh PTID selaku Walidata.
3. **Sinkronisasi Melalui API:** Tidak diperkenankan membuat basis data bayangan (*shadow database*) yang tidak tersinkronisasi. Semua proses update data harus dikomunikasikan kembali ke *Master Data* melalui *API Gateway*.
4. **Keamanan di Tingkat Unit:** Menjaga kerahasiaan *credentials* akses bagi pegawai penginput data, dan melaporkan setiap anomali atau dugaan pelanggaran keamanan data ke PTID.
