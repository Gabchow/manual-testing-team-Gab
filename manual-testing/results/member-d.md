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
| Status    | Pass   |

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

After leaving the username empty, entering `secret_sauce` as the password and selecting Login, the page stayed on the login screen. The error message "Epic sadface: Username is required" appeared. The inventory page was not reached. This matches the expected result.

#### Evidence

Not captured.

---

## Equivalence Partitioning

### Test ID: AGE-FMT-BLANK-D

| Item | Details |
|---|---|
| Test type | Negative (input-format observation) |
| Tester | member-d |
| Website | Test Pages validation form |
| Technique | Equivalence partitioning (input format) |
| Status | Observation only |

#### Purpose

Observe how the form handles a blank age.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field | Value |
|---|---|
| Age | Empty |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Clear the age field so it is empty.
4. Submit.
5. Observe the response and any feedback.

#### Expected Result

A blank age is not a valid whole number from 18 to 80, so I expect submission to be prevented or a validation message to appear. The requirement does not clearly define blank-age behaviour, so I am recording this as an observation.

#### Actual Result

With the baseline entered (first name `Alexander`) and the age field left empty, I selected Submit. The form was not submitted. A browser pop-up appeared beside the age field saying "Please fill out this field." The pop-up looks like Chrome's built-in validation, so the attempt appears to have been stopped in the browser rather than by the server. The published requirement does not say what should happen with a blank age, so I am recording this as an observation. It is consistent with my expectation that submission would be prevented.

#### Evidence

Not captured.

---

### Test ID: AGE-FMT-ABC-D

| Item | Details |
|---|---|
| Test type | Negative (input-format observation) |
| Tester | member-d |
| Website | Test Pages validation form |
| Technique | Equivalence partitioning (input format) |
| Status | Observation Only |

#### Purpose

Observe how the form handles non-numeric age input.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field | Value |
|---|---|
| Age | `abc` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Try to replace age with `abc`.
4. Note whether the characters can be typed at all.
5. Submit if possible.
6. Observe the response and any feedback.

#### Expected Result

Non-numeric text is not a valid age, so I expect it to be prevented, cleared or rejected. The requirement does not define exactly which, so I am recording this as an observation.

#### Actual Result

With the baseline entered, I clicked in the age field and tried to type `abc`. The letters could not be entered and the field stayed empty. Because the input was blocked in the browser, nothing was submitted, so I cannot say how the server handles non-numeric age. The published requirement does not define behaviour for non-numeric input, so I am recording this as an observation. It is consistent with my expectation that `abc` would be prevented.

#### Evidence

Not captured.

---

## 2-Point Boundary Tests

## 3-Point Boundary Tests
