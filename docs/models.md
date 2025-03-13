# Model & Migration

## 🚀 Membuat Model & Migration dengan ChatGPT
Gunakan prompt berikut untuk mempercepat pembuatan model dan migration dalam Laravel:

### 🔹 Membuat Model dengan Migration
```
Saya ingin membuat model `Post` dengan atribut berikut:
- `title` (string)
- `content` (text)
- `user_id` (foreign key ke tabel users)
- `published_at` (datetime, nullable)
Bantu saya dengan perintah artisan untuk membuat model dan migration-nya.
```

### 🔹 Menambahkan Relasi ke Model
```
Saya ingin menambahkan relasi antara `Post` dan `User`.
- Seorang user memiliki banyak post.
- Sebuah post hanya dimiliki oleh satu user.
Bantu saya menambahkan relasi di model `User` dan `Post`.
```

### 🔹 Menjalankan Migration
```
Saya telah membuat migration untuk model `Post`. Bantu saya menjalankan perintah untuk mengeksekusi migration dan memastikan database telah diperbarui.
```

### 🔹 Menambahkan Factory untuk Model
```
Saya ingin membuat factory untuk model `Post` agar bisa digunakan dalam seeding. Bantu saya dengan perintah untuk membuat factory dan contoh data yang akan di-generate.
```

## 🎯 Tips Tambahan
- Gunakan `php artisan migrate` untuk menjalankan migration.
- Gunakan `php artisan tinker` untuk menguji model secara langsung.
- Gunakan `php artisan db:seed` untuk mengisi data awal ke dalam database.

---
Setelah membuat model, lanjut ke [Controller & API](controllers.md) untuk langkah berikutnya! 🚀

