# Bug Notes – Student Utilities

This file records the bugs found in the original Python script and their fixes.

| Bug | Incorrect Behaviour | Reason | Fix Applied |
|---|---|---|---|
| Average Calculation | Returned 135 instead of 90; single mark caused an error | Divided by `len(marks) - 1` | Changed to `total / len(marks)` |
| Pass Boundary | Score of 40 returned False | Used `>` instead of `>=` | Changed to `mark >= PASS_MARK` |
| Grade Classification | Score of 95 returned First instead of Distinction | Checked `>= 60` before `>= 90` | Checked `>= 90` first |

## Final Result

All three bugs were fixed successfully.

The original 9 unit tests were kept unchanged.

**Final test result: 9 tests passed (GREEN).**