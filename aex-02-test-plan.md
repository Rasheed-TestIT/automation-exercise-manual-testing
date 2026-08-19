# Test Plan — Automation Exercise (Web)

**Project:** Automation Exercise
**Application URL:** https://automationexercise.com
**Prepared by:** Rasheed Ayokanmi
**Test Type:** Manual, Black-box functional testing
**Status:** Approved for execution

---

## 1. Introduction

This document defines the scope, approach, resources, and schedule for manual testing of the Automation Exercise website. It builds on the findings from the Test Discovery stage, where core features and areas of risk were identified.

## 2. Objectives

- Verify that the full user journey (registration, login, browsing, cart, checkout, payment, order confirmation) functions correctly end-to-end.
- Verify key business rules (cart calculations, category/brand filtering, form validation) behave as expected.
- Verify the site is usable and consistent across major browsers and on mobile.
- Verify basic account and session behavior (login validation, logout) are met.
- Identify, log, and report any defects found during execution.

## 3. Scope

### In Scope
- User registration (valid and invalid input handling)
- Login — valid credentials, invalid credentials
- Logout
- Product browsing by category (Women, Men, Kids) and sub-category
- Product browsing/filtering by brand
- Product detail pages
- Shopping cart (add, remove, update quantity, subtotal calculation)
- Checkout flow, including delivery and billing address entry
- Payment step and order placement (dummy card details, no live gateway)
- Order confirmation
- Contact Us form, including file attachment
- Newsletter subscription
- Account/profile management
- Cross-browser rendering (Safari, Chrome, Firefox)
- Mobile responsiveness (iPhone 12 Pro)
- Basic performance (page load time, responsiveness under normal use)

### Out of Scope
- Backend/API-level testing (the site does expose a public API, but this project is scoped to UI/manual testing)
- Automated regression testing (covered separately in an automation-focused project)
- Load/stress testing beyond normal manual browsing
- Real payment gateway testing (the application accepts dummy card details with no live payment processor)

## 4. Test Approach

Testing will be performed manually, following pre-written test cases derived from the Test Discovery stage. Each test case will be executed step-by-step, with actual results recorded and compared against expected results. Failures will be logged as defects with enough detail to reproduce and prioritize them.

Techniques used:
- **Functional testing** — verifying each feature behaves as expected
- **Boundary Value Analysis** — e.g. cart quantity limits, password length rules
- **Equivalence Partitioning** — e.g. valid vs invalid registration input, valid vs invalid login credentials
- **Cross-browser / cross-device testing** — manual checks across Safari, Chrome, Firefox, and mobile

## 5. Test Environment

| Item | Detail |
|---|---|
| Application | https://automationexercise.com (demo/practice application) |
| Browsers | Microsoft Edge (primary), Google Chrome (secondary) |
| Devices | Desktop, iPhone 12 Pro |
| Test data | Newly registered test account, unique email per test run where relevant |
| Network | Standard broadband/mobile connection |

## 6. Entry Criteria

- Test Discovery is complete and key features identified.
- Test cases are written and reviewed for the in-scope features.
- The site is accessible and stable enough to begin testing.

## 7. Exit Criteria

- All planned test cases have been executed.
- All identified defects have been logged with severity and priority.
- No outstanding **critical** or **high-severity** defects remain undocumented.
- A Test Summary Report has been produced.

## 8. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| Rasheed Ayokanmi | Test planning, test case design, execution, defect logging, reporting |

## 9. Risks & Assumptions

- **Assumption:** the application is a demo/practice site intentionally built for testing practice, not a live commercial business — this project demonstrates testing process and skill rather than real business risk mitigation.
- **Risk:** as a widely used public demo site, test data may occasionally clash with other testers' activity (e.g. duplicate emails, shared product data). **Mitigation:** unique, timestamped test data will be used where uniqueness matters (e.g. registration email).
- **Risk:** the site publishes its own suggested test scenarios, which could unintentionally bias test design. **Mitigation:** test cases in this project are derived independently from the Test Discovery stage, not copied from the site's published list.

## 10. Deliverables

1. Test Discovery notes
2. Test Plan (this document)
3. Test Case specification (Excel)
4. Test Execution log with results (Excel)
5. Defect log (Excel)
6. Test Summary Report

## 11. Next Step

Proceed to **Test Specification**, where the full set of test cases is written and organized against this plan's scope.
