# 🚀 Custom GitHub Readme Stats (Self-Hosted)

Dapatkan kartu statistik GitHub yang dinamis, cepat, dan selalu terbarui langsung di profil GitHub Anda! Repositori ini adalah hasil fork dari [anuraghazra/github-readme-stats](https://github.com/anuraghazra/github-readme-stats) yang di-deploy secara mandiri (*self-hosted*) untuk performa optimal dan pembaruan data yang cepat.

> [!TIP]
> **Kelebihan Instance Ini:**
> - **Update Cepat:** Menggunakan konfigurasi cache super cepat (hanya 1 menit / 60 detik) dibandingkan versi publik yang memakan waktu hingga 24 jam.
> - **Lebih Stabil:** Bebas dari batas limit (*rate limit*) API publik karena menggunakan token akses personal khusus.
> - **Mendukung Siapa Saja:** Instance ini dikonfigurasi terbuka sehingga Anda dan orang lain dapat menggunakannya langsung.

---

## 🛠️ Cara Penggunaan

Cukup salin kode Markdown di bawah ini dan tempelkan di file `README.md` profil GitHub Anda. Pastikan untuk mengubah parameter `?username=` dengan username GitHub Anda sendiri.

### 1. Kartu Statistik Utama (GitHub Stats Card)
Kartu ini menampilkan ringkasan jumlah bintang, komit, pull request, isu, dan kontribusi Anda.

```markdown
[![Stats GitHub](https://github-readme-stats-master.vercel.app/api?username=username-anda&show_icons=true&theme=radical)](https://github.com/username-anda)
```

### 2. Kartu Bahasa Terbanyak (Top Languages Card)
Kartu ini menampilkan persentase bahasa pemrograman yang paling sering Anda gunakan dalam repositori Anda.

```markdown
[![Bahasa Terbanyak](https://github-readme-stats-master.vercel.app/api/top-langs?username=username-anda&layout=compact&theme=radical)](https://github.com/username-anda)
```

*(Catatan: Ganti `github-readme-stats-master.vercel.app` dengan domain Vercel hasil deployment Anda yang sebenarnya jika berbeda).*

---

## 🎨 Kustomisasi Tampilan

Anda dapat mengubah tampilan kartu sesuai selera menggunakan parameter URL tambahan:

### 🌈 Pilihan Tema (Theme)
Tambahkan parameter `&theme=NAMA_TEMA` di akhir URL. Beberapa tema populer yang didukung:
- `default` (Terang klasik)
- `dark` (Gelap klasik)
- `radical` (Gelap dengan aksen neon pink/biru)
- `tokyonight` (Nuansa malam Tokyo)
- `onedark` (Tema editor Atom/VSCode)
- `dracula` (Tema Dracula populer)

*Contoh:* `&theme=tokyonight`

### ⚙️ Parameter Berguna Lainnya
| Parameter | Deskripsi | Nilai Contoh |
| :--- | :--- | :--- |
| `show_icons` | Menampilkan ikon di samping teks statistik | `true` atau `false` |
| `hide` | Menyembunyikan statistik tertentu | `&hide=stars,issues` |
| `hide_border` | Menyembunyikan garis bingkai luar kartu | `true` |
| `count_private` | Menghitung kontribusi dari repositori privat | `true` *(memerlukan token akses khusus)* |

---

## ⚙️ Cara Deploy Sendiri (Opsional)

Jika Anda ingin men-deploy instance ini secara mandiri ke akun Vercel Anda sendiri:

1. **Fork** repositori ini.
2. Buat **Personal Access Token (PAT)** di GitHub dengan izin `repo` dan `read:user`.
3. Buka **Vercel** dan impor repositori hasil fork tersebut.
4. Tambahkan **Environment Variables** berikut di Vercel sebelum deploy:
   - `PAT_1` : *Isi dengan Token GitHub Anda*
   - `CACHE_SECONDS` : `60` *(untuk update status setiap 1 menit)*
5. Klik **Deploy** dan server Anda siap digunakan!
