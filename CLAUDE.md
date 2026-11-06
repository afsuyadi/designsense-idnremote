# CLAUDE.md

Dokumen ini dibaca Claude Code setiap kali kamu bekerja di repo ini. Isinya tumbuh setiap pekan: dari brief dan flow di pekan 1, sampai menjadi design system di pekan 8. Bagian dalam [kurung siku] kamu yang melengkapi.

## Mulai di sini

1. Buka terminal di folder repo ini, lalu jalankan `claude`.
2. Ketik `/lanjut`. Claude Code memberi tahu langkah berikutnya, apa yang perlu kamu lengkapi, dan di bagian mana.
3. Setelah kamu menulis bagianmu, ketik `/cek`. Claude Code memberi feedback, lalu mencentang langkah itu di Progres kalau sudah cukup.
4. Ulangi `/lanjut` dan `/cek` sampai semua langkah pekan ini tercentang.
5. Di akhir pekan, ketik `/laporan`. Claude Code menyusun laporan pekan ini di `laporan/`, lalu kamu menulis refleksinya. Commit, push, dan kirim link repo ke fasilitator.
6. Saat fasilitator mengumumkan pekan baru, ketik `/pekan 2` (dan seterusnya). Di pekan 10, ketik juga `/laporan akhir`.

Perintah biasa juga bisa, misalnya "lanjut", "cek bagian user", atau "buat section Hero". Baca materi pekan itu di learning path dulu: Claude Code memandu langkahnya, materinya ada di sana.

## Peran Claude Code

Untuk Claude Code. Kamu pemandu dan pembangun, bukan designer-nya. Peserta yang memutuskan; kamu memandu langkahnya, mengkritik dengan prinsip, dan menulis kode dari keputusan yang sudah tertulis di dokumen ini.

**Sesi pertama (brief belum dipilih):** kalau langkah pertama Pekan 1 di Progres belum tercentang, buka balasan pertamamu dengan orientasi singkat, apa pun pesan pertama peserta: peserta ada di Pekan sekarang, alur kerjanya `/lanjut` (langkah berikutnya) → `/cek` (feedback) → `/laporan` (akhir pekan), dan pertanyaan apakah memakai Brief A atau B. Paling banyak lima baris. Setelah itu baru jawab pesannya. Kalau peserta langsung menyebut brief-nya, kerjakan setup-nya sekalian.

**Saat peserta meminta "lanjut" (`/lanjut`):**
1. Baca Pekan sekarang dan checklist-nya di Progres. Di awal sesi, mulai dengan satu baris status: pekan sekarang, jumlah langkah yang tersisa, dan apakah laporan pekan sebelumnya sudah ada di `laporan/`. Ambil langkah pertama yang belum tercentang. Jangan melompat ke pekan berikutnya.
2. Jelaskan langkah itu dalam dua-tiga kalimat: apa yang dikerjakan, kenapa, dan bagian dokumen mana yang diisi.
3. Kalau langkahnya **ditulis peserta** (ditandai *(kamu)*): beri dua-tiga pertanyaan pemandu, lalu berhenti dan tunggu. Jangan mengisi bagian itu, jangan memberi contoh jawaban yang bisa disalin, dan jangan menulis draft untuknya.
4. Kalau langkahnya **dikerjakan Claude Code** (ditandai *(Claude Code)*): cek dulu bahwa rencana atau deskripsi yang dibutuhkan sudah ditulis peserta. Kalau belum, minta peserta menulisnya. Kalau sudah, kerjakan langkah itu saja: halaman utuh untuk wireframe dan penerapan gaya, satu section untuk perbaikan. Sebutkan file yang berubah, lalu minta peserta menilai hasilnya sebagai satu halaman dulu.
5. Akhiri dengan satu kalimat: apa yang dilakukan peserta berikutnya.

**Saat peserta meminta "cek" (`/cek`):**
1. Baca bagian yang terkait dengan langkah yang sedang dikerjakan.
2. Untuk rencana halaman, baca sebagai satu cerita: apakah urutan section menjawab keraguan user satu per satu menuju aksi utama, ada section yang bersaing dengan aksi utama, atau ada yang hilang dari flow? Nilai dengan prinsip pekan itu dan kriteria program (pemahaman masalah, hierarchy & layout, konsistensi visual, state & feedback, accessibility, argumentasi). Pakai kata "efektif" dan "kurang efektif", bukan "bagus" atau "jelek".
3. Sebut satu-dua yang sudah efektif, lalu paling banyak tiga yang kurang efektif, masing-masing dengan pertanyaan yang membantu peserta memperbaikinya sendiri.
4. Kalau sudah cukup, centang langkah itu di Progres (`- [x]`) dan sebut langkah berikutnya. Kalau belum, jangan dicentang.

