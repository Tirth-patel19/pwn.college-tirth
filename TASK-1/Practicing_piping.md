# Practicing Piping

## Redirecting output

### Solve
**Flag:** `pwn.college{w1kCxj1-Wm3vWFWE6OKHZ9q_ABC.QX0YTN0wSM1EzNzEzW}`

I used the redirection command to store PWN in COLLEGE file and got the flag.

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{w1kCxj1-Wm3vWFWE6OKHZ9q_ABC.QX0YTN0wSM1EzNzEzW}
```

### New Learnings
I learnt that we could redirect the commands output to some other files.
### References
-NA-


## Redirecting more Output

### Solve
**Flag:** `pwn.college{AUQgVTaYGcfv7HfVAAqx85j1WZE.QX1YTN0wSM1EzNzEzW}`

for this challenge I first redirected the output of the function in the myflag file and the read that file using the "cat" function.

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{AUQgVTaYGcfv7HfVAAqx85j1WZE.QX1YTN0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References
-NA-

## Appending output

### Solve
**Flag:** `pwn.college{Av829BSDewurB9_Joak4CttJgad.QX3ATO0wSM1EzNzEzW}`

for this challenge we frist opend the file in append mode to run the "/challenge/run" command this appedned both the first half and second half togeter and we got our flag.

```bash
hacker@piping~appending-output:~$ /challenge/run > /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
9BSDewurB9_Joak4CttJgad.QX3ATO0wSM1EzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 |
\|/ This is the first half:
 v
pwn.college{Av829BSDewurB9_Joak4CttJgad.QX3ATO0wSM1EzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```

### New Learnings
I learnt how the appending feature in linux works.
### References
-NA-

## Redirecting errors

### Solve
**Flag:** `pwn.college{gJXvzw2W7Nx3r3KoAmDwEqv5-iS.QX3YTN0wSM1EzNzEzW}`

I used the same format that they used in the example first the redirection of the file and then the error.

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{gJXvzw2W7Nx3r3KoAmDwEqv5-iS.QX3YTN0wSM1EzNzEzW}
```

### New Learnings
I learnt what is error and how to redirect them.
### References
-NA-

## Redirecting input 

### Solve
**Flag:** `pwn.college{wd6FuulL0-KMk85VQHHsYrA-71r.QXwcTN0wSM1EzNzEzW}`

for this as given in the above instruction, I first performed the redirecting output and then the input part.

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{wd6FuulL0-KMk85VQHHsYrA-71r.QXwcTN0wSM1EzNzEzW}
```

### New Learnings
I learnt what redirecting input means and its usage.
### References
-NA-


## Grepping stored results

### Solve
**Flag:** `pwn.college{I8BxakwxnL0qMfRmfdHEOM1jgBZ.QX4EDO0wSM1EzNzEzW}`

This challenge was just the mixing of concept of redicting and grepping. thus first i redirected the output and then used the grep function to match with the "pwn.college" line.

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt
pwn.college{I8BxakwxnL0qMfRmfdHEOM1jgBZ.QX4EDO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References
-NA-


## Grepping Live output

### Solve
**Flag:** `pwn.college{YOHssVter9iIT59wrD8xv8v21QO.QX5EDO0wSM1EzNzEzW}`

In this challenge the challenege function printed out various bunch of file then we used the greeping tool to obtain the flag.

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn.college"
pwn.college{YOHssVter9iIT59wrD8xv8v21QO.QX5EDO0wSM1EzNzEzW}
```

### New Learnings
how to use multiple command together using the pipe operator(|).
### References
-NA-

## Grepping errors

### Solve
**Flag:** `pwn.college{goIw0H5maYcyFFZtS-QM1-Ife1j.QX1ATO0wSM1EzNzEzW}`

To solve this problem at first I got confuse about what command to use but then i looked in the question above and then followed the instruction to receive the flag.

```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep "pwn.college"
pwn.college{goIw0H5maYcyFFZtS-QM1-Ife1j.QX1ATO0wSM1EzNzEzW}
```

### New Learnings
got to learn how to extract information from redirecting the error and using the pipe function together.
### References
-NA

## Filtering with grep -v

### Solve
**Flag:** `pwn.college{QnGUufKJcQg5k6r49Ki-B9xo-L9.0FOxEzNxwSM1EzNzEzW}`

I just had to follow the instruction given to reach the flag.

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v "DECOY"
pwn.college{QnGUufKJcQg5k6r49Ki-B9xo-L9.0FOxEzNxwSM1EzNzEzW}
```

### New Learnings
Got to learn new arguments available in the grep function.
### References
-NA-


## Duplicating piped data with tee.

### Solve
**Flag:** `pwn.college{kGXanwSjdK8agwbzfa_tZoe7EeI.QXxITO0wSM1EzNzEzW}`

for this I first used the command and then mapped the output to a file and then the error gave me the correct syntax to use to obtain the flag.

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee output.txt | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output.txt
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "kGXanwSj"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret kGXanwSj | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{kGXanwSjdK8agwbzfa_tZoe7EeI.QXxITO0wSM1EzNzEzW}
```

### New Learnings
I learnt the function of tee and its usefullness in detecting errors.
### References
-NA-

## Process substitution for input

### Solve
**Flag:** `pwn.college{Qpc8i13pxIKnuptoV8eOJs4DQed.0lNwMDOxwSM1EzNzEzW}`

At first to find the flag Used various different commands like cat etc together with substituting the output but then at last I got it that I just needed to give the file paths as argument form the help section the command.

```bash
hacker@piping~process-substitution-for-input:~$ diff <( /challenge/print_decoys ) <( /challenge/print_decoys_and_flag )
70a71
> pwn.college{Qpc8i13pxIKnuptoV8eOJs4DQed.0lNwMDOxwSM1EzNzEzW}
```

### New Learnings
I got to learn how to directly compare the output of the command rather than storing each and every command in different files and then using those files.
### References
https://youtu.be/yBNPZISyuCg?si=FZrdaXJ-qle7GEfe \
https://youtu.be/dR0X0-B9ObA?si=7AR7juySGt3HYlt9

## Writing to multiple programs

### Solve
**Flag:** `pwn.college{8IvuIPsdyzt4wTsTQlvddGWymxO.QXwgDN1wSM1EzNzEzW}`

First i used the hack command to get the output then provided this output as an input to the "the" and "planet" commands using the "tee" function.

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/the < <(/challenge/hack | tee >( /challenge/planet ))
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{8IvuIPsdyzt4wTsTQlvddGWymxO.QXwgDN1wSM1EzNzEzW}
```

### New Learnings
I just learned how to duplicate 2 commands in linux using tee.
### References
-NA-

## Split-piping stderr and stdout

### Solve
**Flag:** `pwn.college{kzzEC8jRNftEX5f6jEzArjmT-X8.QXxQDM2wSM1EzNzEzW}`



```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 1> >( /challenge/planet ) 2> >( /challenge/the )
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{kzzEC8jRNftEX5f6jEzArjmT-X8.QXxQDM2wSM1EzNzEzW}
```

### New Learnings
-NA-
### References
-NA-

## Named Pipes 

### Solve
**Flag:** `pwn.college{Isu1IMl3i7GDy2LSu6Y99TAQo2z.01MzMDOxwSM1EzNzEzW}`

For this challenge i had to open 2 terminal in my laptop and run the code side by side to obtain the output of flag.

```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag-fifo
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{Isu1IMl3i7GDy2LSu6Y99TAQo2z.01MzMDOxwSM1EzNzEzW}
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
```

### New Learnings
Learnt about what is FIFO file and there working and use cases.
### References
-NA-

