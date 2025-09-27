# Shell Variables

## Printing Variables

### Solve
**Flag:** `pwn.college{YKQkh9xiB6CBZjLHq0mKzyfXWlT.QX3UTN0wSM1EzNzEzW}`

In this i just had to follow the given instructions to get the flag.

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{YKQkh9xiB6CBZjLHq0mKzyfXWlT.QX3UTN0wSM1EzNzEzW}
```

### New Learnings
How to print out the variables using "$".
### References
-NA-


## Challenge Name

### Solve
**Flag:** `pwn.college{IrpWVMAiUdNh4ZQtiaed_7xyw_n.QX5UTN0wSM1EzNzEzW}`

In this i had to set the new variable in the shell to get the flag.

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IrpWVMAiUdNh4ZQtiaed_7xyw_n.QX5UTN0wSM1EzNzEzW}
```

### New Learnings
I got to learnt how to create a variable in the shell and then use it.
### References
-NA-


## Multi-Word Variables

### Solve
**Flag:** `pwn.college{sreS_oeXdfbUhzSr1J5yyRIf8By.QXwYTN0wSM1EzNzEzW}`

In this question as instructed we just have to add everything under quotation to assign them to variables as a whole.

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{sreS_oeXdfbUhzSr1J5yyRIf8By.QXwYTN0wSM1EzNzEzW}
```

### New Learnings
I learnt how to assign a block of word or a sentence to a variable.
### References
-NA-


## Exporting Variables

### Solve
**Flag:** `pwn.college{cSXYxaHNJbKxBtoGq4Az5dYtdWi.QXyYTN0wSM1EzNzEzW}`

To solve this problem i frist exported the "pwn" variable and assigned it to the value "college" then i assigned variable "college" to "pwn" and then called the command to get the output.

```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE 
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{cSXYxaHNJbKxBtoGq4Az5dYtdWi.QXyYTN0wSM1EzNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

### New Learnings
I learnt about what is the meaning of exporting, what is child shell how to access it and its functions.
### References
-NA-

## Printing Exported Variables.

### Solve
**Flag:** `pwn.college{IVrzbCd9Odvf7Ntn21q_0PXH440.QX4UTN0wSM1EzNzEzW}`



```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=769bebd1c7f26027426df2d4fdbbb0fc9740043355483627797fb62c56310190
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{IVrzbCd9Odvf7Ntn21q_0PXH440.QX4UTN0wSM1EzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

### New Learnings
I learned about a new command "env" and about its function in shell.
### References
-NA-


## Storing command output

### Solve
**Flag:** `pwn.college{ArMhx-11d2grGBV81fY-4YENO0Y.QX1cDN1wSM1EzNzEzW}`

In this problem i first stored the output of the command in the "PWN" file and then called that file to give me the flag.

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{ArMhx-11d2grGBV81fY-4YENO0Y.QX1cDN1wSM1EzNzEzW}
```

### New Learnings
I learnt how to store the output of the command directly into a file.
### References
-NA-


## Reading Input

### Solve
**Flag:** `pwn.college{wvkbcmM7c9Db-5Iubm7wEuA2m_j.QX4cTN0wSM1EzNzEzW}`

To solve this I used the rea command to read the inputn from the user and then specified the name of the variable i want to store my input into and received the flag.

```bash
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{wvkbcmM7c9Db-5Iubm7wEuA2m_j.QX4cTN0wSM1EzNzEzW}
```

### New Learnings
I learnt how take the input femm the user using the read command.
### References
-NA-

## Challenge Name

### Solve
**Flag:** `pwn.college{w3a6PEMcERkBkOyFDCqwZ2sUleV.QXwIDO0wSM1EzNzEzW}`

To solve this question i just had to read the "/challenge/read" function into the "PWN" file to receive my flag so I used the read function together with the use of redirection to obtain the flag. 

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{w3a6PEMcERkBkOyFDCqwZ2sUleV.QXwIDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References
-NA-