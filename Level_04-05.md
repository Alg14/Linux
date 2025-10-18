# Level 4 → Level 5 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the only human-readable file in the inhere directory.

## 💻 Solution 

```bash
ls
```

**ls:** list the contents of the current directory and reveals a folder called 'inhere'.

```bash
cd inhere
```

**cd:** changes the directory to 'inhere'

```bash
ls
```

**ls:** reveals multiple files and I know that the password is in the only human-readable file

```bash
file ./*
```
**file:** is a command that reveal the file type

**./*:** checks all the files in the directory

This then reveals the only file in ASCII text which is the only human-readable one.

```bash
cat ./-file07
```
**cat:** reads the file and outputs the password for the next level 