# Test Summary Report — Automation Exercise (Web)

**Project:** Automation Exercise
**Application URL:** https://automationexercise.com
**Prepared by:** Rasheed Ayokanmi
**Test Type:** Manual, Black-box functional testing
**Test Period:** Discovery through Execution, single test cycle

---

## 1. Purpose

This report summarizes the results of manual testing carried out on Automation Exercise, covering the full user journey from registration through order placement. It closes out the five-stage manual testing lifecycle: Test Discovery, Test Planning, Test Specification, Test Execution, and Defect Management.

## 2. Scope Covered

Testing covered registration, login/logout, category and brand browsing, product detail pages, cart management, checkout (address entry and dummy payment), order confirmation, account details, Contact Us (including file upload), newsletter subscription, session/URL protection, and cross-browser, mobile, and basic performance checks. Full scope and exclusions are documented in the Test Plan (`aex-02-test-plan.md`).

## 3. Test Execution Summary

| Metric | Result |
|---|---|
| Total test cases executed | 37 |
| Total test steps executed | 115 |
| Steps passed | 102 |
| Steps failed | 13 |
| **Overall step pass rate** | **88.7%** |
| Test cases with zero defects | 29 / 37 (78%) |
| Test cases with at least one defect | 8 / 37 (22%) |

## 4. Defect Summary

| Severity | Count | Defect IDs |
|---|---|---|
| Critical | 1 | DEF-006 |
| High | 1 | DEF-005 |
| Medium | 3 | DEF-001, DEF-002, DEF-004 |
| Low | 1 | DEF-007 |
| Could not reproduce consistently | 1 | DEF-003 |
| Rejected (not a defect) | 1 | DEF-008 |
| **Total logged** | **8** | |

**Update:** DEF-003 (session not invalidated on logout) was originally logged as High severity based on a single manual observation. On subsequent re-testing — both an automated Cypress check and a manual re-test — the back button correctly returned to the login page with no logged-in content shown. It could not be reproduced consistently and has been reclassified accordingly; see the Defect Log for full detail. This is left in the log rather than removed, since an unreproducible finding is still worth a record, even if it isn't currently actionable.

Full details, reproduction steps, and rationale for each are in the Defect Log (`aex-05-defect-log.xlsx`).

## 5. Key Findings

- **Cart functionality is the weakest area tested.** Two of the three most severe defects (DEF-005, DEF-006) live in the cart: quantities cannot be updated, and no subtotal or total is ever displayed. For an e-commerce flow, this is a significant gap — a shopper has no way to see what they're about to pay before reaching checkout.
- **A suspected session-handling issue did not hold up on re-test.** DEF-003 initially suggested the browser back button showed account content after logout. Re-testing — both an automated Cypress check and a manual pass — showed the back button correctly returning to the login page each time. Rather than discard the original observation, it's recorded as "could not reproduce consistently" so the finding remains visible without being treated as a confirmed defect.
- **Input validation is inconsistent.** Registration accepts malformed emails missing a domain suffix (DEF-001) and passwords with no minimum length (DEF-002) — both are low-effort fixes with real impact on data quality and account security.
- **Brand filtering does not correctly scope results** (DEF-004), which would erode user trust in the site's search/filter features if left unresolved.
- **One expected "failure" was not actually a defect** (DEF-008) — the site enforces required address fields earlier in the flow (at registration) than the test script anticipated (at checkout). This distinction — between a test not matching reality and the system genuinely misbehaving — was confirmed by re-reading the actual site behavior before logging it, rather than logging it as a straightforward fail.
- **Core account and checkout flows work correctly.** Registration, login, logout (aside from the back-button issue), category/brand navigation to product level, checkout with address and dummy payment, order confirmation, Contact Us (including file upload), and newsletter subscription all passed without issue.

## 6. Test Environment

| Item | Detail |
|---|---|
| Application | https://automationexercise.com (demo/practice application) |
| Primary browser | Microsoft Edge |
| Secondary browser | Google Chrome |
| Cross-browser check | Microsoft Edge, Google Chrome, Firefox |
| Mobile | Safari on iPhone 12 Pro |

## 7. Recommendation

Based on the defects found, the two cart issues (DEF-005, DEF-006) should be treated as release blockers if this were a live application — a shopping cart that doesn't show a total is not fit for purpose. The remaining Medium and Low severity issues can be scheduled into a normal backlog. DEF-003 does not currently warrant action given it could not be reproduced on re-test, but is worth a quick re-check in a future test cycle in case it resurfaces under different conditions (e.g. slower network, different browser).

## 8. Conclusion

This project exercised the complete manual testing lifecycle — from unstructured exploration through to a defect log with triaged severity, a rejected non-defect, and one finding walked back after it failed to reproduce — against a live, publicly accessible application. 88.7% of executed steps passed, with genuine, reproducible defects found across cart and input validation areas. The DEF-003 re-test, prompted by a companion Cypress automation project, is a reminder that a single manual observation is a starting point, not a verdict — worth confirming before treating any finding as settled. The full project, including test discovery notes, plan, 37 test cases, execution results, and defect log, is available in the accompanying files.
