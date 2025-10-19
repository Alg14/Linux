# Level 5 → Level 6 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

human-readable
1033 bytes in size
not executable

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

**ls:** reveals multiple directories with multiple files and I know that the password is 1033 bytes big.

```bash
du -ba | grep 1033
```
**du -ba:** reveals the size of a file and -ba show all the files and in bytes only.

**|:** pipes the outputs the of 'du -ba' into the grep command

**grep:** this is a search command that out puts the row with 1033

```bash
cat ./maybehere07/.file2 
```
**cat:** reads the file and outputs the password for the next level 