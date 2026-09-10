# Test Summary Report
## Toko Abunawas Inventory Application

### 1. Project Information

**Project Name:** Toko Abunawas Inventory Application  
**Testing Role:** Software Quality Assurance / Manual Tester  
**Testing Method:** Manual Testing  
**Testing Approach:** Black Box Testing  
**Test Cycle Status:** Completed with Open Defects  

---

### 2. Testing Objective

Pengujian dilakukan untuk memastikan fungsi utama pada Toko Abunawas Inventory Application berjalan sesuai dengan kebutuhan sistem dan menghasilkan output yang sesuai dengan expected result.

Pengujian mencakup validasi fungsi utama aplikasi, skenario positif dan negatif, validasi input, pengujian batas, pengecekan navigasi, serta penanganan kondisi error pada aplikasi.

---

### 3. Testing Scope

Modul yang diuji meliputi:

- Authentication
- Dashboard
- Product Management
- Stock In
- Stock Out
- QR / Barcode Scanner
- Transaction History
- Reports
- User Management
- Alerts
- Analysis
- Navigation

---

### 4. Test Execution Summary

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

---

### 5. Defect Summary

Selama proses pengujian ditemukan 3 defect yang masih berstatus Open.

| Bug ID | Related Test Case | Module | Summary | Severity | Priority | Status |
|---|---|---|---|---|---|---|
| BUG-001 | TC-SCAN-003 | Scanner / Stock Out | Unknown QR code menampilkan raw Cloud Firestore assertion error | High | High | Open |
| BUG-002 | TC-NAV-002 | History / Navigation | Back arrow pada halaman Transaction History tidak konsisten dengan halaman lain | Low | Medium | Open |
| BUG-003 | TC-NAV-005 | Stock In / Network Handling | Network interruption menampilkan raw Cloud Firestore unavailable error kepada user | Medium | High | Open |

---

### 6. Key Findings

#### BUG-001 — Unknown QR Handling
Ketika QR code yang tidak dikenal atau tidak terdaftar dipindai, aplikasi menampilkan raw Cloud Firestore assertion error kepada user. Sistem seharusnya menampilkan pesan validasi yang lebih ramah dan tidak mengekspos error internal.

#### BUG-002 — Navigation UI Consistency
Back arrow pada halaman Transaction History memiliki tampilan yang berbeda dibandingkan halaman lain yang sejenis. Fungsi navigasi tetap tersedia, tetapi konsistensi UI perlu diperbaiki.

#### BUG-003 — Network Error Handling
Ketika koneksi jaringan atau layanan Firestore tidak tersedia pada proses Stock In, aplikasi menampilkan raw Cloud Firestore error. Sistem seharusnya menampilkan pesan koneksi yang lebih mudah dipahami serta memberikan kemungkinan retry setelah koneksi kembali tersedia.

---

### 7. Retesting and Regression Testing Status

Retesting dan regression testing belum dieksekusi karena ketiga defect masih berstatus Open dan belum tersedia perbaikan dari sisi development.

Dokumen retesting dan regression testing telah disiapkan untuk digunakan setelah defect diperbaiki.

Alur berikutnya:

1. Developer melakukan perbaikan terhadap BUG-001, BUG-002, dan BUG-003.
2. QA melakukan retesting terhadap test case yang sebelumnya gagal.
3. Jika retesting berhasil, QA menjalankan focused regression testing pada fitur terkait.
4. Defect dapat ditutup apabila hasil retesting dan regression testing sesuai expected result.

**Current Retest Status:** Not Executed  
**Current Regression Testing Status:** Not Executed  

---

### 8. Testing Evidence

Screenshot evidence disimpan pada direktori:

`06-Evidence/`

Evidence diberi nama berdasarkan Test Case ID agar memiliki traceability dengan dokumen Test Cases dan Bug Report.

Evidence utama untuk defect:

- `06-Evidence/Scanner/TC-SCAN-003.png`
- `06-Evidence/Navigation/TC-NAV-002.png`
- `06-Evidence/Navigation/TC-NAV-005.png`

---

### 9. Test Deliverables

Dokumentasi QA yang telah disiapkan:

- Test Plan
- Test Scenarios
- Test Cases
- Bug Report
- Testing Evidence
- Retesting & Regression Testing Plan
- Test Summary Report

---

### 10. Final Conclusion

Berdasarkan hasil manual testing terhadap 78 test case, sebanyak 75 test case menghasilkan status PASS dan 3 test case menghasilkan status FAIL.

Execution progress mencapai 100% dengan pass rate sebesar 96.15%.

Tiga defect berhasil diidentifikasi dan didokumentasikan melalui Bug Report. Ketiga defect masih berstatus Open sehingga retesting dan regression testing belum dijalankan.

Secara umum, fungsi utama aplikasi telah berjalan sesuai expected result pada sebagian besar skenario pengujian. Namun, aplikasi masih membutuhkan perbaikan pada penanganan QR tidak dikenal, konsistensi navigasi pada halaman Transaction History, serta penanganan error saat terjadi gangguan koneksi sebelum defect dapat ditutup.

**Final Test Cycle Status: COMPLETED WITH OPEN DEFECTS**
