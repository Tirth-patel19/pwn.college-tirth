# Bandit.

## Level 0

### Solve
**Flag:** `bandit0`

In this we had to connect the terminal to the ssh key and use the given password as the flag to pass the challenge.

```bash

```

### New Learnings
-NA-
### References 
NA

## Level 0>1

### Solve
**Flag:** `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`

I just had to use the ls command to list all the available files and then use the cat command to print the password for the next level.

```bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

### New Learnings
NA
### References 
NA

## Level 1>2

### Solve
**Flag:** `263JGJPfgU6LtdEvgfWU1XP5yac29mFx`

I first tried to cat the file by its name then i didn't run so i used some help and found out htat we need to specify the absolute path of the dashed filename to open them.

```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

### New Learnings
I learnt that dashed filename cannot be opened using just the name they need to be opened by it absolute path.
### References 
https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal


## Level 2>3

### Solve
**Flag:** `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

I just had to use the absoulute path to obtain the flag.

```bash
bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename--
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

### New Learnings
NA
### References 
NA

## Level 3>4

### Solve
**Flag:** `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`

For this i had to enter the directory using the cd command and then use the "ls -a" to list the dot files and then use the cat command to obtain the next level password.

```bash
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

### New Learnings
NA
### References 
NA

## Level 4>5

### Solve
**Flag:** `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`

For this i entered the inhere  directory and then listed all the fiels and checked each file using the cat function to find the password. 

```bash
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls -a
.  ..  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
\�G�I�d�� �`"��g���     '�����␦bandit4@bandit:~/inhere$ cat ./-file01
�Y��:bl�A��t�1�ν%gM������bandit4@bandit:~/inhere$ cat ./-file02
�
 ��u.Tq␦`h���Ee�+�<��"!^"�bandit4@bandit:~/inhere$ cat ./-file03
Jߑߟ����>jŠ␦��C�f�w��f>�<?�bandit4@bandit:~/inhere$ cat ./-file04
�>��@F��kYq~Jjs�o��;���6���d�Hbandit4@bandit:~/inhere$ cat ./-file05
@�9��I�}�v,��C�����Cy>f�|7�`ibandit4@bandit:~/inhere$ cat ./-file06
�}
  �ت�=ؑ�Hz����1�Uk�U���켼�Ubandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

### New Learnings
NA
### References 
NA

## Level 5>6

### Solve
**Flag:** `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`

In this challenge i used the find function to locate the file with 1033 byte words in it among many different file located in the terminal and then used the cat function to read the file.

```bash
bandit5@bandit:~$ find ./inhere -type f -size 1033c
./inhere/maybehere07/.file2
bandit5@bandit:~$ cat ./inhere/maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

### New Learnings
I learnt about the usage of the find function and its various differnt argument that can be passed into the command.
### References 
https://manpages.ubuntu.com/manpages/noble/man1/find.1.html

## Level 6>7

### Solve
**Flag:** `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`

In this level i used the find function with the user group and size arguments then i received various bunch of error and the file name in it so i found the file name and then used the cat function to read the file.

