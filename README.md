# Laravel Prompting Guide

**Laravel Prompting Guide** adalah repositori yang berisi kumpulan **prompt terbaik** untuk mempercepat pengembangan proyek Laravel menggunakan **ChatGPT**. Dengan koleksi prompt ini, Anda dapat dengan mudah menghasilkan kode, mengoptimalkan workflow, dan mempercepat debugging.

## 🚀 Fitur
- **Prompt untuk Setup Proyek** – Memulai Laravel dengan cepat.
- **Prompt untuk Model & Migration** – Generate model, migrasi, dan relasi dengan cepat.
- **Prompt untuk Controller & API** – Membantu membuat controller dan API endpoint.
- **Prompt untuk Livewire & Filament** – Mempermudah pengembangan aplikasi berbasis komponen.
- **Prompt untuk Debugging & Optimasi** – Memecahkan error dan meningkatkan performa aplikasi.

## 📂 Struktur Dokumentasi
Repositori ini menggunakan format dokumentasi berbasis Markdown:

```
laravel-prompting/
│── docs/
│   ├── index.md          # Halaman utama dokumentasi
│   ├── setup.md          # Prompt untuk setup Laravel
│   ├── models.md         # Prompt untuk model dan migration
│   ├── controllers.md    # Prompt untuk membuat controller
│   ├── livewire.md       # Prompt untuk komponen Livewire
│   ├── filament.md       # Prompt untuk admin panel Filament
│   ├── api.md            # Prompt untuk membuat API
│   ├── debugging.md      # Prompt untuk debugging & optimasi
│── README.md
│── mkdocs.yml            # (Opsional) Untuk membuat dokumentasi web
```

## ✨ Contoh Prompt
### 🔹 Setup Laravel dengan Livewire & Filament
```
Saya ingin membuat proyek Laravel 11 dengan Filament dan Livewire.  
Bantu saya membuat langkah-langkah setup proyek ini di lokal menggunakan Composer dan menjalankan server.  
Saya juga ingin menambahkan autentikasi menggunakan Laravel Breeze dengan Livewire.
```

### 🔹 Generate Model & Migration dengan Relasi
```
Bantu saya membuat model `Post` dengan atribut berikut:
- `title` (string)
- `content` (text)
- `user_id` (foreign key ke tabel users)
- `published_at` (datetime, nullable)
Tambahkan juga relasi ke model User.
```

### 🔹 Debugging Error di Laravel
```
Saya mendapatkan error saat melakukan migrasi di Laravel:  
`SQLSTATE[HY000]: General error: 1215 Cannot add foreign key constraint`
Apa kemungkinan penyebabnya dan bagaimana cara memperbaikinya?
```

## 🛠️ Cara Menggunakan
1. **Clone repositori ini**
   ```sh
   git clone https://github.com/username/laravel-prompting.git
   ```
2. **Baca dokumentasi di dalam folder `docs/`**
3. **Gunakan prompt dalam workflow pengembangan Laravel Anda**
4. **(Opsional) Jalankan dokumentasi sebagai website**
   ```sh
   pip install mkdocs-material
   mkdocs serve
   ```

## 📢 Kontribusi
Kami sangat terbuka untuk kontribusi! Jika Anda memiliki prompt baru yang berguna untuk pengembangan Laravel, silakan buat **pull request** atau diskusikan di **Issues**.

---
Happy Coding! 🚀


