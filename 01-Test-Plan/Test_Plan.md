# Test Plan
## Toko Abunawas Inventory Application

### 1. Project Information

**Project Name:** Toko Abunawas Inventory Application  
**Testing Role:** Software Quality Assurance / Manual Tester  
**Testing Type:** Manual Software Testing  
**Testing Approach:** Black Box Testing  
**Application Type:** Inventory Management Application  
**Platform:** Flutter Application  
**Tester:** Bayu Sukmo Adji  

---

### 2. Test Objective

Tujuan pengujian adalah memastikan fungsi utama pada Toko Abunawas Inventory Application berjalan sesuai kebutuhan sistem dan menghasilkan output yang sesuai dengan expected result.

Pengujian juga bertujuan untuk:

- Memastikan fitur utama dapat digunakan sesuai fungsi yang dirancang.
- Memastikan input valid dapat diproses dengan benar.
- Memastikan input tidak valid ditangani dengan aman.
- Memastikan aturan stok, batch, FIFO, dan hak akses berjalan sesuai kebutuhan.
- Mengidentifikasi defect atau perilaku aplikasi yang tidak sesuai expected result.
- Mendokumentasikan actual result dan evidence yang relevan.
- Menyiapkan retesting setelah defect diperbaiki oleh developer.
- Menyiapkan focused regression testing untuk memastikan perbaikan tidak menimbulkan regression pada fungsi terkait.

---

### 3. Scope of Testing

Pengujian dilakukan terhadap 12 area utama aplikasi.

#### 3.1 Authentication

- Login menggunakan akun valid.
- Login menggunakan akun tidak valid.
- Validasi field login.
- Validasi akun aktif dan tidak aktif.
- Password visibility.
- Redirect setelah login.
- Logout dan session access.

#### 3.2 Dashboard

- Menampilkan informasi dashboard.
- Memastikan data ringkasan dapat dimuat.
- Memastikan data dashboard sesuai kondisi aplikasi.
- Memastikan akses dan navigasi dari dashboard berjalan dengan benar.

#### 3.3 Product Management

- Menampilkan daftar produk.
- Menambahkan produk.
- Mengubah data produk.
- Mengelola status/data produk sesuai hak akses.
- Validasi input produk.
- Pencarian dan pengelolaan data produk.
- Memastikan konsistensi stok dan data produk.

#### 3.4 Stock In

- Menambahkan transaksi stok masuk.
- Memilih produk.
- Memasukkan jumlah stok.
- Memilih lokasi penyimpanan.
- Memilih tanggal masuk.
- Membuat batch baru.
- Memastikan perubahan stok setelah transaksi.
- Validasi input dan kondisi transaksi.
- Penanganan kegagalan proses penyimpanan.

#### 3.5 Stock Out

- Membuat transaksi stok keluar.
- Memastikan stok tersedia.
- Memastikan quantity tidak menyebabkan stok negatif.
- Validasi batch.
- Validasi urutan FIFO.
- Pengeluaran lintas-batch jika diperlukan.
- Memastikan perubahan stok setelah transaksi.
- Memastikan histori transaksi tersimpan.
- Validasi kondisi gagal.

#### 3.6 QR / Scanner

- Membaca QR code yang valid.
- Memastikan QR mengarah ke data yang benar.
- Menangani QR yang tidak dikenal.
- Menangani QR/input yang tidak dapat dibaca.
- Memastikan scan tidak memilih produk atau batch yang salah.

#### 3.7 Transaction History

- Menampilkan riwayat transaksi.
- Memastikan transaksi stok masuk tercatat.
- Memastikan transaksi stok keluar tercatat.
- Menampilkan detail transaksi.
- Memastikan histori konsisten dengan transaksi yang terjadi.

#### 3.8 Reports

- Menampilkan laporan stok.
- Memastikan nilai stok dan status sesuai data aplikasi.
- Generate/print laporan PDF.
- Menampilkan laporan kondisi batch.
- Memastikan aplikasi menangani kondisi data laporan kosong dengan aman.

#### 3.9 User Management

- Menampilkan daftar pengguna.
- Menambahkan pengguna.
- Validasi input pengguna.
- Mengubah role pengguna sesuai kewenangan.
- Mengaktifkan dan menonaktifkan pengguna.
- Memastikan pengguna nonaktif tidak mendapatkan akses.
- Validasi proteksi terhadap akun yang sedang digunakan dan operasi penghapusan user.

#### 3.10 Alerts

- Menampilkan alert sesuai kondisi stok atau batch.
- Memastikan isi alert sesuai kondisi aktual.
- Memastikan navigasi dari alert menuju halaman terkait berjalan sesuai tujuan.
- Memastikan alert diperbarui ketika kondisi pemicu sudah berubah.

#### 3.11 Analysis

