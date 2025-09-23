# Comprehending Commands

## cat: not the pet, but the command!

### Solve
**Flag:** `pwn.college{QCbBrpQYxZCcLSm1uawttdFgUT0.QXxcTN0wSM1EzNzEzW}`

It was just a simply typing cat function and its argument

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{QCbBrpQYxZCcLSm1uawttdFgUT0.QXxcTN0wSM1EzNzEzW}
```

### New Learnings
Use of the "cat" function.
### References 
-NA-


## catting absolute paths

### Solve
**Flag:** `pwn.college{A33PaSn_YqBydfJC3DaC7wLxi0j.QX5ETO0wSM1EzNzEzW}`

In this i used the concept of absolute path and use of cat function to obtain the flag. 

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{A33PaSn_YqBydfJC3DaC7wLxi0j.QX5ETO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## More catting practice

### Solve
**Flag:** `pwn.college{AkOitHI_bFMDnkFu48lm2OvVpwx.QXwITO0wSM1EzNzEzW}`

At first I was unable to find the flag file using various new commands like the "ls" etc. Then i tried to cd into the directory there it gave me an error and also the absolute path of where the flag is hidden.  

```bash
hacker@commands~more-catting-practice:~$ ls
Desktop  a  d  not-the-flag
hacker@commands~more-catting-practice:~$ cat not-the-flag
cat: not-the-flag: No such file or directory
hacker@commands~more-catting-practice:~$ cd challenge
You used 'cd'! In this level, I don't allow you to change the working directory
--- you MUST chase pass 'cat' the absolute path of where I put it on the
filesystem (which is /lib/firefox/browser/flag).
hacker@commands~more-catting-practice:~$ cat /lib/firefox/browser/flag
pwn.college{AkOitHI_bFMDnkFu48lm2OvVpwx.QXwITO0wSM1EzNzEzW}
```

### New Learnings
learned new command like "ls","grep",etc
### References 
https://youtu.be/7fs1i7TAMck?si=6Q_aWg3fPCyYMYnL


## Grepping for a needle in a haystack

### Solve
**Flag:** `pwn.college{8wKiEXjCZc8V-3BcCfS-3B1CGkL.QX3EDO0wSM1EzNzEzW}`

I used the grep command and as argument i gave the staring of every flag i.e "pwn.college" and obtained the flag.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{8wKiEXjCZc8V-3BcCfS-3B1CGkL.QX3EDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Comparing files

### Solve
**Flag:** `pwn.college{ca5AXys-9DnAnCUxHSzwlCNFP2J.01MwMDOxwSM1EzNzEzW}`

In this i used the "diff" command to distinguish the fake and real flag from the 2 files.

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
82a83
> pwn.college{ca5AXys-9DnAnCUxHSzwlCNFP2J.01MwMDOxwSM1EzNzEzW}
```

### New Learnings
working of the "diff" command.
### References 
-NA


## Listing files

### Solve
**Flag:** `pwn.college{krGrDBO0KL7cGSRNa5tPSEFu9QH.QX4IDO0wSM1EzNzEzW}`

First i peeked into the challenge directory and found 2 files and then i tried running the first file and it gave me the flag and the second file had the informatio  about the question.

```bash
hacker@commands~listing-files:~$ ls /challenge
31727-renamed-run-3909  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/31727-renamed-run-3909
Yahaha, you found me! Here is your flag:
pwn.college{krGrDBO0KL7cGSRNa5tPSEFu9QH.QX4IDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Touching files

### Solve
**Flag:** `pwn.college{Y1hZrGC2DZHmORMm7dmAnZkqSuM.QXwMDO0wSM1EzNzEzW}`

I used the "touch" command to create 2 new files adn then run the given command to obtain the flag.

```bash
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{Y1hZrGC2DZHmORMm7dmAnZkqSuM.QXwMDO0wSM1EzNzEzW}
```

### New Learnings
uses of the "touch" command.
### References 
-Na-


## Removing files

### Solve
**Flag:** `pwn.college{gXCejmR_zQI5lUPxRbZI51q85iF.QX2kDM1wSM1EzNzEzW}`

In this i used the "rm" command to remove the exsisting file and then obatained the flag.

```bash
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{gXCejmR_zQI5lUPxRbZI51q85iF.QX2kDM1wSM1EzNzEzW}
```

### New Learnings
Function of the "rm" i.e remove command.
### References 
-NA-

## Moving files

### Solve
**Flag:** `pwn.college{QAqNcu0LKPwSDLAA0S5Jy__X7pC.0VOxEzNxwSM1EzNzEzW}`

I used the "mv" commmand to move the file to the given location in the question.

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{QAqNcu0LKPwSDLAA0S5Jy__X7pC.0VOxEzNxwSM1EzNzEzW}
```