```bash
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/sys/kernel/tracing/osnoise’: Permission denied
find: ‘/sys/kernel/tracing/hwlat_detector’: Permission denied
find: ‘/sys/kernel/tracing/instances’: Permission denied
find: ‘/sys/kernel/tracing/trace_stat’: Permission denied
find: ‘/sys/kernel/tracing/per_cpu’: Permission denied
find: ‘/sys/kernel/tracing/options’: Permission denied
find: ‘/sys/kernel/tracing/rv’: Permission denied
find: ‘/sys/kernel/debug’: Permission denied
find: ‘/sys/fs/pstore’: Permission denied
find: ‘/sys/fs/bpf’: Permission denied
find: ‘/root’: Permission denied
find: ‘/boot/lost+found’: Permission denied
find: ‘/boot/efi’: Permission denied
find: ‘/run/udisks2’: Permission denied
find: ‘/run/chrony’: Permission denied
find: ‘/run/user/11527’: Permission denied
find: ‘/run/user/11014’: Permission denied
find: ‘/run/user/11009’: Permission denied
find: ‘/run/user/11003’: Permission denied
find: ‘/run/user/11027’: Permission denied
find: ‘/run/user/11026’: Permission denied
find: ‘/run/user/11028’: Permission denied
find: ‘/run/user/11007’: Permission denied
find: ‘/run/user/12001’: Permission denied
find: ‘/run/user/12002’: Permission denied
find: ‘/run/user/11025’: Permission denied
find: ‘/run/user/11004’: Permission denied
find: ‘/run/user/11023’: Permission denied
find: ‘/run/user/13002’: Permission denied
find: ‘/run/user/11002’: Permission denied
find: ‘/run/user/11001’: Permission denied
find: ‘/run/user/11015’: Permission denied
find: ‘/run/user/11000’: Permission denied
find: ‘/run/user/11010’: Permission denied
find: ‘/run/user/11008’: Permission denied
find: ‘/run/user/11006/systemd/inaccessible/dir’: Permission denied
find: ‘/run/user/11011’: Permission denied
find: ‘/run/user/11005’: Permission denied
find: ‘/run/user/13003’: Permission denied
find: ‘/run/user/11013’: Permission denied
find: ‘/run/user/11012’: Permission denied
find: ‘/run/user/11016’: Permission denied
find: ‘/run/user/11021’: Permission denied
find: ‘/run/user/14000’: Permission denied
find: ‘/run/user/5022’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/run/screen/S-bandit24’: Permission denied
find: ‘/run/screen/S-bandit12’: Permission denied
find: ‘/run/screen/S-bandit21’: Permission denied
find: ‘/run/screen/S-bandit23’: Permission denied
find: ‘/run/screen/S-bandit25’: Permission denied
find: ‘/run/screen/S-bandit20’: Permission denied
find: ‘/run/multipath’: Permission denied
find: ‘/run/cryptsetup’: Permission denied
find: ‘/run/lvm’: Permission denied
find: ‘/run/systemd/propagate/fwupd.service’: Permission denied
find: ‘/run/systemd/propagate/ModemManager.service’: Permission denied
find: ‘/run/systemd/propagate/polkit.service’: Permission denied
find: ‘/run/systemd/propagate/chrony.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-logind.service’: Permission denied
find: ‘/run/systemd/propagate/irqbalance.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-networkd.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-resolved.service’: Permission denied
find: ‘/run/systemd/propagate/systemd-udevd.service’: Permission denied
find: ‘/run/systemd/inaccessible/dir’: Permission denied
find: ‘/run/lock/lvm’: Permission denied
find: ‘/dev/mqueue’: Permission denied
find: ‘/dev/shm’: Permission denied
find: ‘/lost+found’: Permission denied
find: ‘/drifter/drifter14_src/axTLS’: Permission denied
find: ‘/manpage/manpage3-pw’: Permission denied
find: ‘/var/log’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/udisks2’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/update-notifier/package-data-downloads/partial’: Permission denied
find: ‘/var/lib/chrony’: Permission denied
find: ‘/var/lib/snapd/void’: Permission denied
find: ‘/var/lib/snapd/cookie’: Permission denied
find: ‘/var/lib/ubuntu-advantage/apt-esm/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/amazon’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/spool/bandit24’: Permission denied
find: ‘/var/spool/rsyslog’: Permission denied
find: ‘/var/spool/cron/crontabs’: Permission denied
find: ‘/var/cache/pollinate’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apparmor/0fb44ac6.0’: Permission denied
find: ‘/var/cache/apparmor/208b6430.0’: Permission denied
find: ‘/var/crash’: Permission denied
find: ‘/var/tmp’: Permission denied
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1751919/task/1751919/fd/6’: No such file or directory
find: ‘/proc/1751919/task/1751919/fdinfo/6’: No such file or directory
find: ‘/proc/1751919/fd/5’: No such file or directory
find: ‘/proc/1751919/fdinfo/5’: No such file or directory
find: ‘/snap’: Permission denied
find: ‘/tmp’: Permission denied
find: ‘/etc/credstore’: Permission denied
find: ‘/etc/credstore.encrypted’: Permission denied
find: ‘/etc/sudoers.d’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
find: ‘/etc/xinetd.d’: Permission denied
find: ‘/etc/stunnel’: Permission denied
find: ‘/etc/polkit-1/rules.d’: Permission denied
find: ‘/etc/multipath’: Permission denied
find: ‘/home/bandit31-git’: Permission denied
find: ‘/home/bandit5/inhere’: Permission denied
find: ‘/home/leviathan4/.trash’: Permission denied
find: ‘/home/bandit30-git’: Permission denied
find: ‘/home/bandit27-git’: Permission denied
find: ‘/home/leviathan0/.backup’: Permission denied
find: ‘/home/drifter6/data’: Permission denied
find: ‘/home/ubuntu’: Permission denied
find: ‘/home/bandit28-git’: Permission denied
find: ‘/home/bandit29-git’: Permission denied
find: ‘/home/drifter8/chroot’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

### New Learnings
NA
### References 
NA

## Level 7>8

### Solve
**Flag:** `dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`

In this level i had to use the grep command and give the argument of "millionth" to grab the whole line containing the password.

```bash
bandit7@bandit:~$ grep "millionth" data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

