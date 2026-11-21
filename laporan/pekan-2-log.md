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
- **Feedback `/cek`:** kedua deskripsi section menyebut prinsip (hierarchy, perbandingan) dan referensi relevan · tercentang: ya

### 2026-11-21 · 2.5 Deskripsi section yang diperbaiki (Harga)
- **Permintaan:** deskripsi section "Kartu paket tahunan di harga" — direvisi karena aksi utama awalnya "Daftar tahunan atau bulanan" (dua aksi, beda dari aksi utama halaman "Mulai gratis 7 hari" dan di luar scope — pemilihan paket terjadi di Checkout langganan, bukan di website), isi masih umum ("karena ada diskon"), referensi berupa link iklan Coursera dengan parameter tracking, dan "kenapa layout ini" awalnya "karena menunjukkan harga yg lebih bagus" (bukan prinsip)
- **Yang dikerjakan:** mengisi blok Section: Kartu paket Tahunan di Harga di `CLAUDE.md` bagian 4 P1 · Website SaaS › Harga, dengan angka konkret (Rp74.916/bulan ditagih Rp899.000/tahun) dan referensi disederhanakan
- **Tanggapan peserta:** diterima ("pas") setelah revisi
- **Feedback `/cek`:** kedua deskripsi section menyebut prinsip (hierarchy, perbandingan) dan referensi relevan · tercentang: ya

### 2026-11-21 · 2.6 Perbaiki section, lalu cek di HP dan desktop
- **Permintaan:** "/lanjut" (lanjut ke langkah Claude Code setelah kedua deskripsi section disetujui)
- **Yang dikerjakan:** menambahkan tombol "Mulai gratis" di tiap dari 12 course card di `website/katalog.html` (gaya sama dengan tombol utama, lebar penuh kartu) dan styling-nya di `website/style.css`; mengubah kartu paket Tahunan di `website/harga.html` untuk menampilkan Rp74.916/bulan dengan keterangan "Ditagih Rp899.000/tahun · hemat 24% dibanding bulanan"
- **Tanggapan peserta:** mengubah rencana dulu — minta di tampilan HP, kartu paket Tahunan (direkomendasikan) ditaruh di atas Bulanan karena urutan tumpukan di satu kolom jadi urutan prioritas (hierarchy)
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · 2.6 Perbaiki section, lalu cek di HP dan desktop (urutan kartu paket di HP)
- **Permintaan:** "untuk versi HP katalog.html [maksudnya harga.html], seharusnya card Tahunan berada di atasnya Bulanan"
- **Yang dikerjakan:** menambahkan `order: -1` untuk `.plan-card.recommended` di media query HP (≤720px) di `website/style.css`, supaya kartu Tahunan tampil di atas Bulanan saat ditumpuk satu kolom; desktop tetap dua kolom seperti sebelumnya
- **Tanggapan peserta:** diterima ("sudah pas")
- **Feedback `/cek`:** urutan prioritas sama di HP dan desktop (kartu rekomendasi tetap menonjol di keduanya), tanpa scroll ke samping · tercentang: ya

### 2026-11-21 · Revisi tambahan dari review manager (di luar checklist pekan 2)
- **Permintaan:** "perlu display beberapa course di index.html (paling diminati, 3-4 course. ada tombol liat lebih lengkap)" / "Tambahkan 'about' di index.html. rename jadi 'Privilege kenapa belajar di KelasKu', disertai dengan poin2nya" / "Di footer, selalu munculkan tombol CTA"
- **Yang dikerjakan:** menambahkan dua section baru di `website/index.html` — "Privilege kenapa belajar di KelasKu" (4 poin, dari brief dan `data/plans.json` fitur yang sama di kedua paket) dan "Kursus paling diminati" (4 kursus rating tertinggi, dengan link sekunder "Lihat semua kursus" ke katalog.html, gaya outline supaya tidak bersaing dengan aksi utama "Mulai gratis"); menambahkan tombol CTA (aksi utama halaman yang sama, bukan aksi baru) di footer ketiga halaman (`index.html`, `katalog.html`, `harga.html`); styling di `website/style.css`; memperbarui urutan section Beranda dan aturan footer di `CLAUDE.md` bagian 4 dan 10
- **Tanggapan peserta:** mengubah rencana — minta tombol "Mulai gratis" di bawah section testimoni Katalog kursus dihapus (bukan yang di footer)
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · Hapus tombol Mulai gratis di section testimoni Katalog kursus
- **Permintaan:** "hapus tombol Mulai Gratis di katalog.html (bukan yang di footer), yyang ada di testimoni"
- **Yang dikerjakan:** menghapus tombol "Mulai gratis" di bawah section testimoni di `website/katalog.html` (tombol per card dan tombol footer tetap ada)
- **Tanggapan peserta:** diterima ("ya")
- **Feedback `/cek`:** tidak ada tombol yang berlebihan/bersaing di section testimoni · tercentang: ya

