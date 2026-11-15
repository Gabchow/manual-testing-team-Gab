# Self-Designed Testing — Member A

## Testing Idea

Check if the Firstname Character limit rejects an input that crosses the character boundary.

## Reason

To validate the input boundary.

## Test Basis

Character boundary for the firstname.

## Approach

Using a firstname with 90 characters. 1 more than the boundary.


### Test ID: FN-Length-90char-A
| Item | Details |
|---|---|
| Test type | Negative |
| Tester | member-a |
| Website | https://testpages.eviltester.com/apps/client-server-form-validation/ |
| Status | Rejected |

#### Purpose

Checks if the First name length requirements rejects a firstname outside the boundary of
90 characters.

#### Preconditions

The page loads, all the other input fields are the agreed and positive baseline values.

#### Test Data

| Field | Value |
|---|---|
| First name | Alexanderalexanderaalexanderalexanderalexanderalexanderalexanderalexanderalexanderalexander |
| All other input fields | Agreed baseline |

#### Steps

1. Restore the validation form.
2. Enter the agreed baseline.
3. Replace Firstname with `Alexanderalexanderaalexanderalexanderalexanderalexanderalexanderalexanderalexanderalexander`.
4. Submit.
5. Observe the response.

#### Expected Result

The form rejects the Name `Alexanderalexanderaalexanderalexanderalexanderalexanderalexanderalexanderalexanderalexander` because it is above the length requirements of the firstname, below 90 characters.

#### Actual Result

The form as expected rejects the input `Alexanderalexanderaalexanderalexanderalexanderalexanderalexanderalexanderalexanderalexander`. Giving a message shown, 'Firstname provided is too long'.

#### Evidence

[View screenshot](../evidence/member-a/FN-Length-90char-A.png)

## Next Question

What happens when the user corrects an error and tries again?