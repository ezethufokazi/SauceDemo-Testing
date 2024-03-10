# SauceDemo Manual Testing

## Project Overview
This QA project contains test cases, test execution results, and bug reports for the SauceDemo web application (https://www.saucedemo.com/). The tests validate functionality, UI elements, and error handling across the login, products, product details, cart, checkout, and checkout complete pages for various user types.

---

## Tools Used
- **Test Management:** Microsoft Excel
- **Bug Tracking:** Excel Bug Report
- **Browser:** Chrome (latest version)
- **OS:** Windows 11
- **Screenshot Tool:** Snipping Tool

---

## Test Environment
- **OS:** Windows 11
- **Browser:** Chrome (latest version)
- **URL:** https://www.saucedemo.com/
- **User Accounts:** standard_user, locked_out_user, problem_user, performance_glitch_user, error_user, visual_user
- **Password:** secret_sauce (all accounts)

---

## Test Scope
- **Login Page:** Valid/invalid credentials, locked users, field validations, password masking, leading/trailing spaces, case sensitivity, multiple failed attempts
- **Products Page:** Product display, sorting, add/remove to cart, hamburger menu options, UI for problem/visual/error users, product details validation
- **Product Details Page:** Navigation from Products page, product details display, add/remove buttons, Back to Products navigation
- **Cart Page:** Navigation, product display, remove functionality, continue shopping, checkout button, empty cart behaviour, cart persistence on refresh
- **Checkout - Your Information:** Required field validations, invalid input handling, navigation to overview page, cancel button
- **Checkout - Overview:** Review order details, Finish button functionality
- **Checkout Complete:** Success message display, Back Home button functionality

---

## Test Summary

| Total Test Cases | Passed | Failed | Blocked | Pass Rate |
|---|---|---|---|---|
| 68 | 64 | 4 | 0 | 94.1% |

---

## Per Module Summary

| Module | Total | Passed | Failed | Blocked |
|---|---|---|---|---|
| Login | 14 | 13 | 1 | 0 |
| Products Page | 23 | 21 | 2 | 0 |
| Product Details Page | 6 | 6 | 0 | 0 |
| Cart Page | 9 | 9 | 0 | 0 |
| Checkout Information Page | 7 | 6 | 1 | 0 |
| Checkout Overview Page | 7 | 7 | 0 | 0 |
| Checkout Complete Page | 2 | 2 | 0 | 0 |
| **TOTAL** | **68** | **64** | **4** | **0** |

---

## Bug Report Summary

| Bug ID | Description | Severity | Priority |
|---|---|---|---|
| SD_BUG_001 | Leading and trailing spaces in username are not trimmed and user is not logged in | Medium | P0 (High) |
| SD_BUG_002 | Product name does not follow standard naming format on Products page | Minor | P2 (Low) |
| SD_BUG_003 | Product description for Sauce Labs Backpack contains incorrect syntax | Medium | P1 (Medium) |
| SD_BUG_004 | Invalid input on Checkout: Your Information page is accepted and no error message is displayed | High | P0 (High) |

---

## Test Case Structure
Each test case includes:
- TC ID
- Test Scenario
- Pre-requisites
- Test Steps
- Test Data
- Expected Result

---

## Bug Report Structure
Each bug report includes:
- Bug ID
- Title/Description
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Priority
- Screenshot

Failed test cases link to their corresponding bug report via Bug ID.

---

## How to Execute Tests
1. Open https://www.saucedemo.com/ in a supported browser
2. Follow the preconditions listed in each test case
3. Execute the steps and compare actual results to expected results
4. Log any discrepancies as bugs

---

## Repository Structure
```
SauceDemo-Testing
├── README.md
└── SauceDemo/
    ├── SauceDemo_TestCases.xlsx
    ├── SauceDemo_TestExecutionResults.xlsx
    ├── SauceDemo_BugReport.xlsx
    └── Screenshots/
        ├── SD_BUG_001_Leading_Trailing_Spaces_Username.png
        ├── SD_BUG_002_Product_Naming_Format.png
        ├── SD_BUG_003_Backpack_Description_Syntax.png
        ├── SD_BUG_004_Invalid_Input.png
        └── SD_BUG_004_Checkout_Overview.png
```

---

## Notes
- All tests were executed using the standard_user account unless stated otherwise
- Certain user accounts have known issues — problem_user has incorrect product images, error_user has cart issues
- Leading and trailing spaces in the password field are treated as part of the password input which is correct behaviour for a password field
- No account lockout mechanism is implemented after multiple failed login attempts. This may be a security concern but was not classified as a bug due to lack of documented requirements
- A consistent browser should be used for repeatable results
