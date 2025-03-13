# Pengembangan API dengan Laravel

## 🚀 Membangun API dengan ChatGPT
Gunakan prompt berikut untuk mempercepat pengembangan API di Laravel:

### 🔹 Membuat Controller API Dasar
```
Saya ingin membuat controller API `PostController` dengan metode CRUD (`index`, `store`, `show`, `update`, `destroy`). Berikan perintah Artisan dan kode yang sesuai.
```

### 🔹 Menyiapkan Route API
```
Bagaimana cara mendefinisikan route API untuk `PostController` di `routes/api.php`?
```

### 🔹 Menerapkan Autentikasi API
```
Saya ingin melindungi API saya menggunakan Laravel Sanctum. Bagaimana cara mengatur autentikasi berbasis token?
```

### 🔹 Menambahkan Validasi pada Request API
```
Saya ingin menambahkan validasi pada metode `store` di `PostController`.
- `title` harus diisi dan maksimal 255 karakter.
- `content` harus diisi.
- `user_id` harus ada di tabel `users`.
Berikan kode yang sesuai.
```

### 🔹 Menggunakan API Resource
```
Bagaimana cara membuat resource API `PostResource` untuk memformat respons JSON?
```

### 🔹 Menangani Error dan Respons API
```
Bagaimana cara menyusun respons API yang standar, termasuk penanganan error?
```

### 🔹 Menambahkan Filter dan Paginasi pada API
```
Saya ingin menerapkan filter dan paginasi pada metode `index` di `PostController`. Bagaimana cara melakukannya?
```

## 🎯 Tips Tambahan
- Gunakan `php artisan make:controller PostController --api` untuk membuat controller API.
- Gunakan `php artisan make:resource PostResource` untuk respons API yang terstruktur.
- Gunakan `Route::middleware('auth:sanctum')->group(...)` untuk mengamankan route API.
- Gunakan `Resource::collection()` untuk respons dengan paginasi.

---
Setelah memahami pengembangan API, lanjut ke [Debugging](debugging.md) untuk menangani masalah! 🚀

