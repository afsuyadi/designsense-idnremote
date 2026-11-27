# Laporan Pekan 2 · Wireframe tiga halaman website

## 1. Progres

- [x] 2.1 Tulis rencana Beranda website: tujuan, aksi utama, urutan section
- [x] 2.2 Tulis rencana dua halaman website lainnya
- [x] 2.3 Bangun wireframe ketiga halaman, masing-masing satu halaman utuh
- [x] 2.4 Nilai halaman utuh dengan squint test
- [x] 2.5 Tulis deskripsi dan "kenapa layout ini" untuk section yang kurang efektif
- [x] 2.6 Perbaiki section itu, lalu cek di HP dan desktop
- [x] 2.7 Laporan pekan ini

Setelah checklist pekan 2 selesai, ada beberapa ronde revisi tambahan dari review manager dan mentor peserta (di luar checklist pekan 2 — dicatat di bagian 2–4 di bawah karena mengubah keputusan halaman Beranda, Katalog kursus, dan Harga).

## 2. Keputusan design

**Rencana Beranda, keadaan akhir (langkah 2.1 + revisi tambahan):**

> - Tujuan halaman: ketika user mengunjungi website pertama kali, dia harus paham tentang apa yang dijual oleh website ini, yaitu course-course soft skills untuk developer, dan hal-hal yang membuat dia yakin untuk mendaftar masuk web app & subscribe free trial.
> - Posisi di flow: datang dari pencarian atau LinkedIn, lanjut ke Daftar.
> - Satu aksi utama: Mulai gratis
> - Urutan section:
>   1. Hero: "apakah ini bermanfaat untuk saya dan sesuai dengan yang saya butuhkan?" · menjawab M1
>   2. Privilege kenapa belajar di KelasKu: "apa untungnya dibanding belajar sendiri?" · menjawab M1 (tambahan dari review manager; CTA "Lihat kelas" sempat ditambahkan atas saran mentor peserta, lalu dihapus lagi atas permintaan peserta)
>   3. Kursus paling diminati (4 kursus teratas, dengan link "Lihat semua kursus"): "course mana yang terbukti diminati orang lain?" · menjawab M1 (tambahan dari review manager)
>   4. Testimoni: "apakah coursenya seampuh itu dan sesuai dengan role saya?" · menjawab M3 (ditukar ke atas Trial 7 hari, atas permintaan mentor peserta)
>   5. Trial 7 hari (dengan CTA "Mulai gratis"): "kapan free trial ini berakhir, dan apa yang terjadi setelahnya?" · menjawab M2

**Rencana Katalog kursus, keadaan akhir (langkah 2.2):**

> - Tujuan halaman: pengunjung menemukan course yang tepat untuk dirinya, tanpa bingung memilih dari puluhan course yang direkomendasikan kepadanya.
> - Posisi di flow: datang dari Beranda atau pencarian, lanjut ke Daftar.
> - Satu aksi utama: Mulai gratis.
> - Urutan section:
>   1. Filter berdasarkan popularitas (rating tertinggi dan jumlah pembeli) · menjawab M1
>   2. Durasi trial (7 hari gratis, dihitung dari hari kamu daftar, dengan CTA "Mulai gratis") · menjawab M2
>   3. Top-5 testimoni beserta rating · menjawab M3

**Rencana Harga, keadaan akhir (langkah 2.2 + revisi tambahan):**

> - Tujuan halaman: pengunjung paham persis apa yang terjadi setelah 7 hari dan merasa aman untuk mulai, bukan takut ditagih diam-diam.
> - Posisi di flow: datang dari Beranda atau Katalog, lanjut ke Daftar.
> - Satu aksi utama: Mulai gratis 7 hari.
> - Urutan section:
>   1. Paket dan harga (Bulanan dan Tahunan, Tahunan sebagai rekomendasi, masing-masing kartu punya CTA "Mulai gratis 7 hari") · menjawab M2
>   2. FAQ: Apa yang terjadi setelah 7 hari (bisa berhenti kapan saja) · menjawab M2 (diganti dari section penjelasan biasa menjadi FAQ dengan judul "FAQ", atas permintaan peserta, supaya tidak memecah alur halaman setelah CTA utama)

