Baik, ini adalah **skill inti seorang AI-native engineer**:
**menerjemahkan requirement client → prompt Laravel Boost siap eksekusi**.

Aku akan beri:

### ✔ Framework berpikirnya

### ✔ Template yang bisa dipakai untuk semua project

### ✔ Contoh real tingkat senior

### ✔ Checklist untuk memastikan prompt kamu optimal

Setelah memahami ini, kamu bisa ambil requirement apa pun dari client → langsung jadi prompt Boost yang rapi dan lengkap.

---

# 🧠 **STEP 1 — Ambil Essence Dari Requirement Client**

Client ngomongnya biasanya berantakan:

* "Mau fitur absensi yang hitung gaji juga."
* "Bisa nggak tagihan yang sudah dibayar jangan muncul lagi."
* "Tolong ada laporan stok per bulan."
* "Saya ingin ada booking ruang, tapi kalau bentrok ditolak."

**Tugas kamu: BUKAN langsung bikin kode.**
Tugas kamu adalah mengubah kata-kata itu menjadi 4 hal:

### 1. **Masalah utama**

Apa pain point yang mau diselesaikan?

### 2. **Objek yang terlibat**

Model apa saja yang diperankan?

### 3. **Aturan bisnis (business rules)**

Logic penting yang mempengaruhi hasil.

### 4. **Alur interaksi (flow)**

Apa yang terjadi urutannya?

---

# 🧩 **STEP 2 — Ubah Menjadi “Software Requirements”**

Kamu bikin ringkasan teknis seperti ini:

```
Kita butuh modul Booking Ruangan:
- User bisa booking ruangan
- Tidak boleh ada overlapping booking
- Admin bisa melihat semua booking
- User hanya bisa edit booking miliknya
- Booking menggunakan start_at & end_at
```

Ini masih **bukan prompt**.
Tapi sudah siap diproses.

---

# 🟦 **STEP 3 — Masukkan Constraints (aturan engineering)**

Bagian ini yang bikin prompt kamu “senior”.

Contoh:

* logic harus ada di service
* gunakan repository
* FormRequest untuk validasi
* migration wajib ada FK + index
* gunakan dependency injection

Jadi requirements tadi berubah jadi:

```
Constraints:
- Migration harus include index (room_id + start_at)
- Service harus handle conflict booking
- Controller hanya delegator
- Validasi menggunakan FormRequest
- Repository wajib dipakai untuk query
```

---

# 🟩 **STEP 4 — Tentukan Output (file apa saja yang harus dihasilkan)**

Laravel Boost bekerja paling bagus jika output jelas:

```
Output:
- Model
- Migration
- Repository interface + Eloquent implementation
- Service
- FormRequest: StoreBookingRequest / UpdateBookingRequest
- Controller (API)
- Routes
- Unit test service
```

---

# 🔥 **STEP 5 — Satukan Menjadi Prompt Boost Siap Eksekusi**

Sekarang kita gabungkan semuanya.

**Final Prompt:**

```
Context:
Saya ingin fitur Booking Ruangan untuk sebuah aplikasi manajemen kampus.
User dapat booking ruangan dengan waktu mulai dan selesai, dan booking tidak 
boleh saling tumpang tindih dalam ruangan yang sama.

Requirements:
- User dapat membuat, melihat, edit, delete booking milik sendiri.
- Admin dapat melihat semua booking.
- Booking memiliki: user_id, room_id, start_at, end_at, status.
- Booking tidak boleh overlap: jika ada booking lain pada rentang waktu sama, tolak.
- Harus mendukung pagination pada list booking.

Constraints:
- Gerakkan seluruh logic ke BookingService.
- Gunakan repository pattern: BookingRepositoryInterface + BookingRepository.
- Validasi menggunakan FormRequest.
- Migration harus menggunakan index untuk room_id + start_at.
- Controller tidak boleh ada logic selain panggil service.
- Return response menggunakan BookingResource.

Output:
Tolong generate:
1. Migration
2. Model
3. Repository interface + Eloquent implementation
4. BookingService
5. FormRequest (store + update)
6. Controller (API)
7. Routes
8. BookingResource
9. Unit test untuk BookingService
```

Panggil:

```
boost> (paste prompt di atas)
```

Boom — kamu dapet satu modul **production-ready**.

---

# 🎯 CONTOH LAIN (SUPER REAL)

## Requirement Client:

> “Jika asisten datang kurang dari kapasitas ruang, asisten yang hadir dapat jatah gaji asisten yang tidak hadir. Buatkan penggajian otomatis setiap bulan.”

**Translate → Prompt Boost:**

```
Context:
Saya sedang membangun modul Payroll untuk asisten laboratorium.

Requirements:
- Gaji dihitung per bulan.
- Input: attendance log tiap pertemuan.
- Formula:
  total = hadir * rate_per_jam
  bonus = (kapasitas - hadir) * rate_per_jam jika hadir < kapasitas
- Asisten bisa melihat slip gajinya.
- Admin bisa generate payroll bulanan.

Constraints:
- Gunakan Service Pattern (PayrollService).
- Buat PayrollRepositoryInterface + implementation.
- Migration: payrolls, payroll_items, attendance_logs.
- Controller khusus untuk admin + endpoint untuk slip user.
- Buat unit test untuk skenario bonus.
- Controller tidak boleh menyimpan logic.

Output:
1. Migration 3 tabel
2. Model
3. Repository Pattern
4. PayrollService (full logic)
5. FormRequest generate payroll
6. Controller
7. Route (api/admin + api/user)
8. Unit test PayrollService
```

---

# 🧨 **CHECKLIST PROMPT SENIOR**

Sebelum kamu kirim prompt ke Boost, cek:

### ✔ Apa context-nya?

### ✔ Ada aturan bisnis?

### ✔ Ada constraints teknis?

### ✔ Sudah tentukan output file?

### ✔ Flow sudah jelas?

### ✔ Edge-case disebutkan?

### ✔ Ada hal yang harus dihindari (misal: logic di controller)?

Jika semua ✔, itu prompt kualitas senior.
