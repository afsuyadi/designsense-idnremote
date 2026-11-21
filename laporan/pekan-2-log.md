### 2026-11-20 · 2.1 Rencana Beranda website
- **Permintaan:** "Tujuan halaman: ketika user mengunjungi website pertama kali, dia harus paham tentang apa yg dijual oleh website ini... Urutan section: 1. Hero ... 2. Daftar (lalu melihat tgl uji coba berakhir) ... 3. Testimoni..."
- **Yang dikerjakan:** mengisi bagian Beranda di `CLAUDE.md` bagian 4 P1 · Website SaaS; section 2 diklarifikasi dulu karena dinamai "Daftar" (nama halaman tujuan, bukan section Beranda) lalu diganti jadi "Trial 7 hari"
- **Tanggapan peserta:** diterima ("sudah pas")
- **Feedback `/cek`:** urutan section menjawab M1, M2, M3 satu per satu menuju satu aksi utama · tercentang: ya

### 2026-11-20 · 2.2 Rencana dua halaman website lainnya
- **Permintaan:** rencana Katalog kursus (filter popularitas, durasi trial, top-5 testimoni) dan rencana Harga (paket dan harga, apa yang terjadi setelah 7 hari)
- **Yang dikerjakan:** mengisi blok Katalog kursus dan Harga di `CLAUDE.md` bagian 4 P1 · Website SaaS; Katalog direvisi dari "tanggal pasti trial berakhir" jadi "durasi trial umum" karena trial belum mulai sebelum user daftar; Harga diperjelas untuk menampilkan kedua paket (Bulanan dan Tahunan) sesuai data/plans.json
- **Tanggapan peserta:** diterima ("pas" untuk keduanya)
- **Feedback `/cek`:** kedua halaman punya tujuan berbeda dari Beranda dan satu aksi utama; bersama Beranda, M1–M3 terjawab sesuai kolom Halaman di brief · tercentang: ya

### 2026-11-20 · 2.3 Bangun wireframe ketiga halaman
- **Permintaan:** "/lanjut" (lanjut ke langkah Claude Code setelah rencana ketiga halaman disetujui)
- **Yang dikerjakan:** membangun `website/index.html` (Beranda), `website/katalog.html` (Katalog kursus), `website/harga.html` (Harga), dan `website/style.css`, mengikuti urutan section di rencana masing-masing, grayscale, satu font sistem, placeholder abu-abu untuk gambar. Katalog menampilkan 3 testimoni (bukan "top-5" seperti ditulis di rencana), karena `data/testimonials.json` cuma punya 3 testimoni dan tidak ada field rating per testimoni
- **Tanggapan peserta:** diterima ("ok")
- **Feedback `/cek`:** halaman mengikuti urutan section di rencana, tanpa section tambahan · tercentang: ya

### 2026-11-20 · 2.4 Nilai halaman utuh dengan squint test
- **Permintaan:** "untuk index.html... untuk katalog.html... untuk harga.html..." (urutan yang terlihat pertama di tiap halaman), lalu "terlalu banyak course yg ditampilkan (ada 12), apakah sebaiknya 9 saja?... tombol mulai seharusnya ada untuk setiap card course" dan "seharusnya bukan 899000 per tahun, tetapi 74916 per bulan yg ditampilkan"
- **Yang dikerjakan:** dicatat temuan squint test di log ini (bukan diubah ke CLAUDE.md, sesuai "Masuk ke" langkah 2.4):
  - Beranda: tidak ada yang kurang efektif.
  - Katalog kursus: jumlah 12 course dipertahankan (bukan dipotong ke 9, karena memotong berarti menyembunyikan course asli tanpa alasan prinsip); tombol "Mulai gratis" ditambahkan di tiap card course sebagai aksi yang sama (bukan aksi baru) untuk mengurangi jarak klik (proximity), dengan gaya tombol yang sama seperti tombol utama.
  - Harga: kartu paket Tahunan akan menampilkan harga per bulan (Rp74.916, dari Rp899.000 ÷ 12) disertai keterangan ditagih per tahun, supaya tetap transparan soal billing (M2).
- **Tanggapan peserta:** diterima semua, termasuk gaya tombol per card di Katalog sama seperti tombol utama ("ok")
- **Feedback `/cek`:** temuan menyebut prinsip (hierarchy, proximity, framing harga terkait M2), bukan selera · tercentang: ya

### 2026-11-21 · 2.5 Deskripsi section yang diperbaiki (Katalog kursus)
- **Permintaan:** deskripsi section "Daftar Courses" — direvisi tiga kali: (1) awalnya ada "Harga course" (tidak ada di data, model satu langganan) dan "klik button masukkan keranjang" (beda dari kesepakatan 2.4, dan di luar model bisnis brief) dan "karena bagus" (bukan prinsip); (2) harga course dihapus, tapi aksi utama dan prinsip belum diperbaiki; (3) aksi utama sempat jadi "satu tombol di paling bawah katalog" (beda dari kesepakatan 2.4 soal tombol per card), lalu dikonfirmasi tetap tombol di tiap card
- **Yang dikerjakan:** mengisi blok Section: Daftar Courses di `CLAUDE.md` bagian 4 P1 · Website SaaS › Katalog kursus
- **Tanggapan peserta:** diterima ("pas") setelah tiga iterasi
- **Feedback `/cek`:** menunggu (section kedua, Harga, belum ditulis)