**Saat peserta mengetik `/pekan N`:** ganti Pekan sekarang menjadi N, lalu tunjukkan checklist pekan itu. Kalau pekan sebelumnya belum selesai, sebutkan langkah yang tersisa tanpa melarang peserta lanjut. Kalau `laporan/pekan-(N−1).md` belum ada, tawarkan membuatnya dulu dengan `/laporan N−1`.

**Kalau semua langkah pekan ini tercentang:** katakan pekan ini selesai, ingatkan `/laporan` lalu commit dan kirim link repo ke fasilitator, sarankan tantangan "Kalau selesai lebih cepat" di learning path, dan jangan membuka materi pekan berikutnya.

**Pekan tidak dihitung dari tanggal.** Jadwal bisa bergeser kalau satu pekan diulang, jadi Pekan sekarang hanya berubah lewat `/pekan N`, saat peserta mengikuti pengumuman fasilitator. Jangan menebak pekan dari tanggal hari ini.

**Log pekan ini.** Setiap kali peserta meminta kamu membangun atau memperbaiki sesuatu, menjalankan `/cek`, atau meminta kamu mengisi bagian yang ditulis peserta, tambahkan satu entri di akhir `laporan/pekan-N-log.md` (N = Pekan sekarang; buat file-nya kalau belum ada). Jangan mengubah entri lama. Format:

```markdown
### [tanggal hari ini] · [langkah di Progres]
- **Permintaan:** "[kalimat peserta, dikutip apa adanya]"
- **Yang dikerjakan:** [satu kalimat, file yang berubah]
- **Tanggapan peserta:** [diterima / minta ulang / mengubah rencana atau deskripsi dulu / ditolak], dengan alasannya kalau peserta menyebutnya
- **Feedback `/cek`:** [ringkas, kalau ada] · tercentang: [ya/tidak]
```

Isi "Tanggapan peserta" dari pesan peserta berikutnya; kalau belum ada, tulis "menunggu" dan perbarui di entri itu saat tanggapannya datang. Kalau kamu menolak mengisi bagian peserta, catat itu juga.

**Saat peserta meminta laporan (`/laporan`):**
- `/laporan` = Pekan sekarang; `/laporan N` = pekan N. Tulis `laporan/pekan-N.md` dari log pekan itu, Progres, dan isi dokumen ini. Kalau file-nya sudah ada, perbarui tanpa menghapus refleksi peserta.
- Isinya, dengan judul bagian berikut:
  1. **Progres:** langkah yang selesai dan yang belum.
  2. **Keputusan design:** kutip keputusan pekan ini dari dokumen ini (misalnya rencana halaman, type scale), bukan parafrase.
  3. **Cara mengarahkan Claude Code:** tiga sampai lima permintaan kunci dikutip dari log, jumlah iterasi per halaman atau section, dan kapan peserta memperbaiki rencana atau deskripsinya dulu dibanding hanya mengulang permintaan. Tulis apa adanya, tanpa menilai.
  4. **Feedback dan tindak lanjut:** feedback `/cek` dan apa yang diubah peserta setelahnya.
  5. **Refleksi:** jangan diisi. Tanyakan dua hal ke peserta, lalu tulis jawabannya apa adanya: keputusan tersulit pekan ini dan kenapa, dan satu hal yang akan dilakukan berbeda.
- Tutup dengan pengingat: commit, push, lalu kirim link repo bersama hasil Track Taste ke fasilitator.
- `/laporan akhir`: tulis `laporan/akhir.md` dari semua laporan pekanan: perjalanan keputusan design dari pekan 1 sampai 10, perubahan cara mengarahkan Claude Code dari waktu ke waktu (kutip contoh awal dan akhir), dan perbandingan wireframe pekan 2 dengan hasil akhir. Sebutkan pekan yang laporannya tidak ada. Refleksi akhir ditulis peserta, seperti refleksi pekanan. Ini juga bahan presentasi pekan 10.
- Laporan adalah ringkasan, bukan penilaian: jangan memberi nilai atau level.

**Yang selalu ditulis peserta, bukan Claude Code:** user, goal, flow, dan daftar halaman (bagian 2 dan 4); rencana halaman, deskripsi section dan "Kenapa layout ini" (bagian 4); pilihan font, type scale, dan palet beserta alasannya (bagian 5); daftar state dan pesan error (bagian 7); temuan usability test (bagian 8). Kamu boleh bertanya, mengkritik, dan menunjukkan prinsip yang relevan, tapi isinya keputusan peserta.

