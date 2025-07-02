## Summary

This project addresses the problem of generating all possible expressions from a set of digits and basic arithmetic operators, evaluating them to find all integer results, and optimizing the brute-force search with pruning and memorization techniques.

### Problem Statement
- We have nine digits (1 through 9) and four operators (+, -, *, /).
- We must form expressions of the form `d1 op1 d2 op2 d3 op3 d4 op4 d5`, using five digits and four distinct operators in sequence.
- Evaluate each expression and record the integer results.

## Experimental Results

After implementing **pruning and operation caching**, the algorithm achieved the following **reduction in the number of combinations calculated while maintaining accuracy in maximum and minimum results**:

| Test Set Size | Brute-Force Combos | Pruned Combos | Pruning Rate |
|--------------:|-------------------:|--------------:|-------------:|
| 10 digits     |         362,880    |      65,788   |     82%      |
| 30 digits     |     342,014,400    |   27,778,183  |     92%      |
| 50 digits     |   5,491,825,920    |  312,056,258  |     94%      |

---

## Conclusions

The **pruning techniques** applied allow the algorithm to **discard between 82% and 94% of the combinations** without losing accuracy in the final results (`-69` and `77`). This substantial reduction makes it feasible to handle larger input ranges efficiently while maintaining the precision of the brute-force method.

---

*Developed by Alberto García Parrado, Master of Artificial Intelligence from VIU*