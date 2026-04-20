# ISR Lab Website — Jekyll + GitHub Pages

Website resmi **Intelligent Systems & Robotics Laboratory**  
Universitas Jember (UNEJ) · Dept. Teknik Elektro

---

## 🚀 Cara Deploy ke GitHub Pages (5 Langkah)

### 1. Buat Repository GitHub
- Login ke [github.com](https://github.com)
- Klik **New repository**
- Nama repo: `isr-lab` (atau bebas)
- Set ke **Public**
- Klik **Create repository**

### 2. Upload Semua File
```bash
# Di terminal lokal (jika ada Git):
git init
git add .
git commit -m "Initial commit: ISR Lab website"
git remote add origin https://github.com/USERNAME/isr-lab.git
git push -u origin main
```
Atau drag-and-drop semua file lewat antarmuka web GitHub.

### 3. Aktifkan GitHub Pages
- Buka **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: `main` / `root`
- Klik **Save**

### 4. Website Live!
URL otomatis: `https://USERNAME.github.io/isr-lab`

---

## ✏️ Cara Menulis Berita Mingguan

Buat file baru di folder `_posts/` dengan format nama:

```
YYYY-MM-DD-judul-singkat.md
```

Contoh: `2025-04-20-seminar-nasional-robotika.md`

Isi file dengan template berikut:

```markdown
---
layout: post
title: "Judul Berita Anda"
date: 2025-04-20
author: "Nama Penulis"
category: "News"          # News / Publication / Activity / Announcement
emoji: "📰"               # Emoji untuk thumbnail
tags: [tag1, tag2, tag3]
excerpt: "Ringkasan singkat 1-2 kalimat yang muncul di halaman daftar berita."
---

Isi berita Anda di sini dalam format Markdown...

## Subjudul

Paragraf...

- Item list
- Item list

**Teks tebal**, *teks miring*
```

Commit file → otomatis tampil di website dalam 1-2 menit!

---

## ⚙️ Konfigurasi Penting

Edit file `_config.yml` untuk mengubah:

```yaml
url: "https://USERNAME.github.io"  # ← Ganti USERNAME
baseurl: "/isr-lab"                 # ← Ganti nama repo

lab:
  pi_name: "Prof. Nama Lengkap"    # ← Ganti nama Anda
  email: "anda@unej.ac.id"         # ← Ganti email
  scholar: "https://..."           # ← Link Google Scholar Anda
```

---

## 📬 Mengaktifkan Form Kontak

Form kontak menggunakan **Formspree** (gratis, 50 pesan/bulan):

1. Daftar di [formspree.io](https://formspree.io)
2. Buat form baru → dapatkan ID (misal: `xbjnpqkr`)
3. Di `index.html`, ganti:
   ```html
   action="https://formspree.io/f/YOUR_ID"
   ```
   menjadi:
   ```html
   action="https://formspree.io/f/xbjnpqkr"
   ```

---

## 📁 Struktur File

```
isr-lab-jekyll/
├── _config.yml          ← Konfigurasi utama
├── _layouts/
│   ├── default.html     ← Template semua halaman
│   └── post.html        ← Template halaman berita
├── _posts/              ← FOLDER BERITA MINGGUAN
│   └── 2025-04-14-*.md
├── assets/
│   └── css/main.css     ← Semua styling
├── news/
│   └── index.html       ← Halaman daftar berita
├── index.html           ← Halaman utama
└── Gemfile
```

---

## 🎨 Kategori Berita

| Category | Digunakan untuk |
|----------|----------------|
| `News` | Berita umum lab |
| `Publication` | Paper diterima/terbit |
| `Activity` | Workshop, seminar, kunjungan |
| `Announcement` | Pengumuman penting (beasiswa, S3, dll) |

---

Dibuat dengan ❤️ untuk ISR Lab UNEJ
