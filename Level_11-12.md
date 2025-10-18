# Level 11 → Level 12 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## 💻 Solution 

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
**cat data.txt** reads the file and outputs the content of data.txt

**|:** inputs the output of the first command into the tr command

**tr 'A-Za-z' 'N-ZA-Mn-za-m':** translates and decodes the letters by shifting them by 13 positions back