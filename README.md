# COBOL MOVE CORRESPONDING Data Mismatch Bug

This repository demonstrates a subtle bug that can occur in COBOL programs using the `MOVE CORRESPONDING` statement.  When the data structures involved do not have perfectly matching data types and lengths in corresponding fields, data truncation or corruption can occur without obvious compiler warnings.  The example shows a scenario where this leads to unexpected results.

## Bug Description
The bug arises from using `MOVE CORRESPONDING` to transfer data between records with slightly different field definitions.  Specifically, differences in field lengths or data types lead to data loss or corruption.

## How to Reproduce
Compile and run the `bug.cob` program.  The output will show that data has been truncated or corrupted, demonstrating the effect of the `MOVE CORRESPONDING` statement when data types don't precisely align.

## Solution
The `bugSolution.cob` program shows how to avoid this issue by explicitly defining moves for each field.  This makes the logic explicit and ensures data integrity.