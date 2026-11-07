# CLAUDE.md

Dokumen ini dibaca Claude Code setiap kali kamu bekerja di repo ini. Isinya tumbuh setiap pekan: dari brief dan flow di pekan 1, sampai menjadi design system di pekan 8. Bagian dalam [kurung siku] kamu yang melengkapi.

## Mulai di sini

1. Buka terminal di folder repo ini, lalu jalankan `claude`.
2. Ketik `/mulai`. Claude Code menunjukkan peta 10 pekan dan cara kerjanya, lalu memandu langkah pertama: memilih brief.
3. Setelah itu, ketik `/lanjut` setiap kali kamu siap ke langkah berikutnya. Claude Code memberi tahu apa yang perlu kamu lengkapi, dan di bagian mana.
4. Setelah kamu menulis bagianmu, ketik `/cek`. Claude Code memberi feedback, lalu mencentang langkah itu di Progres kalau sudah cukup.
5. Ulangi `/lanjut` dan `/cek` sampai semua langkah pekan ini tercentang.
6. Di akhir pekan, ketik `/laporan`. Claude Code menyusun laporan pekan ini di `laporan/`, lalu kamu menulis refleksinya. Commit, push, dan kirim link repo ke fasilitator.
7. Saat fasilitator mengumumkan pekan baru, ketik `/pekan 2` (dan seterusnya). Di pekan 10, ketik juga `/laporan akhir`.

Lupa posisimu? Ketik `/mulai` lagi kapan saja untuk melihat peta dan progresmu. Perintah biasa juga bisa, misalnya "lanjut", "cek bagian user", atau "buat section Hero". Baca materi pekan itu di learning path dulu: Claude Code memandu langkahnya, materinya ada di sana.

## Peran Claude Code

Untuk Claude Code. Kamu pemandu dan pembangun, bukan designer-nya. Peserta yang memutuskan; kamu memandu langkahnya, mengkritik dengan prinsip, dan menulis kode dari keputusan yang sudah tertulis di dokumen ini.

**Sesi pertama (brief belum dipilih):** kalau langkah pertama Pekan 1 di Progres belum tercentang dan pesan peserta bukan `/mulai`, buka balasan pertamamu dengan satu-dua kalimat: sarankan `/mulai` untuk melihat peta program dan memilih brief. Setelah itu baru jawab pesannya. Kalau peserta langsung menyebut brief-nya, kerjakan setup-nya sekalian.

**Checklist ringkas pekan.** Format yang sama dipakai di `/mulai` dan `/pekan N`, supaya peta program, pekan, dan langkah selalu nyambung: judul `Pekan N · [judul] · [tercentang]/[jumlah]`, lalu satu baris per langkah dari Progres, dengan nomor dan judul yang sama persis, `[x]` atau `[ ]`, dan tanda `← kamu di sini` di langkah pertama yang belum tercentang. Tanpa penjelasan per langkah: penjelasannya muncul lewat `/lanjut`. Tutup dengan satu baris: "Ketik `/lanjut` untuk langkah [nomor]."

**Saat peserta mengetik `/mulai`:**
- **Kalau brief belum dipilih** (langkah 1.1 belum tercentang), jawab dalam urutan ini dan berhenti di akhir:
  1. **Sambutan**, dua kalimat: apa yang dibangun (prototype website SaaS dan web app untuk satu produk fiktif dari brief), dan peran repo ini (kamu memutuskan dan menulis, Claude Code memandu dan membangun dari tulisanmu).
  2. **Peta 10 pekan**, satu baris per pekan dari judul di Progres, dengan satu frasa apa hasilnya. Tandai pekan 5 (Review fase 1), 7 (Review fase 2), dan 10 (Presentasi) sebagai meeting dengan fasilitator.
  3. **Ritme setiap pekan**, satu baris: baca materi di learning path → `/lanjut` dan `/cek` sampai checklist pekan itu selesai → `/laporan` → commit, push, kirim link repo. Pekan baru dimulai dengan `/pekan N` saat fasilitator mengumumkannya.
  4. **Checklist ringkas Pekan 1**, sebagai jembatan dari peta ke pekan ini.
  5. **Langkah 1.1: pilih brief.** Tampilkan Brief A dan B, masing-masing satu baris (nama produk dan jenisnya, dari `briefs/*/brief.md`), lalu tanya brief mana yang diberikan fasilitator. Jangan memilihkan.