**Deskripsi section yang diperbaiki (langkah 2.5, keadaan akhir):**

> **Section: Daftar Courses** (Katalog kursus)
> - Tujuan: agar user paham daftar course yang sesuai minatnya dengan rankingnya
> - Isi: jumlah rating, jumlah orang yang beli, tags relevan terkait course itu, harga per course (Rp149.000 untuk level Pemula, Rp199.000 untuk Menengah — harga dummy ditambahkan ke `data/courses.json` atas saran mentor peserta)
> - Aksi utama: tidak ada tombol per card lagi; harga ditampilkan sebagai info, aksi utama tetap "Mulai gratis" di header/footer halaman
> - Referensi: Udemy, Coursera
> - Kenapa layout ini: prinsipnya ingin meyakinkan course mana yang perlu dibeli, berdasarkan rating, jumlah pembeli, dan harga yang ditonjolkan (hierarchy)
>
> **Section: Kartu paket Tahunan di Harga**
> - Tujuan: user paham bahwa berlangganan tahunan lebih murah daripada bulanan.
> - Isi: harga Tahunan ditampilkan sebagai Rp74.916/bulan (ditagih Rp899.000/tahun), dibandingkan Rp99.000/bulan untuk paket Bulanan.
> - Aksi utama: Mulai gratis 7 hari.
> - Referensi: Coursera, halaman perbandingan harga tahunan/bulanan.
> - Kenapa layout ini: prinsip perbandingan — angka per bulan ditonjolkan di kartu Tahunan supaya langsung bisa dibandingkan dengan harga per bulan di kartu Bulanan, tanpa user perlu menghitung sendiri.

## 3. Cara mengarahkan Claude Code

Permintaan kunci dikutip dari log (`laporan/pekan-2-log.md`):

- 2.1: rencana Beranda ditulis lengkap dalam satu giliran, termasuk section "Daftar (lalu melihat tgl uji coba berakhir)" — direvisi 1 iterasi karena "Daftar" sebenarnya nama halaman tujuan, bukan section Beranda, diganti jadi "Trial 7 hari".
- 2.2: rencana Katalog kursus awalnya menampilkan tanggal pasti trial berakhir ("misal user mengakses 20 nov, berarti berakhirnya 28 nov") — direvisi 1 iterasi jadi durasi umum, karena trial belum mulai sebelum user daftar.
- 2.4: squint test menemukan "terlalu banyak course yg ditampilkan (ada 12), apakah sebaiknya 9 saja? tombol mulai seharusnya ada untuk setiap card course" dan "seharusnya bukan 899000 per tahun, tetapi 74916 per bulan yg ditampilkan" — opsi memotong jadi 9 course tidak dipakai, tombol per card dan framing harga per bulan dipakai.
- 2.5 (Katalog): deskripsi section "Daftar Courses" direvisi 3 iterasi — "Harga course" (tidak ada di data) dan "klik button masukkan keranjang" (beda dari model satu langganan di brief) dihapus, "karena bagus" diganti jadi alasan hierarchy.
- 2.5 (Harga): deskripsi section kartu Tahunan direvisi 1 iterasi — aksi utama "Daftar tahunan atau bulanan" (dua aksi) disamakan jadi "Mulai gratis 7 hari", isi dilengkapi dengan angka konkret.
- 2.6: setelah kedua section dibangun, peserta mengubah rencana lagi — minta urutan kartu paket di tampilan HP dibalik (Tahunan di atas Bulanan) berdasarkan prinsip hierarchy saat ditumpuk satu kolom.
- Revisi tambahan dari review manager: tiga permintaan sekaligus ("perlu display beberapa course di index.html... ada tombol liat lebih lengkap", "Tambahkan 'about'... rename jadi 'Privilege kenapa belajar di KelasKu'", "Di footer, selalu munculkan tombol CTA") — dikerjakan langsung sebagai section baru dan aturan footer baru, lalu peserta minta satu penyesuaian: tombol "Mulai gratis" yang duplikat di bawah testimoni Katalog dihapus.
- Revisi tambahan dari mentor peserta: permintaan CTA di tiap section penjelasan, dan pertanyaan kenapa harga per course tidak ditampilkan di Katalog — untuk harga per course, Claude Code memberi satu clue dulu (`data/courses.json` tidak punya field harga, dan bertentangan dengan model satu langganan di brief) sebelum peserta mengonfirmasi tetap mau pakai angka dummy.
- Beberapa permintaan susulan berupa micro-adjustment singkat (hapus tombol yang berdekatan di index.html dan Privilege, ganti section "Apa yang terjadi setelah 7 hari" jadi FAQ, tombol di tiap kartu paket Harga, rata bawah tombol kartu, ganti judul FAQ) — dikerjakan langsung tanpa iterasi karena peserta sudah menulis keputusan konkret, bukan draf yang perlu dipertajam.

