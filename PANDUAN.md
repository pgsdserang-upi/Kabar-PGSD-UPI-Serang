# Panduan Menambah Berita (untuk Kontributor)

Berita di portal ini ditulis dalam berkas teks sederhana. Menambah berita **tidak perlu dashboard** dan tidak perlu tahu pemrograman — cukup lewat website GitHub.

> Prasyarat: Anda punya akun GitHub dan sudah ditambahkan sebagai *collaborator* pada repositori ini (diatur oleh pengelola).

---

## A. Menambah satu berita baru

1. Buka repositori ini di **github.com**, lalu masuk ke folder **`_posts`**.
2. Klik tombol **Add file → Create new file** (di kanan atas).
3. Di kolom nama berkas, tulis nama dengan **format wajib**:

   ```
   TAHUN-BULAN-TANGGAL-judul-singkat.md
   ```

   Contoh: `2026-08-17-upacara-hut-ri.md`

   Aturan nama berkas:
   - Tanggal ditulis **4 digit tahun – 2 digit bulan – 2 digit tanggal** (mis. `2026-08-17`).
   - Judul singkat: huruf kecil, tanpa spasi, kata dipisah tanda minus `-`.
   - Wajib diakhiri `.md`.

4. **Salin template** di bawah ini ke dalam berkas, lalu ubah isinya:

   ```
   ---
   layout: post
   title: "Tulis Judul Berita di Sini"
   date: 2026-08-17 09:00:00 +0700
   penulis: "Nama Penulis"
   kategori: "Kegiatan"
   ---

   Tulis isi berita di sini. Boleh beberapa paragraf.

   Poin-poin bisa ditulis seperti ini:

   - Poin pertama
   - Poin kedua
   ```

   Keterangan bagian atas (di antara dua garis `---`):
   - `title` — judul berita (dalam tanda kutip).
   - `date` — tanggal & jam terbit. `+0700` adalah zona WIB, biarkan.
   - `penulis` — nama penulis/redaksi (boleh dihapus jika tidak perlu).
   - `kategori` — mis. Kegiatan, Pengumuman, Prestasi (boleh dihapus).

5. (Opsional) **Menambahkan gambar utama**: unggah dulu fotonya ke folder `gambar`
   (lihat `gambar/README.md`), lalu tambahkan satu baris ini di bagian atas, di dalam blok `---`:

   ```
   gambar: "/gambar/nama-foto-anda.jpg"
   ```

6. Scroll ke bawah, pada bagian **Commit new file**: pilih **"Commit directly to the `main` branch"**, lalu klik **Commit new file**.
7. Tunggu **±1–2 menit**. GitHub akan membangun ulang situs, dan berita otomatis muncul di halaman depan.

---

## B. Mengedit atau menghapus berita

1. Masuk folder **`_posts`**, klik berkas berita yang dimaksud.
2. Untuk **mengedit**: klik ikon **pensil** (Edit), ubah isinya, lalu Commit.
3. Untuk **menghapus**: klik ikon **tong sampah** (Delete), lalu Commit.

---

## C. Cara menulis (Markdown ringkas)

| Ingin menulis         | Ketik seperti ini                         |
| --------------------- | ----------------------------------------- |
| Tebal                 | `**teks tebal**`                          |
| Miring                | `*teks miring*`                           |
| Sub-judul             | `## Sub-judul`                            |
| Daftar berpoin        | `- item` (satu baris tiap poin)           |
| Daftar bernomor       | `1. item`                                 |
| Tautan                | `[teks tautan](https://alamat.web)`       |
| Gambar di dalam isi   | `![keterangan](/gambar/foto.jpg)`         |

---

## Penting

- **Format nama berkas dan tanggal harus benar.** Jika salah, berita bisa tidak muncul.
- Satu berkas = satu berita.
- Kalau ragu, tiru salah satu berkas contoh yang sudah ada di folder `_posts`.
