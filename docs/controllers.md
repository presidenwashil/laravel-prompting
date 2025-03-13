# Controller & API

## 🚀 Membuat Controller & API dengan ChatGPT
Gunakan prompt berikut untuk mempercepat pembuatan controller dan API dalam Laravel:

### 🔹 Membuat Controller
```
Saya ingin membuat controller `PostController` dengan resource methods (`index`, `store`, `show`, `update`, `destroy`). Bantu saya dengan perintah artisan dan kode yang sesuai.
```

### 🔹 Menambahkan Validasi Request
```
Saya ingin menambahkan validasi pada method `store` di `PostController`.
- `title` harus diisi dan maksimal 255 karakter.
- `content` harus diisi.
- `user_id` harus ada di tabel `users`.
Bantu saya menambahkan validasi ini dalam controller.
```

### 🔹 Membuat API Resource Controller
```
Saya ingin membuat API resource controller `PostController` untuk menangani CRUD dengan format JSON. Bantu saya dengan kode yang sesuai.
```

### 🔹 Menambahkan Route untuk Controller
```
Saya ingin menambahkan route resource untuk `PostController`. Bantu saya menuliskan kode di `routes/web.php` dan `routes/api.php`.
```

### 🔹 Menambahkan Authorization ke Controller
```
Saya ingin menambahkan authorization ke `PostController`, sehingga hanya user yang memiliki post yang bisa mengedit atau menghapusnya. Bantu saya menuliskan policy dan menerapkannya di controller.
```

## 🎯 Tips Tambahan
- Gunakan `php artisan make:controller PostController --resource` untuk membuat resource controller.
- Gunakan `php artisan route:list` untuk melihat daftar route yang tersedia.
- Gunakan Laravel Policy untuk mengelola authorization dengan `php artisan make:policy PostPolicy`.

---
Setelah membuat controller, lanjut ke [Livewire & Filament](livewire.md) untuk langkah berikutnya! 🚀

