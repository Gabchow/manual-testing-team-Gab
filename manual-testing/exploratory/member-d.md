# Self-Designed Testing — Member D

## Testing Idea

I want to investigate how the validation form handles a decimal age, such as 18.5, 30.5 and 80.5.

## Reason

The age field accepts numbers, but decimals sit between the whole numbers used in the guided tests. A decimal near the boundaries (18.5 and 80.5) could show whether the form rounds, rejects, or accepts them. It is also worth knowing whether the browser or the server handles them.

## Test Basis

The published requirement says "age between 18 and 80". It does not say whether decimals are allowed. The classroom model treats age as a whole number from 18 to 80, but it also says decimal behaviour is unspecified, so I will not invent an expected result. Each test records the question being investigated.

## Approach

I will use the agreed valid baseline (first name `Alexander`, last name `TestingStudent`, country Singapore, notes `Manual testing classroom exercise`) and change only age. I chose one decimal inside the range (30.5) and one next to each boundary (18.5 and 80.5). For each, I will record whether the browser stops the submission, whether the form is submitted, and what feedback appears.

## Test Cases

### Test ID: OWN-D-01

| Item      | Details          |
| --------- | ---------------- |
| Test type | Exploratory      |
| Tester    | member-d         |
| Status    | Observation only |

#### Purpose

Observe how the form handles a decimal age just above the minimum boundary.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field        | Value                 |
| ------------ | --------------------- |
| Age          | `18.5`                |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `18.5`.
4. Submit.
5. Observe the response and any feedback.

#### Expected Result

The requirement does not define decimal behaviour. The question being investigated is whether 18.5 is accepted, rejected, or rounded. I will record what happens without labelling it a defect.

#### Actual Result

With the baseline entered and age set to `18.5`, the number was accepted into the age field, but a browser pop-up appeared beside it saying "Please enter a valid value. The two nearest valid values are 18 and 19." The form was not submitted. The message looks like the browser's built-in validation, so the decimal was stopped on the client side. Because nothing reached the server, I cannot say how the server treats 18.5. The requirement does not define decimal behaviour, so this is recorded as an observation.

#### Evidence

Not captured. The result is described in the actual result above.

---

### Test ID: OWN-D-02

| Item      | Details          |
| --------- | ---------------- |
| Test type | Exploratory      |
| Tester    | member-d         |
| Status    | Observation only |

#### Purpose

Observe how the form handles a decimal age inside the valid range.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field        | Value                 |
| ------------ | --------------------- |
| Age          | `30.5`                |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `30.5`.
4. Submit.
5. Observe the response and any feedback.

#### Expected Result

The requirement does not define decimal behaviour. The question being investigated is whether a decimal in the middle of the range is accepted or rejected, and whether the response matches OWN-D-01.

#### Actual Result

With the baseline entered and age set to `30.5`, a browser pop-up appeared beside the age field saying "Please enter a valid value. The two nearest valid values are 30 and 31." The form was not submitted. This matches the response to 18.5 in OWN-D-01, even though 30.5 lies inside the 18 to 80 range, so the rejection appears to be about the value not being a whole number rather than about the range. Nothing reached the server, so server behaviour is unknown. The requirement does not define decimal behaviour, so this is recorded as an observation.

#### Evidence

Not captured. The result is described in the actual result above.

---

### Test ID: OWN-D-03

| Item      | Details          |
| --------- | ---------------- |
| Test type | Exploratory      |
| Tester    | member-d         |
| Status    | Observation only |

#### Purpose

Observe how the form handles a decimal age just above the maximum boundary.

#### Preconditions

The validation form is open and the agreed baseline is entered in every other field.

#### Test Data

| Field        | Value                 |
| ------------ | --------------------- |
| Age          | `80.5`                |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace age with `80.5`.
4. Submit.
5. Observe the response and any feedback.

#### Expected Result

The requirement does not define decimal behaviour. 80.5 is above the maximum of 80, so one possibility is rejection for being out of range, but the question being investigated is how the form actually treats it.

#### Actual Result

With the baseline entered and age set to `80.5`, a browser pop-up appeared beside the age field saying "Value must be less than or equal to 80." The form was not submitted. The message is about the maximum, not about whole numbers, which differs from the messages for 18.5 and 30.5. This suggests the browser reported the range problem first when a value was both a decimal and out of range. Nothing reached the server, so server behaviour is unknown. The requirement does not define decimal behaviour, so this is recorded as an observation.

#### Evidence

Not captured. The result is described in the actual result above.

---

## Overall Observations

I tested three decimal ages: 18.5, 30.5 and 80.5. All three were stopped by the browser's built-in validation before anything was submitted. For 18.5 and 30.5 the pop-up said the nearest valid values were whole numbers, so the form appears to accept only whole-number ages, which matches the classroom model. 30.5 was blocked even though it is inside the valid range. For 80.5 the pop-up reported the maximum of 80 instead, so when a value is both a decimal and out of range, the range message appeared. The published requirement does not mention decimals, so I treated these as observations rather than defects.

## Next Question

Would the server also reject decimal ages if the browser checks were bypassed, for example by sending the request directly, and is the server's response the same as the browser's? I would also like to confirm with the requirement owner whether decimal ages are meant to be allowed.
