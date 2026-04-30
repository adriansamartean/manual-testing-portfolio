[README.md](https://github.com/user-attachments/files/27247995/README.md)
# Manual Testing Portfolio

[![Manual Testing](https://img.shields.io/badge/Testing-Manual%20%2B%20API-blue)]()
[![Black Box](https://img.shields.io/badge/Approach-Black%20Box-orange)]()
[![Test Cases](https://img.shields.io/badge/Test%20Cases-106-informational)]()
[![Bugs Reported](https://img.shields.io/badge/Bugs%20Reported-6-red)]()
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)]()

Hands-on QA portfolio - real test plans, test cases, bug reports, and a Postman collection across two complementary web applications. This repository documents my work as I grow into a Manual QA Engineer role, applying industry-standard practices to publicly available demo applications.

> **Author:** Adrian-Stefan Samartean
> **Role:** Aspiring QA Engineer (Manual + API Testing) - Entry Level
> **Location:** Cluj-Napoca, Romania
> **Email:** samarteanadrian245@gmail.com
> **Phone:** +40 740 565 596
> **Certification:** QA Manual Testing - Azimut Vision (accredited by the Romanian Ministry of Labour)

---

## About Me

I am a Master's student in Global Politics and Human Rights at Babes-Bolyai University, with a Manual Testing certification accredited by the Romanian Ministry of Labour and a strong analytical background from my Security Studies degree. My academic training taught me to dissect complex systems, document findings precisely, and communicate clearly - skills that translate directly into QA work.

This portfolio is my way of demonstrating, not just claiming, that I can plan, execute, and report on manual and API tests at a professional level.

---

## Projects

| # | Project | Application Type | Test Cases | Bugs Found | Status |
|---|---------|-----------------|------------|------------|--------|
| 01 | [SauceDemo](./01-saucedemo) | E-commerce demo (UI only) | 32 | 5 | Complete |
| 02 | [Automation Exercise](./02-automation-exercise) | E-commerce + REST API | 74 (50 UI + 24 API) | 1 High | Complete |

Each project folder contains its own Test Plan, Test Cases, Bug Reports, and supporting evidence.

---

## What You Will Find in Each Project

Every project in this portfolio follows the same professional structure:

- **Test Plan** (Word document) - scope, objectives, approach, environment, schedule, risks, and exit criteria
- **Test Cases** (Excel) - functional test cases with full details: ID, module, scenario, priority, preconditions, steps, test data, expected vs. actual result, status, and execution summary with auto-calculated pass rate
- **Bug Reports** (Excel) - bug tracker, reusable bug report template, and detailed reports for each defect found
- **Screenshots** - visual evidence supporting each bug report
- **README.md** - quick navigation and project summary

The second project (Automation Exercise) additionally includes a **Postman Collection** (JSON) that can be imported directly into Postman to reproduce all API tests.

---

## Skills Demonstrated

| Area | Specifics |
|------|-----------|
| Test Design | Equivalence Partitioning, Boundary Value Analysis, Decision Tables, State Transition Testing, Error Guessing, Exploratory Testing |
| Test Levels | Functional, UI, API, Smoke, Regression, Negative, Stateful CRUD |
| API Testing | Postman (request building, body parameters, environment variables, full collection export) |
| Documentation | Test Plans, Test Cases, Bug Reports, Test Summary Reports |
| Tools | Microsoft Excel, Microsoft Word, Postman, Chrome DevTools, ShareX, Git, GitHub |
| Methodology | Black Box testing, SDLC, STLC, Bug Life Cycle, CRUD lifecycle |
| Soft Skills | Clear written communication, attention to detail, analytical thinking, defect investigation |

---

## Combined Statistics

Aggregated across both completed projects:

| Metric | Value |
|--------|-------|
| Total Test Cases Designed | 106 |
| Test Cases Executed | 106 |
| UI Test Cases | 82 |
| API Test Cases | 24 |
| Combined Pass Rate | ~94% |
| Bugs Reported | 6 |
| High-Severity Bugs | 2 |
| Medium-Severity Bugs | 4 |
| Applications Tested | 2 |
| API Endpoints Validated | 14 |

---

## Highlight: Real Defect Discovered Through API Testing

While testing the Automation Exercise application, I uncovered a significant defect in the `/api/createAccount` endpoint: the server accepts and persists user accounts with email values that do not match a valid email format. This bypasses the UI's HTML5 client-side validation and demonstrates a missing server-side validation that has historical impact on the database.

I confirmed the defect with multiple unique test inputs, then queried `/api/getUserDetailByEmail` to prove the accounts were genuinely created and persisted. I also discovered an existing account in the database (created by a previous tester) that confirmed the issue had been impacting the application over time.

Full details, reproduction steps, and screenshots are in the [Automation Exercise Bug Report](./02-automation-exercise/03_Bug_Reports_AutomationExercise.xlsx).

This kind of finding - reachable only through systematic API testing, not through the UI - is exactly what makes API testing a valuable addition to manual QA.

---

## What Is Next

I am actively expanding this portfolio with:

- A third manual testing project on a different application type (HR systems or government services)
- Deeper API testing including authentication tokens and request chaining
- SQL practice for database validation scenarios common in QA interviews
- **Test automation** - planned stack: Selenium WebDriver with Java + TestNG (industry standard in Cluj outsourcing companies) or Playwright with TypeScript (modern alternative used by product companies)

Each new project will follow the same documentation standard so that my growth is visible and measurable across the portfolio.

---

## How to Navigate This Repository

1. Start with this README for an overview
2. Open any project folder (`01-saucedemo/`, `02-automation-exercise/`) to see the dedicated project README and deliverables
3. Inside each project folder, deliverables are numbered in the order they would be produced in a real QA workflow:
   - `01_Test_Plan_*.docx` - planning phase
   - `02_Test_Cases_*.xlsx` - design and execution phase
   - `03_Bug_Reports_*.xlsx` - reporting phase
   - `04_API_Test_Cases_*.xlsx` - API testing (project 02 only)
   - `05_*_Postman_Collection.json` - importable API collection (project 02 only)
   - `screenshots/` - supporting evidence

---

## Contact

If you are a recruiter or QA Lead reviewing this portfolio, I would be happy to talk.

- **Email:** samarteanadrian245@gmail.com
- **Phone:** +40 740 565 596
- **Location:** Cluj-Napoca, RO (open to on-site, hybrid, or remote)

---

*Last updated: April 2026*