### New Learnings
NA
### References 
NA

## Level 8>9

### Solve
**Flag:** `4CKMh1JI91bUIZZPXDqGanal4xvAg0JM`

In this I took help of the "uniq" command to give me output of the line that is not repeated using the syntax "uniq -u", for this to work i sorted the file first and then piped it with the uniq command to get the password.

```bash
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

### New Learnings
Learnt about uniq command and various different functions of this commnad.
### References 
https://www.geeksforgeeks.org/linux-unix/uniq-command-in-linux-with-examples/

## Level 9>10

### Solve
**Flag:** `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`

In this level i first tried to use the grep function alone and it did not print the password, then i tried the with cat and piped the grep function to segregate the files with "=" but it also did not work and then i learnt to use the string command to print all the printable files in the file to obtain the password.

```bash
bandit9@bandit:~$ grep "=" data.txt
grep: data.txt: binary file matches
bandit9@bandit:~$ cat data.txt | grep "=" data.txt
grep: data.txt: binary file matches
bandit9@bandit:~$ cat data.txt | grep = data.txt
grep: data.txt: binary file matches
bandit9@bandit:~$ grep "^strt" data.txt
bandit9@bandit:~$ strings data.txt | grep '='
========== theg
VQ=97
[m=K1x
/i8D2[U?=
========== password
LU=W
========== is
=v$,
h{=,rw_c
=}%q
=D!7
YU=<
5=fq
vJ=ho
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
=AdD
```

### New Learnings
Learnt about the usage of the String function 
### References 
https://man7.org/linux/man-pages/man1/strings.1.html

## Level 10>11

### Solve
**Flag:** `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`

In this challenge i had to decode the base64 encoded data to obatin the paswword so i used the base64 -d command to decode the file.


```bash
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

### New Learnings
Learnt about how to encode and decode the data in base64 format in linux.
### References 
https://stackoverflow.com/questions/72858435/how-to-decode-base64-from-each-line-in-file-in-bash

## Level 11>12

### Solve
**Flag:** `7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`

For this challenge i used the "tr" command to rotate the charecters of the password back by 13 palces adn used the ROT13 documentation available on the wikipedia to achieve the flag.

```bash
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

### New Learnings
I learnt the method to rotate the charecters of the string by some amount.
### References 
https://en.wikipedia.org/wiki/ROT13

## Level 12>13

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


## Challenge Name

### Solve
**Flag:** ``



```bash

```

### New Learnings

### References 


