### 2026-11-11 · 1.2 Pahami brief-mu
- **Permintaan:** "[M3] paling mengancam goal, karena kalau tidak terjawab, pengunjung akan menyebarkan rating yang buruk tentang produk ini" (dan jawaban lanjutan untuk 4 pertanyaan berikutnya di langkah 1.2)
- **Yang dikerjakan:** mengisi bagian Prioritasku di `CLAUDE.md` bagian 2 dengan jawaban peserta apa adanya
- **Tanggapan peserta:** diterima ("pas")
- **Feedback `/cek`:** setiap pilihan sudah punya alasan dari sisi user dengan kata-kata sendiri · tercentang: ya

### 2026-11-14 · 1.3 Isi yang menjawab masalah M1–M3 website
- **Permintaan:** "M1 - ... disuguhkan dengan pertanyaan2 apa yg kamu cari / ingin menambah skill? ... direkomendasikan course2 dari data/courses.json" / "M2: pengunjung perlu melihat kapan date of free trial berakhir, ... disertai dengan hanya beberapa course awal yang terbuka" / "M3: pengunjung perlu melihat daftar testimonial orang2 yang sudah mengikuti coursenya serta skrg kerja dmn"
- **Yang dikerjakan:** mengisi bagian Isi yang menjawab masalah website di `CLAUDE.md` bagian 4 untuk M1–M3, disesuaikan ke format template dan ditandai (asumsi) untuk bagian di luar brief/data; M3 dikoreksi karena `data/testimonials.json` tidak punya field tempat kerja, hanya role
- **Tanggapan peserta:** diterima ("sudah pas")
- **Feedback `/cek`:** ketiga masalah sudah punya isi spesifik dengan sumber jelas · tercentang: ya

### 2026-11-14 · 1.4 Tandai titik di flow kunci yang butuh validasi, loading, atau pesan error
- **Permintaan:** jawaban bertahap untuk titik rawan F1 (Daftar: validasi, loading, error), F2 (rekomendasi kursus: dianggap tidak perlu loading karena idempotent, error jika gagal masuk daftar), F3 (peringatan sebelum uji coba habis)
- **Yang dikerjakan:** mengisi bagian Titik yang butuh validasi, loading, atau pesan error di `CLAUDE.md` bagian 2; dikoreksi dulu karena draf awal peserta menyebut halaman login dan SSO yang tidak ada di scope brief (F1 brief cuma punya langkah Daftar)
- **Tanggapan peserta:** diterima ("sudah ok") setelah revisi
- **Feedback `/cek`:** ketiga pertanyaan terjawab dengan alasan dari sisi user · tercentang: ya
