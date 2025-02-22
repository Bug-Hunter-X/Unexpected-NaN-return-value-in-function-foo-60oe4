# Unexpected NaN return value in function foo

This repository contains a JavaScript code example demonstrating an unexpected `NaN` return value in a function.  The function `foo` is intended to return `null` if either input `a` or `b` is `null` or `undefined`. However, it currently returns `NaN` when one of the inputs is `undefined`. 

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## Bug Description
The issue lies in the strict equality check (`===`). `undefined` and `null` are different values, and the strict equality check won't treat them as equal.  Therefore, when one input is `undefined`, the condition `a === null || b === null` evaluates to `false`, leading to the `a + b` operation. If `a` or `b` is `undefined`, this operation results in `NaN`.