- Menampilkan analisis tren stok berdasarkan data aplikasi.
- Memastikan hasil regresi menggunakan data historis yang relevan.
- Memastikan slope, relative slope, R², dan prediksi dapat ditampilkan pada kondisi data yang memadai.
- Memastikan validasi regresi seperti MAE, RMSE, dan WAPE dapat ditampilkan jika data memadai.
- Memastikan kondisi data tidak mencukupi ditangani dengan aman.

#### 3.12 Navigation

- Memastikan menu membuka halaman yang sesuai.
- Memastikan back navigation bekerja dengan benar dan konsisten.
- Mengamati stabilitas navigasi berulang.
- Mengamati loading state pada halaman yang bergantung pada data.
- Memastikan gangguan koneksi ditangani tanpa crash dan tanpa mengekspos error teknis yang tidak ramah pengguna.

> Catatan: pemeriksaan kondisi batch yang berkaitan dengan stok/condition tidak dipisahkan sebagai modul test case tersendiri. Perilaku tersebut tercakup pada Reports, Alerts, dan Analysis sesuai fungsi yang diuji.

---

### 4. Test Types

#### Functional Testing

Memastikan fungsi aplikasi menghasilkan perilaku sesuai requirement dan expected result.

#### Black Box Testing

Pengujian dilakukan melalui input, action, dan output yang dapat diamati tanpa menjadikan implementasi internal source code sebagai dasar hasil PASS/FAIL.

#### Positive Testing

Pengujian menggunakan input dan kondisi valid untuk memastikan fungsi normal berjalan dengan benar.

#### Negative Testing

Pengujian menggunakan input tidak valid, kondisi tidak tersedia, atau error state untuk memastikan aplikasi menangani kegagalan dengan aman.

#### Boundary Testing

Pengujian dilakukan pada nilai atau kondisi batas tertentu, misalnya stok 0, jumlah maksimum berdasarkan stok tersedia, dan kondisi di sekitar batas input.

#### Validation Testing

Memastikan form, input, rule, dan proses memiliki validasi sesuai kebutuhan.

#### Authorization Testing

Memastikan akses dan tindakan pengguna sesuai dengan role serta status akun.

#### UI/UX Consistency Testing

Memastikan elemen antarmuka dan navigasi pada halaman sejenis menggunakan pola yang konsisten.

#### Stability Testing

Mengamati apakah aplikasi tetap stabil ketika digunakan melalui beberapa navigasi atau flow secara berulang.

#### Retesting

Retesting dilakukan **setelah developer menyediakan fix** untuk defect yang ditemukan. Retesting memverifikasi bahwa test case yang sebelumnya FAIL sudah menghasilkan actual result sesuai expected result.

#### Focused Regression Testing

Focused regression testing dilakukan **setelah fix tersedia dan retest berhasil**, dengan menguji fungsi yang berkaitan dengan area perubahan untuk memastikan fix tidak menyebabkan masalah baru.

---

### 5. Test Environment

**Application:** Toko Abunawas Inventory Application  
**Framework:** Flutter  
**Authentication:** Firebase Authentication  
**Database:** Cloud Firestore  
**Testing Method:** Manual Testing  
**Test Environment:** Development / Local Application  
**Test Device:** Android physical device and/or emulator sesuai kebutuhan pengujian  

Pengujian yang bergantung pada Firebase memerlukan koneksi jaringan, kecuali pada skenario yang memang menguji gangguan koneksi.

---

### 6. Test Data

Data pengujian dapat meliputi:

- User valid dan tidak valid.
- User aktif dan tidak aktif.
- Role Pemilik/Owner dan Karyawan.
- Produk valid.
- Produk dengan data/input tidak valid.
- Stok tersedia dan stok kosong.
- Batch aktif.
- Beberapa batch untuk pengujian FIFO.
- Quantity valid.
- Quantity sama dengan atau melebihi batas stok.
- Transaksi stok masuk.
- Transaksi stok keluar.
- QR code valid.
- QR code tidak dikenal atau tidak valid.
- Data historis yang memadai untuk analisis.
- Data historis yang tidak memadai.
- Kondisi jaringan normal.
- Kondisi jaringan/Firestore tidak tersedia.

Data digunakan khusus untuk kebutuhan pengujian dan disiapkan sesuai skenario masing-masing test case.

---

### 7. Entry Criteria

Initial test execution dapat dimulai apabila:

- Aplikasi dapat dijalankan.
- Modul yang akan diuji tersedia.
- Akun pengujian tersedia.
- Data pengujian dapat disiapkan.
- Database/Firebase dapat diakses untuk skenario normal.
- Perangkat memiliki izin yang diperlukan, seperti camera permission untuk QR scanner.
- Test scenario dan test case telah tersedia.

---

### 8. Exit Criteria

#### 8.1 Initial Manual Test Cycle

Initial manual test cycle dianggap selesai apabila:

