# Profil Organisasi Kampus — IMATIKA Universitas Pancasila

Tugas praktikum individu: halaman profil statis untuk organisasi kampus (Himpunan Mahasiswa Teknik Informatika) menggunakan HTML semantik, tanpa CSS.

## Struktur Folder

```
project/
├── index.html
├── img/
│   ├── logo.jpg
│   └── gedung-FTUP.jpg
└── README.md
```

## Fitur yang Dipenuhi

| Ketentuan | Implementasi |
|---|---|
| Minimal 2 gambar ber-`alt` | Logo imatika (`img/logo.jpg`) dan foto gedung FTUP (`img/gedung-FTUP.jpg`), masing-masing punya atribut `alt` deskriptif |
| Anchor internal | Navigasi `#identitas`, `#program`, `#pendaftaran`, `#kontak` + tombol "Kembali ke Identitas Organisasi" |
| Link eksternal | Instagram (`instagram.com/hmti_up`) dan website kampus (`univpancasila.ac.id`) |
| Link mailto | `mailto:hmti@univpancasila.ac.id` |
| Unordered list | Program kerja, kontak & media sosial |
| Ordered list | Alur pendaftaran anggota |
| Definition list | Struktur kepengurusan (`<dl>`, `<dt>`, `<dd>`) |

## Cara Menjalankan

1. Pastikan folder `img/` berisi `logo.jpg` dan `gedung-FTUP.jpg`.
2. Buka `index.html` langsung di browser (double-click atau `Live Server` di VS Code).

## Ringkasan Perubahan, Masalah, dan Solusi

Halaman ini dibuat untuk memenuhi ketentuan tugas praktikum: menyajikan identitas organisasi kampus lengkap dengan gambar, navigasi internal, tautan eksternal, kontak email, serta tiga jenis list. Struktur disusun dengan elemen semantik (`header`, `nav`, `main`, `section`, `footer`) agar konten mudah dibaca screen reader dan sesuai kaidah aksesibilitas dasar HTML5.

Masalah utama yang ditemui adalah menentukan konten mana yang paling cocok direpresentasikan sebagai *ordered list* dibanding *unordered list*. Alur pendaftaran anggota bersifat berurutan (harus diikuti tahap demi tahap), sehingga dipilih `<ol>`. Sebaliknya, daftar program kerja dan kontak tidak punya urutan wajib, sehingga tetap memakai `<ul>`. Struktur kepengurusan awalnya ditulis sebagai list biasa, namun diganti ke `<dl>` karena tiap jabatan punya deskripsi tugas yang lebih pas direpresentasikan sebagai pasangan istilah–definisi.

Solusi lain adalah menambahkan `target="_blank"` dan `rel="noopener"` pada link eksternal agar terbuka di tab baru tanpa membuka celah keamanan `window.opener`. Path gambar juga dirapikan ke dalam folder `img/` agar struktur project lebih terorganisir dan mudah dikelola saat proyek berkembang.

## Pembagian Peran

Tugas ini dikerjakan secara individu oleh Aulia Fachri (NIM 4525210098), meliputi seluruh proses: penyusunan struktur konten, penulisan markup HTML, penempatan gambar, serta penyusunan laporan.
