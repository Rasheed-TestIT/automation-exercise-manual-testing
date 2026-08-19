# Manual Testing Project — Automation Exercise

A complete manual testing lifecycle project performed against [automationexercise.com](https://automationexercise.com), a live demo e-commerce application. This project walks through all five stages of manual testing: **Discovery, Planning, Specification, Execution and Defect Management, and Test Report**, closing out with a Test Summary Report.

## Why this project

Most QA portfolios show a pile of test cases with no context. This one shows the full thought process — from first exploring an unfamiliar application, to defining scope and risk, to writing test cases, executing them for real, and triaging the results into a defect log with severity and priority. It also documents one deliberate mid-project pivot: an earlier version of this project targeted a live UK retail site, which turned out to be geo-restricted from my location — that constraint, and how I scoped around it, is preserved as a case study in judgment rather than hidden.

## Results at a glance

| Metric              | Result                                                                        |
| ------------------- | ----------------------------------------------------------------------------- |
| Test cases executed | 37                                                                            |
| Test steps executed | 115                                                                           |
| Pass rate           | 88.7%                                                                         |
| Defects logged      | 8 (1 Critical, 2 High, 3 Medium, 1 Low, 1 correctly rejected as not-a-defect) |

## Project structure

| Stage                  | File                                                               | Description                                                                |
| ---------------------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| 1. Test Discovery      | [`aex-01-test-discovery.md`](./aex-01-test-discovery.md)           | Exploratory notes on the application before formal test design             |
| 2. Test Planning       | [`aex-02-test-plan.md`](./aex-02-test-plan.md)                     | Scope, objectives, environment, entry/exit criteria, risks                 |
| 3. Test Specification  | [`aex-03-test-cases.xlsx`](./aex-03-test-cases.xlsx)               | 37 written test cases across registration, login, cart, checkout, and more |
| 4. Test Execution      | [`aex-04-test-execution.xlsx`](./aex-04-test-execution.xlsx)       | Step-by-step execution log with actual results and Pass/Fail status        |
| 5. Defect Management   | [`aex-05-defect-log.xlsx`](./aex-05-defect-log.xlsx)               | 8 defects with severity, priority, and reproduction steps                  |
| 6. Test Summary Report | [`aex-06-test-summary-report.md`](./aex-06-test-summary-report.md) | Final results, key findings, and recommendations                           |

## Tools & environment

- **Type:** Manual, black-box functional testing
- **Browsers:** Microsoft Edge (primary), Google Chrome (secondary), Firefox (compatibility check)
- **Mobile:** Safari on iPhone 12 Pro
- **Documentation:** Markdown for narrative stages, Excel for structured test data

## Key defects found

- Cart displays no subtotal/total (**Critical**)
- Cart item quantity cannot be updated (**High**)
- Session not fully invalidated after logout — browser back button exposes account content (**High**)
- Registration email field accepts addresses missing a top-level domain (**Medium**)
- No minimum password length enforced (**Medium**)
- Brand filter returns unrelated products (**Medium**)

Full details and reproduction steps for each are in the [Defect Log](./aex-05-defect-log.xlsx).

## About me

Rasheed Ayokanmi — Certified Software Tester. [LinkedIn](www.linkedin.com/in/rasheed-ayokanmi-39651ba6) · [Email](ayokanmirasheed@gmail.com)