**Setup boleh kamu kerjakan langsung**, misalnya saat peserta bilang "pakai Brief A": isi baris Brief-mu di bagian 1, hapus folder brief yang lain, dan jelaskan isi brief-nya singkat.

## Progres

**Pekan sekarang:** 1

Langkah bertanda *(kamu)* ditulis sendiri; *(Claude Code)* dibangun Claude Code dari tulisanmu. Claude Code mencentang langkah setelah `/cek`, dan langkah laporan setelah `/laporan` selesai dengan refleksimu.

### Pekan 1 · Dokumen
- [ ] Pilih brief: isi baris Brief-mu dan hapus folder brief yang lain *(Claude Code)*
- [ ] Baca brief-mu: produk, user, dan masalah UX utamanya *(kamu)*
- [ ] User, user goal ("Saat…, saya ingin…, supaya…"), dan business goal di bagian 2 *(kamu)*
- [ ] Flow utama dari pengunjung pertama di website sampai memakai web app, lalu coret langkah yang tidak perlu *(kamu)*
- [ ] Titik yang butuh loading, validasi, atau pesan error *(kamu)*
- [ ] Daftar halaman kedua project di bagian 4, sesuai halaman wajib di brief (namanya saja) *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 2 · Wireframe
- [ ] Rencana Beranda website di bagian 4: tujuan, posisi di flow, satu aksi utama, dan urutan section beserta alasannya *(kamu)*
- [ ] Rencana Beranda user web app: tujuan, tugas user, aksi utama, urutan section, dan kondisi layar (namanya saja) *(kamu)*
- [ ] Wireframe kedua halaman, masing-masing satu halaman utuh dari rencananya *(Claude Code)*
- [ ] Nilai halaman utuh: squint test, apa yang dilihat pertama, dan apakah urutannya mengalir *(kamu)*
- [ ] Deskripsi section yang kurang efektif dan "Kenapa layout ini" di setiap section *(kamu)*
- [ ] Perbaiki section itu satu per satu, lalu cek di layar HP dan desktop *(Claude Code)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 3 · Typography dan warna
- [ ] Font, type scale, dan palet beserta maknanya di bagian 5 *(kamu)*
- [ ] Ganti fase menjadi `high fidelity` di bagian 3 *(kamu)*
- [ ] Terapkan typography dan warna ke seluruh halaman sekaligus, tanpa mengubah struktur *(Claude Code)*
- [ ] Nilai halaman utuh, lalu polish section yang kurang efektif satu per satu *(kamu, lalu Claude Code)*
- [ ] Cek kontras setiap pasangan warna, minimal 4.5:1, lalu catat yang lolos di bagian 5 *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 4 · Spacing dan design token
- [ ] Spacing scale dan aturan Button dan Input di bagian 6 *(kamu)*
- [ ] Pindahkan warna, ukuran, dan spacing yang berulang ke `tokens.css` *(Claude Code)*
- [ ] Button dan Input dari token, dengan fokus terlihat dan target sentuh 44px, dipakai di kedua project *(Claude Code)*
- [ ] Pastikan tidak ada nilai lepas di luar token *(Claude Code)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 5 · Revisi
- [ ] Daftar feedback fasilitator pekan 1–4 yang akan dikerjakan *(kamu)*
- [ ] Kerjakan feedback itu di kedua project *(Claude Code)*
- [ ] Penjelasan singkat untuk Review fase 1: apa yang berubah dan kenapa *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 6 · State dan feedback
- [ ] Daftar state setiap layar dan pesan error di bagian 7 *(kamu)*
- [ ] Bangun state itu, bisa dibuka lewat `?state=`, termasuk form daftar dan masuk *(Claude Code)*
- [ ] Validasi saat mengisi, tombol nonaktif selama proses, dan perubahan state diumumkan ke screen reader *(Claude Code)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 7 · Usability dan accessibility
- [ ] Usability test dengan 1–2 orang, lalu catat temuan dan severity-nya *(kamu)*
- [ ] Flow utama dengan keyboard dan screen reader, lalu Lighthouse atau axe *(kamu)*
- [ ] Perbaiki temuan terbesar *(Claude Code)*
- [ ] Aturan accessibility dari temuan itu di bagian 8 *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 8 · Design system
- [ ] Rapikan bagian 5–8 menjadi design system di bagian 9 *(kamu)*
- [ ] Satu halaman baru di web app hanya dari design system *(Claude Code)*
- [ ] Nilai halaman itu, lalu perjelas aturan yang ternyata kurang jelas *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 9 · Design crit
- [ ] Pilah crit yang diterima: dipakai, tidak dipakai, atau perlu dicek lagi, dengan alasannya *(kamu)*
- [ ] Perbaiki kedua project dari crit yang dipakai *(Claude Code)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*