- Seluruh test case yang direncanakan telah dieksekusi.
- Expected result telah dibandingkan dengan actual result.
- Status PASS/FAIL telah dicatat.
- Defect yang ditemukan telah didokumentasikan.
- Evidence atau execution notes yang relevan telah dicatat.
- Tidak ada test case yang masih berstatus Not Executed pada scope current cycle.

Initial cycle **dapat berakhir dengan Open Defects** selama defect tersebut sudah dicatat dan dilaporkan dengan jelas.

#### 8.2 Defect Closure Cycle

Suatu defect dapat dinyatakan Closed/Resolved setelah:

- Developer menyediakan fix.
- QA menjalankan retesting pada test case yang sebelumnya gagal.
- Retesting menghasilkan PASS.
- Focused regression testing pada fungsi terkait telah dijalankan dan tidak menemukan regression yang menghalangi closure.

Dengan demikian, completion dari initial test cycle tidak sama dengan closure seluruh defect.

---

### 9. Test Deliverables

Dokumentasi yang dihasilkan pada portfolio ini:

- Test Plan
- Test Scenarios
- Test Cases
- Test Execution Results
- Bug / Defect Report
- Testing Evidence / Execution Notes
- Retesting Plan
- Focused Regression Testing Plan
- Test Summary Report

Jika fix tersedia pada siklus berikutnya, deliverable dapat diperbarui dengan hasil retesting dan regression testing aktual.

---

### 10. Defect Handling Process

Jika ditemukan defect, alur yang digunakan adalah:

1. QA menemukan perilaku sistem yang tidak sesuai expected result.
2. QA memastikan defect dapat direproduksi.
3. QA mencatat langkah reproduksi.
4. QA mencatat expected result dan actual result.
5. QA menentukan severity dan priority sesuai dampak dan urgensi.
6. QA melampirkan evidence yang relevan.
7. QA membuat atau memperbarui Bug Report.
8. Defect diserahkan kepada developer untuk dilakukan perbaikan.
9. Setelah fix tersedia, QA melakukan retesting.
10. Jika retesting PASS, QA menjalankan focused regression testing pada fungsi terkait.
11. Defect dapat diubah menjadi Closed/Resolved setelah hasil retest dan regression memenuhi kriteria.

Pada current cycle, QA **tidak melakukan perubahan kode sebagai bagian dari aktivitas testing**. Tiga defect yang ditemukan masih berstatus Open sehingga retesting dan regression testing belum dieksekusi.

---

### 11. Evidence Strategy

Screenshot tidak diwajibkan untuk setiap test case PASS.

Evidence diprioritaskan untuk:

- Test case yang FAIL.
- Confirmed defect.
- Critical/high-risk scenario.
- Representative functional test.
- Kondisi yang lebih efektif dibuktikan melalui visual.

Untuk test observasional yang mencakup banyak layar atau flow, hasil dapat dicatat melalui **Actual Result** dan **Notes** tanpa dedicated screenshot.

Contoh:

- `TC-NAV-003` menggunakan observational execution untuk stabilitas navigasi berulang.
- `TC-NAV-004` menggunakan observational execution untuk verifikasi loading state di beberapa halaman.

---

### 12. Risk

Risiko selama testing meliputi:

- Ketergantungan terhadap koneksi internet.
- Gangguan layanan Firebase/Cloud Firestore.
- Perbedaan perilaku pada perangkat yang berbeda.
- Data testing dapat memengaruhi database.
- Perubahan fitur dapat membutuhkan retesting dan regression testing.
- QR scanner bergantung pada camera permission dan kualitas input QR.

Mitigasi dilakukan menggunakan data testing yang terkontrol, pencatatan kondisi sebelum/sesudah transaksi, serta pengujian ulang pada skenario yang relevan apabila terjadi perubahan.

---

### 13. Current Test Cycle Result

Pada current manual testing cycle:

| Metric | Result |
|---|---:|
| Total Test Cases | 78 |
| Executed | 78 |
| Passed | 75 |
| Failed | 3 |
| Blocked | 0 |
| Not Executed | 0 |
| Execution Progress | 100% |
| Pass Rate | 96.15% |

Tiga defect yang ditemukan:

- **BUG-001 / TC-SCAN-003** — Unknown QR code menampilkan raw Cloud Firestore assertion error.
- **BUG-002 / TC-NAV-002** — Back arrow pada Transaction History tidak konsisten.
- **BUG-003 / TC-NAV-005** — Gangguan jaringan/Firestore pada Stock In menampilkan raw technical error kepada user.

Ketiga defect masih berstatus **Open**.

**Retesting Status:** Not Executed  
**Regression Testing Status:** Not Executed  

Retesting dan focused regression testing telah direncanakan melalui dokumen `05-Regression-Testing/Regression_Testing.xlsx` dan akan dieksekusi apabila fix dari development tersedia.

**Current Test Cycle Status: COMPLETED WITH OPEN DEFECTS**
