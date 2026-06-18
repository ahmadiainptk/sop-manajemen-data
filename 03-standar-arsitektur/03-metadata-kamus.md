# Metadata dan Kamus Data

Untuk mempermudah pemahaman antar pengembang sistem serta untuk menghindari ambiguasi arti dari setiap kolom pangkalan data, Walidata (PTID) bertanggung jawab untuk menyusun, menerbitkan, dan memutakhirkan **Kamus Data Institusional**.

## Ketentuan Penyusunan Kamus Data:
1. **Definisi Operasional:** Kamus data harus memuat definisi operasional dari setiap entitas. Contoh: Definisi pasti dari "Status Mahasiswa Aktif" harus dijelaskan secara tertulis (misalnya: *Mahasiswa yang telah melakukan registrasi dan pembayaran UKT pada semester berjalan*).
2. **Struktur Metadata minimal yang dikelola meliputi:**
   - Nama Tabel / Entitas
   - Nama Kolom (Field)
   - Tipe Data (Data Type) dan Panjang Maksimal (Length)
   - Sifat *Nullability* (Apakah kolom boleh kosong/NULL)
   - Keterangan Relasi (Primary Key / Foreign Key)
   - Deskripsi Singkat Kegunaan Kolom
3. **Dokumentasi Terpusat:** Metadata dan Kamus Data ini harus didokumentasikan di dalam sebuah repositori internal (seperti *Wiki Institusi* atau repositori git) yang dapat diakses dengan mudah oleh semua pengembang *in-house* di IAIN Pontianak.

## Contoh Format Kamus Data

Berikut adalah ilustrasi tabel Kamus Data yang wajib diisi oleh pengembang saat merancang tabel referensi utama (misal: tabel `mahasiswa`):

| Nama Kolom (Field) | Tipe Data | Panjang | Wajib (*Not Null*) | Keterangan / Definisi Operasional |
| :--- | :--- | :--- | :---: | :--- |
| `id_mahasiswa` | String / VARCHAR | 20 | Ya | *Primary Key*. Berisi NIM tanpa spasi/karakter khusus. |
| `nama_lengkap` | String / VARCHAR | 100 | Ya | Nama lengkap mahasiswa sesuai Ijazah/KTP terakhir. |
| `tanggal_lahir` | Date | - | Ya | Wajib mengikuti format baku ISO 8601 (YYYY-MM-DD). |
| `status_aktif` | Enum / Boolean | - | Ya | `True` jika semester ini KRS aktif, `False` jika cuti/DO/lulus. |
| `id_prodi` | String / VARCHAR | 10 | Ya | *Foreign Key* ke tabel `program_studi` (Sesuai kode PDDIKTI). |
