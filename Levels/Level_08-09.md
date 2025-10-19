# Level 8 → Level 9 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## 💻 Solution 

```bash
sort data.txt | uniq -u
```
**sort data.txt:** sorts the content of data.txt

**|:** inputs the output of the sort command into the uniq command

**uniq -u:** shows the lines that only appear once in a file