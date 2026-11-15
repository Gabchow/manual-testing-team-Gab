# Team Summary

## Guided Testing Coverage

### Login Testing

Required coverage:
- Valid credentials.
- Incorrect password.
- Missing password.
- Missing username.
- Recovery after an invalid attempt.

Results:
[View the results for valid credentials](results/member-a.md)
[View results for incorrect password](results/member-b.md)
[View results for Missing password](results/member-c.md)
[View results for Missing username](results/member-d.md)
[View results for Recovery after an invalid attempt](results/member-e.md)

### Equivalence Partitioning

Required coverage:
- Age below the accepted range.
- Age within the accepted range.
- Age above the accepted range.

Results:
[View results for accepted range of age 30](results/member-a.md)
[View results for age 10 below range](results/member-b.md)
[View results for age 90 above range](results/member-c.md)
[View results for blank age handling](results/member-d.md)
[View results for non-numeric input handling using abc](results/member-e.md)

### Input-Format Observations

Required observations:
- Blank age.
- Non-numeric age input.

Results:
Add links to the relevant member records.

### 2-Point Boundary Testing

Required values:
17, 18, 80, 81.

Results:
[View results for age 17](results/member-a.md)
[View results for age 18](results/member-b.md)
[View results for age 80](results/member-c.md)
[View results for age 81](results/member-d.md)
[View results for Independently repeat 18 and 81](results/member-e.md)

### 3-Point Boundary Testing

Required values:
16, 17, 18, 19, 79, 80, 81, 82.

Results:
[View results for age 16](results/member-a.md)
[View results for age 19](results/member-b.md)
[View results for age 79](results/member-c.md)
[View results for age 82](results/member-d.md)
[View results for Independently repeat 16 and 79](results/member-e.md)

## Member Contributions

### Member A

- Guided results: [View results](results/member-a.md)
- Self-designed tests: [View tests](exploratory/member-a.md)
- Reflection: [View reflection](reflections/member-a.md)
- Chosen investigation: Firstname below 90 Character boundary.
- Main observation: Rejected a 90 Character firstname input.

### Member B

- Guided results: [View results](results/member-b.md)
- Self-designed tests: [View tests](exploratory/member-b.md)
- Reflection: [View reflection](reflections/member-b.md)
- Chosen investigation:
- Main observation:

### Member C

- Guided results: [View results](results/member-c.md)
- Self-designed tests: [View tests](exploratory/member-c.md)
- Reflection: [View reflection](reflections/member-c.md)
- Chosen investigation:
- Main observation:

### Member D

- Guided results: [View results](results/member-d.md)
- Self-designed tests: [View tests](exploratory/member-d.md)
- Reflection: [View reflection](reflections/member-d.md)
- Chosen investigation:
- Main observation:

### Member E

- Guided results: [View results](results/member-e.md)
- Self-designed tests: [View tests](exploratory/member-e.md)
- Reflection: [View reflection](reflections/member-e.md)
- Chosen investigation:
- Main observation: