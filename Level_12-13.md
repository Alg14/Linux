# Level 12 → Level 13 — OverTheWire Bandit 

## 🎯 Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## 💻 Solution 

```bash
mktemp -d
cd /tmp/tmp.YK1xFDUfEa
cp ~/data.txt . 
mv data.txt hexdump
```
**mktemp -d:** creates a directory in the temp directory with a random name.
**cd:** changes the directory
**cp:** copies the file to the current directory (.)
**mv:** renames the file

```bash
xxd -r hexdump compressed.gz
```

**xxd -r:** reverses the hexdump to its orginal form and changes the name to compressed.gz

I identified that once the hexdump is reversed the file a compressed gzip file. 

```bash
gzip -d compressed.gz
```
**gzip -d:** This command decompresses gzip files but the file must have the .gz extension for it to work.

Once I completed this I identified that the decompressed file was bzip2 compressed file.

```bash
bzip2 -d compressed
```

**bzip2 -d:** This command decompresses bzip2 files but the file doesnt need the .bz2 extension for it to work. 

```bash
mv compressed.out compressed.gz
gzip -d compressed.gz
```
Then I decompress the gzip file. After completing this I identified an archived file.

```bash
 tar -xf compressed
```
**tar -xf:** This command extarcts the contents of the archive file

```bash
 tar -xf data5.bin
```
Then i repeat it and find a bzip2 file.

```bash
bzip2 -d data6.bin
```
Then decompress the bzip2

```bash
tar -xf data6.bin.out
```
Then extract the archived file

```bash
gzip -d data8.gz
```
Then decompress the gzip file

```bash
cat data8
```
Finally, I find the file containing the password.