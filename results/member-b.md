# Manual Testing Results — Member B

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-b |
| Date and time | 10 Nov 11.18am |
| Browser and version | Chrome 156 |
| Operating system | Windows 11 |

## Login Tests

### Test ID: LOGIN-N01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-b |
| Website | https://www.saucedemo.com/ |
| Status | Pass |

#### Purpose

This test checks the displayed output/result upon entering a failed password.

#### Preconditions

The user must be logged out of any account.

#### Test Data

| Field | Value |
|---|---|
| Username | standard_user |
| Password | wrong_password |

#### Steps

1. Follow the shared starting procedure.
2. Enter the valid username.
3. Enter the incorrect password.
4. Select Login.
5. Observe the page and feedback.

#### Expected Result

User should not be allowed to login, an error message should appear telling the user the error

#### Actual Result

User is not logged in
Error message displayed: "Epic sadface: Username and password do not match any user in this service".

#### Evidence

[View screenshot](../evidence/member-b/login-n01.png)

---

## Equivalence Partitioning

## 2-Point Boundary Tests

## 3-Point Boundary Tests