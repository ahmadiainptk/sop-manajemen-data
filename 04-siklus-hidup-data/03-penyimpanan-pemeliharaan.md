# Penyimpanan dan Pemeliharaan Data

Fase pasca-validasi menginstruksikan bagaimana data disimpan, dikelola, dan dipertahankan dalam infrastruktur internal agar keutuhan dan performa layanan tetap terjaga.

## Manajemen Basis Data (*DBMS Management*):
1. **Sentralisasi Infrastruktur:** Seluruh basis data dari aplikasi operasional vital wajib di-*host* pada infrastruktur *server* atau klaster *cloud* yang dikelola langsung oleh PTID. Penggunaan server *hosting* pihak ketiga yang dikelola mandiri oleh unit kerja secara lepas tidak diizinkan untuk operasional sistem inti.
2. **Optimasi Performa:** PTID melakukan *tuning* performa basis data (misal: *indexing*, *partitioning*) secara berkala guna mengimbangi laju pertumbuhan data transaksi, seperti data *log* presensi atau *log* aktivitas *e-learning*.

## Masa Retensi dan Pengarsipan (*Data Archiving*):
1. **Data Aktif vs Data Historis:** Data transaksi yang berusia lebih dari batas operasional standar (misalnya data KRS 5 tahun ke belakang) dipisahkan dari tabel *database* transaksional aktif dan dipindahkan ke tabel arsip (*Cold Storage*). Hal ini dilakukan guna mempercepat akses pembacaan data aktif aplikasi.
2. **Ketersediaan Permanen (Perpetual Data):** Walaupun dipindahkan ke penyimpanan arsip, data transkrip akademik, nomor ijazah, dan profil dasar alumni harus dipertahankan secara permanen (*no deletion policy*) untuk kebutuhan verifikasi ijazah di masa depan.
