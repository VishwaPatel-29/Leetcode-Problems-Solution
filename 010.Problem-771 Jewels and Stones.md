# 🔹 771. Jewels and Stones

## 🧠 Problem Statement
You're given strings `jewels` representing the types of stones that are jewels, and `stones` representing the stones you have.

Each character in `stones` is a type of stone you have. You want to know how many of the stones are also jewels.

Letters are case-sensitive, so `"a"` and `"A"` are considered different.

---

## 📌 Examples

```
Input:  jewels = "aA", stones = "aAAbbbb"
Output: 3
```

```
Input:  jewels = "z", stones = "ZZ"
Output: 0
```

---

## 💡 Approach
- Traverse each character in `stones`
- Use `find()` to check whether the character exists in `jewels`
- If found, increase the count
- Return the final count

---

## ⚡ C++ Solution

```cpp
class Solution {
public:
    int numJewelsInStones(string jewels, string stones) {

        int count = 0;

        for(char stone : stones){

            // npos means character not found
            if(jewels.find(stone) != string::npos){
                count++;
            }
        }

        return count;
    }
};
```

---

## 🧪 Dry Run

```cpp
jewels = "ab"
stones = "aabbc"

Initially:
count = 0

First character  -> 'a'
'a' present in jewels --> count = 1

Second character -> 'a'
'a' present in jewels --> count = 2

Third character  -> 'b'
'b' present in jewels --> count = 3

Fourth character -> 'b'
'b' present in jewels --> count = 4

Fifth character  -> 'c'
'c' not present in jewels
```

---

## 🚀 Notes
- Time Complexity: O(n × m)  
- Space Complexity: O(1)

---

## 🏷️ Tags
`String` `Easy`
