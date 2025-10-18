# Level 7 → Level 8 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the file data.txt next to the word millionth

## 💻 Solution 

```bash
cat data.txt | grep "millionth"
```
**cat:** reads the file and outputs the password for the next level 

**|:** inputs the output of the cat command into the grep command

**grep "millionth":** searches the file for the line that contains "millionth" and outputs it