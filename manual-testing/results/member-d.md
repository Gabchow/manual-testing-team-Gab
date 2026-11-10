# Manual Testing Results — Member D

## Environment

| Item                | Details                              |
| ------------------- | ------------------------------------ |
| Tester identifier   | member-d                             |
| Date and time       | 10 Nov 2026                          |
| Browser and version | Google Chrome 157.0.8103.38 (64-bit) |
| Operating system    | Windows                              |

## Login Tests

### Test ID: LOGIN-N03

| Item      | Details   |
| --------- | --------- |
| Test type | Negative  |
| Tester    | member-d  |
| Website   | SauceDemo |
| Status    | Not run   |

#### Purpose

Check that login is rejected when the username is missing.

#### Preconditions

The SauceDemo login page is open, no user is logged in, and both fields are empty.

#### Test Data

| Field    | Value          |
| -------- | -------------- |
| Username | Empty          |
| Password | `secret_sauce` |

#### Steps

1. Open https://www.saucedemo.com/ and confirm you are logged out.
2. Leave the username field empty.
3. Enter `secret_sauce` in the password field.
4. Select Login.
5. Observe the page and any feedback.

#### Expected Result

The attempt is rejected with validation feedback. The inventory page is not reached.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---

## Equivalence Partitioning

## 2-Point Boundary Tests

## 3-Point Boundary Tests
