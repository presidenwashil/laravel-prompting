Baik, ini **panduan paling lengkap dan praktis** tentang **cara menulis prompt tingkat senior untuk Laravel Boost**, khusus untuk programmer yang ingin AI mengerjakan *80% kode*, tapi tetap menghasilkan kualitas yang layak produksi.

Ini gaya prompt yang dipakai oleh engineer di Laravel, Vercel AI, dan tim produk modern lainnya.

---

# 🎯 **GOAL**

Kamu akan belajar bagaimana menginstruksikan Boost seperti seorang **senior engineer**, bukan seperti user biasa.

> *Senior prompt = jelas, terstruktur, context-aware, dan langsung membimbing AI untuk menulis implementasi PREMIUM.*

---

# 🧠 **PRINSIP DASAR: "Context → Constraints → Output"**

Prompt yang baik *tidak panjang*, tapi selalu punya tiga bagian:

1. **Context**
   Ceritakan apa yang sedang kamu bangun.

2. **Constraints**
   Aturan main yang harus AI patuhi.

3. **Output**
   Format/struktur yang kamu ingin Boost hasilkan.

---

# 🟦 **1. TEMPLATE PROMPT SENIOR — Laravel Boost**

Gunakan struktur ini:

```
Context:
Saya sedang membangun fitur [nama fitur] untuk modul [nama modul] dalam project Laravel 12.

Requirements:
- [tuliskan kebutuhan fungsi]
- [aturan bisnis]
- [flow data]
- [kondisi edge-case]
- [hal yang harus dicegah]

Constraints:
- Gunakan [Service Pattern / Repository Pattern / Clean Architecture / Filament]
- Validasi menggunakan FormRequest
- Migration harus include index dan constraint
- Pastikan service tidak menyentuh request langsung
- Controller hanya jadi delegator
- Gunakan naming convention Laravel

Output:
Tolong generate:
1. Model  
2. Migration  
3. Service  
4. Controller  
5. Route  
6. Test (opsional)
```

---

# 🔥 **2. CONTOH PROMPT SENIOR SESUNGGUHNYA (REAL)**

## **Case: Fitur Payroll Asisten Lab (punya kamu sendiri)**

```
Context:
Saya sedang membangun fitur Payroll Asisten Laboratorium untuk sistem akademik. 
Payroll dihitung berdasarkan kehadiran praktikum setiap pertemuan, 
dan jika asisten yang hadir kurang dari kapasitas ruangan, 
asisten yang hadir mendapatkan jatah gaji asisten yang tidak hadir.

Requirements:
- Model: Assistant, Room, Attendance, PayrollRecord
- Payroll dihitung bulanan.
- Formula: 
  gaji = (jumlah pertemuan hadir * rate_per_jam) 
  + bonus jika kapasitas room > asisten hadir.
- Bonus = selisih kapasitas - jumlah hadir * rate_per_jam.
- Harus menangani kondisi: asisten hadir 0, kapasitas berlebih, absen berturut-turut.

Constraints:
- Gunakan Service Pattern: PayrollService
- Jangan tulis logic di Controller.
- Migration harus include foreign key dan index.
- Validasi di FormRequest.
- Buatkan contract + implementation untuk repository.
- Controller harus menggunakan dependency injection.
- Buatkan unit test untuk PayrollService.

Output:
Silakan generate:
1. Migration (semua tabel)
2. Model
3. Repository interface + Eloquent implementation
4. PayrollService
5. PayrollController
6. Routes (api)
7. Unit test untuk PayrollService
```

👉 Boost akan menghasilkan modul lengkap dan STRUKTURNYA BERSIH.

---

# 🧩 **3. PROMPT SENIOR SANGAT TERGANTUNG JENIS TASK**

## **A. Prompt Senior untuk Generate Fitur Baru**

```
boost> buat modul Booking Ruangan seperti di kampus:
- model
- migration
- service
- controller (API)
- route
- test
Dengan constraints:
- hanya service yang punya logic
- controller minimalis
- pakai FormRequest untuk store & update
- handle conflict booking (range waktu)
```

## **B. Prompt Senior untuk Refactor**

```
boost> refactor file app/Services/BookingService.php
Goals:
- hilangkan duplication
- pisahkan query ke repository
- buat method private untuk pengecekan konflik
- buat custom exception BookingConflictException
- tetap menjaga backward compatibility
```

## **C. Prompt Senior untuk Generate Test**

```
boost> buatkan test untuk PayrollService.
Test scenario:
- asisten hadir semua → tidak ada bonus
- asisten kurang dari kapasitas → ada bonus
- asisten tidak hadir sama sekali
- overlapping attendance dihitung hanya sekali
Gunakan mocks untuk AttendanceRepository.
```

## **D. Prompt Senior untuk Membuat Clean Architecture**

```
boost> pindahkan modul Booking ke folder:
- Domain/Booking
- Application/Booking
- Infrastructure/Booking

Generate interface:
BookingRepositoryInterface
BookingConflictCheckerInterface
Dan implementation eloquent.

Sesuaikan namespace.
```

---

# 🧨 **4. HAL PENTING: JANGAN BILANG “BUATKAN MIGRATION”**

Tapi bilang:

- “Migration harus berisi…”
- “Pastikan ada foreign key…”
- “Pastikan ada index untuk…”
- “Gunakan tipe column yang optimal…”

Prompt teknis lebih presisi → hasil jauh lebih senior.

---

# ✨ **5. KUMPULAN PROMPT SENIOR SIAP PAKAI**

## **1. Prompt generate API CRUD full**

```
boost> generate CRUD API untuk modul Product:
- model
- migration
- controller
- service
- route
Constraints:
- Validasi menggunakan FormRequest
- Controller tidak boleh punya logic selain delegasi ke service
- Gunakan Resource class untuk response
```

## **2. Prompt generate Filament Resource**

```
boost> generate Filament Resource untuk Booking model.
Constraints:
- Table harus include column: user, room, start_at, end_at.
- Form: select2 untuk room & user.
- Filters: date range.
```

## **3. Prompt untuk arsitektur besar**

```
boost> buat arsitektur modul Inventory berbasis Clean Architecture:
- Domain: entity + value objects
- Application: use cases
- Infrastructure: repository + model
- Interface: controller + request
Tolong generate folder & file skeleton.
```

---

# 🏆 **Kesimpulan**

Prompt tingkat senior itu:

### ✔ jelas

### ✔ lengkap

### ✔ ada constraints

### ✔ ada expected output

### ✔ menggunakan bahasa yang mirip “spec” daripada “permintaan samar”

Dan AI akan memberikan output **kelas production**, bukan kode asal.
