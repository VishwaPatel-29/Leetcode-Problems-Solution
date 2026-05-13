# 🔹 1512. Number of Good Pairs

## 🧠 Problem Statement
Given an array of integers `nums`, return the number of good pairs.

A pair `(i, j)` is called good if:

- `nums[i] == nums[j]`
- and `i < j`

---

## 📌 Examples

```
Input:  nums = [1,2,3,1,1,3]
Output: 4

Explanation:
There are 4 good pairs:
(0,3), (0,4), (3,4), (2,5)
```

```
Input:  nums = [1,1,1,1]
Output: 6

Explanation:
Every pair in the array is a good pair.
```

```
Input:  nums = [1,2,3]
Output: 0
```

---

## 💡 Approach
- Traverse the array using two loops
- Compare every pair of elements
- If both elements are equal, increase the count
- Return the total number of good pairs

---

## ⚡ C++ Solution 

```cpp
class Solution {
public:
    int numIdenticalPairs(vector<int>& nums) {

        int count = 0;

        for(int i = 0; i < nums.size(); i++){

            for(int j = i + 1; j < nums.size(); j++){

                if(nums[i] == nums[j]){
                    count++;
                }
            }
        }

        return count;
    }
};
```

---

## 🧪 Dry Run

```cpp
nums = [1,2,3,1,1,3]

i = 0 -> nums[i] = 1

j = 1 -> 1 != 2
j = 2 -> 1 != 3
j = 3 -> 1 == 1 --> count = 1
j = 4 -> 1 == 1 --> count = 2
j = 5 -> 1 != 3

i = 2 -> nums[i] = 3
j = 5 -> 3 == 3 --> count = 3

i = 3 -> nums[i] = 1
j = 4 -> 1 == 1 --> count = 4
```

---

## 🚀 Notes
- Time Complexity: O(n²)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`Array` `Easy`
