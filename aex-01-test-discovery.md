# Test Discovery — Automation Exercise (Web)

**Project:** Automation Exercise
**Application URL:** https://automationexercise.com
**Tester:** Rasheed Ayokanmi
**Test Type:** Manual, Black-box exploratory testing
**Platform:** Web (Desktop & Mobile)

---

## 1. Purpose

Before writing formal test cases, the site was explored end-to-end to understand its structure, core user journeys, and areas that carry higher risk of defects. This discovery phase forms the foundation for the Test Plan and Test Specification stages that follow.

## 2. Approach

Exploration was carried out by navigating the site as a typical customer would — registering a new account, browsing categories and brands, adding items to the cart, applying the newsletter subscription, using the contact form, and stepping through checkout to order completion — while noting every feature, rule, and edge case encountered along the way.

## 3. Environment

| Item                                     | Detail                              |
| ---------------------------------------- | ----------------------------------- |
| Primary browser                          | Safari                              |
| Secondary browsers (compatibility check) | Google Chrome, Firefox              |
| Devices                                  | Desktop, iPhone 12 Pro Max (mobile) |
| Account type                             | Newly registered test account       |

## 4. Key Features Identified

- User registration (Signup / Login page)
- Login with registered credentials
- Product browsing by category: Women (Dress, Tops, Saree), Men (Tshirts, Jeans), Kids (Dress, Tops & Shirts)
- Product browsing/filtering by brand (Polo, H&M, Madame, Mast & Harbour, Babyhug, Allen Solly Junior, Kookie Kids, Biba)
- Product detail pages
- Shopping cart — add to cart, view cart, update quantity, remove item, subtotal calculation
- "Recommended items" section
- Checkout flow, including delivery and billing address entry
- Payment step and order placement
- Order confirmation
- Contact Us form (with file attachment)
- Newsletter subscription (footer)
- Account/profile management
- Logout
- Published Test Cases and API list pages (site's own reference material — useful context, not to be copied into this project's own test design)

## 5. Observations & Areas of Interest

- **Registration form:** collects a wide set of fields (name, email, password, address, country, state, city, mobile number) — a strong candidate for field-level validation testing.
- **Category and brand filtering:** two independent ways to narrow products — worth verifying both work correctly and consistently together.
- **Cart behavior:** quantity updates and removal are testable in detail since the cart is fully functional without restriction.
- **Checkout flow:** includes delivery and billing address, which can be tested as same-address vs different-address scenarios.
- **Payment step:** the site accepts dummy card details (no live payment gateway), so the full order-placement journey can be tested end-to-end without any real-world risk.
- **Contact Us form:** supports file upload — worth checking file type/size handling.
- **Newsletter subscription:** simple email field in the footer — good candidate for basic validation testing.

## 6. Risks & Constraints Noted

- This is a **demo/practice application** built specifically for automation and manual testing practice, not a live commercial business — findings here demonstrate testing skill and process rather than real business impact, and should be framed as such in the portfolio.
- As a widely used public practice site, test data (e.g. registered emails) should be kept unique to avoid conflicts with other testers using the same site concurrently.
- The site publishes its own suggested test scenarios; this project's test cases are independently designed based on exploration rather than copied from that reference, so the resulting documentation reflects the tester's own judgment.

## 7. Next Step

Proceed to **Test Planning**, where scope, objectives, and entry/exit criteria are formally defined based on the features identified here — covering the full account lifecycle from registration through order completion.
