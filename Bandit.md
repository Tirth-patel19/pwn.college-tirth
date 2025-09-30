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


