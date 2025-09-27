# File Globbing 

## Matching with *

### Solve
**Flag:** `pwn.college{cqSveEWh8PjuT0l-RuZAeJ3SJjK.QXxIDO0wSM1EzNzEzW}`

In this problem i used the globbing function (*) to change the directory to "/challenge" and then run the command instructed to obtain the flag.

```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{cqSveEWh8PjuT0l-RuZAeJ3SJjK.QXxIDO0wSM1EzNzEzW}
```

### New Learnings
I learnt what is globbing different types of globbing tool and thei usage.
### References 
-NA-

## Matching with ?

### Solve
**Flag:** `pwn.college{Yjp8LW_OGTzd7EfG0TfW7YgM4VF.QXyIDO0wSM1EzNzEzW}`

In this we need to replace the "c" and "l" with the "?" to enter the challenge directory and run the function.

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Yjp8LW_OGTzd7EfG0TfW7YgM4VF.QXyIDO0wSM1EzNzEzW}
```

### New Learnings
Usage and function of "?".
### References 
-NA-

## Matching with []

### Solve
**Flag:** `pwn.college{kGAJKwLdHulqPqrK4FPuF1cHDwF.QXzIDO0wSM1EzNzEzW}`

for this we first changed the directory and then used the globbing tool "[]" to find the files and get the flag.

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{kGAJKwLdHulqPqrK4FPuF1cHDwF.QXzIDO0wSM1EzNzEzW}
```

### New Learnings
Usage and Function of "[]".
### References
-NA


## Challenge Name

### Solve
**Flag:** `pwn.college{M4alnzNM29N1R6oPQoNWe7r0xFh.QX0IDO0wSM1EzNzEzW}`

For this we started from home direcotry itself and gve the path of the files as an argument together with with use of globbing tool.

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{M4alnzNM29N1R6oPQoNWe7r0xFh.QX0IDO0wSM1EzNzEzW}
```

### New Learnings
the gloobing tool "[]" alson accepts file's path as an argument.
### References
-NA-

## Multiple Globs.

### Solve
**Flag:** `pwn.college{QGly-16VaiCNAfH0KwZzapplKSz.0lM3kjNxwSM1EzNzEzW}`

First we entered the directory then used the concept of relative path and used "*p*" as an argument which will fetch all the files with "p" in it.

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{QGly-16VaiCNAfH0KwZzapplKSz.0lM3kjNxwSM1EzNzEzW}
```

### New Learnings
-NA-
### References
-NA-

## Mixing globs.

### Solve
**Flag:** `pwn.college{UMDlK6xnV5h6xxxhemr1IgV8iQv.QX1IDO0wSM1EzNzEzW}`

First I changed my directory and then later i tried with many differnt argument but got error then i tried using the firstname of each file and then using "*" to obtain all the files that start with [cep] and ends wwith something else names.

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{UMDlK6xnV5h6xxxhemr1IgV8iQv.QX1IDO0wSM1EzNzEzW}
```

### New Learnings
I learnt how to implement all different types of globs together.
### References
https://youtu.be/hQyXuuBbCOo?si=o1-fOxPyAp80uHkv 


## Exclusionary globbing.

### Solve
**Flag:** `pwn.college{44EhXqZH4nDlbTH38bH9k0RFtyb.QX2IDO0wSM1EzNzEzW}`

I used the "!" function to find all the other files in the directory.

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{44EhXqZH4nDlbTH38bH9k0RFtyb.QX2IDO0wSM1EzNzEzW}
```

### New Learnings
Usage and function of "!", "^".
### References
-NA-

## Tab completion.

### Solve
**Flag:** `pwn.college{sfzE2sO2cXOpnEQ8ClHV9xf01Dd.0FN0EzNxwSM1EzNzEzW}`

For this challenge we just had to type a few starting words and then hit the tab button to auto complete the argument.

```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{sfzE2sO2cXOpnEQ8ClHV9xf01Dd.0FN0EzNxwSM1EzNzEzW}
```

### New Learnings
Usefullnes of the auto completion available in the command line.
### References
-NA-

## Multiple options for tab completion

### Solve
**Flag:** `pwn.college{Qb4adW-pK_gacgXVsRos5EU6c5A.0lN0EzNxwSM1EzNzEzW}`

for this we tried the tab completion for te word p and it gave many options then from those option we found the pwncollege-flag and then run it to find the flag.

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{Qb4adW-pK_gacgXVsRos5EU6c5A.0lN0EzNxwSM1EzNzEzW}
```

### New Learnings
leant new function of tab compeltion.
### References
-NA-

## Globbing tab completion on commands

### Solve
**Flag:** `pwn.college{sO6u5ufseewFBv_gLUso9M2vvzC.0VN0EzNxwSM1EzNzEzW}`

I just had to follow the instruction to get to the flag.

```bash
hacker@globbing~tab-completion-on-commands:~$ pwncollege-2442
Correct! Here is your flag:
pwn.college{sO6u5ufseewFBv_gLUso9M2vvzC.0VN0EzNxwSM1EzNzEzW}
```

### New Learnings
We can auto complete commands as well.
### References
-NA-