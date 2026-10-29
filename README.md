# StoreReport Hub

Aplikasi web sederhana untuk mencatat dan merekap laporan **toko & barang**, lalu mengekspornya ke **PDF**.

Live: https://ugwap.github.io/Report-app/

## Fitur

- Tambah, edit, hapus, dan cari laporan (nama toko, nama barang, tanggal)
- Urutkan tabel berdasarkan toko, barang, atau tanggal
- Statistik ringkas: Total Laporan, Total Barang Unik, Total Toko Unik
- **Export PDF** rapi ukuran A4, kolom Aksi (edit/hapus) tidak ikut tercetak
- **Backup** data ke file JSON dan **Restore** dari file JSON
- Pencegahan data ganda (toko + barang + tanggal yang sama)
- Tampilan responsif untuk HP, tablet, dan desktop

## Cara Pakai

1. Buka https://ugwap.github.io/Report-app/
2. Isi Nama Toko, Nama Barang, dan Tanggal, lalu klik **Simpan Laporan**
3. Ulangi untuk setiap barang
4. Klik **Export PDF** untuk mengunduh rekap laporan
5. Klik **Backup** secara berkala agar data aman

## Penyimpanan Data

Data disimpan di **localStorage** browser, bukan di server. Artinya:

- Data hanya ada di browser/perangkat yang dipakai
- Data di `file://`, `localhost`, dan `ugwap.github.io` **terpisah**
- Menghapus data browser / memakai mode Incognito akan menghilangkan data
- Gunakan tombol **Backup** untuk menyimpan salinan, dan **Restore** untuk memulihkannya
  (termasuk untuk memindahkan data ke perangkat lain)

## Menjalankan Secara Lokal

Cukup buka `index.html` di browser (klik dua kali). Aplikasi memerlukan koneksi internet
untuk memuat Tailwind CSS, FontAwesome, dan html2pdf dari CDN.

## Struktur

```
index.html                     # seluruh aplikasi (HTML + CSS + JavaScript)
.github/workflows/static.yml   # deploy otomatis ke GitHub Pages
```

## Teknologi

- Tailwind CSS (Play CDN, versi dikunci 3.4.16)
- Font Awesome 6.4
- html2pdf.js 0.10.1
- localStorage untuk penyimpanan data
