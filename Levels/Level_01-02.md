# Level 1 → Level 2 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in a file called - located in the home directory

## 💻 Solution 

```bash
ls
```

**ls:** list the contents of the current directory and shows a - file

```bash
cat ./-
```
**cat:** displays the contents of the file. Prefixing it with ./ tells the shell that - is a filename, not an option, revealing the password