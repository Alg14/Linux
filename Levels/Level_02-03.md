# Level 2 → Level 3 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

## 💻 Solution 

```bash
ls
```

**ls:** list the contents of the current directory 

```bash
cat ./"--spaces in this filename--"
```
**cat:** Enclosing the filename in quotes " " allows the shell to read a file with spaces correctly, revealing the password