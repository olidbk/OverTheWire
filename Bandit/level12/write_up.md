# Bandit Level 12

> The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Solution

```shell
sshpass -f "ssh_pass" ssh bandit12@bandit.labs.overthewire.org -p 2220
```

```shell
mktemp -d
cd /tmp/tmp.Jw3XQ1hx0S
```

```shell
xxd -r data.txt > data2.txt
```

```shell
file data2.txt
mv data2.txt data2.gz
gunzip data2.gz
```

```shell
file data2
mv data2 data2.bz
bunzip2 data2.bz
```

```shell
file data2
mv data2 data2.gz
gunzip data2.gz
```

```shell
file data2
mv data2 data2.tar
tar -xvf data2.tar
```

```shell
file data5.bin
mv data5.bin data5.tar
tar -xvf data5.tar
```

```shell
file data6.bin
mv data6.bin data6.bz
bunzip2 data6.bz
```

```shell
file data6
mv data6 data6.tar
tar -xvf data6.tar
```

```shell
file data8.bin
mv data8.bin data8.gz
gunzip data8.gz 
```

```shell
file data8
cat data8
```

```text
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
