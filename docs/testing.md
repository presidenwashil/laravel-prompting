# Pengujian di Laravel

## 🚀 Melakukan Pengujian dengan ChatGPT
Gunakan prompt berikut untuk mempercepat proses pengujian dalam Laravel:

### 🔹 Membuat Test Case dengan PHPUnit
```
Saya ingin membuat pengujian menggunakan PHPUnit untuk metode `store` di `PostController`. Berikan kode untuk pengujian yang mencakup validasi input dan penyimpanan data.
```

### 🔹 Menjalankan Pengujian
```
Bagaimana cara menjalankan pengujian unit dan fitur di Laravel?
```

### 🔹 Menggunakan Laravel Test Factory
```
Saya ingin membuat factory untuk model `Post` agar bisa digunakan dalam pengujian. Bagaimana cara membuatnya?
```

### 🔹 Menggunakan Database dalam Pengujian
```
Bagaimana cara menggunakan database in-memory (`RefreshDatabase`) dalam pengujian Laravel?
```

### 🔹 Menguji API dengan HTTP Test
```
Saya ingin menguji endpoint API `POST /api/posts` menggunakan Laravel HTTP Test. Bagaimana caranya?
```

### 🔹 Mocking dan Faking dalam Pengujian
```
Bagaimana cara menggunakan `fake()` untuk menguji pengiriman email atau event di Laravel?
```

### 🔹 Menggunakan PestPHP untuk Pengujian
```
Saya ingin menulis pengujian menggunakan PestPHP. Bagaimana cara menggunakannya dalam Laravel?
```

## 🎯 Tips Tambahan
- Gunakan `php artisan make:test PostTest` untuk membuat test case baru.
- Gunakan `php artisan test` atau `vendor/bin/phpunit` untuk menjalankan pengujian.
- Gunakan `withoutExceptionHandling()` untuk melihat error lebih jelas dalam pengujian.
- Gunakan `actingAs(User::factory()->create())` untuk menguji fitur yang membutuhkan autentikasi.

---
Setelah memahami pengujian, lanjut ke [Debugging](debugging.md) untuk mengatasi masalah lebih lanjut! 🚀

