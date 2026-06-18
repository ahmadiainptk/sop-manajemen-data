# Perencanaan dan Pengumpulan Data

Siklus hidup data diawali dengan perencanaan kebutuhan dan proses pengumpulan data dari lapangan ke dalam sistem basis data. 

## 1. Perencanaan Data
- Setiap awal tahun akademik atau tahun anggaran, unit kerja (Produsen Data) wajib melakukan inventarisasi kebutuhan data yang akan dikumpulkan selama satu periode berjalan.
- Kebutuhan form digital baru atau sistem pengumpulan data baru harus dikoordinasikan dengan PTID guna memastikan keselarasan arsitektur dan menghindari tumpang tindih pengumpulan data sejenis oleh unit lain.

## 2. Pengumpulan Data
- **Digital-First:** Metode pengumpulan data wajib mengutamakan penggunaan aplikasi operasional (sistem informasi) atau *form* digital terintegrasi. Pengumpulan manual berbasis kertas sangat tidak disarankan kecuali dalam kondisi di mana infrastruktur tidak memungkinkan.
- **Kepatuhan Format:** Saat menginput data dari pengguna (mahasiswa/dosen) melalui *form* input, aplikasi harus mengimplementasikan validasi secara langsung pada sisi aplikasi (*client/server-side validation*) untuk menjamin kesesuaian dengan tipe data yang ditentukan di Kamus Data (misal: validasi alamat email, angka NIK wajib 16 digit, format tanggal lahir yang valid).
- **Audit Trail:** Aplikasi yang menerima *input* data harus mencatat log *timestamp* (kapan data ditambahkan) dan *user identifier* (siapa yang menambahkan data tersebut) guna melacak akuntabilitas *Produsen Data*.
