# Manual Testing Results — Member A

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-a |
| Date and time | |
| Browser and version | |
| Operating system | |

## Login Tests

### Test ID: LOGIN-P01

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | Member-a |
| Website | https://www.saucedemo.com/inventory.html |
| Status | Pass |

#### Purpose

What does this test check?
It checks if the correct login credentials work and brings the user to the correct intended page

#### Preconditions

The Login page is loaded, the username and password is the correct intended values.

#### Test Data

| Field | Value |
|Username|Password|
| standard_user | secret_sauce |

#### Steps
Follow the shared starting procedure.
Enter the username.
Enter the password.
Select Login.
Observe the page reached.
Check that products are visible.

#### Expected Result

Write this before executing the test.
The inventory page appears and products are visible.

#### Actual Result

Brought to the intended inventory page. Able to see the products. Passed the test.

#### Evidence

[View screenshot](../evidence/member-a/login-p01.png)

---

## Equivalence Partitioning

### Test ID: AGE-EP-30-A

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Accept |

#### Purpose

What does this test check?

Age validation if the correct age used responds with the correct output, the form submitting
successfully with the intended age.

#### Preconditions

What must be true before the test starts?
The page loads, and the input can be entered.

#### Test Data

| Field | Value |
|---|---|
First name | Alexander
Surname	| TestingStudent
Age	| 30
Country	| Singapore
Notes | Manual testing classroom exercise

#### Steps

1.Restore the form.
2.Enter the valid baseline.
3.Change only age.
4.Write the expected result.
5.Submit.
6.Observe acceptance or rejection.
7.Where displayed, verify the submitted age.
8.Record the actual result and status in a separate test-case block.

#### Expected Result

the form successfully submits with the intended age

#### Actual Result

The form was successfully submitted with the age 30.

#### Evidence

[View screenshot](../evidence/member-a/AGE-EP-30-A.png)

---

## 2-Point Boundary Tests

### Test ID: YOUR-TEST-ID

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Reject |

#### Purpose

Checking that the age limit immediately below the minimum is rejected.

#### Preconditions

The validation form is open, all other fields used are the values agreed as the baseline.

#### Test Data

| Field | Value |
|---|---|
| Age | `17` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `17`.
4. Submit.
5. Observe the response.

#### Expected Result

Age 17 is rejected because it is below the minimum age requirements of 18.

#### Actual Result

Age 17 is rejected, unable to submit the form, a message shown, rejecting the age.

#### Evidence

[View screenshot](../evidence/member-a/AGE-2P-17-A.png)

---

## 3-Point Boundary Tests

### Test ID: YOUR-TEST-ID

| Item | Details |
|---|---|
| Test type | Positive / Negative / Recovery |
| Tester | Your member identifier |
| Website | Website name |
| Status | Not run |

#### Purpose

What does this test check?

#### Preconditions

What must be true before the test starts?

#### Test Data

| Field | Value |
|---|---|
| Input name | Input value |

#### Steps

1.
2.
3.

#### Expected Result

Write this before executing the test.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.

---