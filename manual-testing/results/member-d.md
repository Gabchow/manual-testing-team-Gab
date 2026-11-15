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
| Status    | Pass      |

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

Screenshot to be added.

---

## Equivalence Partitioning

### Baseline Note

The suggested first name `Alex` was rejected with the message "[paste exact message]". The published requirement says only that first name must be filled and fewer than 90 characters, so this is recorded as a requirement question rather than a confirmed defect. The team agreed to use `Alexander` as the first name in the baseline instead.

### Test ID: AGE-FMT-BLANK-D

| Item      | Details                                 |
| --------- | --------------------------------------- |
| Test type | Negative (input-format observation)     |
| Tester    | member-d                                |
| Website   | Test Pages validation form              |
| Technique | Equivalence partitioning (input format) |
| Status    | Observation only                        |

#### Purpose

Observe how the form handles a blank age.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field        | Value                 |
| ------------ | --------------------- |
| Age          | Empty                 |
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

Screenshot to be added.

---

### Test ID: AGE-FMT-ABC-D

| Item      | Details                                 |
| --------- | --------------------------------------- |
| Test type | Negative (input-format observation)     |
| Tester    | member-d                                |
| Website   | Test Pages validation form              |
| Technique | Equivalence partitioning (input format) |
| Status    | Observation only                        |

#### Purpose

Observe how the form handles non-numeric age input.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field        | Value                 |
| ------------ | --------------------- |
| Age          | `abc`                 |
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

Screenshot to be added.

---

## 2-Point Boundary Tests

### Test ID: AGE-2P-81-D

| Item      | Details                    |
| --------- | -------------------------- |
| Test type | Negative                   |
| Tester    | member-d                   |
| Website   | Test Pages validation form |
| Technique | 2-point boundary testing   |
| Status    | Pass                       |

#### Purpose

Check that an age immediately above the maximum is rejected.

#### Preconditions

The validation form is open. All other fields use the agreed valid baseline.

#### Test Data

| Field        | Value                                                                                                 |
| ------------ | ----------------------------------------------------------------------------------------------------- |
| Age          | `81`                                                                                                  |
| Other fields | Agreed valid baseline (`Alexander`, `TestingStudent`, Singapore, `Manual testing classroom exercise`) |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `81`.
4. Submit.
5. Observe the response.

#### Expected Result

Age 81 is rejected because it is above the maximum age of 80.

#### Actual Result

With the baseline entered (first name `Alexander`, last name `TestingStudent`, country Singapore, notes `Manual testing classroom exercise`) and age changed to `81`, I selected Submit. The form was not submitted. A browser pop-up appeared beside the age field saying "Value must be less than or equal to 80." This looks like the browser's built-in validation, so the rejection happened on the client side before anything reached the server. This matches the expected result.

#### Evidence

Screenshot to be added.

---

## 3-Point Boundary Tests

### Test ID: AGE-3P-82-D

| Item      | Details                    |
| --------- | -------------------------- |
| Test type | Negative                   |
| Tester    | member-d                   |
| Website   | Test Pages validation form |
| Technique | 3-point boundary testing   |
| Status    | pass                       |

#### Purpose

Check that an age two above the maximum is rejected.

#### Preconditions

The validation form is open. All other fields use the agreed valid baseline.

#### Test Data

| Field        | Value                                                                                                 |
| ------------ | ----------------------------------------------------------------------------------------------------- |
| Age          | `82`                                                                                                  |
| Other fields | Agreed valid baseline (`Alexander`, `TestingStudent`, Singapore, `Manual testing classroom exercise`) |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `82`.
4. Submit.
5. Observe the response.

#### Expected Result

Age 82 is rejected because it is above the maximum age of 80.

#### Actual Result

With the baseline entered (first name `Alexander`, last name `TestingStudent`, country Singapore, notes `Manual testing classroom exercise`) and age changed to `82`, I selected Submit. The form was not submitted. A browser pop-up appeared beside the age field saying "Value must be less than or equal to 80." This looks like the browser's built-in validation, so the rejection happened on the client side before anything reached the server. The behaviour was the same as for age 81. This matches the expected result.

#### Evidence

Not captured.

---
