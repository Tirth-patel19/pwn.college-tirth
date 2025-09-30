# Module Name

## chaining~chaining-with-semicolons

### Solve
**Flag:** `pwn.college{IFahw_NUs77gUSKZsQ-1JnNpGa-.QX1UDO0wSM1EzNzEzW}`

In this i just had to type both the commands and seperate them by semicolon(;) to get the flag. 

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{IFahw_NUs77gUSKZsQ-1JnNpGa-.QX1UDO0wSM1EzNzEzW}
```

### New Learnings
I learnt we can enter multiiple commands together sepearted by semicolon to function normally.
### References 
-NA-


## chaining~building-on-success

### Solve
**Flag:** `pwn.college{Uhfir19DVTD2Q6-XZ6_ldXN-L-4.0lM0MDOxwSM1EzNzEzW}`

For this challenge We had to seperated the commands by && to obtain the flag.

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{Uhfir19DVTD2Q6-XZ6_ldXN-L-4.0lM0MDOxwSM1EzNzEzW}
```

### New Learnings
I learnt about the working of && operator.
### References 
-NA-


## chaining~handling-failure

### Solve
**Flag:** `pwn.college{QJeMyz4zAeohusPYR4Bg1qDXFDU.01M0MDOxwSM1EzNzEzW}`

