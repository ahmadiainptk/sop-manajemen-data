# Sinkronisasi Skala Nasional

Perguruan tinggi memiliki kewajiban reguler untuk melaporkan dinamika kegiatan akademik ke pangkalan data eksternal kementerian. Di IAIN Pontianak, kewajiban ini utamanya ditujukan kepada Pangkalan Data Pendidikan Tinggi (PDDIKTI) Kemdikbudristek dan *Education Management Information System* (EMIS) Kementerian Agama.

## Mekanisme Sinkronisasi Eksternal:
1. **Otomatisasi Penjadwalan (*Cron Jobs*):** PTID merancang sistem penarikan dan pendorongan data dari *Master Data* lokal ke pangkalan data kementerian secara otomatis melalui layanan *web service* / API kementerian terkait, meminimalisasi proses unggah/unduh *spreadsheet* manual.
2. **Pemetaan Kode Referensi (*Mapping*):** Jika terdapat perbedaan kode referensi antara sistem internal kampus dengan kode referensi kementerian (misal: perbedaan id agama atau status pendaftaran), PTID bertanggung jawab membuat tabel pemetaan (*mapping table*) di sisi *middleware* agar sinkronisasi berjalan tanpa *error*.
3. **Resolusi Konflik Sinkronisasi:** Apabila terjadi kegagalan sinkronisasi (*sync error*) akibat data lokal tidak memenuhi validasi kementerian (misalnya NIK ibu kosong yang diwajibkan EMIS), sistem *middleware* harus segera mengirimkan peringatan otomatis ke dashboard *Produsen Data* terkait untuk segera dilengkapi.
