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

### Test ID: AGE-EP-10-B

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | Your member identifier |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Pass |

#### Purpose

This test checks the displayed output when an input age is not within the validation requirements range.

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Last name | TestingStudent |
| Age | 10 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |


#### Steps

1. Restore the form.
2. Enter the valid baseline.
3. Change only age to 10.
4. Write the expected result.
5. Submit.
6. Observe acceptance or rejection.
7. Where displayed, verify the submitted age.
8. Record the actual result and status in a separate test-case block.

#### Expected Result

Validation error should be returned for tested age, or successful submission should be prevented.

#### Actual Result

Successful submission is prevented.
Error message pops up under age box: "Value must be greater than or equal to 18."

#### Evidence

[View screenshot](../evidence/member-b/AGE-EP-10-B.png)

---



## 2-Point Boundary Tests

### Test ID: AGE-2P-18-B

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Pass |

#### Purpose

Check that an age at the boundary (exact minimum) is accepted.

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Last name | TestingStudent |
| Age | 18 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the form.
2. Enter the valid baseline.
3. Change only age to 18.
4. Write the expected result.
5. Submit.
6. Observe acceptance or rejection.
7. Where displayed, verify the submitted age.
8. Record the actual result and status in a separate test-case block.

#### Expected Result

Submission should be successful, with no validation error found.

#### Actual Result

Submission is successful.
Message is displayed: "Your Input passed validation".

#### Evidence
[View screenshot](../evidence/member-b/AGE-2P-18-B.png)

---




## 3-Point Boundary Tests

### Test ID: AGE-3P-19-B

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-b |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Pass |

#### Purpose

This test checks if the age above the boundary value is accepted or rejected.

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Last name | TestingStudent |
| Age | 19 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the form.
2. Enter the valid baseline.
3. Change only age to 19.
4. Write the expected result.
5. Submit.
6. Observe acceptance or rejection.
7. Where displayed, verify the submitted age.
8. Record the actual result and status in a separate test-case block.

#### Expected Result

Submission should be successful, with no validation error found.

#### Actual Result

Submission is successful.
Message is displayed: "Your Input passed validation".

#### Evidence

[View screenshot](../evidence/member-b/AGE-3P-19-B.png)

---