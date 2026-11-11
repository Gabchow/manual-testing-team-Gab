# Self-Designed Testing — Member C

## Testing Idea

Surname input testing.

## Reason

If i can have surname as short or as long as possible.

## Test Basis

Surname must be in between 11 to 79

Record any assumptions or unclear requirements.

## Approach

Choose number at the baseline and testing the numbers before or after.

## Test Cases

### Test ID: OWN-C-01

| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Status | Not run |

#### Purpose

To check if it will be valid or invalid if i have a shorter surname

#### Preconditions

The validation form is open.
All other fields will use the agreed valid baseline.

#### Test Data

| Surname | TestingStu |
| Other fields | Agreed valid baseline |

#### Steps

1.Enter the details
2.Replace surname with TestingStu
3.Submit.
4.Observe the response.

#### Expected Result

Not able to submit, error in surname sector.

#### Actual Result

Unable to submit because the number of letters in surname not within the requirement range.

#### Evidence

[View screenshot](../evidence/member-c/OWN-C-01.png)

---

## Overall Observations

Error in surname input.

## Next Question

Whether First Name applies the same.