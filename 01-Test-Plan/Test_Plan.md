# Test Plan
## Toko Abunawas Inventory Application

### 1. Project Information

**Project Name:** Toko Abunawas Inventory Application  
**Testing Type:** Manual Software Testing  
**Testing Approach:** Black Box Testing  
**Tester:** Bayu Sukmo Adji  
**Application Type:** Inventory Management Application  
**Platform:** Flutter Application  

---

### 2. Test Objective

Tujuan pengujian adalah memastikan seluruh fungsi utama pada aplikasi
Toko Abunawas berjalan sesuai dengan kebutuhan sistem dan menghasilkan
output yang sesuai dengan expected result.

Pengujian juga bertujuan untuk:

- Memastikan setiap fitur utama dapat digunakan dengan benar.
- Memastikan input valid dapat diproses dengan sesuai.
- Memastikan input tidak valid ditangani oleh sistem.
- Mengidentifikasi defect atau perilaku aplikasi yang tidak sesuai.
- Memastikan defect yang telah diperbaiki berhasil melalui retesting.
- Memastikan perubahan pada aplikasi tidak menyebabkan masalah pada
  fitur lain melalui regression testing.
- Memastikan versi final aplikasi memiliki fungsi yang stabil sebelum digunakan.

---

### 3. Scope of Testing

Pengujian dilakukan terhadap fitur-fitur utama aplikasi Toko Abunawas.

#### 3.1 Authentication
- Login dengan akun valid.
- Login dengan akun tidak valid.
- Validasi field kosong.
- Validasi akun tidak aktif.
- Logout.
- Hak akses pengguna.

#### 3.2 Dashboard
- Menampilkan informasi dashboard.
- Navigasi menuju fitur utama.
- Validasi data yang ditampilkan pada dashboard.

#### 3.3 Product Management
- Menampilkan daftar produk.
- Menambahkan produk.
- Mengubah data produk.
- Menghapus produk.
- Validasi input produk.
- Pencarian produk.
- Validasi data produk setelah disimpan.

#### 3.4 Stock In
- Menambahkan transaksi barang masuk.
- Memilih produk.
- Input jumlah barang masuk.
- Validasi data transaksi.
- Penyimpanan transaksi.
- Perubahan stok setelah transaksi.
- Pengelolaan batch barang.

#### 3.5 Stock Out
- Membuat transaksi barang keluar.
- Memilih produk.
- Input jumlah barang keluar.
- Validasi stok tersedia.
- Validasi transaksi.
- Perubahan stok setelah barang keluar.
- Pemilihan batch barang.

#### 3.6 QR / Scanner
- Membaca QR atau barcode.
- Menampilkan data produk berdasarkan hasil scan.
- Penanganan QR/barcode yang tidak valid.

#### 3.7 Transaction History
- Menampilkan riwayat transaksi.
- Menampilkan informasi transaksi barang masuk.
- Menampilkan informasi transaksi barang keluar.
- Validasi data riwayat.

#### 3.8 Reports
- Menampilkan laporan.
- Validasi data laporan.
- Export laporan.
- Generate dokumen laporan.

#### 3.9 User Management
- Menampilkan daftar pengguna.
- Menambahkan pengguna.
- Mengubah data pengguna.
- Mengelola status pengguna.
- Validasi hak akses pengguna.

#### 3.10 Alerts
- Menampilkan alert atau notifikasi sesuai kondisi sistem.
- Validasi informasi alert.

#### 3.11 Analysis
- Menampilkan hasil analisis.
- Memastikan data analisis ditampilkan sesuai data aplikasi.

#### 3.12 Condition
- Memastikan fitur kondisi berjalan berdasarkan aturan aplikasi.

---

### 4. Test Types

Pengujian menggunakan beberapa pendekatan berikut:

#### Functional Testing
Memastikan setiap fungsi aplikasi berjalan sesuai kebutuhan.

#### Black Box Testing
Pengujian dilakukan berdasarkan input dan output tanpa bergantung pada
implementasi internal source code.

#### Positive Testing
Pengujian menggunakan data valid untuk memastikan sistem menghasilkan
output yang sesuai.

