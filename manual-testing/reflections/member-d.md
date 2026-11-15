# Individual Reflection — Member D

## 1. What makes a test positive or negative?

A test is positive when it uses valid input and expected actions, and negative when it uses invalid input or an unexpected action. The type depends on the input, not on whether the test passes.

## 2. Why can a negative test pass?

A negative test passes when the application handles the invalid input correctly. In LOGIN-N03, leaving the username empty produced "Epic sadface: Username is required" and the inventory was not reached, so the rejection was the expected result and the test passed.

## 3. How did equivalence partitioning help you select data?

It showed that one representative from each group is enough, and that ages above 80 form one group. My own tasks were the blank-age and `abc` observations, which I treated separately from the three numeric groups because they are about input format rather than numeric ranges.

## 4. What did boundary testing help you investigate?

It let me check the edge just above the maximum age, using 81 for 2-point testing and 82 for 3-point testing. Both were rejected with "Value must be less than or equal to 80.", which suggests the maximum is enforced as 80 and not 81 or more.

## 5. What did you choose to test during the open-ended activity, and why?

I tested decimal ages (18.5, 30.5 and 80.5) because the requirement says "age between 18 and 80" and never mentions decimals. I wanted to see how the form handles values between the whole numbers used in the guided tests.

## 6. Did your observations lead to follow-up tests?

Yes. 18.5 and 30.5 gave a "nearest valid values" message, but 80.5 gave the maximum-value message, so I compared them and noticed that the browser reported different problems. This led to my next question: whether the server would also reject decimals if the browser checks were bypassed.

## 7. How does your Git history show your contribution?

My branch `testing/member-d` has separate commits for preparing my record, the login test, the equivalence and input-format observations, the boundary tests, the self-designed plan, the self-designed results, and this reflection. Each commit is my own work on my own files, pushed to GitHub.
