# 🔹 1678. Goal Parser Interpretation

## 🧠 Problem Statement
You own a Goal Parser that can interpret a string `command`.  

The command consists of:
- `"G"` → interpreted as `"G"`
- `"()"` → interpreted as `"o"`
- `"(al)"` → interpreted as `"al"`

The interpreted strings are concatenated in the original order.

Return the final interpreted string.

---

## 📌 Examples

```
Input:  command = "G()(al)"
Output: "Goal"

Explanation:
G    -> G
()   -> o
(al) -> al

Final Result: "Goal"
```

```
Input:  command = "G()()()()(al)"
Output: "Gooooal"
```

```
Input:  command = "(al)G(al)()()G"
Output: "alGalooG"
```

---

## 💡 Approach
- Traverse the string character by character  
- If the character is `'G'`, append `"G"` to the result  
- If `"()"` is found, append `"o"`  
- Otherwise, append `"al"`  
- Continue until the complete string is processed  

---

## ⚡ C++ Solution 

```cpp
class Solution {
public:
    string interpret(string command) {
        string result = "";
        
        for(int i = 0; i < command.length(); i++){
            if(command[i] == 'G'){
                result += 'G';
            }
            else if(command[i] == '('){
                if(command[i + 1] == ')'){
                    result += 'o';
                    i++;
                }
                else{
                    result += "al";
                    i += 1;
                }
            }
        }
        
        return result;
    }
};
```

---

## 🚀 Notes
- Time Complexity: O(n)  
- Space Complexity: O(n)  

---

## 🏷️ Tags
`String` `Easy`
