# SQL Query with Non-Deterministic Function in WHERE Clause

This repository demonstrates a common SQL error involving the use of non-deterministic functions within the WHERE clause of a query. Non-deterministic functions produce different outputs even with the same input parameters, often due to reliance on system-dependent variables such as timestamps or random number generators. This behavior can lead to unpredictable and unreliable query results.

The `bug.sql` file contains a sample SQL query showcasing this issue.  The `bugSolution.sql` file provides a corrected version, illustrating how to avoid this problem by either removing the non-deterministic function or ensuring that non-deterministic functions only impact parts of the query that do not lead to inconsistent results. 

## Problem

Using non-deterministic functions within a WHERE clause produces unpredictable results because the condition may evaluate differently depending on the specific execution context.

## Solution

The solution is to either remove or replace the non-deterministic function or redesign the query so that it doesn't rely on non-deterministic results in the WHERE clause to filter rows.