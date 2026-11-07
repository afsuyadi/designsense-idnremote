# Pekan 2 · Wireframe

Kedua project mulai punya bentuk, sebagai wireframe HTML abu-abu. Halaman dulu, baru section: kamu menentukan tujuan halaman dan urutan section-nya, Claude Code menggambar halaman utuh, lalu kamu memperbaiki section yang kurang efektif.

## 2.1 · Rencana Beranda website *(kamu)*

- **Kenapa:** halaman dibaca sebagai satu cerita menuju satu aksi utama. Urutan section adalah urutan keraguan user yang dijawab satu per satu.
- **Yang kamu lakukan:** tulis rencana Beranda sebelum menyentuh section mana pun. Pakai referensi dari library-mu.
- **Template:**
  ```
  Tujuan halaman: [apa yang harus dipahami atau dilakukan user di sini]
  Posisi di flow: datang dari [mana], lanjut ke [mana]
  Satu aksi utama: [aksi]
  Urutan section:
  1. [section]: [keraguan user yang dijawab] · menjawab [M1/M2/M3]
  2. …
  ```
- **Pertanyaan pemandu:** apa yang harus dipahami pengunjung dalam lima detik pertama? Keraguan apa yang muncul sebelum dia mau mendaftar, dan section mana yang menjawabnya?
- **Masuk ke:** `CLAUDE.md` › bagian **4. Halaman dan section** › P1 · Website SaaS › Beranda.
- **Cukup kalau:** setiap section punya alasan dan masalah yang dijawabnya, M1–M3 website semuanya terjawab, urutannya menuju satu aksi utama, dan tidak ada section yang bersaing dengan aksi itu.

## 2.2 · Rencana Beranda user web app *(kamu)*

- **Kenapa:** layar web app dipakai berulang kali. Yang penting adalah tugas user, bukan meyakinkan.
- **Yang kamu lakukan:** tulis rencana layar seperti 2.1, ditambah tugas user dan kondisi layarnya.
- **Template:**
  ```
  Tujuan layar: [apa]
  Tugas user di layar ini: [satu kalimat]
  Posisi di flow: datang dari [mana], lanjut ke [mana]
  Satu aksi utama: [aksi]
  Urutan section:
  1. [section]: [alasan] · menjawab [M1/M2/M3]
  Kondisi layar: [misalnya kosong untuk user baru, peringatan, konfirmasi]
  ```
- **Pertanyaan pemandu:** apa yang dilihat user baru yang belum punya data? Apa yang ingin dia lakukan dalam satu klik saat kembali?
- **Masuk ke:** `CLAUDE.md` › bagian **4. Halaman dan section** › P2 · Web app › Beranda user.
- **Cukup kalau:** tugas user jelas, ada satu aksi utama, dan kondisi layarnya sudah didaftar namanya.

## 2.3 · Wireframe kedua halaman *(Claude Code)*

- **Yang kamu lakukan:** pastikan fase di bagian **3. Fase saat ini** masih `wireframe`, lalu ketik `/lanjut`. Claude Code membangun setiap halaman sebagai satu halaman utuh dari rencanamu: abu-abu, satu font sistem, gambar sebagai kotak placeholder.
- **Cukup kalau:** halaman mengikuti urutan section di rencanamu, tanpa section tambahan.

## 2.4 · Nilai halaman utuh *(kamu)*

- **Kenapa:** masalah hierarchy terlihat dari halaman utuh, bukan dari satu section.
- **Yang kamu lakukan:** buka halamannya, lakukan squint test (pandang dengan mata menyipit), lalu tulis temuanmu di chat.
- **Template:**
  ```
  Yang terlihat pertama: [elemen], [elemen], [elemen]
  Seharusnya: [elemen sesuai rencanamu]
  Section yang kurang efektif: [section], karena [prinsip yang dilanggar]
  ```
- **Masuk ke:** dicatat di log pekan ini.
- **Cukup kalau:** temuannya menyebut prinsip (hierarchy, proximity, satu aksi utama), bukan selera.

## 2.5 · Deskripsi section yang diperbaiki *(kamu)*

- **Kenapa:** perbaikan dimulai dari deskripsi yang lebih jelas, bukan dari prompt yang diulang.
- **Yang kamu lakukan:** untuk setiap section yang kurang efektif, tulis deskripsinya dan alasannya.
- **Template:**
  ```
  Section: [nama]
  - Tujuan: [apa yang harus dipahami atau dilakukan user di section ini]
  - Isi: [teks, data dari data/, gambar]
  - Aksi utama: [satu aksi, kalau ada]
  - Referensi: [nama atau link dari library-mu]
  - Kenapa layout ini: [alasan dengan prinsip]
  ```
- **Masuk ke:** `CLAUDE.md` › bagian **4. Halaman dan section**, di bawah halamannya.
- **Cukup kalau:** "Kenapa layout ini" memakai prinsip, dan referensinya relevan dengan masalah, bukan hanya mirip tampilannya.

## 2.6 · Perbaiki section, lalu cek di HP dan desktop *(Claude Code)*

- **Yang kamu lakukan:** ketik `/lanjut`. Claude Code memperbaiki section yang kamu deskripsikan, satu per satu, lalu kamu cek di lebar 360 px dan desktop.
- **Cukup kalau:** urutan prioritas sama di HP dan desktop, tanpa scroll ke samping.

## 2.7 · Laporan pekan ini *(kamu dan Claude Code)*

- **Yang kamu lakukan:** ketik `/laporan`, jawab refleksi, lalu commit, push, dan kirim link repo ke fasilitator.
