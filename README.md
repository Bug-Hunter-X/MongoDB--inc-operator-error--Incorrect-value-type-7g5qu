# MongoDB $inc Operator Error
This repository demonstrates a common error when using the `$inc` operator in MongoDB update operations.  The `$inc` operator is used to increment or decrement a numeric field. However, providing a string value instead of a number will result in an error or unexpected behavior.

## Bug Description
The provided code attempts to increment the `count` field using the `$inc` operator with a string value ('1').  This will lead to an error because `$inc` expects a numeric value.

## Solution
The solution involves correcting the value provided to `$inc` to ensure it's a number (integer or floating point).

## How to reproduce
1.  Set up a MongoDB instance
2.  Create a collection named 'myCollection'
3.  Insert a document with a field named `count`
4.  Execute the incorrect code provided in `bug.js`
5.  Observe the error message from MongoDB.

## How to fix
Replace the incorrect code with the correct code shown in `bugSolution.js`