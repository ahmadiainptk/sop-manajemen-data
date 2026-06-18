# Pemeriksaan dan Validasi Data

Sebelum data mentah disajikan sebagai Laporan Resmi Institusi atau disinkronisasikan ke Pangkalan Data Eksternal (PDDIKTI/EMIS), proses kontrol kualitas data (*Data Quality Assurance*) mutlak diperlukan.

## Prosedur Pemeriksaan:
1. **Data Cleansing:** PTID bekerja sama dengan unit teknis akademik (seperti Biro AUAK / Bagian Akademik) melakukan pendeteksian otomatis secara berkala untuk mencari:
   - Data anomali atau tidak wajar (misalnya umur mahasiswa di bawah standar normal, IPS > 4.00).
   - Data kosong (*NULL* / *missing values*) pada kolom-kolom kritikal (seperti NIK, nama ibu kandung, tanggal lahir).
   - Duplikasi data (seperti NIK ganda untuk dua mahasiswa yang berbeda).
2. **Klarifikasi Produsen Data:** Jika ditemukan data yang bermasalah pada tahapan pemeriksaan, PTID berhak menolak data tersebut untuk masuk ke dalam *Master Data* dan akan mengembalikannya ke *Produsen Data* (Fakultas/Prodi) untuk diverifikasi dan diperbaiki ulang dari sumber aslinya.
3. **Penyegelan Data (*Data Lock*):** Data akademik (seperti nilai semester) yang telah divalidasi dan ditutup pada batas akhir periode pelaporan, akan dikunci (*lock*) di tingkat *database*. Perubahan pada data yang telah disegel memerlukan prosedur *bypass* khusus melalui Berita Acara Perubahan Data yang disetujui pimpinan terkait.
