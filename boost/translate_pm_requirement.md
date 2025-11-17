Oke, ini konteks yang sangat nyata: **Project Manager (PM)** biasanya memberi requirement yang lebih *rapih*, *struktural*, dan *high-level* dibanding client.
Tantangannya adalah mengubah requirement tersebut menjadi **prompt Laravel Boost** yang:

* jelas, tidak multitafsir
* langsung actionable
* tetap memberi ruang bagi Boost untuk mengerjakan *scaffolding* atau *kode kompleks*
* mengikuti standar arsitektur tim
* aman (tidak melanggar domain logic)

Berikut adalah **panduan + template praktis + contoh nyata**.

---

# 🧠 **Cara Translate Requirement Project Manager Menjadi Prompt Laravel Boost**

PM biasanya memberi dokumen seperti:

* User Story
* Acceptance Criteria
* Business Rules
* Flow Diagram / Sequence
* Data requirements
* Edge cases

Tugasmu adalah mengubah dokumen itu menjadi **Prompt Engineering Level Senior**.

---

# 🎯 **1. Identifikasi Struktur Dasar dari Input PM**

PM biasanya memberikan:

### ✔ User Story
- Acceptance Criteria
- Scope / Out of Scope
- Entities involved
- Roles
- Flow singkat
- Notes

Contohnya:

> *"Sebagai admin, saya ingin mencatat transaksi pemasukan dan pengeluaran agar laporan keuangan bisa dihitung otomatis bulanannya."*
> Acceptance Criteria:
>
> * Admin dapat tambah/edit/hapus transaksi
> * Harus memilih kategori
> * Nominal wajib angka > 0
> * Laporan bulanan otomatis rekap per kategori

---

Sekarang, struktur itu diubah menjadi prompt Laravel Boost versi **standar senior**:

---

# 💎 **2. Gunakan Struktur Prompt "TRF" (Target — Rules — Files)**

Ini adalah struktur paling efektif untuk Boost:

---

## 🧩 **(1) TARGET**

Tujuan dari task: apa yang ingin dibuat?

## 🧩 **(2) RULES**

Kumpulan constraint: arsitektur, pattern, hal yang harus/harus tidak dibuat.

## 🧩 **(3) FILES / TASKS**

File, class, atau operasi yang harus digenerate oleh Boost.

---

# 💠 **3. Template Prompt Laravel Boost untuk Requirement PM**

```
You are working inside a Laravel 12 application using Laravel Boost. 
Generate code that satisfies the following requirements.

# TARGET
- [Masukkan tujuan fitur sesuai user story PM]

# BUSINESS RULES
- [Tulis acceptance criteria dari PM]
- [Tambahkan rule teknis jika perlu]

# DOMAIN ENTITIES
- [Daftar model + field + relasi yang dibutuhkan]

# ARCHITECTURE RULES
- Follow clean folder structure (Models, Actions, Services, DTOs).
- Use form requests for validation.
- Use Actions for business logic.
- Use Eloquent resources for API responses.
- Avoid fat controllers.

# IMPLEMENTATION SCOPE
Generate only:
- Migrations
- Models
- Actions
- Controllers
- Form Requests
- Routes
- Policies (jika perlu)

# DO NOT
- Jangan membuat seeder kecuali diminta.
- Jangan membuat UI/Blade/File front-end.

# OUTPUT STYLE
- Output langsung file by file dengan path lengkap.
```

---

# 🧪 **4. Contoh Translasi Requirement PM → Prompt Boost**

### 📌 **REQUIREMENT DARI PM (REAL CASE)**

> **User Story:**
> Sebagai admin, saya ingin mencatat transaksi pemasukan/pengeluaran agar bisa melihat laporan keuangan bulanan dan ringkasan per kategori.
>
> **Acceptance Criteria:**
>
> * Admin dapat CRUD transaksi.
> * Transaksi harus memiliki kategori dan tipe (income/expense).
> * Nominal wajib angka lebih dari 0.
> * Laporan bulanan menampilkan total income, total expense, dan selisih.
> * Laporan harus bisa di-filter per kategori.
>
> **Notes:**
> Kategori di-input manual oleh admin.
> Tidak ada multi-user.

---

# 🎯 **PROMPT BOOST HASIL TERJEMAHAN SENIOR**

```
You are working inside a Laravel 12 project using Laravel Boost.
Generate code implementing the financial transaction module.

# TARGET
Build a transaction management feature with monthly financial reporting.

# BUSINESS RULES
- Admin can create, edit, and delete transactions.
- Each transaction must have:
  - category_id
  - type: income | expense
  - amount: numeric > 0
  - date
  - description (optional)
- Categories are managed manually by admin.
- Monthly report must include:
  - total income
  - total expense
  - balance = income - expense
  - filter by category

# DOMAIN ENTITIES
Category:
- id
- name
- created_at
- updated_at

Transaction:
- id
- category_id (FK)
- type (enum: income, expense)
- amount (decimal 15,2)
- date (date)
- description (nullable)
- created_at, updated_at

# ARCHITECTURE RULES
- Use dedicated Actions for business logic: 
  - CreateTransaction
  - UpdateTransaction
  - DeleteTransaction
  - GenerateMonthlyReport
- Use Eloquent Resources for API output.
- Use Form Requests for validation.
- Split reporting logic into Services/FinancialReportService.php.
- Controllers must remain thin.

# IMPLEMENTATION SCOPE
Generate:
- Migrations
- Models + Relationships
- Form Requests
- Controllers
- Actions
- Services
- API Routes

# DO NOT
- Don’t generate Blade or UI.
- Don’t create factories unless required.

# OUTPUT FORMAT
Output code file by file with correct paths.
```

💥 Ketika prompt ini dikirim ke Boost → kamu akan dapat **seluruh modul transaksi** dalam hitungan detik.

---

# 🧠 **5. Tips Senior-Level Prompting**

### ✔ Jangan kirim user story mentah

Ubah menjadi struktur engineering.

### ✔ Jelaskan tujuan fitur, bukan hanya task

Boost akan mengoptimalkan solusi.

### ✔ Berikan batasan arsitektur

Boost akan mengikuti pola timmu.

### ✔ Sebutkan file apa saja yang boleh dibuat

Supaya tidak keluar scope.

### ✔ Selalu kasih format output (path file)

Supaya mudah paste ke project.
