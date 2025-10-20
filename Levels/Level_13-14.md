# Level 13 → Level 14 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

## 💻 Solution 

```bash
ls 
```
**ls:** list  contents of the current directory and shows a private key, which can be used to login into the next level

```bash
exit
```
**exit:** exits out of the remote machine

```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .  
```
**scp -p:** This command copies files from between remote host and a local machine. 

By using this command I can transfer private key file onto my local machine.

```bash
chmod 700 sshkey.private
```
**chmod 700:** changes the file permission allowing the owner to have control.

```bash
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```
**ssh -i 'privatekey':** This command allows you to connect to a remote host using the private key to authenticate.
