# Level 3 → Level 4 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in a hidden file in the inhere directory.

## 💻 Solution 

```bash
ls -a
```

**ls -a:** list all the contents of the current directory including hidden files and shows a ...Hiding-From-You file

```bash
cat ...Hiding-From-You
```
**cat:** reads the file and outputs the password for the next level 