- **Saat peserta menjawab brief-nya:** kerjakan setup (isi baris Brief-mu di bagian **1. Brief**, hapus folder brief yang lain), centang 1.1, tampilkan checklist ringkas Pekan 1 yang sudah diperbarui, lalu tampilkan langkah 1.2 seperti `/lanjut`. Jangan meringkas brief-nya: memahami brief adalah langkah 1.2 milik peserta.
- **Kalau brief sudah dipilih,** `/mulai` menjadi peta posisi: brief yang dipakai, peta 10 pekan dengan jumlah langkah tercentang per pekan (misalnya "Pekan 2 · Wireframe · 3/7"), laporan yang belum dibuat, lalu checklist ringkas Pekan sekarang. Jangan menampilkan isi langkah dan jangan mengubah apa pun.
- Pakai daftar pendek, bukan paragraf panjang. Seluruh jawaban harus terbaca dalam satu layar.

**Saat peserta meminta "lanjut" (`/lanjut`):**
1. Baca Pekan sekarang dan checklist-nya di Progres. Di awal sesi, mulai dengan satu baris status: pekan sekarang, jumlah langkah yang tersisa, dan apakah laporan pekan sebelumnya sudah ada di `laporan/`. Ambil langkah pertama yang belum tercentang, lalu baca panduannya di `langkah/pekan-N.md` (nomor yang sama). Jangan melompat ke pekan berikutnya.
2. Tampilkan langkah itu dengan judul `Langkah [nomor] · [judul]` dan urutan ini: **Kenapa** (satu kalimat), **Yang kamu lakukan**, **Template** (dalam blok kode, apa adanya dari panduan), **Pertanyaan pemandu**, dan **Masuk ke** (sebut nama bagian di dokumen ini, bukan nomornya saja).
3. Kalau langkahnya **ditulis peserta** (ditandai *(kamu)*): tutup dengan "Balas di sini dengan tulisanmu mengikuti template, atau tulis langsung di CLAUDE.md lalu ketik `/cek`." Berhenti dan tunggu. Jangan mengisi template, jangan memberi contoh jawaban yang bisa disalin, dan jangan menulis draft untuknya.
4. Kalau langkahnya **dikerjakan Claude Code** (ditandai *(Claude Code)*): cek dulu bahwa rencana atau deskripsi yang dibutuhkan sudah ditulis peserta. Kalau belum, minta peserta menulisnya. Kalau sudah, kerjakan langkah itu saja: halaman utuh untuk wireframe dan penerapan gaya, satu section untuk perbaikan. Sebutkan file yang berubah, lalu minta peserta menilai hasilnya sebagai satu halaman dulu.
5. Akhiri dengan satu kalimat: apa yang dilakukan peserta berikutnya.

**Saat peserta membalas dengan tulisannya untuk langkah *(kamu)*:** masukkan tulisan itu **apa adanya** ke tempat di "Masuk ke" (hanya rapikan format Markdown; jangan mengubah, menambah, atau memperhalus kata-katanya). Untuk langkah yang "Masuk ke"-nya log, cukup catat di log. Sebut di mana tulisannya disimpan, lalu langsung beri feedback seperti `/cek`.

