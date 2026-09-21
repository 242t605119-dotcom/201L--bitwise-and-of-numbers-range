# LeetCode 201 - Bitwise AND of Numbers Range

## Problem Description

Given two integers `left` and `right`, find the bitwise AND of all the numbers in the range from `left` to `right`.

The range includes both `left` and `right`.

## Example

Input:
left = 5
right = 7

The numbers are:

5 = 101
6 = 110
7 = 111

Bitwise AND:

101
110
111
---
100

Output:

4

## Approach

Checking every number in the range can be inefficient when the range is large.

Instead, we find the common binary prefix of `left` and `right`.

We repeatedly shift both numbers to the right until they become equal. During every shift, we increase the `shift` counter.

Once both numbers are equal, we have found the common binary part. We then shift it back to the left by the number of positions stored in `shift`.

This gives the required bitwise AND result.

## Algorithm

1. Initialize `shift` as 0.
2. While `left` is less than `right`, right shift both numbers by 1.
3. Increase `shift` after every shift.
4. When both numbers become equal, shift the result back to the left.
5. Return the final result.

## Time Complexity

**O(log n)**

The loop runs based on the number of bits in the numbers.

## Space Complexity

**O(1)**

Only a few variables are used, so constant extra space is required.

## Key Concepts

- Bitwise AND
- Binary numbers
- Right shift operator `>>`
- Left shift operator `<<`
- Common binary prefix

## Author

T.nandhini
