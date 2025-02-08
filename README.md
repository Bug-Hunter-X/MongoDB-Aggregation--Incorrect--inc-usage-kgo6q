# MongoDB Aggregation Pipeline Bug: Incorrect $inc Operator Usage

This repository demonstrates a common error when using the `$inc` operator within a MongoDB aggregation pipeline.  The `$inc` operator is intended to increment a field's value, but it's crucial to apply it correctly within the context of the pipeline stages.

The bug showcases an incorrect application of `$inc` outside of the `$group` stage, leading to unexpected behavior. The solution provides the correct implementation.

## Bug
The `bug.js` file contains the flawed aggregation pipeline.  It attempts to increment the `count` field after grouping, which will not produce the expected result.

## Solution
The `bugSolution.js` file presents the corrected aggregation pipeline.  The `$inc` operation is correctly placed within the `$group` stage, ensuring that the increment is applied to each group's count accurately.
