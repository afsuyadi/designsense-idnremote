# Brief B · Mentorku

**Platform mentoring 1-on-1 skill kerja.** Produk fiktif untuk latihan.

## Produk

Sesi video call satu-satu dengan praktisi, misalnya untuk karier, review CV, interview, atau skill teknis. Bayar per sesi atau beli paket 4 sesi.

## User

Karyawan 22–35 tahun yang butuh arahan spesifik dari orang berpengalaman, bukan materi umum.

## Business goal

Pengunjung memesan sesi pertama, lalu kembali memesan sesi berikutnya.

## Per project

Masalah dan ukuran berhasil di bawah ini **dikunci**: jangan menambah masalah sendiri. Pendekatanmu bebas, selama berangkat dari materi, dan setiap keputusan design menyebut masalah yang dijawabnya (misalnya "Hero · menjawab M1").

### P1 · Website SaaS

- **User saat ini:** Karyawan yang butuh arahan spesifik dan sedang membandingkan pilihan mentoring.
- **Goal:** Menemukan mentor yang cocok, lalu memesan sesi pertama.

| | Masalah | Berhasil kalau | Halaman |
|---|---|---|---|
| M1 | Sulit memilih mentor dari banyak pilihan | Orang baru bisa memilih satu mentor dan menyebut alasannya | Beranda, Daftar mentor |
| M2 | Tidak jelas apa yang didapat dari satu sesi dan berapa biayanya | Orang baru bisa menjelaskan isi satu sesi dan biayanya, tanpa bertanya | Harga |
| M3 | Ragu kualitas mentornya | Orang baru bisa menyebut satu alasan untuk percaya | Beranda, Daftar mentor |

- **Wajib:** Beranda, Daftar mentor, Harga
- **Tambahan, kalau tempo cukup:** Cara kerja, FAQ

### P2 · Web app

- **User saat ini:** User yang baru mendaftar dan akan punya sesi terjadwal.
- **Goal:** Hadir di sesi, lalu memesan sesi berikutnya.

| | Masalah | Berhasil kalau | Halaman |
|---|---|---|---|
| M1 | Memesan jadwal membingungkan: zona waktu, slot penuh, dan konfirmasi | User bisa memesan slot yang benar tanpa salah pilih waktu | Pilih jadwal dan bayar |
| M2 | Lupa sesi, atau perlu menjadwal ulang | User bisa menemukan sesi berikutnya dan menjadwal ulang tanpa bantuan | Beranda user, Detail sesi |
| M3 | Catatan dari mentor setelah sesi sulit ditemukan | User bisa menemukan catatan sesi terakhir tanpa mencari lama | Detail sesi |

- **Wajib:** Daftar, Onboarding: pilih bidang dan tujuan, Beranda user: sesi mendatang, Pilih jadwal dan bayar, dengan profil mentor ringkas, Detail sesi: catatan dan jadwal ulang
- **Tambahan, kalau tempo cukup:** Riwayat sesi, Ulasan setelah sesi

## Flow kunci

Tiga flow yang harus bisa dijalani dari awal sampai akhir. Usability test di pekan 7 memakai flow ini.

| | Flow | Langkah | Menjawab |
|---|---|---|---|
| F1 | Masuk ke produk (Website → web app) | Beranda atau Daftar mentor → Pesan sesi → Daftar → Masuk ke web app | P1 M1, M2 · P2 M1 |
| F2 | Onboarding sampai sesi pertama (Web app) | Pilih bidang dan tujuan → Rekomendasi mentor → Pilih jadwal dan bayar → Sesi terkonfirmasi | P2 M1 |
| F3 | Kembali untuk sesi berikutnya (Web app, sudah masuk) | Beranda user → Detail sesi → Jadwal ulang atau baca catatan → Pesan lagi | P2 M2, M3 |

## Scope

**Termasuk:**

- 3 halaman website dan 5 layar web app di atas, cukup bagian yang dilewati flow kunci; bagian lain boleh berupa kotak placeholder berlabel
- Flow F1–F3 utuh dari awal sampai akhir, dengan state di layar yang dilewatinya: loading, kosong, error, berhasil, gagal, dan validasi
- Daftar langsung masuk ke onboarding, tanpa halaman login di antaranya
- Transaksi disimulasikan dengan data contoh, tanpa pembayaran sungguhan
- Bisa dipakai dengan keyboard, dan nyaman di layar HP dan desktop

**Tidak termasuk:**

- Halaman masuk (login), lupa password, verifikasi email, dan OTP. F3 dianggap user sudah masuk
- Backend, database, akun, dan pembayaran sungguhan
- Sisi admin atau mentor, notifikasi email, dan pengaturan akun
- Halaman di luar daftar wajib, kecuali tambahan kalau tempo cukup

Di luar scope bukan berarti tidak penting. Bagian itu bisa kamu lengkapi setelah program, atau di project-mu sendiri.

## Data contoh

Ada di `data/`. Pakai isi ini, jangan mengarang sendiri.

- `mentors.json`: 8 mentor dengan bidang, pengalaman, rating, dan jadwal kosong
- `plans.json`: 2 pilihan harga, per sesi dan paket 4 sesi
- `user.json`: 1 user (Rina) dengan 1 sesi mendatang dan 2 sesi selesai
- `testimonials.json`: 3 testimoni
- `faq.json`: 5 pertanyaan
