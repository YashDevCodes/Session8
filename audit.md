# Code Audit Report

## Project
Student Utilities – Python Debugging

## Files Reviewed
- student_utils.py
- test_student_utils.py

## Bugs Identified

### 1. Average Calculation Bug
- **Problem:** Average was calculated incorrectly. A single mark also caused a division error.
- **Reason:** The code divided by `len(marks) - 1`.
- **Fix:** Changed the formula to `total / len(marks)`.

### 2. Pass Boundary Bug
- **Problem:** A student scoring exactly 40 was marked as failed.
- **Reason:** The code used `>` instead of `>=`.
- **Fix:** Changed the condition to `mark >= PASS_MARK`.

### 3. Grade Classification Bug
- **Problem:** A score of 95 returned First instead of Distinction.
- **Reason:** The First condition was checked before Distinction.
- **Fix:** Checked `average >= 90` first.

## Testing Summary
- Total tests: 9
- Tests passed after fixes: 9
- Final status: All tests passed.

## Conclusion
All three identified bugs were fixed. The original test file was kept unchanged, and the RED → FIX → GREEN cycle was completed.