### 2026-11-21 · Feedback dari mentor peserta — CTA di tiap section, dan harga per course
- **Permintaan:** "setiap section yg punya konteks menjelaskan/mengajak, harus ada CTA nya... untuk katalog, pada setiap course... kenapa tidak ditampilkan saya biaya masing2 course tersebut", lalu screenshot anotasi: CTA "Lihat kelas, scroll ke bawah" di section Privilege, CTA "untuk coba gratis" di section Trial 7 hari, dan catatan "Section ini bisa dituker" di section Testimoni
- **Yang dikerjakan:** menambahkan link sekunder "Lihat kelas" (anchor `#kursus-populer`) di section Privilege, dan tombol "Mulai gratis" di section Trial 7 hari, keduanya di `website/index.html`. Ide harga per course ditolak sementara karena `data/courses.json` tidak punya field harga dan bertentangan dengan model satu langganan di brief — menunggu konfirmasi peserta. Catatan "section bisa dituker" diklarifikasi: peserta minta urutan section Testimoni ditukar ke atas section Trial 7 hari — dikerjakan, dan urutan section Beranda di `CLAUDE.md` bagian 4 diperbarui
- **Tanggapan peserta:** diterima untuk kedua CTA dan penukaran urutan ("tukar saja urutannya"); harga per course masih menunggu
- **Feedback `/cek`:** section Privilege dan Trial 7 hari sekarang punya CTA yang relevan, dan urutan section tetap menuju aksi utama tanpa bersaing · tercentang: ya

### 2026-11-21 · Harga dummy per course di Katalog
- **Permintaan:** "silakan tambahkan harga dummy di data/courses.json, mentor saya sudah menyarankan"
- **Yang dikerjakan:** menambahkan field `price` (dummy: Rp149.000 untuk level Pemula, Rp199.000 untuk Menengah) ke tiap 12 course di `briefs/A/data/courses.json`; mengganti tombol "Mulai gratis" per card di `website/katalog.html` dengan harga tersebut; styling di `website/style.css`; memperbarui deskripsi Section: Daftar Courses di `CLAUDE.md` bagian 4. Catatan: ini mengubah data referensi brief (`briefs/A/data/`), bukan cuma copy halaman — ditandai jelas sebagai dummy supaya tidak dianggap fakta asli dari brief
- **Tanggapan peserta:** diterima, lalu minta tombol footer di index.html dihapus karena berdekatan dengan tombol "Mulai gratis" di section Trial 7 hari tepat di atasnya
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · Hapus tombol CTA footer di index.html
- **Permintaan:** "untuk index html, karena tombol mulai gratis sudah ada 2 dan berdekatan, apakah bisa dihapus tombol mulai gratis yg di footer?"
- **Yang dikerjakan:** menghapus `div.footer-cta` di footer `website/index.html` (katalog.html dan harga.html tidak diubah, karena tidak ada CTA section lain tepat di atas footernya); memperbarui aturan footer di `CLAUDE.md` bagian 10 untuk mencatat pengecualian ini
- **Tanggapan peserta:** diterima (mengirim screenshot section "7 hari gratis buat nyobain" di katalog.html, minta ditambahkan CTA)
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · Tambah CTA di section "7 hari gratis buat nyobain" (Katalog kursus)
- **Permintaan:** "di katalog html, tolong tambahkan tombol CTA" (untuk section "7 hari gratis buat nyobain")
- **Yang dikerjakan:** menambahkan tombol "Mulai gratis" di section tersebut di `website/katalog.html`; memperbarui rencana Katalog kursus di `CLAUDE.md` bagian 4
- **Tanggapan peserta:** diterima (lanjut ke permintaan baru untuk harga.html tanpa komentar lain)
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · Ubah section penjelasan jadi FAQ, hapus CTA footer, tambah CTA per kartu paket (Harga)
- **Permintaan:** "1. itu 'apa yang terjadi setelah 7 hari' jangan ditaro di akhir dari harga.html, mending diganti FAQ, kalau di situ jadi pecah alurnya. 2. hapus tombol mulai gratis di footer harga.html. 3. tombol CTA mestinya di dalam card masing2 ada. (baik tahunan maupun bulanan)"
- **Yang dikerjakan:** di `website/harga.html`: mengganti section "Apa yang terjadi setelah 7 hari?" jadi section "Yang sering ditanya" dengan format FAQ (judul pertanyaan + jawaban), supaya tidak terbaca sebagai section penjelasan baru yang memecah alur setelah CTA utama; menghapus `div.footer-cta` di footer; menambahkan tombol "Mulai gratis 7 hari" di masing-masing kartu paket (Bulanan dan Tahunan), menggantikan satu tombol bersama di bawah kedua kartu. Styling `.faq-item` ditambahkan di `website/style.css`. Memperbarui rencana Harga di `CLAUDE.md` bagian 4 dan pengecualian aturan footer di bagian 10
- **Tanggapan peserta:** mengubah rencana — minta tombol tiap kartu rata bawah (bottom alignment), dan judul section FAQ diganti jadi "FAQ"
- **Feedback `/cek`:** menunggu · tercentang: tidak

### 2026-11-21 · Rata bawah tombol kartu paket, ganti judul section jadi "FAQ" (Harga)
- **Permintaan:** "1. untuk setiap card, tolong buat tombol mulai gratisnya itu pada posisi bottom alighment yg sama, 2. ubah 'yang sering ditanya' jadi FAQ"
- **Yang dikerjakan:** di `website/style.css`, menjadikan `.plan-card` flex column dan menambahkan `margin-top: auto` pada `.plan-card .cta-center` supaya tombol kedua kartu (Bulanan dan Tahunan) rata di bawah meski jumlah baris fitur berbeda; menghapus inline style margin yang sudah tidak perlu di `website/harga.html`; mengganti judul section FAQ dari "Yang sering ditanya" jadi "FAQ"; memperbarui catatan judul section di `CLAUDE.md` bagian 4
- **Tanggapan peserta:** menunggu
- **Feedback `/cek`:** menunggu · tercentang: tidak
