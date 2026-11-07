# Pekan 6 · State dan feedback

Prototype menunjukkan perjalanan user lengkap, bukan hanya tampilan ideal: kosong, loading, error, berhasil, gagal, validasi, dan tombol nonaktif selama proses. Karena tanpa backend, semua kondisi itu disimulasikan lewat `?state=` di URL.

## 6.1 · Daftar state dan pesan error *(kamu)*

- **Kenapa:** state yang tidak dirancang tetap muncul, hanya saja dalam bentuk yang membingungkan.
- **Yang kamu lakukan:** untuk setiap layar inti dan form daftar dan masuk, tulis seperti apa setiap state-nya, lalu tulis pesan error-nya.
- **Template:**
  ```
  | Layar | Kosong | Loading | Error | Berhasil | Gagal | Nonaktif |
  | [layar] | [apa yang dilihat dan aksi berikutnya] | … |

  Pesan error: [apa yang terjadi]. [kenapa]. [apa yang bisa dilakukan user].
  ```
- **Pertanyaan pemandu:** apa yang dilihat user baru yang belum punya data? Kalau aksi gagal, apakah input-nya hilang? Bagaimana user tahu tombolnya sedang diproses?
- **Masuk ke:** `CLAUDE.md` › bagian **7. State per layar**.
- **Cukup kalau:** setiap state punya aksi berikutnya untuk user, dan pesan error menjelaskan solusinya tanpa bahasa mesin.

## 6.2 · Bangun state dan flow daftar dan masuk *(Claude Code)*

- **Yang kamu lakukan:** ketik `/lanjut`. Claude Code membangun state dari tabelmu, bisa dibuka lewat `?state=kosong`, `?state=loading`, `?state=error`, `?state=gagal`, termasuk form daftar dan masuk yang disimulasikan.
- **Cukup kalau:** setiap state di tabel bisa dibuka lewat URL.

## 6.3 · Validasi, tombol nonaktif, dan screen reader *(Claude Code)*

- **Yang kamu lakukan:** ketik `/lanjut`. Claude Code menambahkan validasi saat mengisi, tombol nonaktif selama proses, dan pengumuman perubahan state untuk screen reader. Coba sendiri setiap form.
- **Cukup kalau:** tidak ada aksi yang bisa terkirim dua kali, dan error muncul di dekat input yang salah.

## 6.4 · Laporan pekan ini *(kamu dan Claude Code)*

- **Yang kamu lakukan:** `/laporan`, refleksi, commit, push, kirim.
