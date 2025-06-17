## Summary

This project addresses the problem of generating all possible expressions from a set of digits and basic arithmetic operators, evaluating them to find all integer results, and optimizing the brute-force search with pruning and memorization techniques.

### Problem Statement
- We have nine digits (1 through 9) and four operators (+, -, *, /).
- We must form expressions of the form `d1 op1 d2 op2 d3 op3 d4 op4 d5`, using five digits and four distinct operators in sequence.
- Evaluate each expression and record the integer results.

## Experimental Results

| Test Set Size | Brute-Force Combos | Pruned Combos | Brute-Force Time | Optimized Time | Pruning Rate | Speedup |
|--------------:|-------------------:|--------------:|-----------------:|---------------:|-------------:|--------:|
| 10 digits     |          90 000    |      35 640   |           1.67 s |        0.28 s  |    60%       |   83%  |
| 30 digits     |    46 218 508      |  26 192 400   |      1 682.25 s  |      298.47 s  |    43%       |   82%  |
| 50 digits     | 5 491 825 920      |2 752 669 440  |     28 027.43 s  |    4 793.36 s  |    50%       |   83%  |

## Conclusions
**Pruning** removes between 40% and 60% of the search space, resulting in a constant speedup of approximately 80%.

---

*Developed by Alberto García Parrado, Master of Artificial Intelligence from VIU*
