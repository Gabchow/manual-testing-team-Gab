
# Manual Testing Results — Member E

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-e |
| Date and time | 12 November 2026 |
| Browser and version | Google Chrome (version to be filled) |
| Operating system | Windows |

---

## Login Tests

### Test ID: LOGIN-R01

| Item | Details |
|---|---|
| Test type | Recovery |
| Tester | member-e |
| Website | SauceDemo |
| Status | Pass |

#### Purpose

To verify that a user can successfully log in after correcting an incorrect password.

#### Preconditions

The user is logged out and the SauceDemo login page is displayed. Both input fields are cleared.

#### Test Data

| Field | Value |
|---|---|
| Username | standard_user |
| Incorrect password | wrong_password |
| Correct password | secret_sauce |

#### Steps

1. Open the SauceDemo login page.
2. Enter `standard_user` as the username.
3. Enter `wrong_password` as the password.
4. Click Login.
5. Observe the error message.
6. Replace the incorrect password with `secret_sauce`.
7. Keep the username unchanged.
8. Click Login again.
9. Check whether the inventory page appears.

#### Expected Result

The first login attempt should be rejected with an error message. After correcting the password, the user should successfully log in and see the inventory page with products.

#### Actual Result

The first login attempt was rejected and an error message appeared. After correcting the password, the second login attempt succeeded. The inventory page was displayed with products visible.

#### Evidence

[Successful Login Screenshot](../evidence/member-e/login-r01-success.png)

#### Conclusion

Pass — The application correctly handled login recovery after an invalid password.

---

## Equivalence Partitioning

### Test ID: AGE-EP-ABC-E

| Item | Details |
|---|---|
| Test type | Input-format observation |
| Tester | member-e |
| Website | Test Pages Validation Form |
| Status | Pass |

#### Purpose

To observe how the Age field handles non-numeric input.

#### Preconditions

The validation form is open and the input fields are available.

#### Test Data

| Field | Value |
|---|---|
| First name | Alex |
| Surname | TestingStudent |
| Age | abc (attempted input) |
| Country | Afghanistan (selected in observed form) |
| Notes | Manual testing classroom exercise |

#### Steps

1. Open the Test Pages validation form.
2. Enter the baseline information.
3. Attempt to enter `abc` into the Age field.
4. Observe whether the input is accepted, blocked, or cleared.
5. If the input can be entered, submit the form.
6. Record the feedback and behaviour.

#### Expected Result

The classroom age model requires a whole number between 18 and 80 inclusive. Non-numeric input should not result in a successful submission with `abc` as the age. The exact input-handling behaviour is to be observed.

#### Actual Result

The Age field did not allow alphabetic characters to be entered. When attempting to type `abc`, the field remained empty. The browser prevented the non-numeric input at the input field level. Server-side rejection was not tested.

#### Evidence

[Non-numeric Age Input Screenshot](../evidence/member-e/age-ep-abc.png)

#### Conclusion

Pass — The browser prevented non-numeric input in the Age field, consistent with the classroom whole-number requirement.

---

## 2-Point Boundary Tests

### Test ID: AGE-2P-18-E

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-e |
| Website | Test Pages Validation Form |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

To verify that age 18, the minimum valid age, is accepted.

#### Preconditions

The validation form is open and all other fields use the corrected valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Surname | TestingStudent |
| Age | 18 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the validation form.
2. Enter the valid baseline.
3. Change Age to `18`.
4. Submit the form.
5. Observe the response.

#### Expected Result

Age 18 should be accepted because it is the minimum valid age.

#### Actual Result

The initial submission using the first name `Alex` produced a validation error stating "Firstname too short". After changing the first name to `Alexander` and keeping Age as `18`, the form displayed "Valid Input — Your Input passed validation". The submitted age of 18 was shown correctly.

#### Evidence

[Age 18 Successful Validation Screenshot](../evidence/member-e/age-2p-18.png)

#### Conclusion

Pass — Age 18 was accepted as the minimum valid age after correcting the baseline first name.

---

### Test ID: AGE-2P-81-E

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-e |
| Website | Test Pages Validation Form |
| Technique | 2-point boundary testing |
| Status | Pass |

#### Purpose

To verify that age 81, immediately above the maximum valid age, is rejected.

#### Preconditions

The validation form is open and all other fields use the corrected valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Surname | TestingStudent |
| Age | 81 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the validation form.
2. Enter the valid baseline.
3. Change Age to `81`.
4. Submit the form.
5. Observe the response.

#### Expected Result

Age 81 should be rejected because it exceeds the maximum valid age of 80.

#### Actual Result

After entering Age 81 and clicking Submit, the browser displayed the validation message "Value must be less than or equal to 80." The form remained on the input page and submission was prevented by client-side validation.

#### Evidence

[Age 81 Validation Screenshot](../evidence/member-e/age-2p-81.png)

#### Conclusion

Pass — The browser correctly prevented submission of Age 81 because it exceeds the maximum valid age of 80.

---

## 3-Point Boundary Tests

### Test ID: AGE-3P-16-E

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-e |
| Website | Test Pages Validation Form |
| Technique | 3-point boundary testing |
| Status | Pass |

#### Purpose

To verify that age 16, below the minimum valid age, is rejected.

#### Preconditions

The validation form is open and all other fields use the corrected valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Surname | TestingStudent |
| Age | 16 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the validation form.
2. Enter the valid baseline.
3. Change Age to `16`.
4. Submit the form.
5. Observe the response.

#### Expected Result

Age 16 should be rejected because it is below the minimum valid age of 18.

#### Actual Result

After entering Age 16 and clicking Submit, the browser displayed the validation message "Value must be greater than or equal to 18." The form remained on the input page, and submission was prevented by client-side validation.

#### Evidence

[Age 16 Validation Screenshot](../evidence/member-e/age-3p-16.png)

#### Conclusion

Pass — The browser correctly prevented submission of Age 16 because it is below the minimum valid age of 18.

---

### Test ID: AGE-3P-79-E

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-e |
| Website | Test Pages Validation Form |
| Technique | 3-point boundary testing |
| Status | Not run |

#### Purpose

To verify that age 79, immediately below the maximum valid age, is accepted.

#### Preconditions

The validation form is open and all other fields use the corrected valid baseline.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexander |
| Surname | TestingStudent |
| Age | 79 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1. Restore the validation form.
2. Enter the valid baseline.
3. Change Age to `79`.
4. Submit the form.
5. Observe the response.

#### Expected Result

Age 79 should be accepted because it is within the valid age range of 18 to 80.

#### Actual Result

Not recorded — test has not been executed.

#### Evidence

Not captured.
