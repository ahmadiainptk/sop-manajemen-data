# Standar Data

Untuk memastikan seluruh aplikasi di IAIN Pontianak dapat saling bertukar informasi secara lancar tanpa terjadi kesalahan *parsing* atau ketidakcocokan format, PTID wajib menetapkan **Standar Data Institusi**.

## Komponen Standar Data:
1. **Format Penamaan (Naming Convention):** Semua kolom (field) pada basis data aplikasi baru harus menggunakan penamaan yang deskriptif dan konsisten, misalnya *snake_case* untuk nama tabel dan kolom (`id_mahasiswa`, `tanggal_lahir`).
2. **Format Standar Tipe Data:**
   - **Tanggal dan Waktu:** Seluruh penyimpanan tanggal harus mengikuti standar ISO 8601 (YYYY-MM-DD).
   - **Teks dan Karakter:** Penyimpanan data teks wajib menggunakan encoding UTF-8 untuk mengakomodasi karakter khusus dengan aman.
   - **Nomor Identitas Utama:** Format entri NIM (Nomor Induk Mahasiswa) dan NIP (Nomor Induk Pegawai) harus disimpan sebagai tipe data *String* (bukan numerik) untuk mencegah hilangnya angka nol di awal dan memudahkan manipulasi teks.
3. **Kepatuhan Aplikasi Pihak Ketiga:** Setiap pengadaan aplikasi dari vendor pihak ketiga wajib melampirkan klausul kontrak yang mengharuskan vendor mematuhi format standar data yang berlaku di IAIN Pontianak.
