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

| Item      | Details     |
| --------- | ----------- |
| Test type | Exploratory |
| Tester    | member-d    |
| Status    | Not run     |

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

The requirement does not define decimal behaviour. The question being investigated is whether 18.5 is accepted, rejected, or rounded. I will record what happens without labelling it a
