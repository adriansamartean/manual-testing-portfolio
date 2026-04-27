# SauceDemo - Manual QA Portfolio Project

[![Manual Testing](https://img.shields.io/badge/Testing-Manual-blue)]()
[![Black Box](https://img.shields.io/badge/Approach-Black%20Box-orange)]()
[![Test Cases](https://img.shields.io/badge/Test%20Cases-32-informational)]()
[![Bugs Found](https://img.shields.io/badge/Bugs%20Found-5-red)]()
[![Pass Rate](https://img.shields.io/badge/Pass%20Rate-84.4%25-brightgreen)]()

End-to-end manual testing project for the [SauceDemo](https://www.saucedemo.com) e-commerce demo application.
This project demonstrates my workflow as a Manual QA Engineer: planning, designing test cases, executing them, reporting bugs, and summarizing results.

> **Author:** Adrian-Stefan Samartean
> **Role applied for:** QA Engineer (Manual Testing) - Entry Level
> **Location:** Cluj-Napoca, Romania
> **Email:** samarteanadrian245@gmail.com
> **Certification:** QA Manual Testing (2023-2024)

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Application Under Test](#application-under-test)
3. [Deliverables](#deliverables)
4. [Test Approach](#test-approach)
5. [Test Coverage](#test-coverage)
6. [Execution Results](#execution-results)
7. [Bugs Found](#bugs-found)
8. [Tools Used](#tools-used)
9. [What I Learned](#what-i-learned)
10. [Next Steps](#next-steps)

---

## Project Overview

This project shows how I approach manual testing of a real web application from scratch, following industry-standard QA practices:

- Defining scope, objectives, and risks in a Test Plan
- Designing functional and exploratory test cases using black-box techniques
- Executing tests and tracking results with auto-calculated metrics
- Logging bugs with reproducible steps, evidence, and severity classification
- Producing a Test Summary Report for stakeholders

The goal is to demonstrate not just that I can run tests, but that I can think like a QA professional: anticipating risks, documenting clearly, and communicating findings to developers and managers.

---

## Application Under Test

**SauceDemo** - a publicly available demo e-commerce site provided by Sauce Labs.

- **URL:** https://www.saucedemo.com
- **Available test users:** `standard_user`, `locked_out_user`, `problem_user`, `performance_glitch_user`, `error_user`, `visual_user`
- **Password (all users):** `secret_sauce`
- **Why this app:** SauceDemo is intentionally seeded with bugs and inconsistencies, making it ideal to demonstrate defect-detection skills.

### Main features tested

- User authentication (login, logout, locked accounts, error states)
- Product catalog (display, sorting, product details)
- Shopping cart (add, remove, persistence across sessions)
- Checkout flow (form validation, totals calculation, confirmation)
- Side navigation menu (Reset App State, Logout, About)
- UI consistency across user types

---

## Deliverables

| # | Document | Format | Description |
|---|----------|--------|-------------|
| 1 | [Test Plan](./01_Test_Plan_SauceDemo.docx) | DOCX | Scope, objectives, approach, environment, schedule, risks, exit criteria |
| 2 | [Test Cases](./02_Test_Cases_SauceDemo.xlsx) | XLSX | 32 functional test cases with full execution results and pass-rate summary |
| 3 | [Bug Reports](./03_Bug_Reports_SauceDemo.xlsx) | XLSX | Bug tracker, reusable template, and 5 fully documented bug reports |
| 4 | [Screenshots](./screenshots) | PNG | Visual evidence supporting each bug report |

---

## Test Approach

I followed a Black Box approach combining several established techniques:

| Technique | Where applied |
|-----------|---------------|
| Equivalence Partitioning | Login credentials, checkout form fields |
| Boundary Value Analysis | Postal code length, name field limits |
| Decision Table Testing | Checkout form valid/invalid combinations |
| Error Guessing | Cart edge cases, "Reset App State" behavior |
| Exploratory Testing | UI inspection with `visual_user` and `problem_user` |

### Test levels covered

- **Smoke Testing** - quick validation of critical paths (login, add to cart, checkout)
- **Functional Testing** - verification of each feature against expected behavior
- **UI Testing** - layout, alignment, button states, badge counter
- **Regression Testing** - re-execution of priority cases after each session

---

## Test Coverage

**32 test cases** distributed across 6 modules:

| Module | Test Cases | Priority Mix |
|--------|------------|--------------|
| Login | 8 | High: 4, Medium: 3, Low: 1 |
| Inventory / Products | 6 | High: 2, Medium: 4 |
| Cart | 7 | High: 4, Medium: 2, Low: 1 |
| Checkout | 8 | High: 5, Medium: 1, Low: 2 |
| Side Menu | 3 | High: 1, Medium: 1, Low: 1 |
| UI / Visual | 2 | Medium: 1, Low: 1 |

Each test case includes: ID, module, scenario, title, priority, preconditions, detailed steps, test data, expected result, actual result, status, tester, execution date, linked bug ID, and notes.

---

## Execution Results

| Metric | Count | Percentage |
|--------|-------|------------|
| Total Test Cases | 32 | 100% |
| Passed | 27 | 84.4% |
| Failed | 5 | 15.6% |
| Blocked | 0 | 0% |
| Not Run | 0 | 0% |

All 5 failed test cases are linked to documented defects (BUG_001 through BUG_005). Critical user flows (login, add to cart, checkout) function correctly for `standard_user`. Defects are concentrated in special user types and the "Reset App State" flow.

---

## Bugs Found

Five defects documented during execution:

| Bug ID | Title | Module | Severity | Priority | Linked TC |
|--------|-------|--------|----------|----------|-----------|
| BUG_001 | Cart badge cleared but Add to cart buttons not reset after "Reset App State" | Side Menu | Medium | P2 | TC_MENU_03 |
| BUG_002 | All product images are identical (dog photo) when logged in as problem_user | Inventory | High | P1 | TC_LOGIN_06 |
| BUG_003 | Login latency >5 seconds with performance_glitch_user | Login | Medium | P2 | TC_LOGIN_07 |
| BUG_004 | Checkout flow allows submission with empty cart | Checkout | Medium | P2 | TC_CHK_01 |
| BUG_005 | Multiple visual defects on inventory page when logged in as visual_user | UI | Medium | P3 | TC_UI_01 |

### Severity breakdown

- Critical: 0
- High: 1
- Medium: 4
- Low: 0

Each bug report includes environment details, user account, preconditions, numbered steps to reproduce, expected vs. actual result, reproducibility rate, screenshots, and additional analysis. See [03_Bug_Reports_SauceDemo.xlsx](./03_Bug_Reports_SauceDemo.xlsx) for full reports.

---

## Tools Used

| Category | Tool |
|----------|------|
| Test Case Management | Microsoft Excel (with planned migration to TestRail free tier) |
| Bug Tracking | Excel tracker (template included), with planned move to Jira / GitHub Issues |
| Documentation | Microsoft Word, Markdown |
| Browsers | Google Chrome (primary), Firefox, Edge |
| Screenshots / Video | ShareX, Windows Snipping Tool |
| Inspection | Chrome DevTools (Network, Elements, Console) |
| Version Control | Git, GitHub |

---

## What I Learned

Working on this project, I practiced:

- Writing a Test Plan that a stakeholder can read and approve
- Translating functional requirements into reproducible test cases
- Distinguishing severity (impact on the product) from priority (urgency to fix)
- Reporting bugs in a way that makes them actionable for developers - clear repro steps, evidence, environment
- Recognizing patterns: how `problem_user` and `performance_glitch_user` mirror real-world defects (broken assets, slow API responses)
- Using DevTools to validate observations (network timing, element inspection)
- Producing summary reports with auto-calculated metrics for stakeholder review

---

## Next Steps

After completing this manual phase, I plan to extend my portfolio with:

- A second manual testing project on a more complex application (Automation Exercise or OrangeHRM)
- API testing using Postman against the public APIs of Automation Exercise
- SQL practice for database validation scenarios common in QA interviews
- Automation testing using either Selenium WebDriver with Java + TestNG (industry standard in Cluj outsourcing companies) or Playwright with TypeScript (modern alternative used by product companies)

The same scenarios from this project (login, add to cart, checkout) will eventually be automated, with reports generated via Allure or built-in reporters, demonstrating end-to-end coverage from manual exploration to automated regression.

---

## Contact

If you are a recruiter or QA Lead reviewing this project, I would be happy to talk.

- **Email:** samarteanadrian245@gmail.com
- **Phone:** +40 740 565 596
- **Location:** Cluj-Napoca, RO (open to on-site, hybrid, or remote)

---

*Last updated: April 2026*