For this we had to seperate both the commands by || operator to get the flag.

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{QJeMyz4zAeohusPYR4Bg1qDXFDU.01M0MDOxwSM1EzNzEzW}
```

### New Learnings
Function of the OR (||) operator.
### References 
-NA-


## Your first shell script

### Solve
**Flag:** `pwn.college{QLn4_uExSZS4vku8lzDOkEn9X7Z.QXxcDO0wSM1EzNzEzW}`

For this level i had to individually enter the command into the "x.sh" file and then bash the file to obtain the flag.

```bash
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn" > x.sh
echo "/challenge/college" >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{QLn4_uExSZS4vku8lzDOkEn9X7Z.QXxcDO0wSM1EzNzEzW}
```

### New Learnings
I learnt about how to run multiple function in one go using the .sh files in the terminal.
### References 
-NA-


## Redirecting script output 

### Solve
**Flag:** `pwn.college{UaQwNDMBVV1A_xYks23RO01S2FF.QX4ETO0wSM1EzNzEzW}`

For this challenge i stored both the command in the x.sh file and then redirected the output of the file into the /challenge/solve command to obtain the flag.

```bash
hacker@chaining~redirecting-script-output:~$ /challenge/pwn > x
hacker@chaining~redirecting-script-output:~$ /challenge/college >> x
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{UaQwNDMBVV1A_xYks23RO01S2FF.QX4ETO0wSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Executable shell scripts

### Solve
**Flag:** `pwn.college{YPolat7UQCLUvaHrz2k-033t5Bf.QX0cjM1wSM1EzNzEzW}`



```bash
hacker@chaining~executable-shell-scripts:~$
hacker@chaining~executable-shell-scripts:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~executable-shell-scripts:~$ echo '/challenge/solve' >> ~/solve.sh
hacker@chaining~executable-shell-scripts:~$ chmod a+x ~/solve.sh
hacker@chaining~executable-shell-scripts:~$ ./solve.sh
Congratulations on your shell script execution! Your flag:
pwn.college{YPolat7UQCLUvaHrz2k-033t5Bf.QX0cjM1wSM1EzNzEzW}
```

### New Learnings
I learnt how to invoke the schell scripted file without using the bash and only but including the shebang as the first line of the file.
### References 
-NA-


## Understanding Shebangs

### Solve
**Flag:** `Flag: pwn.college{IDN7yoI3K3OW1I9YK_iXnqACGvS.0VOzMDOxwSM1EzNzEzW}`

For this challenge i echoed the shebang first then the next line in ths shell scripted file and the ran the file to obtain the output and then run the /challenge/run output the receive the flag.

```bash
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~understanding-shebangs:~$ echo 'echo "hack the planet"' >> ~/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod a+x ~/solve.sh
hacker@chaining~understanding-shebangs:~$ ~/solve.sh
hack the planet
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{IDN7yoI3K3OW1I9YK_iXnqACGvS.0VOzMDOxwSM1EzNzEzW}
```

### New Learnings
i learnt about the "shebang" and its function.
### References 
-NA-


## Challenge Name

### Solve
**Flag:** `pwn.college{4M_KaJEYH-J0vKcFI6NI7pN043c.0VNzMDOxwSM1EzNzEzW}`

For this challenge i used the shebang first and the gave the index in reverse order for printing in the reverse order then run the scripted file and the /challenge/run function the get the flag.

```bash
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~scripting-with-arguments:~$ echo 'echo "$2 $1"' >> ~/solve.sh
hacker@chaining~scripting-with-arguments:~$ bash ~/solve.sh hello world
world hello
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{4M_KaJEYH-J0vKcFI6NI7pN043c.0VNzMDOxwSM1EzNzEzW}
```

### New Learnings
I learnt about the indexing of the scripted file when taking input from the user.
### References 
-NA-


## Scripting with conditionals

### Solve
**Flag:** `pwn.college{sqY1DRTrXz-OTzsK0geya8N2_aN.0lNzMDOxwSM1EzNzEzW}`

For this challenge i first entered the "shebang" into the file then whole if statement and the output of the code and then ran the scripted file with pwn input to receive college as output and then i ran the run command to obtain the flag.

```bash
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" = "pwn" ]' >> ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'then' >> ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo '  echo "college"' >> ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod a+x ~/solve.sh
hacker@chaining~scripting-with-conditionals:~$ bash ~/solve.sh pwn
college
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{sqY1DRTrXz-OTzsK0geya8N2_aN.0lNzMDOxwSM1EzNzEzW}
```

### New Learnings
I learnt about various test condition we can use in the linux from help test command.
### References 
-NA- 


## Scripting with default cases

### Solve
**Flag:** `pwn.college{0MRI7muUSeUs_B72U3evxs4Euzs.01NzMDOxwSM1EzNzEzW}`

This question was similar to above question only in this we had to use the else condtion and perform the steps to get output.

```bash
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'if [ "$1" == "pwn" ]' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'then' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '  echo "college"' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'else' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '  echo "nope"' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'fi' >> ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ chmod a+x ~/solve.sh
hacker@chaining~scripting-with-default-cases:~$ bash ~/solve.sh pwn
college
hacker@chaining~scripting-with-default-cases:~$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{0MRI7muUSeUs_B72U3evxs4Euzs.01NzMDOxwSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Scripting with multiple conditions

### Solve
**Flag:** `pwn.college{whC4uTp88Pof-P99kyyCEYJS56T.0FOzMDOxwSM1EzNzEzW}`

This was also the extension of the above question in this we used the elseif condition to check multiple different outputs.

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ echo '#!/bin/bash' > ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'if [ "$1" = "hack" ]' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '  echo "the planet"' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'elif [ "$1" = "pwn" ]' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '  echo "college"' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'elif [ "$1" = "learn" ]' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'then' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '  echo "linux"' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'else' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo '  echo "unknown"' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'fi' >> ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ chmod a+x ~/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ bash ~/solve.sh hack
the planet
hacker@chaining~scripting-with-multiple-conditions:~$ bash ~/solve.sh pwn
college
hacker@chaining~scripting-with-multiple-conditions:~$ bash ~/solve.sh learn
linux
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{whC4uTp88Pof-P99kyyCEYJS56T.0FOzMDOxwSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-


## Reading shell Scripts

### Solve
**Flag:** `pwn.college{gZYwxfAfJW7D3rTkCgOm_1Xoqbl.0lMwgDOxwSM1EzNzEzW}`

In the problem after reding the file I noticed that the program was comparing the input string with the "hack the PLANET" and if it was true it printed the flag from there I understood the password was "hack the PLANET" and thus obtained the flag.

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
        echo "CORRECT! Your flag:"
        cat /flag
else
        echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{gZYwxfAfJW7D3rTkCgOm_1Xoqbl.0lMwgDOxwSM1EzNzEzW}
```

### New Learnings
-NA-
### References 
-NA-