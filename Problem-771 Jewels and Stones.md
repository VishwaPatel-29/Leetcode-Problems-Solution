# 🔹 771. Jewels and Stones

## 🧠 Problem Statement
You're given strings `jewels` representing the types of stones that are jewels, and `stones` representing the stones you have.  

Each character in `stones` is a type of stone you have. You want to know how many of the stones you have are also jewels.  

Letters are case sensitive, so `"a"` is considered a different type of stone from `"A"`.

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
- For every character, check if it exists in `jewels`  
- If found, increase the count  
- Break inner loop once matched to avoid duplicate counting  

---

## ⚡ C++ Solution (Copy-Paste Ready)

```cpp
class Solution {
public:
    int numJewelsInStones(string jewels, string stones) {
        int count = 0;
        for(int i = 0; i < stones.length(); i++){
            for(int j = 0; j < jewels.length(); j++){
                if(stones[i] == jewels[j]){
                    count++;
                    break;
                }
            }
        }
        return count;
    }
};
```

---

## 🚀 Notes
- Time Complexity: O(n * m)  
- Space Complexity: O(1)  

---

## 🏷️ Tags
`String` `Easy`
