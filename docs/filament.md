# Filament Admin Panel

## 🚀 Menggunakan Filament dengan ChatGPT
Gunakan prompt berikut untuk mempercepat pengembangan fitur dengan Filament di Laravel:

### 🔹 Instalasi Filament
```
Saya ingin menginstal Filament Admin Panel dalam proyek Laravel saya. Berikan perintah instalasi dan cara menggunakannya.
```

### 🔹 Membuat Resource di Filament
```
Saya ingin membuat resource `PostResource` untuk mengelola post dalam admin panel Filament. Bantu saya dengan perintah dan kode yang sesuai.
```

### 🔹 Menambahkan Custom Form di Filament
```
Saya ingin menambahkan field `category` dan `tags` pada form di `PostResource`. Bagaimana cara menambahkannya dengan Filament?
```

### 🔹 Menambahkan Action Kustom di Filament
```
Saya ingin menambahkan tombol "Publish" di dalam `PostResource` yang mengubah status post menjadi "published". Bantu saya menuliskan kodenya.
```

### 🔹 Menyesuaikan Tabel di Filament
```
Saya ingin menampilkan hanya `title`, `author`, dan `status` di tabel Filament pada `PostResource`. Bagaimana cara mengaturnya?
```

### 🔹 Menggunakan Relation Manager
```
Saya ingin menampilkan daftar komentar terkait dalam `PostResource` menggunakan Relation Manager di Filament. Bantu saya dengan contoh kode.
```

## 🎯 Tips Tambahan
- Gunakan `php artisan make:filament-resource NamaResource` untuk membuat resource baru.
- Gunakan `Forms\Components\TextInput::make('nama_field')` untuk menambahkan field di form.
- Gunakan `Tables\Columns\TextColumn::make('nama_field')` untuk menampilkan kolom di tabel.
- Gunakan `Tables\Actions\Action::make('nama_aksi')` untuk menambahkan tombol custom.

---
Setelah memahami Filament, lanjut ke [Livewire](livewire.md) untuk fitur interaktif! 🚀

