# Portal Berita PGSD UPI Kampus Serang

Situs berita statis ringan berbasis **Jekyll**, dibangun otomatis oleh **GitHub Pages**.
Kontributor menambah berita cukup dengan mengunggah berkas teks lewat website GitHub — tanpa dashboard.

- Panduan kontributor: **`PANDUAN.md`**
- Tiap berita: satu berkas di folder **`_posts`**
- Gambar: folder **`gambar`**

---

## Cara deploy (sekali saja)

1. Buat repositori baru di GitHub (mis. `pgsd-berita`), lalu unggah **seluruh isi folder ini** ke repo
   (lewat GitHub Desktop, atau `git push`). **Jangan** unggah zip-nya.
2. **Atur `baseurl`** di berkas **`_config.yml`**:
   - Jika alamat situs berbentuk `https://dika-81.github.io/pgsd-berita/` (project page),
     isi: `baseurl: "/pgsd-berita"` (sesuaikan nama repo).
   - Jika pakai domain sendiri atau *user page*, biarkan `baseurl: ""`.
3. Di GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `root` → Save.**
4. Tunggu ±1–2 menit. Situs live di alamat yang ditampilkan pada halaman Settings → Pages.

> **Penting:** ini situs **Jekyll**, jadi **JANGAN** menaruh berkas `.nojekyll` di sini
> (berbeda dengan salinan clone situs utama). Jekyll harus tetap berjalan agar berita terbangun.

---

## Menambahkan kontributor (sivitas akademika)

Agar rekan dapat menambah berita langsung:

**Settings → Collaborators → Add people** → masukkan username/email GitHub mereka.

Setelah menerima undangan, mereka bisa mengikuti langkah pada `PANDUAN.md`.
(Alternatif tanpa memberi akses tulis: rekan melakukan *fork* lalu mengirim *Pull Request*, dan Anda yang menyetujui.)

---

## Pratinjau lokal (opsional)

Tidak wajib — GitHub Pages sudah membangun otomatis. Namun jika ingin melihat lokal dan sudah punya Ruby:

    gem install bundler jekyll
    jekyll serve
    # buka http://localhost:4000

---

## Struktur berkas

    _config.yml         → pengaturan situs (judul, baseurl)
    index.html          → halaman depan (daftar berita)
    _layouts/           → kerangka halaman (default & post)
    _includes/          → potongan (format tanggal Indonesia)
    _posts/             → berkas berita (satu berkas = satu berita)
    gambar/             → foto/gambar berita
    assets/style.css    → tampilan
    PANDUAN.md          → panduan untuk kontributor