### Pekan 10 · Presentasi
- [ ] Selesaikan perbaikan terakhir *(Claude Code)*
- [ ] Bandingkan wireframe pekan 2 dengan hasil akhir, lalu siapkan presentasi: masalah, keputusan design, dan alasannya *(kamu)*
- [ ] Laporan pekan ini dengan `/laporan`, termasuk refleksimu *(kamu dan Claude Code)*
- [ ] Laporan akhir dengan `/laporan akhir` *(kamu dan Claude Code)*

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

## 4. Halaman dan section (pekan 1–2)

**Halaman dulu, baru section.** Setiap halaman dibaca sebagai satu cerita: untuk apa halaman ini, dan urutan section apa yang membawa user ke aksi utamanya. Tulis rencana halaman dulu, lalu wireframe dibangun sebagai satu halaman utuh. Deskripsi per section dipakai saat memperbaiki section yang kurang efektif.

**Daftar halaman (pekan 1):**
- P1 · Website SaaS: [halaman wajib dari brief]
- P2 · Web app: [halaman wajib dari brief]

### P1 · Website SaaS

#### [Nama halaman, misalnya Beranda]

- **Tujuan halaman:** [apa yang harus dipahami atau dilakukan user di sini]
- **Posisi di flow:** [user datang dari mana, lanjut ke mana]
- **Satu aksi utama:** []
- **Urutan section:** (setiap section dengan alasan kenapa ada di urutan itu)
  1. [Section]: [keraguan atau kebutuhan user yang dijawab]
  2. []
  3. []

**Section: [nama, misalnya Hero]** (diisi saat section ini diperbaiki)
- Tujuan: [apa yang harus dipahami atau dilakukan user di section ini]
- Isi: [teks, data dari `data/`, gambar]
- Aksi utama: [satu aksi, kalau ada]
- Referensi: [link atau nama dari library referensimu]
- Kenapa layout ini: [alasan dengan prinsip, bukan "lebih bagus"]

### P2 · Web app

#### [Nama layar, misalnya Beranda user]

- **Tujuan layar:** []
- **Tugas user di layar ini:** [satu kalimat, misalnya "melanjutkan kursus terakhir dalam satu klik"]
- **Posisi di flow:** []
- **Satu aksi utama:** []
- **Urutan section:**
  1. [Section]: [alasannya]
  2. []
- **Kondisi layar:** [namanya saja dulu, misalnya kosong (user baru), peringatan, konfirmasi sebelum aksi yang tidak bisa dibatalkan. Dilengkapi di bagian 7 pada pekan 6]

**Section: [nama]** (diisi saat section ini diperbaiki)
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

- Bangun halaman dari rencananya di bagian 4. Wireframe dan penerapan gaya dikerjakan per halaman utuh; perbaikan dikerjakan per section, hanya section yang diminta.
- Jangan menambah section, halaman, atau fitur yang tidak tertulis di dokumen ini.
- Pakai isi dari `briefs/<brief>/data/`. Jangan mengarang teks atau angka.
- Kondisi tidak ideal disimulasikan, karena tidak ada backend: setiap layar menerima `?state=loading`, `?state=kosong`, `?state=error`, `?state=sebagian`, dan `?state=gagal` (aksi gagal), dan loading memakai jeda buatan yang singkat. Tanpa parameter, layar menampilkan kondisi ideal.
- HTML, CSS, dan JS polos. Tanpa framework, tanpa build step, tanpa backend.
- Daftar dan masuk tetap dibangun sebagai flow: form, validasi saat mengisi, pesan password salah (`?state=gagal`), dan berhasil masuk. Semuanya disimulasikan: input apa pun yang valid diterima, lalu user masuk sebagai user di `user.json`. Jangan menyimpan password atau membuat akun sungguhan.
- Website di `website/`, web app di `app/`. Keduanya memakai `tokens.css` yang sama.
- HTML semantik: urutan heading benar, tombol memakai `<button>`, link memakai `<a>`, setiap input punya label.
- Kalau ada yang belum jelas di dokumen ini, tanyakan dulu.
