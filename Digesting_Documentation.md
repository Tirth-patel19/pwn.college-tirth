# Module Name

## Learning From Documentation.

### Solve
**Flag:** `pwn.college{Q5LFT_SUyf2rk39_t-50pS-7d74.QX0ITO0wSM1EzNzEzW}`

In this challeneg i just had to follow the given instruction to obtain the flag.

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{Q5LFT_SUyf2rk39_t-50pS-7d74.QX0ITO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Learning Complex usage.

### Solve
**Flag:** `pwn.college{kg8Ucdz_1rUUlIAg7MPV6QNmhm9.QX1ITO0wSM1EzNzEzW}`

In this problem i first needed to locate where the flag was place so I entered into the root directory, then i listed all the files present in the directory and after locating the paths of the flag file i used the given command.

```bash
hacker@man~learning-complex-usage:~$ cd /
hacker@man~learning-complex-usage:/$ ls
bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@man~learning-complex-usage:/$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{kg8Ucdz_1rUUlIAg7MPV6QNmhm9.QX1ITO0wSM1EzNzEzW}
```

### New Learnings
I learned that the commands have arguments and the arguments futher might have some arguments.
### References 
-NA-


## Reading Manual.

### Solve
**Flag:** `pwn.college{0SvAIaDRR81-t_wu7HbpUGMcgSK.QX0EDO0wSM1EzNzEzW}`

For this problem i first opened the documentation of the challenge command in the terminal there i found the syntax of the command and also the additional arguments i need to pass to obtain the flag. 

```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$  /challenge/challenge --vatwub 081
Correct usage! Your flag: pwn.college{0SvAIaDRR81-t_wu7HbpUGMcgSK.QX0EDO0wSM1EzNzEzW}
```

### New Learnings
I learned the usage of man command to open the documentation inside the terminal and not browse it on the internet.
### References 
-NA-


## Searching Mauals

### Solve
**Flag:** `pwn.college{A4ZPXU6XPhhdQzq4qJrecbgM46k.QX1EDO0wSM1EzNzEzW}`

In this question i opened the documentation of the challenge command and used the "/" search feature to search for the flag the I got the argument I need to used to obtain the flag file (--bh).

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --bh
Initializing...
Correct usage! Your flag: pwn.college{A4ZPXU6XPhhdQzq4qJrecbgM46k.QX1EDO0wSM1EzNzEzW}
```

### New Learnings
I learned the how to find a particular word inside of the documentation in a terminal and now to traverse front and back.
### References 
-NA-

## Searching For Manuals

### Solve
**Flag:** `pwn.college{s66sVyEbg31CJr_sik55pwJK4x9.QX2EDO0wSM1EzNzEzW}`

I first used "man man" to open a documentation from there I found how to search for differnet manpages and used it to get to the manpage of the challenge command then I opened the manpage of challenge command and found the argument i need to print the flag.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
ssybgrsikp (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man ssybgrsikp
hacker@man~searching-for-manuals:~$ /challenge/challenge --ssybgr 663
Correct usage! Your flag: pwn.college{s66sVyEbg31CJr_sik55pwJK4x9.QX2EDO0wSM1EzNzEzW}
```

### New Learnings
I learned how to search different manpages in terminal.
### References 
-NA-

## Helpful programs.

### Solve
**Flag:** `pwn.college{YKj71qq2kYhc0AHAEXYBHzUXwmc.QX3IDO0wSM1EzNzEzW}`

in this there was no documentation so i invoked the help function to see the list of argument available in the challeneg command and then using the -p and -g argument i obtained the flag.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 712
hacker@man~helpful-programs:~$ /challenge/challenge -g 712
Correct usage! Your flag: pwn.college{YKj71qq2kYhc0AHAEXYBHzUXwmc.QX3IDO0wSM1EzNzEzW}
```

### New Learnings
how to see the various argument available in a command in the terminal rather than opening its manpage.
### References 
-NA-

## Help for Builtins

### Solve
**Flag:** `pwn.college{AxDl2sBfijSA50jpure7QAfpL7s.QX0ETO0wSM1EzNzEzW}`

For this question as the challenge command is a builtin command there is no manpage for this command so I used the help feature to display the helps for builtin functions there I found the "--secret" argument and the value to this was provided below that.

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "AxDl2sBf".
hacker@man~help-for-builtins:~$ challenge --secret AxDl2sBf
Correct! Here is your flag!
pwn.college{AxDl2sBfijSA50jpure7QAfpL7s.QX0ETO0wSM1EzNzEzW}
```

### New Learnings
Difference between builtin commands and normal commands.
### References 
-NA-

