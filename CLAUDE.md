# CLAUDE.md

Dokumen ini dibaca Claude Code setiap kali kamu bekerja di repo ini. Isinya tumbuh setiap pekan: dari brief dan flow di pekan 1, sampai menjadi design system di pekan 8. Bagian dalam [kurung siku] kamu yang melengkapi.

Untuk Claude Code: ikuti fase dan aturan di dokumen ini. Kalau sebuah bagian masih kosong, tanyakan ke user, jangan mengarang.

---

## 1. Brief

- **Brief-mu:** [A atau B] → baca `briefs/[A atau B]/brief.md`
- **Data contoh:** `briefs/[A atau B]/data/`

## 2. User, goal, dan flow (pekan 1)

**User:** [siapa, dalam situasi apa]

**User goal:** Saat [situasi], saya ingin [aksi], supaya [hasil].

**Business goal:** [apa yang ingin dicapai bisnis dari website dan web app]

**Flow utama** (dari pengunjung pertama di website sampai memakai web app):

1. [langkah]
2. [langkah]
3. [langkah]

**Titik yang butuh loading, validasi, atau pesan error:** [daftar]

## 3. Fase saat ini

**Fase:** wireframe

Ganti sendiri saat fasenya berpindah: `wireframe` (pekan 2) → `high fidelity` (mulai pekan 3).

### Aturan fase wireframe

- Grayscale saja: hitam, putih, dan abu-abu. Tanpa warna merek.
- Satu font sistem (`system-ui`), ukuran hanya untuk membedakan hierarchy.
- Gambar dan icon berupa kotak abu-abu dengan label isinya.
- Tanpa bayangan, gradien, dan animasi.
- Hasilnya wireframe untuk menilai struktur, bukan produk jadi.

### Aturan fase high fidelity

- Pakai type scale dan palet di bagian 5.
- Mulai pekan 4: hanya nilai dari `tokens.css`. Tidak ada hex, px, atau ukuran lepas di luar token.
- Struktur dari wireframe tetap dipakai. Jangan menambah atau memindah section tanpa diminta.

## 4. Halaman dan section (pekan 2)

Satu blok per section. Tulis dulu, baru minta Claude Code membangunnya.

### P1 · Website SaaS

#### [Nama halaman, misalnya Beranda]

**Section: [nama, misalnya Hero]**
- Tujuan: [apa yang harus dipahami atau dilakukan user di section ini]
- Isi: [teks, data dari `data/`, gambar]
- Aksi utama: [satu aksi, kalau ada]
- Referensi: [link atau nama dari library referensimu]
- Kenapa layout ini: [alasan dengan prinsip, bukan "lebih bagus"]

### P2 · Web app

#### [Nama halaman, misalnya Beranda user]

**Section: [nama]**
- Tujuan: []
- Isi: []
- Aksi utama: []
- Referensi: []
- Kenapa layout ini: []

## 5. Typography dan warna (pekan 3)

- **Font:** [nama font dan alasannya]
- **Type scale:** [ukuran/line-height untuk judul, subjudul, body, label]
- **Palet:** [warna dan maknanya: latar, teks, aksen, sukses, error]
- **Pasangan warna yang lolos kontras:** [teks di atas latar, minimal 4.5:1]

## 6. Token dan component (pekan 4)

- Token ada di `tokens.css`. Aturan: semua warna, ukuran, spacing, dan radius lewat token.
- **Spacing scale:** []
- **Button:** [varian, ukuran, fokus terlihat, target sentuh minimal 44px]
- **Input:** [label, hint, error, fokus]

## 7. State per layar (pekan 6)

Prototype menunjukkan perjalanan user lengkap, bukan hanya tampilan ideal: onboarding, happy path, edge case (input salah, data kosong, teks sangat panjang, pilihan tidak tersedia), aksi berhasil dan gagal, validasi saat mengisi, dan tombol nonaktif selama proses. Setiap state bisa dibuka lewat `?state=` di URL (lihat bagian 10).

| Layar | Ideal | Kosong | Loading | Error | Sebagian | Berhasil | Nonaktif |
|---|---|---|---|---|---|---|---|
| [layar] | [] | [] | [] | [] | [] | [] | [] |

**Pesan error:** apa yang terjadi, kenapa, dan apa yang bisa dilakukan user.

## 8. Aturan accessibility (pekan 7)

- [aturan dari temuan usability test dan cek accessibility, misalnya "setiap icon button punya label"]

## 9. Design system (pekan 8)

[Rapikan bagian 5–8 menjadi aturan pemakaian: kapan memakai component apa, dan larangannya.]

## 10. Aturan untuk Claude Code

- Kerjakan satu section per permintaan.
- Jangan menambah section, halaman, atau fitur yang tidak tertulis di dokumen ini.
- Pakai isi dari `briefs/<brief>/data/`. Jangan mengarang teks atau angka.
- Kondisi tidak ideal disimulasikan, karena tidak ada backend: setiap layar menerima `?state=loading`, `?state=kosong`, `?state=error`, `?state=sebagian`, dan `?state=gagal` (aksi gagal), dan loading memakai jeda buatan yang singkat. Tanpa parameter, layar menampilkan kondisi ideal.
- HTML, CSS, dan JS polos. Tanpa framework, tanpa build step, tanpa backend.
- Daftar dan masuk tetap dibangun sebagai flow: form, validasi saat mengisi, pesan password salah (`?state=gagal`), dan berhasil masuk. Semuanya disimulasikan: input apa pun yang valid diterima, lalu user masuk sebagai user di `user.json`. Jangan menyimpan password atau membuat akun sungguhan.
- Website di `website/`, web app di `app/`. Keduanya memakai `tokens.css` yang sama.
- HTML semantik: urutan heading benar, tombol memakai `<button>`, link memakai `<a>`, setiap input punya label.
- Kalau ada yang belum jelas di dokumen ini, tanyakan dulu.
