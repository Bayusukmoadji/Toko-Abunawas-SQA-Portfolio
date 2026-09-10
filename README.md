# Toko Abunawas — Software Quality Assurance Portfolio

This repository contains my **Software Quality Assurance (SQA) portfolio** for the **Toko Abunawas Inventory Application**. The project demonstrates a structured manual testing process, from test planning and test-case design to test execution, defect reporting, evidence collection, and preparation for retesting and regression testing.

> **Current QA Cycle:** Completed with Open Defects  
> **78 Test Cases Executed | 75 Passed | 3 Failed | 3 Defects Identified**

---

## System Under Test

**Toko Abunawas Inventory Application** is an inventory management application developed using **Flutter** with **Firebase Authentication** and **Cloud Firestore**.

The application includes functionality such as:

- Authentication and role-based access
- Dashboard
- Product management
- Stock In and batch management
- Stock Out with FIFO flow
- QR code scanning
- Transaction history
- Reports
- User management
- Alerts
- Stock analysis
- Application navigation

**Application Source Repository:**  
[Bayusukmoadji/toko_abunawas_apk](https://github.com/Bayusukmoadji/toko_abunawas_apk)

---

## Testing Objective

The objective of this testing project is to verify that the application's main functions behave according to their expected results and to identify defects that could affect functionality, usability, data integrity, or user experience.

The testing process was performed manually using a black-box approach based on observable application behavior.

---

## Testing Approach

The portfolio includes practical implementation of:

- Manual Testing
- Black Box Testing
- Functional Testing
- Positive Testing
- Negative Testing
- Validation Testing
- Boundary Testing
- Authorization Testing
- UI/UX Consistency Testing
- Stability Testing
- Defect Reporting
- Retesting Planning
- Focused Regression Testing Planning

---

## Test Scope

Testing covered **12 application modules**:

| No. | Module | Test Cases |
|---:|---|---:|
| 1 | Authentication | 10 |
| 2 | Dashboard | 5 |
| 3 | Product Management | 10 |
| 4 | Stock In | 9 |
| 5 | Stock Out | 10 |
| 6 | Scanner | 5 |
| 7 | Transaction History | 5 |
| 8 | Reports | 5 |
| 9 | User Management | 7 |
| 10 | Alerts | 3 |
| 11 | Analysis | 4 |
| 12 | Navigation | 5 |
|  | **Total** | **78** |

---

## Test Execution Result

| Metric | Result |
|---|---:|
| Total Test Cases | **78** |
| Executed | **78** |
| Passed | **75** |
| Failed | **3** |
| Blocked | **0** |
| Not Executed | **0** |
| Execution Progress | **100%** |
| Pass Rate | **96.15%** |

### Final Test Cycle Status

**COMPLETED WITH OPEN DEFECTS**

The purpose of this portfolio is not to present a system with zero defects, but to demonstrate a realistic QA workflow in which failures are identified, documented, traced to test cases, and prepared for retesting after a fix becomes available.

---

## Defects Identified

Three defects were identified during manual testing:

| Bug ID | Related Test Case | Area | Finding | Severity | Priority | Status |
|---|---|---|---|---|---|---|
| **BUG-001** | TC-SCAN-003 | Scanner / Stock Out | Unknown QR code exposes a raw Cloud Firestore assertion error instead of a user-friendly validation message | High | High | Open |
| **BUG-002** | TC-NAV-002 | History / Navigation | Back arrow on Transaction History is visually inconsistent with comparable pages | Low | Medium | Open |
| **BUG-003** | TC-NAV-005 | Stock In / Network Handling | Network interruption exposes a raw Cloud Firestore unavailable error instead of controlled connectivity feedback | Medium | High | Open |

Detailed reproduction steps, expected results, actual results, severity, priority, evidence references, impact, and recommendations are available in the **Bug Report**.

---

## Retesting & Regression Testing

The three identified defects are currently **Open**.

Therefore:

- **Retesting Status:** Not Executed
- **Regression Testing Status:** Not Executed

Retest and focused regression scenarios have already been prepared and will be executed after fixes become available.

Planned QA flow:

**Defect Found → Bug Report → Developer Fix → Retest → Focused Regression Testing → Defect Closure**

This separation is intentional: a failed test is not marked as passed until the related defect has actually been fixed and verified.

---

## Repository Structure

```text
Toko-Abunawas-SQA-Portfolio/
│
├── 01-Test-Plan/
│   └── Test_Plan.md
│
├── 02-Test-Scenarios/
│   └── Test_Scenarios.xlsx
│
├── 03-Test-Cases/
│   └── Test_Cases.xlsx
│
├── 04-Bug-Reports/
│   └── Bug_Report.xlsx
│
├── 05-Regression-Testing/
│   └── Regression_Testing.xlsx
│
├── 06-Evidence/
│   ├── Authentication/
│   ├── Dashboard/
│   ├── Product-Management/
│   ├── Stock-In/
│   ├── Stock-Out/
│   ├── Scanner/
│   ├── History/
│   ├── Reports/
│   ├── User-Management/
│   ├── Alerts/
│   ├── Analysis/
│   └── Navigation/
│
├── 07-Test-Summary/
│   └── Test_Summary_Report.md
│
└── README.md
```

---

## QA Documentation

| Document | Description |
|---|---|
| [Test Plan](./01-Test-Plan/Test_Plan.md) | Testing objectives, scope, strategy, environment, criteria, and deliverables |
| [Test Scenarios](./02-Test-Scenarios/Test_Scenarios.xlsx) | High-level testing scenarios for the application modules |
| [Test Cases](./03-Test-Cases/Test_Cases.xlsx) | Detailed manual test cases including expected and actual results |
| [Bug Report](./04-Bug-Reports/Bug_Report.xlsx) | Documentation of defects discovered during test execution |
| [Regression Testing](./05-Regression-Testing/Regression_Testing.xlsx) | Retest and focused regression scenarios prepared for future fixes |
| [Testing Evidence](./06-Evidence/) | Screenshot evidence organized by module and Test Case ID |
| [Test Summary Report](./07-Test-Summary/Test_Summary_Report.md) | Final summary of the current manual testing cycle |

---

## Traceability

The documentation uses consistent identifiers to make findings traceable across artifacts.

Example:

```text
Test Scenario
   ↓
Test Case
   ↓
Test Execution Result
   ↓
Evidence
   ↓
Bug Report (if failed)
   ↓
Retest / Regression Plan
```

Example defect trace:

```text
TC-SCAN-003
   ↓
FAIL
   ↓
06-Evidence/Scanner/TC-SCAN-003.png
   ↓
BUG-001
   ↓
RT-001 + related regression scenarios
```

---

## Evidence

Testing evidence is stored in the [`06-Evidence`](./06-Evidence/) directory.

Screenshots are organized by module and named using the corresponding **Test Case ID**.

Key defect evidence:

- [`TC-SCAN-003`](./06-Evidence/Scanner/TC-SCAN-003.png) — BUG-001
- [`TC-NAV-002`](./06-Evidence/Navigation/TC-NAV-002.png) — BUG-002
- [`TC-NAV-005`](./06-Evidence/Navigation/TC-NAV-005.png) — BUG-003

---

## Skills Demonstrated

Through this portfolio, I demonstrate practical understanding of:

- Translating application behavior into test scenarios and test cases
- Designing positive and negative test conditions
- Comparing expected results with actual application behavior
- Identifying and documenting reproducible defects
- Assigning severity and priority based on defect impact
- Maintaining traceability between test cases, evidence, and defects
- Testing QR-based inventory flows
- Testing FIFO-related stock-out behavior
- Testing role and access behavior
- Testing network/error-handling conditions
- Reviewing navigation and UI consistency
- Preparing retesting and regression testing after defect fixes

---

## Tools & Technologies

**QA Documentation**
- Microsoft Excel / Spreadsheet
- Markdown
- Git & GitHub
- Screenshot evidence

**System Under Test**
- Flutter
- Firebase Authentication
- Cloud Firestore
- QR Code / Scanner functionality

---

## Notes

This repository represents an **independent Software Quality Assurance portfolio project** based on an application that I also developed as an academic/final project.

The QA documentation reflects actual manual test execution. Failed cases and open defects are intentionally retained to demonstrate the defect-identification and reporting process rather than presenting artificial 100% test results.

---

## Author

**Bayu Sukmo Adji**  
Fresh Graduate — Informatics Engineering  
Aspiring Software Quality Assurance

- GitHub: [Bayusukmoadji](https://github.com/Bayusukmoadji)
- Application Repository: [toko_abunawas_apk](https://github.com/Bayusukmoadji/toko_abunawas_apk)

---

*Software Quality Assurance Portfolio — Toko Abunawas Inventory Application*
