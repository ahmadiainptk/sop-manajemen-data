# Template Tugas Praktikum Manajemen Data

Dokumen ini berisi standar kerangka kerja (*template*) yang harus diikuti oleh mahasiswa saat mengumpulkan hasil tugas praktikum agar format penyerahan (*deliverables*) menjadi seragam dan mudah dievaluasi oleh Dosen/Asisten Lab.

---

## 1. Template Makalah Identifikasi Silo Data (Modul I)
**Format File:** PDF / Word (`Makalah_SiloData_KelompokX.pdf`)

**Struktur Penulisan Makalah:**
- **Judul:** Identifikasi Potensi *Silo Data* pada Sistem [Nama Sistem, misal: Sistem Peminjaman Perpustakaan IAIN Pontianak]
- **Bab I. Latar Belakang:** Deskripsi sistem yang berjalan saat ini dan mengapa pangkalan data pada sistem tersebut rawan terisolasi (*silo*).
- **Bab II. Analisis Dampak:** Apa kerugian bagi institusi jika data di sistem ini tidak tersinkronisasi otomatis dengan basis data SIAKAD/SIPEG? (Misal: Mahasiswa DO atau sudah lulus masih bisa meminjam buku karena statusnya tidak ter-*update*).
- **Bab III. Rekomendasi Solusi:** Bagaimana arsitektur *Single Source of Truth* harus diterapkan menggunakan *API Gateway* terhadap sistem tersebut.
- **Kesimpulan.**

---

## 2. Template Kamus Data (Modul I)
**Format File:** Excel / Google Sheets (`Kamus_Data_[Nama_Mahasiswa].xlsx`)

**Struktur Kolom Wajib dalam Excel:**
| No | Nama Tabel | Nama Kolom (Field) | Tipe Data | Panjang Maksimal | Wajib Diisi (*Not Null*) | Relasi (PK/FK) | Definisi Operasional |
|:---|:---|:---|:---|:---|:---|:---|:---|
| 1 | `mahasiswa` | `nim` | String | 15 | Ya | *Primary Key* | Nomor Induk Mahasiswa tanpa spasi/karakter khusus. |
| 2 | `mahasiswa` | `id_prodi` | String | 10 | Ya | *Foreign Key* ke tabel `prodi` | Kode program studi sesuai referensi PDDIKTI. |

---

## 3. Template *Data Cleansing* (Modul II)
**Format File:** Excel (`Clean_Data_[Nama_Mahasiswa].xlsx`)

**Struktur Lembar Kerja (Sheets):**
- **Sheet 1 (`Raw_Data`):** Berisi pangkalan data asli yang kotor (disediakan dosen). **Tidak boleh diedit sama sekali.**
- **Sheet 2 (`Cleansing_Process`):** Berisi penyandingan kolom lama dan kolom baru hasil pemrosesan rumus.
  - *Contoh Header Excel:* `NIM Lama` | `NIM Baru (Formula: TRIM)` | `Nama Asli` | `Nama Kapital (Formula: PROPER)`
- **Sheet 3 (`Clean_Data_Final`):** Data akhir yang sudah 100% bersih, siap di-ekspor ke CSV, di mana baris duplikat sudah dihapus secara permanen menggunakan fitur *Remove Duplicates*.

---

## 4. Template *Google Colab Notebook* (Modul III & IV)
**Format File:** Link URL Publik Colab atau File `.ipynb`

**Struktur *Notebook* (*Cell Markdown* & *Code*):**
1. **[Cell Markdown] Judul Proyek, Nama Mahasiswa, & NIM**
2. **[Cell Markdown] Tahap 1. Import Library & Load Data**
   - **[Cell Code]** `import pandas as pd`, `import matplotlib.pyplot as plt`
3. **[Cell Markdown] Tahap 2. Deskripsi Dataset**
   - **[Cell Code]** `df.info()`, `df.head()`, `df.describe()`
4. **[Cell Markdown] Tahap 3. Pemrosesan Data (Hasil Generasi AI)**
   - **[Cell Code]** *Script* hasil modifikasi dari ChatGPT/Gemini. Wajib mencantumkan *prompt* yang digunakan sebagai komentar baris, contoh: `# Prompt: Buatkan kode pandas untuk...`
5. **[Cell Markdown] Tahap 4. Analisis & Deteksi *At-Risk Students***
   - **[Cell Code]** Kueri kondisional *pandas* untuk memfilter IPK rendah dan absensi tinggi.
6. **[Cell Markdown] Tahap 5. Kesimpulan Analitik**
   - Berisi narasi teks 2-3 paragraf dari mahasiswa yang menyimpulkan hasil keluaran statistik dari blok kode di atas.

---

## 5. Template Artikel Publikasi Akhir (Modul V)
**Format File:** Link URL Publik (Medium / Blogger / WordPress / GitHub Pages)

**Struktur Artikel Data (*Data Storytelling*):**
- **Judul Menarik (Bukan Judul Makalah Kaku):** Contoh: *"Meneropong Potensi Masalah Akademik: Analisis Data Simulasi 500 Mahasiswa"*.
- **Paragraf Pembuka (*Hook*):** Pengantar mengapa manajemen data kampus dan keakuratan pelaporan itu krusial.
- **Metodologi Singkat:** *Disclaimer* yang menjelaskan bahwa tulisan ini menggunakan data *dummy* dan dianalisis menggunakan *Python/Pandas* serta divisualisasikan dengan *Looker Studio*.
- **Tangkapan Layar *Dashboard*:** Sisipkan gambar layar (*screenshot*) *Dashboard* interaktif. (Gunakan *Embed HTML* jika *platform blog* mendukung iFrame).
- **Temuan Utama (*Key Findings*):** Jabarkan 3 poin statistik menarik. (Misal: *"Program Studi X memiliki tren penurunan IPK paling signifikan di semester 4"*).
- **Rekomendasi Kebijakan:** Saran konstruktif bagi manajemen institusi (Rektor/Dekan) berdasarkan temuan tersebut (misal: pengadaan kelas tambahan atau bimbingan konseling).
