# Self-Designed Testing — Member B

## Testing Idea

I want to investigate if a decimal number being input as the age will be accepted, and if not, what is the error message displayed.

## Reason

To check if the system allows decimal numbers, and if not, whether the error message displayed is appropriate.

## Test Basis

I am assuming that within the form, I able to input a decimal value in the form field (some websites dont allow "." to be filled in).

## Approach

I'm going to choose a decimal number that is between 18 and 80, as that is the validation requirement for age.

## Test Cases

### Test ID: OWN-A-01

| Item | Details |
|---|---|
| Test type | Exploratory |
| Tester | member-b |
| Status | Pass |

#### Purpose

This test checks if a decimal number within the boundary values is accepted as an input for the age.

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

Unsure because the instructions do not state whether decimal numbers within the boundary can be accepted.

#### Actual Result

Form submission is unsuccessful.
Error message displayed: "Please enter a valid value. The two nearest valid values are 18 and 19."

#### Evidence

[View screenshot](../evidence/member-b/OWN-A-01.png)

---

## Overall Observations

It shows that the website's backend code is coded to only allow whole numbers to be input.

## Next Question

I might investigate what error message will pop up if I use a decimal number that is outside the boundary (e.g. 15.5). Will the error message from test OWN-A-01 or test AGE-EP-10-B show up? (which one takes priority)