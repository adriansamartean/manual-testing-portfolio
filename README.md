# Automation Exercise - Manual + API Testing Project

[![Manual Testing](https://img.shields.io/badge/Testing-Manual%20%2B%20API-blue)]()
[![Black Box](https://img.shields.io/badge/Approach-Black%20Box-orange)]()
[![UI Test Cases](https://img.shields.io/badge/UI%20Test%20Cases-50-informational)]()
[![API Test Cases](https://img.shields.io/badge/API%20Test%20Cases-24-informational)]()
[![Postman](https://img.shields.io/badge/Tool-Postman-orange)]()
[![Bug Found](https://img.shields.io/badge/Bug%20Found-1%20High-red)]()

End-to-end manual testing project for the [Automation Exercise](https://www.automationexercise.com) e-commerce demo application, covering both the **web user interface** and the **public REST API** documented at [/api_list](https://www.automationexercise.com/api_list).

This is the second project in my QA portfolio, building on the foundations from the SauceDemo project and extending into API testing with Postman.

> **Author:** Adrian-Stefan Samartean
> **Role applied for:** QA Engineer (Manual + API Testing) - Entry Level
> **Location:** Cluj-Napoca, Romania
> **Email:** samarteanadrian245@gmail.com
> **Certification:** QA Manual Testing - Azimut Vision (accredited by Romanian Ministry of Labour)

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Application Under Test](#application-under-test)
3. [Deliverables](#deliverables)
4. [Test Approach](#test-approach)
5. [UI Test Coverage](#ui-test-coverage)
6. [API Test Coverage](#api-test-coverage)
7. [Execution Results](#execution-results)
8. [Bug Found](#bug-found)
9. [How to Run the Postman Collection](#how-to-run-the-postman-collection)
10. [Tools Used](#tools-used)
11. [What This Project Adds Beyond SauceDemo](#what-this-project-adds-beyond-saucedemo)

---

## Project Overview

This project demonstrates two complementary types of QA testing on the same application:

- **Manual UI Testing** - functional verification through the web browser, using Black Box techniques to design 50 test cases across 12 modules.
- **API Testing** - direct verification of the application's REST API using Postman, covering all 14 documented endpoints with 24 test cases.

The combination shows that I can validate an application from both the user's perspective (UI) and the integration / backend perspective (API) - a skill set that is specifically called out in junior QA job postings in the Cluj-Napoca area.

---

## Application Under Test

**Automation Exercise** - a publicly available e-commerce demo application designed for QA practice, including a documented public REST API.

- **Web URL:** https://www.automationexercise.com
- **API Base URL:** https://www.automationexercise.com/api
- **API Documentation:** https://www.automationexercise.com/api_list
- **Why this app:** It is significantly more complex than SauceDemo and includes a real API surface, making it ideal to demonstrate full-stack testing skills.

### Main features tested

**UI side:**
- User registration and account creation flow
- Login, logout, account deletion
- Home page navigation and main menu
- Product catalog: browsing, search, category and brand filtering
- Product detail pages: view, add to cart, write reviews
- Shopping cart: add, remove, update quantity, persistence
- Checkout flow: address review, payment form, order confirmation, invoice download
- Contact Us form
- Newsletter subscription

**API side (all 14 documented endpoints):**
- API 1: GET /productsList - get all products
- API 2: POST /productsList - method-not-allowed handling
- API 3: GET /brandsList - get all brands
- API 4: PUT /brandsList - method-not-allowed handling
- API 5: POST /searchProduct - search products
- API 6: POST /searchProduct - missing-parameter handling
- API 7: POST /verifyLogin - login with valid credentials
- API 8: POST /verifyLogin - missing email or password
- API 9: DELETE /verifyLogin - method-not-allowed handling
- API 10: POST /verifyLogin - invalid credentials
- API 11: POST /createAccount - register new user
- API 12: DELETE /deleteAccount - delete account
- API 13: PUT /updateAccount - update account
- API 14: GET /getUserDetailByEmail - retrieve user details

---

## Deliverables

| # | Document | Format | Description |
|---|----------|--------|-------------|
| 1 | [Test Plan](./01_Test_Plan_AutomationExercise.docx) | DOCX | Scope, objectives, approach, environment, schedule, risks, exit criteria - covering both UI and API layers |
| 2 | [UI Test Cases](./02_Test_Cases_AutomationExercise.xlsx) | XLSX | 50 functional UI test cases across 12 modules with execution results and pass-rate summary |
| 3 | [Bug Reports](./03_Bug_Reports_AutomationExercise.xlsx) | XLSX | Bug tracker, reusable template, and full bug report for the defect found |
| 4 | [API Test Cases](./04_API_Test_Cases_AutomationExercise.xlsx) | XLSX | 24 API test cases covering all 14 documented endpoints with execution results |
| 5 | [Postman Collection](./05_AutomationExercise_Postman_Collection.json) | JSON | Importable Postman collection with all 24 API requests pre-configured |
| 6 | [Screenshots](./screenshots) | PNG | Visual evidence supporting the bug report |

---

## Test Approach

I followed a Black Box approach for both layers, combining established techniques:

| Technique | Where applied |
|-----------|---------------|
| Equivalence Partitioning | Login credentials, registration form, search input |
| Boundary Value Analysis | Field length limits (name, address, postal code), quantity bounds |
| Decision Table Testing | Registration form valid / invalid combinations |
| State Transition Testing | Guest -> Registered -> Logged In -> Order Placed -> Logged Out |
| Error Guessing | Duplicate registrations, expired sessions, malformed API payloads |
| Exploratory Testing | Investigating unexpected API responses, database state verification |

### Test levels covered

- **Smoke Testing** - critical path validation (login, add to cart, checkout, key APIs)
- **Functional Testing** - feature-by-feature verification on UI and API
- **API Testing** - status codes, response payloads, error handling, schema validation
- **Negative Testing** - invalid inputs, missing parameters, wrong HTTP methods
- **Stateful Testing** - full CRUD lifecycle on user accounts via API (Create -> Read -> Update -> Read -> Delete -> Read)

---

## UI Test Coverage

**50 test cases** distributed across 12 modules:

| Module | Test Cases |
|--------|------------|
| Products | 10 |
| Cart | 8 |
| Checkout | 8 |
| Homepage | 5 |
| Registration | 5 |
| Login | 4 |
| Negative / Edge cases | 5 |
| Contact | 3 |
| Informational pages | 3 |

Each test case includes: ID, module, scenario, title, priority, preconditions, detailed steps, test data, expected result, actual result observed during execution, status, tester, and execution date.

---

## API Test Coverage

**24 API test cases** distributed by HTTP method:

| Method | Test Cases | Purpose |
|--------|------------|---------|
| POST | 13 | Create, search, login, register, update operations |
| GET | 7 | Retrieve products, brands, user details |
| PUT | 2 | Update operations |
| DELETE | 2 | Delete and method-validation tests |

Each API test case captures: endpoint, HTTP method, full request URL, headers, body payload, expected status code, expected response body, actual status code, and actual response body.

---

## Execution Results

### UI Testing

| Metric | Count | Percentage |
|--------|-------|------------|
| Total Test Cases | 50 | 100% |
| Passed | 50 | 100% |
| Failed | 0 | 0% |

All UI flows function as expected. Critical user journeys (registration, login, add to cart, checkout, place order) work correctly. Several minor UX gaps were observed but did not constitute functional defects.

### API Testing

| Metric | Count | Percentage |
|--------|-------|------------|
| Total Test Cases | 24 | 100% |
| Passed | 23 | 95.8% |
| Failed | 1 | 4.2% |

All 14 documented endpoints behave consistently with the API specification, with one significant exception found in the createAccount endpoint (see Bug Found section below).

### Combined

- **Total test cases executed:** 74
- **Combined pass rate:** 98.6%
- **Defects found:** 1 (High severity)

---

## Bug Found

**BUG_001 - API /createAccount accepts invalid email format**

| Field | Value |
|-------|-------|
| Severity | High |
| Priority | P1 |
| Module | API 11 - createAccount |
| Linked Test Case | TC_API_22 |
| Status | Open |

**Summary:** The POST /api/createAccount endpoint accepts and successfully creates user accounts with email values that do not match a valid email format (no '@' symbol, no domain). The server-side validation is missing entirely, meaning anyone using Postman, curl, or DevTools can bypass the UI's HTML5 type='email' validation.

**Confirmation:** I verified the bug with multiple test attempts using unique invalid email values. Each attempt returned `{"responseCode": 201, "message": "User created!"}`. I then confirmed via GET /api/getUserDetailByEmail that the accounts were genuinely persisted in the database.

**Historical impact:** During investigation, I queried the database for the email value 'notanemail' and discovered an existing account (id 816102, name 'mohamed') created by a previous tester - proof that this defect has been impacting the production database over time.

**Why this matters:**
- Security and data integrity: invalid emails cannot receive password resets, confirmations, or notifications
- Email deliverability: outgoing messages to these accounts hard-bounce, polluting reputation
- UI bypass: HTML5 client-side validation is not a substitute for server-side validation

See [03_Bug_Reports_AutomationExercise.xlsx](./03_Bug_Reports_AutomationExercise.xlsx) for the full bug report with steps to reproduce, expected vs actual results, and screenshots.

---

## How to Run the Postman Collection

1. **Install Postman** from https://www.postman.com/downloads (free)
2. **Open Postman** and click **Import** (top-left)
3. **Drop the file** `05_AutomationExercise_Postman_Collection.json` into the import dialog
4. The collection appears in the left sidebar under "Automation Exercise - API Testing"
5. **Set collection variables** before running:
   - `base_url` - already set to `https://www.automationexercise.com/api`
   - `api_test_email` - **change to a unique email** before each run (e.g., `your_name_test_DATE@example.com`)
   - `api_test_password` - any valid password
6. **Run individual requests** by clicking on each and pressing Send, OR
7. **Run the whole collection** via Collection Runner (recommended order: TC_API_14 -> TC_API_17 -> TC_API_18 -> TC_API_16 for stateful flow)
8. **Cleanup:** after running stateful tests, always run TC_API_16 to delete the test account from the database.

---

## Tools Used

| Category | Tool |
|----------|------|
| Test Case Management | Microsoft Excel |
| API Testing | Postman (with collection export to JSON) |
| Bug Tracking | Excel template |
| Documentation | Microsoft Word, Markdown |
| Browsers | Chrome (primary) |
| Inspection | Chrome DevTools (Network, Elements, Console) |
| Screenshots | ShareX / Snipping Tool |
| Version Control | Git, GitHub |

---

## What This Project Adds Beyond SauceDemo

This second project deliberately covers ground that SauceDemo did not, demonstrating broader QA capability:

| Capability | SauceDemo | Automation Exercise |
|------------|-----------|---------------------|
| Manual UI testing | Yes (32 test cases) | Yes (50 test cases) |
| API testing | No | Yes (24 test cases, Postman collection) |
| Account creation flow | No (pre-existing users) | Yes (full registration + email validation) |
| Search and filtering | No | Yes (search + category + brand filters) |
| Public API documentation | No | Yes (14 endpoints) |
| Application complexity | Small (6 products, fixed users) | Large (30+ products, dynamic user accounts) |
| State transition testing | Limited | Full CRUD via API: Create -> Read -> Update -> Read -> Delete |
| Bug discovered through investigation | UI bugs intentionally seeded | Real backend defect found via API testing (server-side validation gap) |

The combined portfolio demonstrates progression: the SauceDemo project established the fundamentals; this project shows I can apply those fundamentals to a more realistic application, extend them into API-level verification, and uncover non-obvious defects through systematic investigation.

---

## Contact

If you are a recruiter or QA Lead reviewing this project, I would be happy to talk.

- **Email:** samarteanadrian245@gmail.com
- **Phone:** +40 740 565 596
- **Location:** Cluj-Napoca, RO (open to on-site, hybrid, or remote)

---

*Last updated: April 2026*
