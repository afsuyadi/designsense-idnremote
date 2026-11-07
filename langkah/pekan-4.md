# Pekan 4 · Spacing dan design token

Gaya yang berulang dijadikan design token, supaya kedua project konsisten dan satu perubahan cukup di satu tempat.

## 4.1 · Spacing scale, Button, dan Input *(kamu)*

- **Kenapa:** jarak yang konsisten membuat pengelompokan terbaca (proximity). Button dan Input dipakai di mana-mana, jadi aturannya ditulis sekali.
- **Yang kamu lakukan:** tulis spacing scale dan aturan dua component dasar.
- **Template:**
  ```
  Spacing scale: [4, 8, 12, 16, 24, 32, …], dipakai untuk [jarak dalam grup] dan [jarak antar grup]
  Button: varian [primary, sekunder], tinggi [px], fokus [seperti apa], target sentuh minimal 44px
  Input: label di [atas/samping], hint [di mana], error [warna dan posisi], fokus [seperti apa]
  ```
- **Pertanyaan pemandu:** berapa jarak di dalam satu grup dibanding antar grup? Bagaimana user keyboard tahu sedang di tombol mana?
- **Masuk ke:** `CLAUDE.md` › bagian **6. Token dan component**.
- **Cukup kalau:** jarak dalam grup lebih kecil dari jarak antar grup, dan fokus serta target sentuh tertulis.

## 4.2 · Pindahkan ke tokens.css *(Claude Code)*

- **Yang kamu lakukan:** ketik `/lanjut`. Claude Code memindahkan warna, ukuran, dan spacing yang berulang ke `tokens.css`.
- **Cukup kalau:** nilai di `tokens.css` sama dengan keputusanmu di bagian 5 dan 6.

## 4.3 · Button dan Input dari token *(Claude Code)*

- **Yang kamu lakukan:** ketik `/lanjut`. Claude Code membuat Button dan Input dari token dan memakainya di kedua project. Cek fokusnya dengan tombol Tab.
- **Cukup kalau:** fokus terlihat, dan target sentuh minimal 44px.

## 4.4 · Tidak ada nilai lepas *(kamu)*

- **Yang kamu lakukan:** minta Claude Code mencari hex atau px di luar `tokens.css`, lalu putuskan: dipindah ke token, atau dihapus.
- **Template:**
  ```
  Nilai lepas: [nilai] di [file] → [jadi token apa / dihapus], karena [alasan]
  ```
- **Cukup kalau:** tidak ada nilai lepas yang tersisa tanpa alasan.

## 4.5 · Laporan pekan ini *(kamu dan Claude Code)*

- **Yang kamu lakukan:** `/laporan`, refleksi, commit, push, kirim.
