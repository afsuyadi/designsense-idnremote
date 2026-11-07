# Pekan 1 · Dokumen kedua project

Belum ada tampilan. Pekan ini kamu menulis dasar kedua project: untuk siapa, apa goal-nya, dan bagaimana user bergerak dari website sampai web app. Semua pekan berikutnya berangkat dari sini.

## 1.1 · Pilih brief *(Claude Code)*

- **Kenapa:** semua langkah berikutnya bergantung pada produk di brief-mu.
- **Yang kamu lakukan:** sebutkan brief dari fasilitator, A atau B. Claude Code mengisi baris Brief-mu di bagian **Brief** dan menghapus folder brief yang lain.
- **Cukup kalau:** baris Brief-mu terisi dan hanya satu folder brief yang tersisa.

## 1.2 · Pahami brief-mu *(kamu)*

- **Kenapa:** keputusan design yang efektif dimulai dari masalah user, bukan dari tampilan.
- **Yang kamu lakukan:** baca `briefs/<brief-mu>/brief.md`, terutama masalah M1–M3 per project, flow kunci F1–F3, dan scope. Lihat sekilas isi `data/`, lalu ceritakan ulang dengan kata-katamu sendiri di chat. Masalah dan scope sudah dikunci: tugasmu memahaminya, bukan menambah.
- **Template:**
  ```
  Produk: [apa produknya, dalam satu kalimat]
  Untuk: [siapa user-nya, dan kapan dia memakainya]
  Website: masalah yang paling mengancam goal adalah [M1/M2/M3], karena [akibatnya]
  Web app: masalah yang paling mengancam goal adalah [M1/M2/M3], karena [akibatnya]
  Yang tidak termasuk scope: [satu hal yang sengaja tidak dibangun]
  ```
- **Pertanyaan pemandu:** di momen apa user membuka produk ini? Apa yang membuatnya ragu? Dari tiga masalah di setiap project, mana yang paling mengancam goal-nya? Flow kunci mana yang paling sulit?
- **Masuk ke:** tidak ditulis di `CLAUDE.md`; dicatat di log pekan ini.
- **Cukup kalau:** menyebut user dan masalah setiap project dengan kata sendiri, bukan menyalin kalimat brief, dan tahu batas scope-nya.

## 1.3 · Tulis user dan user goal *(kamu)*

- **Kenapa:** user goal adalah problem statement kedua project. Setiap halaman nanti dinilai dari seberapa jauh ia membantu goal ini.
- **Yang kamu lakukan:** tulis siapa user-nya dan apa yang ingin dia capai.
- **Template:**
  ```
  User: [siapa], [situasinya saat membuka produk]
  User goal: Saat [situasi], saya ingin [aksi], supaya [hasil].
  ```
- **Pertanyaan pemandu:** situasi apa yang membuatnya membuka produk, misalnya jam berapa dan dari perangkat apa? Aksi apa yang bisa diamati? Hasil apa yang dia rasakan, bukan fitur apa yang dia pakai?
- **Masuk ke:** `CLAUDE.md` › bagian **2. User, goal, dan flow** › User dan User goal.
- **Cukup kalau:** situasinya spesifik, aksinya bisa diamati, dan hasilnya dari sisi user, bukan nama fitur.

## 1.4 · Tulis business goal *(kamu)*

- **Kenapa:** tampilan yang efektif menjawab dua pihak: user dan bisnis. Konflik keduanya sering menjadi keputusan design terpenting.
- **Yang kamu lakukan:** tulis apa yang ingin dicapai bisnis, di website dan di web app.
- **Template:**
  ```
  Business goal: [aksi pengunjung atau user] di website, lalu [aksi berikutnya] di web app, supaya [hasil bagi bisnis].
  ```
- **Pertanyaan pemandu:** apa yang dihitung bisnis sebagai berhasil? Di mana business goal bisa bertabrakan dengan user goal?
- **Masuk ke:** `CLAUDE.md` › bagian **2. User, goal, dan flow** › Business goal.
- **Cukup kalau:** berbeda dari user goal, dan menyebut titik di website dan di web app.

## 1.5 · Tulis flow utama *(kamu)*

- **Kenapa:** flow menunjukkan halaman apa yang benar-benar dibutuhkan, dan di mana user bisa berhenti.
- **Yang kamu lakukan:** flow kunci F1–F3 sudah ditentukan di brief. Tulis ulang ketiganya dengan kata-katamu sebagai satu perjalanan: di layar mana user berada, apa yang dilakukannya, dan apa yang terjadi kalau gagal. Lalu tandai langkah yang bisa dipersingkat (misalnya diberi default), dengan alasannya. Jangan menambah flow baru.
- **Template:**
  ```
  F1 · [judul]
  1. [layar] · [apa yang dilakukan user] · kalau gagal: [apa yang terjadi]
  2. …
  → masuk web app
  F2 · …
  F3 · …
  Dipersingkat: [langkah], karena [alasan]
  ```
- **Pertanyaan pemandu:** apa yang terjadi kalau user gagal di satu langkah? Langkah mana yang hanya ada karena kebiasaan, bukan karena user butuh?
- **Masuk ke:** `CLAUDE.md` › bagian **2. User, goal, dan flow** › Flow utama.
- **Cukup kalau:** ketiga flow tertulis lengkap dengan layarnya, titik pindah ke web app terlihat, dan setiap flow punya setidaknya satu jalur saat gagal.

## 1.6 · Tandai titik rawan di flow *(kamu)*

- **Kenapa:** loading, validasi, dan error dipikirkan dari awal, bukan ditambal di akhir.
- **Yang kamu lakukan:** dari flow-mu, tandai langkah yang butuh loading, validasi, atau pesan error, aksi yang bisa terkirim dua kali, dan input yang tidak boleh hilang saat error.
- **Template:**
  ```
  - Langkah [n]: butuh [loading / validasi / pesan error], karena [alasannya]
  ```
- **Masuk ke:** `CLAUDE.md` › bagian **2. User, goal, dan flow** › Titik yang butuh loading, validasi, atau pesan error.
- **Cukup kalau:** setiap form dan setiap aksi yang menunggu hasil punya catatan.

## 1.7 · Daftar halaman kedua project *(kamu)*

- **Kenapa:** daftar halaman adalah batas pekerjaan. Yang tidak ada di daftar tidak dibangun.
- **Yang kamu lakukan:** salin halaman wajib dari brief, lalu tulis untuk setiap halaman: flow mana yang melewatinya dan masalah mana yang dipikulnya. Cukup namanya; isinya ditulis nanti. Halaman di luar brief tidak ditambahkan.
- **Template:**
  ```
  P1 · Website SaaS
  - [halaman] · dilewati [F1] · memikul [M1, M3]
  P2 · Web app
  - [halaman] · dilewati [F2, F3] · memikul [M2]
  ```
- **Masuk ke:** `CLAUDE.md` › bagian **4. Halaman dan section** › Daftar halaman.
- **Cukup kalau:** semua halaman wajib ada, dan setiap halaman tersambung ke flow dan masalahnya.

## 1.8 · Laporan pekan ini *(kamu dan Claude Code)*

- **Yang kamu lakukan:** ketik `/laporan`, jawab dua pertanyaan refleksi, lalu commit, push, dan kirim link repo ke fasilitator bersama hasil Track Taste.