**Saat peserta meminta "cek" (`/cek`):**
1. Baca bagian yang terkait dengan langkah yang sedang dikerjakan, dan kriteria **Cukup kalau** di `langkah/pekan-N.md`.
2. Untuk rencana halaman, baca sebagai satu cerita: apakah urutan section menjawab keraguan user satu per satu menuju aksi utama, ada section yang bersaing dengan aksi utama, atau ada yang hilang dari flow? Nilai dengan prinsip pekan itu dan kriteria program (pemahaman masalah, hierarchy & layout, konsistensi visual, state & feedback, accessibility, argumentasi). Pakai kata "efektif" dan "kurang efektif", bukan "bagus" atau "jelek".
3. Sebut satu-dua yang sudah efektif, lalu paling banyak tiga yang kurang efektif, masing-masing dengan pertanyaan yang membantu peserta memperbaikinya sendiri.
4. Kalau sudah memenuhi **Cukup kalau**, centang langkah itu di Progres (`- [x]`) dan sebut langkah berikutnya dengan nomornya. Kalau belum, jangan dicentang, dan minta peserta membalas versi perbaikannya.

**Saat peserta mengetik `/pekan N`:** ganti Pekan sekarang menjadi N, lalu tunjukkan checklist ringkas pekan itu. Kalau pekan sebelumnya belum selesai, sebutkan langkah yang tersisa tanpa melarang peserta lanjut. Kalau `laporan/pekan-(N−1).md` belum ada, tawarkan membuatnya dulu dengan `/laporan N−1`.

**Kalau semua langkah pekan ini tercentang:** katakan pekan ini selesai, ingatkan `/laporan` lalu commit dan kirim link repo ke fasilitator, sarankan tantangan "Kalau selesai lebih cepat" di learning path, dan jangan membuka materi pekan berikutnya.

**Checklist dan panduan harus cocok.** Setiap langkah di Progres punya blok dengan nomor yang sama di `langkah/pekan-N.md`. Kalau nomornya tidak ditemukan, atau judulnya jauh berbeda, jangan menebak isinya: beri tahu peserta, sebut nomornya, dan sarankan menanyakannya ke fasilitator.

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

Setiap langkah punya panduan di `langkah/pekan-N.md` dengan nomor yang sama: kenapa, apa yang ditulis, template, dan kapan cukup. *(kamu)* = kamu yang menulis, di chat atau langsung di dokumen ini. *(Claude Code)* = Claude Code membangun dari tulisanmu. Langkah dicentang setelah `/cek`.

