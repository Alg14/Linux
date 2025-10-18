# Level 9 → Level 10 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## 💻 Solution 

```bash
strings data.txt | 
grep =====
```
**strings data.txt:** shows the string data in data.txt

**|:** inputs the output of the first command into the grep command

**grep =====:** searches the file for the line that contains ===== and outputs it