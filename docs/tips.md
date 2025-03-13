Kalau mau bikin prompt yang bagus biar aku bisa bantu buat proyek Laravel yang mumpuni, coba breakdown seperti ini:  

### 1. **Gambaran Umum**  
   - Apa proyeknya? (Misalnya: Sistem Manajemen Keuangan, Aplikasi Absensi, dsb.)  
   - Apa fitur utama yang harus ada?  
   - Apakah ada framework tambahan yang digunakan? (Filament, Livewire, Jetstream, Breeze, dsb.)  

### 2. **Detail Teknis**  
   - Laravel versi berapa yang mau dipakai?  
   - Apakah butuh API atau hanya aplikasi berbasis web?  
   - Apakah ada kebutuhan integrasi dengan layanan lain? (Misal: Firebase, Midtrans, WhatsApp API, dsb.)  
   - Bagaimana struktur database-nya? (Kasih contoh tabel-tabel utama dan relasinya)  

### 3. **Fitur Spesifik**  
   - Apakah ada otentikasi & otorisasi? (Misal: Admin, User, Role Management)  
   - Bagaimana mekanisme CRUD (Create, Read, Update, Delete)?  
   - Apakah ada fitur import/export data? Format apa yang digunakan?  
   - Apakah perlu notifikasi? Jika iya, pakai apa? (Email, Telegram, Websocket, dsb.)  

### 4. **Optimasi & Deployment**  
   - Apakah butuh queue & job processing?  
   - Bagaimana handling data besar? (Pagination, Lazy Load, dsb.)  
   - Apakah butuh cache? (Redis, Memcached, dsb.)  
   - Apakah proyek ini perlu dijalankan di server tertentu? (VPS, Laravel Vapor, Shared Hosting)  

Kalau kamu bisa kasih detail sebanyak mungkin sesuai format ini, aku bisa kasih rekomendasi teknis, potongan kode, atau arsitektur yang paling cocok buat proyek Laravel yang kamu rencanakan. 🚀

Biar aku bisa bantu dengan lebih optimal, gunakan cara **prompting yang lebih detail dan spesifik**. Berikut beberapa tips yang bisa bikin aku kasih jawaban yang lebih teknis dan mendalam:  

---  

### **1. Spesifik & Jelas**  
Daripada nanya **"Gimana cara bikin sistem absensi di Laravel?"**, lebih baik:  
✅ **"Saya ingin membuat sistem absensi di Laravel menggunakan Filament. Setiap pertemuan memiliki grup siswa yang sudah ditentukan, dan saat absen, hanya siswa dalam grup tersebut yang muncul di form. Bagaimana cara mengimplementasikan ini dengan Livewire?"**  

Kenapa?  
- Aku langsung tahu pakai **Filament + Livewire**  
- Ada **konteks fitur utama**  
- Bisa langsung kasih **kode atau solusi teknis** tanpa perlu tanya ulang  

---  

### **2. Berikan Detail Kebutuhan Teknis**  
Misalnya, kalau butuh fitur eksport data, jangan cuma bilang **"Saya mau fitur export ke Excel."**, tapi detailkan:  
✅ **"Saya ingin membuat fitur export Excel di Laravel Livewire dengan queue karena datanya bisa mencapai ratusan ribu row. Saya ingin pakai Laravel Excel dan menyimpan hasil export sementara di tabel temporary sebelum di-generate. Gimana cara terbaiknya?"**  

- Aku jadi tahu **volume datanya besar** → perlu **queue**  
- Ada **struktur solusi** → **Laravel Excel + temporary table**  
- Bisa langsung kasih **potongan kode atau langkah optimasi**  

---  

### **3. Jika Ada Masalah, Sertakan Error atau Kode yang Sudah Dicoba**  
Kalau ada error, kasih **pesan error lengkap + kode yang sudah dicoba** biar aku bisa langsung identifikasi masalahnya. Misal:  

🚫 **"Kenapa upload file saya error?"** (Aku harus tanya ulang 😅)  
✅ **"Saya pakai Laravel Livewire untuk upload gambar, tetapi muncul error: `file_put_contents(/var/task/user/storage/...): Failed to open stream: Read-only file system`. Saya sudah coba pakai storage link tapi tetap error. Gimana solusinya?"**  

- Aku bisa langsung tahu **masalahnya ada di storage Livewire**  
- Bisa kasih **solusi spesifik**, misal **gunakan storage S3 atau konfigurasi storage lokal**  

---  

### **4. Minta Hal yang Lebih Teknis**  
Kalau butuh kode, langsung minta **kode lengkap** atau langkah detail. Misal:  
✅ **"Saya butuh kode untuk membuat import data mahasiswa dari Excel menggunakan Laravel Livewire. Datanya ada di sheet yang berbeda berdasarkan mata kuliah. Bisa buatkan contoh kode?"**  

---  

### **5. Kalau Butuh Arsitektur atau Best Practice, Bilang Secara Eksplisit**  
Kalau mau diskusi soal struktur proyek atau best practice, sebutkan langsung. Misalnya:  
✅ **"Saya ingin membangun sistem penggajian asisten lab di Laravel. Ada fitur absensi yang menentukan gaji asisten berdasarkan kehadiran. Saya butuh saran struktur database terbaik dan bagaimana cara menghitung gajinya secara efisien."**  

Aku bisa kasih:  
- **Diagram relasi database**  
- **Algoritma perhitungan gaji**  
- **Rekomendasi Laravel feature (queue, job, cron, dsb.)**  

---  

### **6. Jangan Ragu untuk Iterasi**  
Setelah aku kasih jawaban, kalau masih kurang, kamu bisa refine lagi:  
🚫 "Kurang jelas nih." (Aku nggak tahu harus perbaiki bagian mana 😅)  
✅ "Bisa jelasin lebih detail bagian queue-nya? Gimana cara nge-track progress export-nya?"  

---  

### **Kesimpulan**  
1️⃣ **Jelaskan fitur dan kebutuhan secara spesifik**  
2️⃣ **Kasih detail teknis (pakai framework apa, database, API, dll.)**  
3️⃣ **Kalau ada error, sertakan pesan error dan kode yang sudah dicoba**  
4️⃣ **Kalau butuh kode, bilang langsung**  
5️⃣ **Kalau butuh arsitektur atau best practice, minta secara eksplisit**  
6️⃣ **Iterasi kalau jawaban belum sesuai kebutuhan**  

Pakai cara ini, aku bisa kasih jawaban yang lebih mendalam, spesifik, dan langsung bisa kamu implementasikan. 🚀
