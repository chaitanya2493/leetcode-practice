# 📌 Two Sum – LeetCode

## 🧩 Problem Statement

Given an array of integers `nums` and an integer `target`, return the **indices** of the two numbers such that they add up to `target`.

### Rules:

- Each input has **exactly one solution**
- You may **not use the same element twice**
- You can return the answer in **any order**

---

## 📥 Examples

### Example 1

```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: nums[0] + nums[1] = 2 + 7 = 9
```

### Example 2

```
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

### Example 3

```
Input: nums = [3,3], target = 6
Output: [0,1]
```

---

## 📏 Constraints

- `2 <= nums.length <= 10^4`
- `-10^9 <= nums[i] <= 10^9`
- `-10^9 <= target <= 10^9`
- Only **one valid answer** exists.

---

## 🚀 Approach

To improve from the brute-force **O(n²)** solution, we use a **HashMap** to store previously visited numbers.

### 💡 Idea:

- Iterate through the array once.

- For each number, calculate:

  ```
  complement = target - currentNumber
  ```

- If the complement exists in the map → return indices.

- Otherwise, store the current number and its index in the map.

### ⏱ Time Complexity:

- **O(n)**

### 📦 Space Complexity:

- **O(n)**