### New Learnings
Learned about usage of the move i.e "mv" command.
### References 
-NA- 

## Hidden files

### Solve
**Flag:** `pwn.college{gle5rERL0MEtLsBiPg5Cti7y6Lg.QXwUDO0wSM1EzNzEzW}`

First i entered into the root directory and then I searched for the hidden files i.e file preponded with "." there i found the flag file and read the file using the flag command. 

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv         bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-24219267030  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-24219267030
pwn.college{gle5rERL0MEtLsBiPg5Cti7y6Lg.QXwUDO0wSM1EzNzEzW}
```

### New Learnings
Difference between normal files and Hidden files and how to see the hidden files using the "ls" function.
### References 
-NA-

## An epic filesystem Quest

### Solve
**Flag:** `pwn.college{YicqsVytHq-6E1Yih_wwo3dlStB.QX5IDO0wSM1EzNzEzW}`

first I entered the root directory adn then i used "ls" command to display all the file and found a file and read it using the "cat" function adn then i proceeded as it was instructed in the upcoming files.

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
TIP  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat TIP
Tubular find!
The next clue is in: /opt/linux/linux-5.4/include/config/cpu/freq/default/gov

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/include/config/cpu/freq/default/gov
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/cpu/freq/default/gov$ ls -a
.  ..  .NUGGET  userspace.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/cpu/freq/default/gov$ cat  .NUGGET
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/Documentation/firmware_class

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/cpu/freq/default/gov$ cd  /opt/linux/linux-5.4/Documentation/firmware_class
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/firmware_class$ ls -a
.  ..  TRACE  hotplug-script
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/firmware_class$ cat TRACE
Tubular find!
The next clue is in: /usr/lib/R/library/grDevices/Meta
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/Documentation/firmware_class$ cd /usr/lib/R/library/grDevices/Meta
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/grDevices/Meta$ ls -a
.  ..  DOSSIER  Rd.rds  demo.rds  features.rds  hsearch.rds  links.rds  nsInfo.rds  package.rds
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/grDevices/Meta$ cat ^C
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/grDevices/Meta$ cat DOSSIER
Yahaha, you found me!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/split

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/R/library/grDevices/Meta$ cd /opt/busybox/busybox-1.33.2/include/config/feature/split
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/split$ ls -a
.  ..  BLUEPRINT  fancy.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/split$ cat BLUEPRINT
Yahaha, you found me!
The next clue is in: /usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/split$ cd /usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ ls -a
.  ..  .DISPATCH  __init__.cpython-38.pyc  system.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ cat .DISPATCH
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/dt-bindings/pinctrl

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ ls /opt/linux/linux-5.4/include/dt-bindings/pinctrl
ALERT-TRAPPED  at91.h                   dm814x.h  k3.h         mt6397-pinfunc.h  mt7623-pinfunc.h  pads-imx8qm.h           pinctrl-tegra-xusb.h  qcom,pmic-mpp.h     rockchip.h      stm32-pinfunc.h
am33xx.h       bcm2835.h                dra.h     keystone.h   mt65xx.h          nomadik.h         pads-imx8qxp.h          pinctrl-tegra.h       r7s72100-pinctrl.h  rzn1-pinctrl.h  sun4i-a10.h
am43xx.h       brcm,pinctrl-stingray.h  hisi.h    lochnagar.h  mt6797-pinfunc.h  omap.h            pinctrl-tegra-io-pad.h  qcom,pmic-gpio.h      r7s9210-pinctrl.h   samsung.h
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ cat /usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__/ALERT-TRAPPED
cat: /usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__/ALERT-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ cat /opt/linux/linux-5.4/include/dt-bindings/pinctrl/ALERT-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/share/racket/pkgs/draw-lib/file/compiled

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ ls /usr/share/racket/pkgs/draw-lib/file/compiled
REVELATION-TRAPPED  gif_rkt.dep  gif_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ cat /usr/share/racket/pkgs/draw-lib/file/compiled/REVELATION-TRAPPED
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/arm/mach-mv78xx0

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/prompt_toolkit/contrib/completers/__pycache__$ cd /opt/linux/linux-5.4/arch/arm/mach-mv78xx0
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-mv78xx0$ ls -a
.  ..  GIST  Kconfig  Makefile  bridge-regs.h  buffalo-wxl-setup.c  common.c  common.h  db78x00-bp-setup.c  irq.c  irqs.h  mpp.c  mpp.h  mv78xx0.h  pcie.c  rd78x00-masa-setup.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/arm/mach-mv78xx0$ cat GIST
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{YicqsVytHq-6E1Yih_wwo3dlStB.QX5IDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-

## Making driectories

### Solve
**Flag:** `pwn.college{c-BiAzv3er-CUkncJR2CgZSa9IR.QXxMDO0wSM1EzNzEzW}`

First I created a direcortory using "mkdir" command and then i used the absolute path knowledge to create a new file using "touch" command and created new file in the directory.

```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ ls /tmp/pwn
college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{c-BiAzv3er-CUkncJR2CgZSa9IR.QXxMDO0wSM1EzNzEzW}
```

### New Learnings
uses of "mkdir" command.
### References 
-NA-

## Finding files

### Solve
**Flag:** `pwn.college{cEQCGQa7lmcNQ-6K9qXVh5GEbU4.QXyMDO0wSM1EzNzEzW}`

first i tried finding the flag file in the home directory but i dint found anything so i jumped to root direcotory adn found multiple files matching the arguments. I read each file using the "cat" function and found the flag.

```bash
hacker@commands~finding-files:~$ find -name flag
hacker@commands~finding-files:~$ cd /
hacker@commands~finding-files:/$ find -name flag
find: ‘./root’: Permission denied
find: ‘./etc/ssl/private’: Permission denied
find: ‘./tmp/tmp.TpSOPGOVKK’: Permission denied
./usr/local/lib/python3.8/dist-packages/zipp-3.20.2.dist-info/flag
./usr/local/lib/python3.8/dist-packages/pwnlib/flag
find: ‘./var/cache/apt/archives/partial’: Permission denied
find: ‘./var/cache/ldconfig’: Permission denied
find: ‘./var/cache/private’: Permission denied
find: ‘./var/log/private’: Permission denied
find: ‘./var/log/apache2’: Permission denied
find: ‘./var/log/mysql’: Permission denied
find: ‘./var/lib/apt/lists/partial’: Permission denied
find: ‘./var/lib/mysql-keyring’: Permission denied
find: ‘./var/lib/php/sessions’: Permission denied
find: ‘./var/lib/private’: Permission denied
find: ‘./var/lib/mysql-files’: Permission denied
find: ‘./var/lib/mysql’: Permission denied
find: ‘./run/mysqld’: Permission denied
find: ‘./run/sudo’: Permission denied
find: ‘./proc/tty/driver’: Permission denied
find: ‘./proc/1/task/1/fd’: Permission denied
find: ‘./proc/1/task/1/fdinfo’: Permission denied
find: ‘./proc/1/task/1/ns’: Permission denied
find: ‘./proc/1/fd’: Permission denied
find: ‘./proc/1/map_files’: Permission denied
find: ‘./proc/1/fdinfo’: Permission denied
find: ‘./proc/1/ns’: Permission denied
find: ‘./proc/7/task/7/fd’: Permission denied
find: ‘./proc/7/task/7/fdinfo’: Permission denied
find: ‘./proc/7/task/7/ns’: Permission denied
find: ‘./proc/7/fd’: Permission denied
find: ‘./proc/7/map_files’: Permission denied
find: ‘./proc/7/fdinfo’: Permission denied
find: ‘./proc/7/ns’: Permission denied
./opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
./nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
./nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
./nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
./nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
./nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
./nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
./nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
./nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
hacker@commands~finding-files:/$ cat ./usr/local/lib/python3.8/dist-packages/zipp-3.20.2.dist-info/flag
pwn.college{cEQCGQa7lmcNQ-6K9qXVh5GEbU4.QXyMDO0wSM1EzNzEzW}
```

### New Learnings
Uses of find command.
### References 
-NA-

## Linking files

### Solve
**Flag:** `pwn.college{U3dG28IB2bGYoV-cNlcp0pjGth1.QX5ETN1wSM1EzNzEzW}`

At first when I used the command it showed me the error that file already exsisted in the direcotry so I removed it from the directory and then established a new symlink connection to obtain the flag.

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
ln: failed to create symbolic link '/home/hacker/not-the-flag': File exists
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{U3dG28IB2bGYoV-cNlcp0pjGth1.QX5ETN1wSM1EzNzEzW}
```

### New Learnings
I learned what are link, types of links, hard and soft links how to establish connection between 2 files.
### References 
https://youtu.be/mA08E59-zo8?si=tPVhVVyVZUAeGf9W \
https://youtu.be/tkuYrwzQ7N4?si=1PTm5aeDngPTckr7