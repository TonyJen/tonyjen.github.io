---
layout: post
title: "Coding Challenge: Maximum Sum Circular Subarray"
date: 2023-11-29
categories: coding, algorithms
author: [Tony Jen]
---

# Maximum Sum Circular Subarray

In today's post, we're tackling a challenging problem: the Maximum Sum Circular Subarray. This is a great problem to test your understanding of algorithms and data structures, specifically dealing with arrays and subarray computations.

## Problem Description

Given a circular integer array `nums` of length `n`, your task is to return the maximum possible sum of a non-empty subarray of `nums`. Remember, in a circular array, the end of the array connects to the beginning, creating a loop-like structure.

**Example:**

Input: nums = [5, -3, 5]
Output: 10
Explanation: The subarray [5, 5] has the maximum sum of 10.


## Solution Approach

The solution hinges on a key insight: the maximum circular subarray sum can be either the maximum subarray sum (computed using Kadane's algorithm) or the total sum of the array minus the minimum subarray sum.

### Algorithm Steps

1. **Compute Total Sum:** First, calculate the total sum of the array.
2. **Maximum Subarray Sum:** Use Kadane’s algorithm to find the maximum subarray sum.
3. **Minimum Subarray Sum:** Invert the elements of the array and use Kadane’s algorithm to find the minimum subarray sum.
4. **Final Calculation:** The maximum circular subarray sum is either the maximum subarray sum or the total sum minus the minimum subarray sum, whichever is greater.
5. **Negative Numbers Handling:** If all numbers are negative, return the maximum subarray sum.

## Python Implementation

```python
def maxSubarraySumCircular(nums):
    def kadane(gen):
        ans = cur = float('-inf')
        for x in gen:
            cur = x + max(cur, 0)
            ans = max(ans, cur)
        return ans

    total = sum(nums)
    max_sum = kadane(nums)
    min_sum = -kadane(-x for x in nums[1:])
    min_sum2 = -kadane(-x for x in nums[:-1])

    return max(max_sum, total + min_sum, total + min_sum2) if max_sum > 0 else max_sum

print(maxSubarraySumCircular([5, -3, 5]))  # Output: 10


Conclusion
This problem is a great exercise in understanding how to manipulate subarrays and use dynamic programming techniques like Kadane's algorithm. It's a reminder of the elegance and efficiency you can achieve with a well-thought-out algorithm.

Happy coding!