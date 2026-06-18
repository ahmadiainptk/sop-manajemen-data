# Hak Akses dan Autentikasi

Pengelolaan identitas digital merupakan garis pertahanan pertama dalam mengamankan sistem informasi di IAIN Pontianak. 

## Kebijakan Akses:
1. **Single Sign-On (SSO):** IAIN Pontianak mengimplementasikan *Single Sign-On* sebagai gerbang autentikasi tunggal. Pengguna (mahasiswa, dosen, dan tendik) hanya perlu mengingat satu identitas akun (kredensial) terpusat untuk mengakses semua aplikasi institusi yang relevan.
2. **Manajemen Kata Sandi:** *Password* atau kata sandi tidak boleh disimpan dalam bentuk teks biasa (*plaintext*) di basis data manapun, melainkan wajib dienkripsi menggunakan algoritma *hashing* yang kuat (seperti *bcrypt* atau *Argon2*).
3. **Role-Based Access Control (RBAC):** Setiap aplikasi wajib mendefinisikan matriks peran (*roles*) pengguna secara tegas. Misalnya, akun dengan peran `mahasiswa` hanya dapat melihat nilai miliknya sendiri, sementara akun dengan peran `admin_fakultas` hanya dapat mengelola data mahasiswa dalam ruang lingkup fakultasnya.
4. **Pencabutan Akses Otomatis:** Apabila seorang mahasiswa telah lulus/keluar, atau pegawai telah pensiun/berhenti, maka sinkronisasi *Master Data* harus secara otomatis mencabut (*revoke*) atau menonaktifkan hak akses mereka dari layanan sistem informasi institusi yang dibatasi.
