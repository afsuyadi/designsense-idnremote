### 2026-11-27 · 3.1 Font, type scale, dan palet
- **Permintaan:** dijawab bertahap lewat 3 pertanyaan — Font: awalnya "IBM Plex Mono, karena sudah terbukti digunakan di course fullstackopen.com, enak dilihat di malam hari, dan terasa elegan", lalu diganti "Source Sans Pro, karena lebih universal dan netral, cocok buat produk edukasi". Type scale: "judul 28/36, subjudul 18/26, body 16/26, label 13/18" (nilai diusulkan Claude Code, diterima). Palet: awalnya "latar rgb(237,237,237), teks rgb(255,255,255)" (kontras gagal, ~1.1:1), lalu aksen "#2563EB", sukses "#16A34A", error "#DC2626" (nilai aksen/sukses/error diusulkan Claude Code, diterima); teks akhirnya diperbaiki jadi "#1A1A1A" (nilai diusulkan Claude Code untuk memperbaiki kontras, diterima — "ya, pakai ini")
- **Yang dikerjakan:** mengisi bagian Font, Type scale, dan Palet di `CLAUDE.md` bagian 5; kontras latar/teks diperiksa manual dan diusulkan nilai pengganti sebelum masuk ke dokumen
- **Tanggapan peserta:** diterima ("sudah pas")
- **Feedback `/cek`:** setiap ukuran type scale punya peran, palet punya makna dan jumlahnya terbatas (5 warna) · tercentang: ya

### 2026-11-27 · 3.2 Ganti mode tampilan ke high fidelity
- **Permintaan:** "/lanjut" (lanjut setelah bagian 5 Typography dan warna disetujui)
- **Yang dikerjakan:** mengganti `CLAUDE.md` bagian 3 Mode tampilan dari `wireframe` jadi `high fidelity`; belum mengubah halaman apa pun
- **Tanggapan peserta:** diterima ("sudah pas, lanjut")
- **Feedback `/cek`:** mode sudah berganti · tercentang: ya

### 2026-11-27 · 3.3 Terapkan typography dan warna ke seluruh halaman
- **Permintaan:** "/lanjut" (lanjut setelah mode high fidelity disetujui)
- **Yang dikerjakan:** menulis ulang `website/style.css` memakai font Source Sans Pro (dimuat dari Google Fonts sebagai "Source Sans 3", nama family di layanannya), type scale (judul 28/36, subjudul 18/26, h3/body 16/26, label 13/18 — h3 dan harga paket dipetakan ke ukuran body/judul terdekat karena scale cuma punya 4 peran), dan palet (latar, teks, aksen, sukses belum terpakai di halaman manapun, error juga belum) dari `CLAUDE.md` bagian 5; teks sekunder (meta, label, lead) memakai warna teks dengan opacity, dan border memakai teks dengan opacity rendah, supaya tidak menambah warna baru di luar palet; menambahkan link Google Fonts di `<head>` ketiga halaman website. Struktur section tidak diubah
- **Tanggapan peserta:** diterima ("sudah pas")
- **Feedback `/cek`:** struktur dari wireframe tetap utuh di ketiga halaman · tercentang: ya

### 2026-11-27 · Revisi: background utama pakai latar, bukan putih
- **Permintaan:** "boleh" (menyetujui usulan mengganti background utama dari putih ke latar `#EDEDED`, supaya lebih nyaman buat user yang belajar malam hari)
- **Yang dikerjakan:** di `website/style.css`, `body` sekarang berlatar `var(--color-latar)` (dulu putih), dan `section.alt` dibalik jadi putih supaya ritme selang-seling antar section tetap kebaca; `.placeholder` juga diubah jadi putih supaya kotak foto/thumbnail tetap kontras di atas section yang sekarang abu
- **Tanggapan peserta:** diganti arah — peserta minta dark theme penuh setelah bertanya "kenapa tidak hitam saja semua"
- **Feedback `/cek`:** sudah dilanjutkan ke revisi dark theme penuh di bawah · tercentang: tidak (digantikan revisi berikutnya)

### 2026-11-27 · Revisi: dark theme penuh
- **Permintaan:** "ya dark theme" (setelah dijelaskan konsekuensinya: latar dan teks bertukar peran, dan aksen biru sebagai warna teks langsung di atas latar gelap cuma dapat kontras ~3.4:1, lolos UI/large text tapi belum lolos teks normal)
- **Yang dikerjakan:** di `CLAUDE.md` bagian 5, Palet ditandai dark theme dengan latar dan teks bertukar hex (latar #1A1A1A, teks #EDEDED). Di `website/style.css`: variabel `--color-latar`/`--color-teks` ditukar nilainya, ditambah `--color-teks-rgb` untuk border dan tint yang sebelumnya hardcode `rgba(26,26,26,...)` (sekarang `rgba(var(--color-teks-rgb),...)` supaya tetap kebaca di atas latar gelap); `section.alt` dan `.placeholder` yang sebelumnya putih solid diganti jadi tint tipis dari teks (`rgba(var(--color-teks-rgb), 0.04)` dan `0.12`) biar nggak jadi bidang putih terang yang mencolok di tengah halaman gelap; teks label "halaman aktif" di navigasi dan tombol `.btn-secondary` yang sebelumnya pakai warna aksen langsung sebagai teks diganti ke warna teks (kontrasnya nggak cukup di ukuran segitu), aksen tetap dipakai sebagai garis bawah/border supaya perannya sebagai penanda masih kelihatan
- **Tanggapan peserta:** diterima ("ok")
- **Feedback `/cek`:** latar-teks konsisten dipakai sebagai pasangan dark theme di seluruh halaman, aksen tetap kepakai sebagai penanda (border/garis bawah) tanpa jadi warna teks yang gagal kontras · tercentang: ya (bagian dari 3.3, sudah tercentang sebelumnya)
