# JavaScript Null Check Subtlety

This repository demonstrates a common, yet subtle, bug in JavaScript related to null checks within functions. The `foo` function aims to add two numbers but returns `null` if either input is `null`.  This behavior might not always align with desired functionality, especially if the intent is to treat `null` as 0.

## Bug Description

The provided `bug.js` file contains a JavaScript function that checks for null values in its arguments before performing an addition operation. If either argument is null, the function returns null. While this is correct for strict null checking, it might not be the intended behavior in all situations.  For example, if the goal is to treat null as 0, this function will fail to produce the correct sum. 

## Solution

The `bugSolution.js` file provides a corrected version of the function. It now explicitly handles null values by assigning them a value of 0, thus providing more flexible handling of null inputs.