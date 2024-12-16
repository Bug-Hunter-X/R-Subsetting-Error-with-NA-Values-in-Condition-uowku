# R Subsetting Error with NA Values in Condition

This repository demonstrates a common error in R when subsetting data frames based on conditions that involve columns containing NA (Not Available) values.

The `bug.R` file contains code that attempts to subset a data frame based on a condition, but fails due to the presence of NA values in the 'value' column.  The solution, provided in `bugSolution.R`, shows how to handle NA values appropriately to avoid this error.

## Problem

When subsetting a data frame in R using logical indexing (like `df[df$value > 2, ]`), if the column being tested ('value' in this case) contains NA values, R throws an error or produces unexpected results because comparisons with NA always return NA.

## Solution

The solution involves explicitly handling NA values using functions such as `is.na()` to exclude them from the subsetting condition.