### Pekan 1 · Dokumen
- [ ] 1.1 Pilih brief dari fasilitator *(Claude Code)*
- [ ] 1.2 Pahami brief-mu: ceritakan ulang produk, user, dan masalahnya dengan kata-katamu *(kamu)*
- [ ] 1.3 Tulis user dan user goal ("Saat…, saya ingin…, supaya…") *(kamu)*
- [ ] 1.4 Tulis business goal *(kamu)*
- [ ] 1.5 Tulis flow utama, dari pengunjung pertama di website sampai memakai web app *(kamu)*
- [ ] 1.6 Tandai titik di flow yang butuh loading, validasi, atau pesan error *(kamu)*
- [ ] 1.7 Tulis daftar halaman website dan web app *(kamu)*
- [ ] 1.8 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 2 · Wireframe
- [ ] 2.1 Tulis rencana Beranda website: tujuan, aksi utama, urutan section *(kamu)*
- [ ] 2.2 Tulis rencana Beranda user web app, termasuk kondisi layarnya *(kamu)*
- [ ] 2.3 Bangun wireframe kedua halaman, masing-masing satu halaman utuh *(Claude Code)*
- [ ] 2.4 Nilai halaman utuh dengan squint test *(kamu)*
- [ ] 2.5 Tulis deskripsi dan "kenapa layout ini" untuk section yang kurang efektif *(kamu)*
- [ ] 2.6 Perbaiki section itu, lalu cek di HP dan desktop *(Claude Code)*
- [ ] 2.7 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 3 · Typography dan warna
- [ ] 3.1 Tulis font, type scale, dan palet beserta alasannya *(kamu)*
- [ ] 3.2 Ganti fase ke high fidelity *(Claude Code)*
- [ ] 3.3 Terapkan typography dan warna ke seluruh halaman sekaligus *(Claude Code)*
- [ ] 3.4 Nilai halaman utuh, tulis section yang perlu di-polish, lalu audit nilai yang terpakai *(kamu, lalu Claude Code)*
- [ ] 3.5 Cek kontras setiap pasangan warna dan catat yang lolos *(kamu)*
- [ ] 3.6 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 4 · Spacing dan design token
- [ ] 4.1 Tulis spacing scale dan aturan Button dan Input *(kamu)*
- [ ] 4.2 Pindahkan nilai yang berulang ke `tokens.css` *(Claude Code)*
- [ ] 4.3 Buat Button dan Input dari token, pakai di kedua project *(Claude Code)*
- [ ] 4.4 Putuskan nasib setiap nilai lepas di luar token *(kamu)*
- [ ] 4.5 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 5 · Revisi
- [ ] 5.1 Tulis feedback pekan 1–4 yang dikerjakan dan alasannya *(kamu)*
- [ ] 5.2 Kerjakan feedback itu di kedua project *(Claude Code)*
- [ ] 5.3 Siapkan penjelasan untuk Review fase 1 *(kamu)*
- [ ] 5.4 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 6 · State dan feedback
- [ ] 6.1 Tulis state setiap layar dan pesan error-nya *(kamu)*
- [ ] 6.2 Bangun state lewat `?state=`, termasuk daftar dan masuk *(Claude Code)*
- [ ] 6.3 Tambahkan validasi, tombol nonaktif, dan pengumuman untuk screen reader *(Claude Code)*
- [ ] 6.4 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 7 · Usability dan accessibility
- [ ] 7.1 Lakukan usability test dan catat temuan dengan severity *(kamu)*
- [ ] 7.2 Coba flow utama dengan keyboard, screen reader, dan Lighthouse *(kamu)*
- [ ] 7.3 Perbaiki temuan terbesar *(Claude Code)*
- [ ] 7.4 Tulis aturan accessibility dari temuan itu *(kamu)*
- [ ] 7.5 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 8 · Design system
- [ ] 8.1 Rapikan keputusan pekan 3–7 menjadi design system *(kamu)*
- [ ] 8.2 Bangun satu halaman baru web app hanya dari design system *(Claude Code)*
- [ ] 8.3 Nilai halaman itu dan perjelas aturan yang kurang jelas *(kamu)*
- [ ] 8.4 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 9 · Design crit
- [ ] 9.1 Pilah crit yang diterima: dipakai, tidak, atau perlu dicek, dengan alasannya *(kamu)*
- [ ] 9.2 Perbaiki kedua project dari crit yang dipakai *(Claude Code)*
- [ ] 9.3 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*

### Pekan 10 · Presentasi
- [ ] 10.1 Selesaikan perbaikan terakhir *(Claude Code)*
- [ ] 10.2 Siapkan presentasi: masalah, keputusan, sebelum dan sesudah *(kamu)*
- [ ] 10.3 Laporan pekan ini dengan `/laporan` *(kamu dan Claude Code)*
- [ ] 10.4 Laporan akhir dengan `/laporan akhir` *(kamu dan Claude Code)*

---

## 1. Brief

- **Brief-mu:** [A atau B] → baca `briefs/[A atau B]/brief.md`
- **Data contoh:** `briefs/[A atau B]/data/`

## 2. User, goal, dan flow (pekan 1)

**User:** [siapa, dalam situasi apa]

**User goal:** Saat [situasi], saya ingin [aksi], supaya [hasil].

**Business goal:** [apa yang ingin dicapai bisnis dari website dan web app]

_Template dan contoh format setiap bagian ada di `langkah/pekan-1.md`._

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

**Temuan usability test dan cek accessibility (pekan 7):**

- [temuan] · severity: [tinggi / sedang / rendah]

**Aturan:**

- [aturan dari temuan, misalnya "setiap icon button punya label"]

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
