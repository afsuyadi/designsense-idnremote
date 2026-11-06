# Starter kit · Sense of UI/UX untuk Developer

Repo awal untuk kedua project program: **website SaaS** (P1) dan **web app** (P2). Keduanya prototype interaktif di kode, bukan produk lengkap: HTML, CSS, dan JS dengan data contoh, tanpa backend, login sungguhan, atau database. Kamu membangunnya dengan Claude Code: kamu menentukan struktur, isi, dan alasannya, Claude Code menulis kodenya.

## Mulai di pekan 1

1. Buat repo sendiri dari template ini (tombol **Use this template** di GitHub), lalu clone.
2. Fasilitator memberi tahu brief-mu: **A** atau **B**. Baca `briefs/A/brief.md` atau `briefs/B/brief.md`.
3. Buka `CLAUDE.md`, isi baris **Brief-mu**, lalu hapus folder brief yang bukan milikmu.
4. Lengkapi bagian pekan 1 di `CLAUDE.md`: user, goal, flow, dan daftar halaman.

## Isi repo

```
CLAUDE.md        Kerangka yang kamu lengkapi setiap pekan. Claude Code membacanya otomatis.
briefs/A/        Brief A: brief.md dan data contoh (data/*.json)
briefs/B/        Brief B: brief.md dan data contoh (data/*.json)
tokens.css       Design token. Kosong sampai pekan 4.
website/         P1 · Website SaaS
app/             P2 · Web app
```

## Tiga fase

| Fase | Pekan | Hasilnya |
|---|---|---|
| Dokumen | 1 | User, goal, flow, dan daftar halaman di `CLAUDE.md`. Belum ada UI. |
| Wireframe | 2 | Halaman HTML abu-abu dari deskripsi section-mu. Yang dinilai hanya struktur. |
| High fidelity | 3–10 | Typography, warna, token, state, dan accessibility, ditambahkan bertahap. |

Fase yang sedang berjalan ditulis di `CLAUDE.md`, dan kamu sendiri yang menggantinya. Claude Code mengikuti aturan fase itu.

## Cara bekerja dengan Claude Code

- Kerjakan **satu section per permintaan**, bukan satu halaman sekaligus.
- Sebelum meminta, tulis dulu deskripsi section itu di `CLAUDE.md`: tujuan, isi, referensi, dan aksi utamanya.
- Setelah hasilnya keluar, nilai dengan prinsip pekan itu. Kalau kurang efektif, perbaiki deskripsinya atau prompt-mu, lalu minta lagi.
- Isi **"Kenapa layout ini"** di setiap section. Bagian ini yang dinilai, bukan hanya tampilannya.

## Menjalankan

Semua halaman HTML, CSS, dan JS polos, tanpa build step dan tanpa backend. Isi diambil dari `briefs/<brief-mu>/data/`.

```bash
python3 -m http.server 8000
```

Lalu buka `http://localhost:8000/website/` dan `http://localhost:8000/app/`.

Kondisi yang tidak ideal disimulasikan lewat URL, misalnya `http://localhost:8000/app/?state=error` atau `?state=kosong`. Prototype tetap menunjukkan perjalanan user lengkap: onboarding, happy path, edge case, loading, kosong, error, aksi berhasil, dan aksi gagal.

## Mengirim tugas

Tugas setiap pekan dikirim langsung ke fasilitator, bersama hasil Track Taste: link repo-mu dan catatan singkat apa yang berubah. Feedback-nya juga langsung ke kamu.
