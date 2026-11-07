# Brief A · Kelasku

**Platform kursus mandiri skill kerja.** Produk fiktif untuk latihan.

## Produk

Perpustakaan kursus video skill kerja, misalnya spreadsheet, presentasi, komunikasi, dan manajemen waktu. Satu langganan untuk semua kursus, dengan uji coba gratis 7 hari.

## User

Karyawan 22–35 tahun yang ingin naik level, dengan waktu terbatas di malam hari atau akhir pekan.

## Business goal

Pengunjung memulai uji coba gratis, lalu tetap berlangganan setelah uji coba selesai.

## Per project

Masalah dan ukuran berhasil di bawah ini **dikunci**: jangan menambah masalah sendiri. Pendekatanmu bebas, selama berangkat dari materi, dan setiap keputusan design menyebut masalah yang dijawabnya (misalnya "Hero · menjawab M1").

### P1 · Website SaaS

- **User saat ini:** Pengunjung yang baru menemukan Kelasku dan belum tahu isinya.
- **Goal:** Paham kursusnya relevan untuk pekerjaannya, lalu memulai uji coba gratis.

| | Masalah | Berhasil kalau | Halaman |
|---|---|---|---|
| M1 | Katalog terlalu banyak, jadi bingung mulai dari mana | Orang baru bisa menyebut satu kursus yang cocok untuknya | Beranda, Katalog kursus |
| M2 | Takut ditagih setelah uji coba gratis | Orang baru bisa menjelaskan apa yang terjadi setelah 7 hari, tanpa bertanya | Harga |
| M3 | Ragu kursusnya bermutu | Orang baru bisa menyebut satu alasan untuk percaya | Beranda, Katalog kursus |

- **Wajib:** Beranda, Katalog kursus, Harga
- **Tambahan:** Detail kursus, FAQ, Tentang

### P2 · Web app

- **User saat ini:** User yang baru mendaftar, belajar sebentar di malam hari setelah bekerja.
- **Goal:** Menyelesaikan kursus pertama dan tetap berlangganan.

| | Masalah | Berhasil kalau | Halaman |
|---|---|---|---|
| M1 | Setelah daftar, layar kosong dan bingung mulai | User baru bisa memulai pelajaran pertama tanpa mencari | Daftar, Onboarding, Beranda user |
| M2 | Berhenti di tengah kursus dan lupa posisinya | User yang kembali bisa melanjutkan dari posisi terakhir dalam satu klik | Beranda user, Halaman pelajaran |
| M3 | Tidak merasa ada kemajuan | User bisa menyebut seberapa jauh progresnya di satu kursus | Beranda user, Halaman pelajaran |

- **Wajib:** Daftar, Onboarding: pilih tujuan belajar, Beranda user: lanjutkan belajar dan progres, Halaman pelajaran, Checkout langganan
- **Tambahan:** Katalog dan pencarian, Sertifikat, Profil

## Flow kunci

Tiga flow yang harus bisa dijalani dari awal sampai akhir. Usability test di pekan 7 memakai flow ini.

| | Flow | Langkah | Menjawab |
|---|---|---|---|
| F1 | Dari website sampai masuk ke web app | Beranda atau Harga → Mulai uji coba → Daftar → Masuk ke web app | P1 M1, M2 · P2 M1 |
| F2 | Onboarding sampai pelajaran pertama (Web app) | Pilih tujuan belajar → Rekomendasi kursus di akhir onboarding → Pelajaran pertama | P2 M1 |
| F3 | Kembali dan berlangganan (Web app, sudah masuk) | Beranda user → Lanjutkan pelajaran → Lihat progres → Uji coba hampir habis → Checkout berhasil atau gagal | P2 M2, M3 |

## Scope

**Termasuk:**

- **Halaman dan layar:** 3 halaman website dan 5 layar web app di atas. Cukup bagian yang dilewati flow kunci; bagian lain boleh berupa kotak placeholder berlabel
- **Flow kunci utuh:** F1–F3 dari awal sampai akhir, dengan state di layar yang dilewatinya: loading, kosong, error, berhasil, gagal, dan validasi
- **Daftar tanpa login:** Setelah daftar, user langsung masuk ke onboarding
- **Transaksi simulasi:** Memakai data contoh, tanpa pembayaran sungguhan
- **Keyboard dan layar HP:** Flow kunci bisa diselesaikan dengan keyboard, dan nyaman di HP maupun desktop

**Tidak termasuk:**

- **Login dan akun:** Halaman masuk, lupa password, verifikasi email, dan OTP. F3 dianggap user sudah masuk
- **Backend:** Database, akun sungguhan, dan pembayaran sungguhan
- **Sisi lain produk:** Admin atau mentor, notifikasi email, dan pengaturan akun
- **Halaman lain:** Di luar daftar wajib, kecuali tambahan kalau tempo cukup

Di luar scope bukan berarti tidak penting. Bagian itu bisa kamu lengkapi setelah program, atau di project-mu sendiri.

## Data contoh

Ada di `data/`. Pakai isi ini, jangan mengarang sendiri.

- `courses.json`: 12 kursus dalam 4 kategori, masing-masing dengan pelajaran
- `plans.json`: 2 paket harga, bulanan dan tahunan
- `user.json`: 1 user (Rina) dengan 2 kursus berjalan
- `testimonials.json`: 3 testimoni
- `faq.json`: 5 pertanyaan
