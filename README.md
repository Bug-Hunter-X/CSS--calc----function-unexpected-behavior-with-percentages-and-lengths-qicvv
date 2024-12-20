# CSS `calc()` Function Unexpected Behavior

This repository demonstrates an uncommon error related to the CSS `calc()` function when combining percentages and lengths. The issue stems from the unexpected order of operations within the `calc()` function, leading to inconsistent and potentially incorrect width calculations.

## Problem

The provided CSS code snippet attempts to set the width of a div to 50% of its parent's width minus 20 pixels.  However, due to the left-to-right evaluation of `calc()`, the subtraction occurs before the percentage is calculated, resulting in an inaccurate final width.

## Solution

The solution involves explicitly using parentheses to enforce the desired order of operations. By grouping the percentage calculation, we ensure that 50% of the parent width is computed first, then 20 pixels are subtracted from the result.