# Mitigasi Bencana (Disaster Recovery)

Untuk meminimalkan waktu henti layanan (*downtime*) dan mencegah hilangnya aset informasi akibat bencana alam, kegagalan perangkat keras, atau serangan siber (seperti *ransomware*), PTID diwajibkan mengelola standar ketahanan infrastruktur.

## Perencanaan Pemulihan Bencana (DRP):
1. **Pencadangan Otomatis (*Automated Backup*):** 
   - Salinan *database* untuk sistem-sistem inti wajib dilakukan pencadangan secara otomatis setiap hari (*daily backup*).
   - Pencadangan mingguan (*weekly backup*) dilakukan untuk mencakup *file storage* (berkas unggahan pengguna, foto, dokumen arsip).
2. **Penyimpanan Terdistribusi (Off-site / Cloud Storage):** Data cadangan (file *backup*) dilarang disimpan secara eksklusif pada server fisik yang sama dengan aplikasi aktif. Salinan data wajib diduplikasi ke lokasi server yang berbeda gedung secara geografis atau pada fasilitas penyedia layanan *cloud storage* aman.
3. **Simulasi Pemulihan (*Recovery Drill*):** PTID wajib melakukan simulasi uji coba pengembalian data (*restore testing*) secara berkala minimal satu kali dalam setahun guna memastikan *file backup* yang dihasilkan tidak rusak (*corrupt*) dan memperkirakan waktu estimasi pemulihan (*Recovery Time Objective* / RTO) yang dibutuhkan apabila terjadi krisis.
