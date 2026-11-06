# Brief B · Temu

**Platform mentoring 1-on-1 skill kerja.** Produk fiktif untuk latihan.

## Produk

Sesi video call satu-satu dengan praktisi, misalnya untuk karier, review CV, interview, atau skill teknis. Bayar per sesi, atau beli paket 4 sesi. User belajar dari orang, di jadwal yang dipesan.

## User

Karyawan 22–35 tahun yang butuh arahan spesifik dari orang berpengalaman, bukan materi umum.

## Business goal

Pengunjung memesan sesi pertama, lalu kembali memesan sesi berikutnya.

## Masalah UX utama

1. Sulit memilih mentor yang tepat dari banyak pilihan.
2. Memesan jadwal membingungkan: zona waktu, slot penuh, dan konfirmasi.
3. User lupa sesi, atau perlu menjadwalkan ulang.

## Halaman

| | Wajib | Tambahan, kalau tempo cukup |
|---|---|---|
| P1 · Website SaaS | Beranda, Daftar mentor, Harga | Profil mentor, FAQ, Cara kerja |
| P2 · Web app | Daftar dan masuk, Beranda user (sesi mendatang), Pilih jadwal dan pesan, Detail sesi (link call dan catatan dari mentor) | Riwayat sesi, Ulasan setelah sesi |

## Data contoh

Ada di `data/`. Pakai isi ini, jangan mengarang sendiri.

- `mentors.json`: 8 mentor dengan bidang, pengalaman, rating, dan jadwal kosong
- `plans.json`: 2 pilihan harga, per sesi dan paket 4 sesi
- `user.json`: 1 user (Rina) dengan 1 sesi mendatang dan 2 sesi selesai
- `testimonials.json`: 3 testimoni
- `faq.json`: 5 pertanyaan
