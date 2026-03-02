# 📌 Add Two Numbers – LeetCode

## 🧩 Problem Statement

You are given two **non-empty linked lists** representing two non-negative integers.

- The digits are stored in **reverse order**
- Each node contains a **single digit**
- Add the two numbers and return the sum as a linked list

You may assume:

- The two numbers do not contain any leading zero (except the number 0 itself)

---

## 📥 Examples

### Example 1

```
Input:  l1 = [2,4,3], l2 = [5,6,4]
Output: [7,0,8]
Explanation:
342 + 465 = 807
```

### Example 2

```
Input:  l1 = [0], l2 = [0]
Output: [0]
```

### Example 3

```
Input:  l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]
Output: [8,9,9,9,0,0,0,1]
```

---

## 📏 Constraints

- Number of nodes: `1 <= n <= 100`
- `0 <= Node.val <= 9`
- No leading zeros except number `0`

---

# 🚀 Approach

Since the digits are stored in **reverse order**, we can simulate addition just like elementary school math:

### 💡 Algorithm

1. Initialize:
   - `carry = 0`
   - Dummy node to build result

2. Traverse both linked lists simultaneously
3. At each step:

   ```
   sum = value1 + value2 + carry
   digit = sum % 10
   carry = sum / 10
   ```

4. Create a new node with `digit`
5. Move pointers forward
6. After traversal, if `carry > 0`, add final node

---

## ⏱ Time Complexity

- **O(max(n, m))**
  - We traverse both lists once.

## 📦 Space Complexity

- **O(max(n, m))**
  - New linked list is created.
