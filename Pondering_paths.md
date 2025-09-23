# Module: Pondering Paths

## The Root

### solve 
**Flag:** `pwn.college{IbDNciBCN0TNSkzIACU-5EdN0aq.QX4cTO0wSM1EzNzEzW}`

As the absolute path starts with "/" i.e the root symbol, I used it and then the name of the file.

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{IbDNciBCN0TNSkzIACU-5EdN0aq.QX4cTO0wSM1EzNzEzW}
```

### New Learning
I learned how the paths work in a system.

### Reference 
-NA-


## Programs and Absolute Paths

### solve 
**Flag:** `pwn.college{0VhDzD0m8e8oGPSO7n5HeoTcZyD.QX1QTN0wSM1EzNzEzW}`

To solve this first I needed to get into the challenge directory and then run the "run" file to obtain the flag. 

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{0VhDzD0m8e8oGPSO7n5HeoTcZyD.QX1QTN0wSM1EzNzEzW}
```

### New Learning 
We do not require to enter the directory and then execute the program we can do it directly using its absolute path.

### Reference
-NA-


## Position thy self

### Solve

**Flag:** `pwn.college{Ij_zR0nkRtoL1A_AKw7fn9Lregv.QX2QTN0wSM1EzNzEzW}`

For this challenge I had to run the command first so it gave an error adn directed me to the path i had to go into for running the code.
Then with "cd" function I entered the directory and executed the given command.


```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd  /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Ij_zR0nkRtoL1A_AKw7fn9Lregv.QX2QTN0wSM1EzNzEzW}
```

### New Learning 
-NA-

### Reference
-NA-


## Position Elsewhere

### Solve 
**Flag:** `pwn.college{Qk7UqlBtEKXx8_5MJKMpmnsOZuU.QX3QTN0wSM1EzNzEzW}`

This problem was similar to the one above this.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/bin
hacker@paths~position-elsewhere:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Qk7UqlBtEKXx8_5MJKMpmnsOZuU.QX3QTN0wSM1EzNzEzW}
```

### New Learning 
-NA-

### Reference
-NA-


## Position yet elsewhere

### Solve 
**Flag:** `pwn.college{0KjcMywDRckmM0nwswPfAt-7Nl0.QX4QTN0wSM1EzNzEzW}`

THis one was also pretty similar to the above 2 questions.

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/bin
hacker@paths~position-yet-elsewhere:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0KjcMywDRckmM0nwswPfAt-7Nl0.QX4QTN0wSM1EzNzEzW}
```

### New Learning 
-NA-

### Reference
-NA-


## Implicit relative paths, from /

### Solve

**Flag:** `pwn.college{MYD1fZsO-vst9gkcfOjSyimPcaz.QX5QTN0wSM1EzNzEzW}`

In this we needed to use the concept of relative path so first I jumped into the root directory using "cd" function then i used the relative path to obtain the flag.

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MYD1fZsO-vst9gkcfOjSyimPcaz.QX5QTN0wSM1EzNzEzW}
```

### New Learning
I got to learn the differnce between absolute and relative paths.

### Reference 
-NA-


## Explicit Relative paths, from /

### Solve
**Flag:** `pwn.college{gU9DrieH0a6wyjOXbaugTb5PCP9.QXwUTN0wSM1EzNzEzW}`

For this question we needed to enter the root directory and then use the "." operator to get the flag.

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gU9DrieH0a6wyjOXbaugTb5PCP9.QXwUTN0wSM1EzNzEzW}
```

### New Learnings
Function of "." and ".." operators.
### References 
-NA-


## Implicit Relative Paths

### Solve
**Flag:** `pwn.college{EopPGGJyvZf2uTs3YdM1q218vwW.QXxUTN0wSM1EzNzEzW}`

For this I entered the challenge directory then used the relative paths concept to run the "run" file and got the flag.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EopPGGJyvZf2uTs3YdM1q218vwW.QXxUTN0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Home Sweet Home

### Solve
**Flag:** `pwn.college{4IXlVA0caC4jTisWzqLl0ETuMBv.QXzMDO0wSM1EzNzEzW}`

I just gave a random file name in place of the argument section to execute the program. 

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{4IXlVA0caC4jTisWzqLl0ETuMBv.QXzMDO0wSM1EzNzEzW}
```

### New Learnings
U can access some function in some other directory without entering the directory with the help of absolute path.
### References 
-NA-