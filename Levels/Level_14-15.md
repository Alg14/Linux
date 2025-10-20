# Level 14 → Level 15 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## 💻 Solution 

```bash
cat /etc/bandit_pass/bandit14
```
**cat:** reads and outputs the file containing the password of the current level.

```bash
nc localhost 30000
```
**nc localhost 30000:** This command allows me to open a network connection to port 30000 on my local machine. Next I enter the password of the current level to retrieve the next password.

