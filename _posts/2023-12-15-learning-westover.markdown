---
layout: post
title: "Solving the Array Element Parity Problem"
date: 2023-12-03
categories: coding algorithm
author: [Tony Jen]
---

## Array Element Parity Problem

In this post, we're going to explore a common interview question that's often seen in coding challenges, such as LeetCode. The problem is known as **Array Element Parity**.

### Problem Statement

**Given**: An array of integers where each integer appears exactly twice except for one integer which appears only once.

**Task**: Find that single integer.

### Examples

1. **Input**: `[4, 1, 2, 1, 2]`  
   **Output**: `4`

2. **Input**: `[2, 2, 1]`  
   **Output**: `1`

### Constraints

- The array will not be empty.
- The array size will be in the range of `[1, 30000]`.
- Each element in the array will be an integer in the range of `[-30000, 30000]`.

### Solution Approach

The key to solving this problem efficiently lies in understanding the properties of the bitwise XOR operation. The XOR of two identical numbers is 0, and the XOR of any number with 0 is the number itself. Since our array contains each number twice except for one, using XOR on all elements will effectively cancel out the pairs and leave us with the single number.

### Python Solution

```python
def singleNumber(nums):
    result = 0
    for num in nums:
        result ^= num
    return result

# Testing the function
print(singleNumber([4, 1, 2, 1, 2]))  # Output: 4
print(singleNumber([2, 2, 1]))        # Output: 1

```

This solution has a time complexity of O(n) and a space complexity of O(1), which makes it quite efficient for large arrays.
Conclusion

The Array Element Parity problem is a great example of how a simple bitwise operation can be incredibly powerful in solving seemingly complex problems. It's a reminder that sometimes, the most efficient solutions are also the most elegant.

Happy coding!