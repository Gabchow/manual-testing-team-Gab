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

### Equivalence Partitioning

Required coverage:
- Age below the accepted range.
- Age within the accepted range.
- Age above the accepted range.

Results:
[View results for accepted range of age 30](results/member-a.md)

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

### 3-Point Boundary Testing

Required values:
16, 17, 18, 19, 79, 80, 81, 82.

Results:
[View results for age 16](results/member-a.md)


## Member Contributions

### Member A

- Guided results: [View results](results/member-a.md)
- Self-designed tests: [View tests](exploratory/member-a.md)
- Reflection: [View reflection](reflections/member-a.md)
- Chosen investigation: Firstname below 90 Character boundary.
- Main observation: Rejected a 90 Character firstname input.
- Pull request: Add the actual pull-request link.

### Member B

- Guided results: [View results](results/member-b.md)
- Self-designed tests: [View tests](exploratory/member-b.md)
- Reflection: [View reflection](reflections/member-b.md)
- Chosen investigation:
- Main observation:
- Pull request: Add the actual pull-request link.