Pola yang terlihat: hampir di setiap langkah formal (2.1–2.6), peserta memperbaiki rencana atau deskripsinya dulu (bukan hanya mengulang permintaan yang sama) setelah diberi pertanyaan atau clue — terutama soal konsistensi dengan model bisnis di brief (satu langganan, bukan keranjang/beli per course) dan konsistensi dengan keputusan sebelumnya (aksi utama, tombol per card). Pada revisi tambahan di luar checklist, pola bergeser: permintaan datang sudah sebagai keputusan dari pihak luar (manager/mentor) yang diteruskan peserta, dan Claude Code memberi satu clue saat bertentangan dengan data atau model bisnis brief, baru dikerjakan setelah peserta mengonfirmasi.

## 4. Feedback dan tindak lanjut

- **2.1:** urutan section menjawab M1, M2, M3 satu per satu menuju satu aksi utama — diterima tanpa perubahan setelah section "Daftar" diganti nama jadi "Trial 7 hari".
- **2.2:** kedua halaman punya tujuan berbeda dari Beranda dan satu aksi utama; bersama Beranda, M1–M3 terjawab sesuai kolom Halaman di brief.
- **2.3:** wireframe mengikuti urutan section di rencana, tanpa section tambahan — diterima.
- **2.4:** temuan squint test menyebut prinsip (hierarchy, proximity, framing harga terkait M2) — opsi memotong jumlah course ke 9 tidak dipakai karena memotong data asli tanpa alasan prinsip; tombol per card dan framing harga per bulan dipakai.
- **2.5:** kedua deskripsi section menyebut prinsip dan referensi relevan, setelah beberapa bagian (isi yang mengarang data, aksi utama yang di luar model bisnis, alasan layout yang bukan prinsip) diperbaiki peserta.
- **2.6:** urutan prioritas sama di HP dan desktop, tanpa scroll ke samping — diterima setelah urutan kartu paket di HP dibalik sesuai permintaan peserta.
- **Revisi tambahan (manager):** section Privilege dan Kursus paling diminati menambah bukti M1 tanpa bersaing dengan aksi utama (gaya tombol sekunder); tombol duplikat di Katalog dihapus setelah ditunjukkan berdekatan dengan aksi yang sama.
- **Revisi tambahan (mentor):** section Privilege dan Trial 7 hari sekarang punya CTA yang relevan; urutan section Testimoni dan Trial 7 hari ditukar tanpa mengubah jawaban M2/M3; harga dummy per course ditandai jelas sebagai dummy supaya tidak dikira fakta asli brief.
- **Revisi tambahan (micro-adjustment):** tombol footer index.html dan harga.html dihapus setelah berdekatan dengan CTA section tepat di atasnya (didokumentasikan sebagai pengecualian aturan footer); section "Apa yang terjadi setelah 7 hari" jadi FAQ supaya tidak memecah alur setelah CTA utama; kartu paket Harga masing-masing dapat CTA sendiri, rata bawah.

## 5. Refleksi

**Keputusan tersulit pekan ini, dan kenapa:** menentukan mana elemen penting yg user perlu lihat di harga.html, dan bagaimana menampilkan agar user tertarik untuk subscribe tahunan.

**Satu hal yang akan dilakukan berbeda:** mestinya saya cek data, dan lebih enak untuk langsung melihat wireframenya di browser.
