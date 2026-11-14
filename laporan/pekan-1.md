# Laporan Pekan 1 · Dokumen kedua project

## 1. Progres

- [x] 1.1 Pilih brief dari fasilitator — Brief A (Kelasku)
- [x] 1.2 Pahami brief-mu: prioritas masalah dan sikap saat bertabrakan
- [x] 1.3 Isi yang menjawab masalah M1–M3 website
- [x] 1.4 Tandai titik di flow kunci yang butuh validasi, loading, atau pesan error
- [ ] 1.5 Laporan pekan ini — sedang disusun, menunggu refleksi

## 2. Keputusan design

**Prioritasku (langkah 1.2):**

> - **Website:** M3 paling mengancam goal, karena kalau tidak terjawab, pengunjung akan menyebarkan rating yang buruk tentang produk ini
> - **Web app:** M3 paling mengancam goal, sebab jika merasa tidak ada kemajuan, maka mereka akan berhenti di tengah jalan
> - **Saat bertabrakan:** di halaman pembayaran, bisnis ingin user subscribe, sedangkan user takut dengan harganya yang mahal di bulan-bulan selanjutnya. Kalau bisnis didahulukan, user akan keluar dari halaman tanpa subscribe. Kalau user didahulukan, bisnis rentan kehilangan user yang ingin subscribe. Aku mendahulukan user, dan tampilannya menjawab keduanya dengan kalimat yang ringkas untuk hal-hal krusial, lalu ada tombol subscribe untuk memudahkan user

**Isi yang menjawab masalah website (langkah 1.3):**

> - M1: pengunjung perlu melihat kursus yang cocok dengan tujuan belajarnya (dipetakan dari 6 kategori: Presentasi, Menulis di tempat kerja, Bahasa Inggris untuk kerja, Interview, Negosiasi, Memimpin tim), isinya dari data/courses.json, disaring lewat pertanyaan singkat tentang tujuan belajar (asumsi).
> - M2: pengunjung perlu melihat kapan tanggal uji coba berakhir, dan catatan bahwa tagihan mulai setelah tanggal itu, isinya dari brief (durasi trial 7 hari) dan data/plans.json (harga paket). Selama trial hanya beberapa course awal yang terbuka (asumsi).
> - M3: pengunjung perlu melihat testimoni orang yang sudah ikut kursusnya beserta rolenya (misalnya Frontend developer, Backend developer), isinya dari data/testimonials.json.

**Titik yang butuh validasi, loading, atau pesan error (langkah 1.4):**

> - F1 langkah 3 (Daftar): butuh validasi email dan kriteria password, karena kalau formatnya salah, user tidak bisa lanjut dan perlu muncul pesan validasi supaya dia tahu apa yang salah.
> - F1 langkah 3 (Daftar, klik tombol Daftar): butuh loading dan tombol nonaktif setelah diklik sekali, karena kalau diklik dua kali bisa memicu error saat registrasi.
> - F1 langkah 3 (Daftar, proses gagal): butuh pesan error, dan input atau pilihan user tidak boleh hilang, karena user tidak perlu mengisi kembali.
> - F2 langkah 2 (Rekomendasi kursus di akhir onboarding, klik untuk mulai course): tidak perlu loading/tombol nonaktif khusus, karena kalau diklik dua kali, user tetap terhubung dengan satu course yang sama.
> - F2 langkah 2 (course gagal masuk ke daftar course saya): butuh pesan error, karena request yang dikirim gagal sampai (misalnya koneksi terputus).
> - F3 langkah 4 (Uji coba hampir habis, user lanjut belajar course yang masih trial): butuh pesan peringatan, karena kalau tidak muncul, user akan merasa kecewa dan ditipu saat course-nya tiba-tiba terkunci.

## 3. Cara mengarahkan Claude Code

Permintaan kunci dikutip dari log (`laporan/pekan-1-log.md`):

- 1.2: *"[M3] paling mengancam goal, karena kalau tidak terjawab, pengunjung akan menyebarkan rating yang buruk tentang produk ini"* (dan jawaban lanjutan untuk 4 pertanyaan berikutnya) — diterima langsung, tanpa iterasi.
- 1.3: *"M1 - ... disuguhkan dengan pertanyaan2 apa yg kamu cari / ingin menambah skill? ... direkomendasikan course2 dari data/courses.json"* — mekanisme (quiz rekomendasi) diterima sebagai asumsi, lalu disusun ke format template.
- 1.3: *"M3: pengunjung perlu melihat daftar testimonial orang2 yang sudah mengikuti coursenya serta skrg kerja dmn"* — direvisi 1 iterasi, karena `data/testimonials.json` tidak punya field tempat kerja, hanya role.
- 1.4: jawaban awal untuk F1 menyebut halaman login dan SSO ("klik tombol register/login", "jika login") — direvisi 1 iterasi, karena brief tidak punya halaman login (F1 cuma punya langkah Daftar, F3 dianggap user sudah masuk).
- 1.4: setelah revisi, peserta menjawab titik rawan F1–F3 bertahap satu per satu (bukan mengulang jawaban gabungan yang sama), termasuk memutuskan satu titik (F2, klik course rekomendasi) tidak perlu loading karena aksinya idempoten.

Pola yang terlihat: untuk 1.3 dan 1.4, peserta memperbaiki isi rencananya dulu (ganti sumber data, hapus bagian di luar scope) sebelum melanjutkan ke pertanyaan berikutnya, bukan hanya mengulang permintaan yang sama.

## 4. Feedback dan tindak lanjut

- **1.2:** feedback `/cek` — setiap pilihan sudah punya alasan dari sisi user dengan kata-kata sendiri. Diterima tanpa perubahan.
- **1.3:** feedback — ketiga masalah sudah punya isi spesifik dengan sumber jelas. Tindak lanjut: M3 diganti dari "kerja dimana" menjadi "role" karena datanya tidak mendukung klaim tempat kerja.
- **1.4:** feedback — ketiga jenis titik rawan (validasi, loading, pesan error) terisi dengan alasan dari sisi user. Tindak lanjut: bagian F1 direvisi menghapus referensi login/SSO yang di luar scope brief.

## 5. Refleksi

**Keputusan tersulit pekan ini, dan kenapa:** memikirkan seluruh flow unhappy path. Menurut saya itu sulit karena ada banyak kemungkinan buruk yang dapat terjadi.

**Satu hal yang akan dilakukan berbeda:** mencari banyak referensi agar saya tahu platform KelasKu mana yang cocok untuk behaviour masyarakat Indonesia.
