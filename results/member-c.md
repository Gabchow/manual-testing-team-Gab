# Manual Testing Results — Member C

## Environment

| Item | Details |
|---|---|
| Tester identifier | member-c |
| Check that all required guided test values are covered | |
| Identify missing or unexecuted cases | |

## Login Tests

### Test ID: LOGIN-N02

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-c |
| Website | https://www.saucedemo.com/ |
| Status | pass |

#### Purpose

Shows error when tried to log in without password.

#### Preconditions

Should reflect error message when tried to log in without password.

#### Test Data

| Field | Value |
|---|---|
| standard_user | Empty |

#### Steps

1.Enter username
2.Leave password empty
3.Select login and observe

#### Expected Result

The attempt is rejected with validation feedback. The inventory is not reached.

#### Actual Result

attempt was rejected with validation feedback.

#### Evidence

[View screenshot](../evidence/member-c/lOGIN-N02.png)

---


## Equivalence Partitioning


### Test ID: AGE-EP-90-C

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | Member c |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Pass |

#### Purpose

Whether can inuput age of 90

#### Preconditions

Returns a fail feedback of aged between 18 and 80

#### Test Data

| Field | Value |
|---|---|
| FirstName | Alexander |
| LastName | TestingStudent |
| Age | 90 | 
| Country | Singapore |
| Notes | Manual testing classroom exercise |

#### Steps

1.Fill in the details required.
2.Set age as 90.
3.Submit.

#### Expected Result

A fail message should appear.

#### Actual Result

Failed feedback popup saying "Value must be less than or equal to 80".

#### Evidence

[View screenshot](../evidence/member-c/AGE-EP-90-C.png)

---

## 2-Point Boundary Tests

### Test ID: AGE-2P-80-C

| Item | Details |
|---|---|
| Test type | Positive |
| Tester | member-c |
| Website | Test Pages validation form |
| Technique | 2-point boundary testing |
| Status | Not run |

#### Purpose

Check that it is able to submit.

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Field | Value |
|---|---|
| Age | `80` |
| Other fields | Agreed valid baseline |

#### Steps

1. Restore the validation form.
2. Replace age with `80`.
3. Submit.
4. Observe the response.

#### Expected Result

Age 80 is accepted as it is the maximum age you can put.

#### Actual Result

Successfully submitted.

#### Evidence

[View screenshot](../evidence/member-c/AGE-2P-80-C.png)

---

## 3-Point Boundary Tests


