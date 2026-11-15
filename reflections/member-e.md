
# Individual Manual Testing Reflection — Member E

## 1. What makes a test positive or negative?

A positive test uses valid input to check whether the application works as expected, such as entering Age 18 or 79. A negative test uses invalid input to check whether the application rejects it correctly, such as entering Age 16 or 81.

## 2. Why can a negative test pass?

A negative test passes when the application correctly rejects invalid input. For example, my Age 81 test passed because the browser prevented submission and displayed "Value must be less than or equal to 80."

## 3. How did equivalence partitioning help you select data?

Equivalence partitioning helped me divide inputs into valid and invalid groups instead of testing every possible value. I tested `abc` as a non-numeric age input and observed that the browser prevented letters from being entered.

## 4. What did boundary testing help you investigate?

Boundary testing helped me check how the application handles values near the minimum and maximum allowed ages of 18 and 80. My tests confirmed that Ages 18 and 79 were accepted, while Ages 16 and 81 were rejected.

## 5. What did you choose to test during the open-ended activity, and why?

I chose to test whether the form accepts an empty first name because I had previously encountered a first-name length validation error during guided testing. The browser displayed "Please fill in this field" and prevented submission.

## 6. Did your observations lead to follow-up tests?

Yes. When the first name `Alex` was rejected as too short, I changed it to `Alexander` and repeated the Age 18 test successfully. My empty first-name test also suggested a possible follow-up test using whitespace-only input.

## 7. How does your Git history show your contribution?

My Git history shows individual commits on the `testing/member-e` branch for preparing test records, recording guided test results, and completing self-designed testing. I also committed screenshots and Markdown documentation as evidence of my testing contributions.
