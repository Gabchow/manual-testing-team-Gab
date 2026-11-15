
# Self-Designed Manual Testing — Member E

## Test ID: EXP-E-01

### Test Information

| Item | Details |
|---|---|
| Tester | member-e |
| Date | 12 November 2026 |
| Website | Test Pages Validation Form |
| Test type | Negative testing |
| Test scenario | Empty first name |
| Status | Pass |

### Objective

To verify that the validation form prevents submission when the First name field is left empty.

### Reason for Choosing This Test

During guided testing, I observed that the application validated the length of the first name. I wanted to investigate whether the form also prevents users from submitting an empty first name.

### Preconditions

The validation form is open and all fields except First name contain valid values.

### Test Data

| Field | Value |
|---|---|
| First name | Empty |
| Last name | TestingStudent |
| Age | 25 |
| Country | Singapore |
| Notes | Manual testing classroom exercise |

### Test Steps

1. Open the Test Pages validation form.
2. Leave the First name field empty.
3. Enter `TestingStudent` as the last name.
4. Enter `25` as the age.
5. Select `Singapore` as the country.
6. Enter `Manual testing classroom exercise` in Notes.
7. Click Submit.
8. Observe the validation behaviour.

### Expected Result

The browser should prevent submission and display a validation message because the First name field is required.

### Actual Result

After clicking Submit with an empty First name field, the browser displayed the message "Please fill in this field." The form remained on the input page, and submission was prevented by client-side validation.

### Evidence

[Empty First Name Validation Screenshot](../evidence/member-e/exp-empty-firstname.png)

### Conclusion

Pass — The browser correctly prevented submission when the required First name field was empty.

### Observation

The browser's built-in required-field validation prevented the form from being submitted. This indicates that the empty first-name scenario is handled at the client-side level. Server-side validation was not tested.

### Follow-Up Testing

A useful follow-up would be to enter a first name containing only spaces to investigate whether the application treats whitespace-only input as valid.