#### Negative Testing
Pengujian menggunakan data tidak valid, kosong, atau tidak sesuai untuk
memastikan aplikasi dapat menangani kesalahan dengan benar.

#### Boundary Testing
Pengujian dilakukan pada nilai batas tertentu seperti stok 0, jumlah minimum,
atau nilai yang berada di sekitar batas input.

#### Validation Testing
Memastikan setiap form, input, dan proses memiliki validasi yang sesuai.

#### Retesting
Defect yang ditemukan selama proses pengembangan diuji kembali setelah
dilakukan perbaikan.

#### Regression Testing
Fitur-fitur terkait diuji kembali setelah perubahan untuk memastikan perbaikan
tidak menyebabkan defect baru pada fungsi lain.

---

### 5. Test Environment

**Application:** Toko Abunawas Inventory Application  
**Framework:** Flutter  
**Authentication:** Firebase Authentication  
**Database:** Cloud Firestore  
**Testing Method:** Manual Testing  
**Test Environment:** Development / Local Application  
**Test Device:** Android / Emulator / Physical Device

Catatan:
Detail perangkat dan versi sistem operasi dapat ditambahkan sesuai perangkat
yang digunakan saat pengujian.

---

### 6. Test Data

Data pengujian meliputi:

- User valid.
- User tidak valid.
- User aktif.
- User tidak aktif.
- Produk valid.
- Produk dengan input tidak valid.
- Stok tersedia.
- Stok kosong.
- Jumlah transaksi valid.
- Jumlah transaksi melebihi stok.
- Data transaksi barang masuk.
- Data transaksi barang keluar.
- QR/barcode valid.
- QR/barcode tidak valid.

Data pengujian digunakan khusus untuk kebutuhan testing.

---

### 7. Entry Criteria

Testing dapat dimulai apabila:

- Aplikasi dapat dijalankan.
- Modul yang akan diuji sudah tersedia.
- Database dapat diakses.
- Akun pengujian tersedia.
- Data pengujian telah disiapkan.
- Fitur utama aplikasi dapat diakses.

---

### 8. Exit Criteria

Testing dinyatakan selesai apabila:

- Seluruh test case telah dieksekusi.
- Expected result telah dibandingkan dengan actual result.
- Defect yang ditemukan telah didokumentasikan.
- Defect yang telah diperbaiki sudah melalui retesting.
- Regression testing telah dilakukan pada fungsi terkait.
- Tidak terdapat defect kritis pada versi final.
- Seluruh test case pada versi final memiliki hasil sesuai expected result.

---

### 9. Test Deliverables

Dokumen yang dihasilkan dari proses pengujian adalah:

- Test Plan
- Test Scenario
- Test Cases
- Test Execution Result
- Bug / Defect Report
- Testing Evidence
- Regression Testing Result
- Test Summary Report

---

### 10. Defect Handling Process

Jika ditemukan defect, proses yang dilakukan adalah:

1. Menemukan perilaku sistem yang tidak sesuai expected result.
2. Mencatat langkah reproduksi.
3. Mendokumentasikan expected result dan actual result.
4. Menentukan severity defect.
5. Melampirkan evidence.
6. Melakukan perbaikan.
7. Melakukan retesting.
8. Jika sudah sesuai, status defect diubah menjadi Closed/Resolved.
9. Melakukan regression testing pada fitur terkait.

Pada versi final aplikasi, defect yang ditemukan selama proses development
telah diperbaiki dan test case terkait telah diuji kembali.

---

### 11. Risk

Beberapa risiko selama proses testing antara lain:

- Ketergantungan terhadap koneksi internet.
- Gangguan koneksi Firebase.
- Perbedaan perilaku aplikasi pada perangkat berbeda.
- Data testing memengaruhi data yang tersimpan pada database.
- Perubahan fitur selama proses development membutuhkan regression testing.

Mitigasi dilakukan dengan menggunakan data khusus testing, melakukan backup
jika diperlukan, dan melakukan pengujian ulang setelah perubahan aplikasi.

---

### 12. Final Testing Status

Pada versi final Toko Abunawas Inventory Application, seluruh test case yang
telah dieksekusi menghasilkan status PASS sesuai expected result setelah proses
development, defect fixing, retesting, dan regression testing.
