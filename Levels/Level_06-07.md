# Level 6 → Level 7 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored somewhere on the server and has all of the following properties:

owned by user bandit7
owned by group bandit6
33 bytes in size

## 💻 Solution 

```bash
find / -user "bandit7" -group "bandit6" -size 33c 2>/dev/null
```
**find /:** searches the root directory

**-user "bandit7":** shows files owned by bandit7

**-group "bandit6":** "bandit6: shows files owned by group bandit6

**-size 33c:** shows files sizes that are 33 bytes

 **2>/dev/null:** bypasses error messages such as "Permission denied" and redirects them to /dev/null

```bash
cat /var/lib/dpkg/info/bandit7.password
```
**cat:** reads the file and outputs the password for the next level 

 