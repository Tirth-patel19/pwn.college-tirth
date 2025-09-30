# Data Manipulation

## Translating charecters

### Solve
**Flag:** `pwn.college{ID0qHwYkM1KGeGgyymQYHxBPdae.01MxEzNxwSM1EzNzEzW}`

First i tried to write all the alphabets in upper and then in lowercase but it didn't work then i referred to some tutorial online regarding the use of "tr" command and found the way to give the argument in proper order.

```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'a-zA-Z' 'A-Za-z'
yOUR CASE-SWAPPED FLAG:
pwn.college{ID0qHwYkM1KGeGgyymQYHxBPdae.01MxEzNxwSM1EzNzEzW}
```

### New Learnings
I learnt how to translate alphabets in shell using "tr" command also variou type of inputs it can accept.
### References
https://youtu.be/gv-WsgXvhPQ?si=Dd6mC62qmjGvsSlQ \
https://youtu.be/iNWdEWWYo50?si=JzIF4KdERPFg_bzG \
https://youtu.be/fxJ1dS9fd04?si=xuS2ZUoS0D-9qQQn


## Deleting Charecter

### Solve
**Flag:** `pwn.college{kN7yjEJe9-a6RFSfm1ILngfdeLA.0FNxEzNxwSM1EzNzEzW}`

This was pretty straight forwad I just had to use the -d flag and give the charecter to delete as an argument.

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{kN7yjEJe9-a6RFSfm1ILngfdeLA.0FNxEzNxwSM1EzNzEzW}
```

### New Learning 
I learnt how to delete charecter from a file using the tr command.
### Reference
-NA


## Deleting Newlines

### Solve
**Flag:** `pwn.college{8uFGAO7aqDYOndBZmsB1DOloM5a.0VNxEzNxwSM1EzNzEzW}`

For this challenge the logic was similar to last question in the question the argument was changed to "\n".

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{8uFGAO7aqDYOndBZmsB1DOloM5a.0VNxEzNxwSM1EzNzEzW}
```

### New Learning 
-NA-
### Reference
-NA-


## Extracting the first lines with head

### Solve
**Flag:** `pwn.college{0uJwr6XIAww7mjIlYzOCnOUi5W2.0lNxEzNxwSM1EzNzEzW}`

For this challenge I had to use piping tool twice first for the head then i used it to sent it to college file to obtain my flag.

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{0uJwr6XIAww7mjIlYzOCnOUi5W2.0lNxEzNxwSM1EzNzEzW}
```

### New Learning 
-NA
### Reference
-NA-

## Extracting Specific section of text

### Solve
**Flag:** `pwn.college{w8HoTzQpNS622OZzKMDNYtkIbI5.01NxEzNxwSM1EzNzEzW}`

At first to solve this problem i struggeled to understand the location of the flag column then i got it was the "2nd" column then i gave 2 as the argument to "-f" to receive the output.

```bash
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{w8HoTzQpNS622OZzKMDNYtkIbI5.01NxEzNxwSM1EzNzEzW}
```

### New Learning 
How to segregate/cut the ouput using the command(cut) and column number.
### Reference
-NA-

## Sorting data

### Solve
**Flag:** ``

For this question I just needed to sort the files alphabetically and use the last flag as the real flag to complete the challenge.

```bash
hacker@data~sorting-data:~$ sort /challenge/flags.txt
ovm.boklegd{Q08X0aN6fM4TvWLRoDG4R2XcaZ_.0EM0MDNxwSM0EzNyEzV}
ovn.bolldge{P07W0aN6gN5TwWMQnDG3Q3XdaY_.0EM0LDNwvRM1DzNzEzW}
ovn.cnklege{P08W0aO5gN5UwWMRnDH4R3YcaZ_.0FM0MDOxwRM1EzNyEzW}
ovn.colkege{Q07X0aO6gN4UvWMRnCH4Q3XcaZ_.0FM0LCNxwSL0EzNyDyV}
ovn.college{P08X0aO6fN4UwWLRnDH4Q2YdaZ_.0FM0MDOxvRM1DzMzEzW}
owm.cnllege{P07X0aN6gN4UvVMQoDH3R2YdaZ_.0EM0MDNwwSL1EzNzDyV}
owm.cnllege{Q08W0aO6fN4UwWLRoCH4Q3YdaZ_.0EL0MCNxwSM0DzNzDzW}
owm.coklefe{Q08X0aN5gM5UvWMRoDH4Q3YdaZ_.0FL0MCOxwSL1EzNzEzW}
owm.collegd{Q07X0aO5fM5UvVMRnDH3R2YcaY_.0EL0MCOwwSM1EzNzDyV}
owm.collegd{Q08X0aO6fN5UwWLRoDH4R3XdaZ_.0FL0MDOxwSM1EzNzEzW}
owm.college{Q08X0aO6gN4UwWMRoDH4R3YdaZ_.0FM0MDOxvSM1EzNzEzW}
own.boklefd{P08W0aO5gN5UwWMRnDH3Q3XdaZ_.0FM0MDOwvSL1EzMzDzV}
own.bolkege{Q08X0aO6gN5UwWMQoDH4R3YcaZ_.0FM0MDOxwSM1EzNzEzW}
own.bollegd{Q07X0aO6gN4UwWMRoCH4R3XcaY_.0FM0MDOxwSL1EzNzDyW}
own.bollege{P08X0aO6fN4TwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzDzW}
own.cnlldfd{Q08W0aO6fN5UvWMRoDH3R3XdaZ_.0FM0MDNxwSM0DzNzEzW}
own.coklegd{Q07X0aO5fN4UwVLRoDH3R3XdaZ_.0FM0MDOwvRM1EzNzDzW}
own.coklege{P08X0aN6gN5UwVMQoDH4R3YcaZ_.0FM0LCOxwRM0EzNzEzW}
own.coklege{Q08X0aN6gN5UwWLRoDH4R3YcaZ_.0EM0LDOwwRL1EyNzEzW}
own.colkdge{P08X0aO5fN5UwWMRoDH3R3YdaY_.0EM0MCOxwSM0EyMzEzW}
own.colldge{Q07X0aO6gN5UwWMRoDG4R2YdaY_.0EM0MCOxwRM1DyMzEzV}
own.colldge{Q08W0aN5gM5UwWMQoDH4R2YdaZ_.0FM0MDOxwSM1EzMzEzW}
own.colldge{Q08X0aN5fN5TwWMQoCH4R3YdaZ_.0EL0MDOwvRM1EyNyEyW}
own.collegd{P08X0aO6fN4UvWMRoDH4Q2YdaZ_.0FM0LDOxvSL1EzNzDzW}
own.collegd{Q08X0aO6gN5UwVMRoDH4Q3YdaY_.0FM0MCOxwSM1EzNzEzW}
own.college{Q08X0aO6fN5UwVMRoDH4R3YdaZ_.0FM0MDOxwRL1EzNyEzW}
own.college{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOwwSM1EzNzEzW}
pvm.bolldge{Q07X0aO6fM5UvWMRoDG4Q3YdaY_.0EL0MDNxwRL1DzNzEzW}
pvm.cnlkdfe{P07W0aO6fN5TwWMRoDH4Q3XcaZ_.0FL0MDOwwRM1DyNyEzW}
pvm.cnllefe{P07X0aO5fN5TwWMQoDG4R3YcaZ_.0FM0MDNxwRL0EyNyEyW}
pvm.colldge{Q08W0aO6gN4UvVMRoCG4R3YdaZ_.0FM0MDOxwRM1DzNyEzW}
pvm.collegd{P08X0aO5fN4UwVMRoDH4R2XdaZ_.0EM0MDOxwSM1EzNyDzV}
pvm.collegd{Q07X0aO6gM5UwVLRnDH3R3XdaZ_.0FL0MDOwvSL1EzNzDzW}
pvn.boklegd{Q07W0aO6gM4TvWMRoDG4Q3YcaY_.0FL0MCOwvSL0EzNzEzW}
pvn.bollege{P08X0aO5gM5TwWLRoDH4R3YdaY_.0FL0MDOxvSM1EzMzEyW}
pvn.bollege{Q08X0aN6gN5UwWMRoDH4R3YdaZ_.0FM0MCOxwSM1EzNzEyW}
pvn.cnklefe{Q08X0aO6fN5UvWLQoDH4R2XdaZ_.0FL0MDOxwSM1EzMzEzW}
pvn.cnklege{Q07X0aN6gM5UvWLRoDH3Q3YdaZ_.0FM0MDNwwSM1EzNyDzW}
pvn.cnlkdge{Q07X0aO6gN4UwWMRoDH3R3YdaZ_.0FM0MCNxwRM1DyNzDzW}
pvn.cnlldfe{Q08X0aN6gN4UwWMQoCH4R2YdaY_.0FL0MDNwvSM1EzMzDzW}
pvn.cnllegd{Q07X0aO6gN4TwWMRnDG4R3XdaY_.0EL0LCNxwRL0EyMzDyW}
pvn.colkdfe{Q07X0aO6gN5UvWLQnCH4Q3YdaY_.0EL0MCOwvSL0EyNzEyW}
pvn.colkdge{Q07X0aO6gN5UvWMRnDG4R3YdaY_.0EM0MCOxwRL1EzNzEzW}
pvn.colkege{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzDzW}
pvn.colldgd{P07X0aO5gM5UwWMRoDG4Q3YdaY_.0FL0MDNwvRM1EyNyEzV}
pvn.collefe{Q07X0aO6gN4UwWMRoDH4Q3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pvn.collegd{Q08X0aO6gM4TvWMRoDG4Q2YdaZ_.0FM0MDNxwSM0EzNzDzW}
pvn.college{P08W0aN6gN5UwVMQoDG3R2YcaZ_.0FL0MDNxwSM1EzNzEyW}
pvn.college{P08X0aO6gM4UwWLRoDH4R3YdaY_.0FM0LDOwwRM1DzNzEzW}
pvn.college{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDNxwSM1EzNzEyW}
pwm.bnklege{P08X0aN6fM5UwVMRoDH4R3YdaY_.0EM0MDOwvRL1EyNzEzV}
pwm.bnllege{Q08X0aO6gN5UwWMRoCG4Q3YdaZ_.0FM0MDOxwRM1EzNzEzW}
pwm.bokkege{Q08X0aO6gN4UwWMRoDG4R3YdaZ_.0FL0MDOxwSM1EzMzEzW}
pwm.bolkdgd{Q08X0aO5fN5UwVMRoCH3Q2XcaZ_.0FL0MDOwwRM1EzNzEzW}
pwm.bolkege{Q07X0aO6gN4UwWMRnDH4Q2YdaZ_.0EL0MCOxwRM1DzNzEzW}
pwm.cnlldfe{P08W0aO5gN4TwVLRoDH4Q3YdaZ_.0FL0MCOwwRL1EyNzDyV}
pwm.cnlldge{P08X0aN6gM4UvVLQoDH4R3YdaZ_.0EM0LDOwwRM1DzMzEzW}
pwm.cnllegd{Q08X0aO5gN4UvVMRoDH4Q3YcaY_.0FM0MDNxwSM1DzMzDzV}
pwm.cokldgd{Q08X0aO5gN5UwWLRoDH4Q3YdaY_.0FM0MDOxwRM0DzNzDzW}
pwm.coklefe{Q08X0aO6gM4UvWMRoDG3R3YdaZ_.0FL0LCOxwRM1EzMzDyW}
pwm.coklege{Q08W0aN6gN5UwWMRnDH4R3YdaZ_.0FM0MDOxwSM1EzNyEzV}
pwn.bnklege{Q08X0aN6gN5UwWMRoCH4R2XcaZ_.0FL0MDOxvRL1EzNzEzW}
pwn.bolkegd{Q08X0aN6gN5UwWMRoCH3R2YdaZ_.0EL0MDNwvSM1DzNzEzW}
pwn.bolkege{Q08X0aO6gN4UwWMRoCH4R3YdaZ_.0FM0MCOwwSM0EzNzDyW}
pwn.bollege{Q08W0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOwwSM1EyNyEzW}
pwn.cnkldge{Q08X0aN6gN5UwWMRoDH4Q3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.cnlldfd{Q08X0aN5gN4UwWLRoDG4R3YdaZ_.0EM0MCNxwSL1EzMyDzW}
pwn.cnlldfe{Q08W0aO5gM5UwWMQnDG4Q3XcaZ_.0FM0MCOwvSM1DzNzEyV}
pwn.cnllefe{Q08W0aO5gN4TvWLQoDH4Q3YdaZ_.0FM0LCOwwSM1DzMzEzW}
pwn.cnllege{Q08W0aO6fN4TwWMRnDH4Q3YdaZ_.0EL0LDOxwSL1EzMzEzW}
pwn.cnllege{Q08X0aO5gM4UwWMRnDH4R2YdaY_.0FM0MDOxwSM0EzNzEzW}
pwn.cokkdge{Q08X0aO5gN5UwWLRoCH4R3XdaZ_.0FL0MDOxwSM1EzMzEzV}
pwn.cokkefe{Q08X0aN5fN5UvWMQnCG4R2XdaZ_.0EL0MDNxvSL1DzMzEzW}
pwn.coklegd{Q08W0aO5gN4UwWLQoCG4R3YcaZ_.0FM0MCOxwSM1EyNzEzV}
pwn.coklege{P08X0aN5fN5TvWLRoDH4R3XdaY_.0FM0MDOxwSM1DyNzEzW}
pwn.coklege{Q07X0aN6gN5UwVMRnDH3R2YdaZ_.0FM0LDOxwSM1EzNzDzW}
pwn.coklege{Q08X0aO6gN4UwWMQoDH4R3XdaZ_.0FM0MDOxwSL1EzMzEzW}
pwn.coklege{Q08X0aO6gN5UwWMQoDH4R3YcaZ_.0FM0MDOxwSM0EyNzEzV}
pwn.colkdfd{P07X0aO6gM5UwVLQoCH3R3XdaZ_.0FM0MDOxvSM1EyMzDzW}
pwn.colkefe{Q08W0aO6fN4TwWMQoDH4Q2XdaY_.0EM0MDNwvRL1EzMyEzV}
pwn.colkegd{P07X0aN5gN4TvWLRoDH3R3YcaY_.0FM0LDOwwRM1EyNzDzV}
pwn.colkege{Q08X0aO5gM5UwVMQoDH3R2YdaZ_.0EL0LDOwwSL1EzNzEyW}
pwn.colldge{P08W0aN6gM5UvWMRoDH4R3YcaZ_.0EL0MDOxwSL1DyMyEyW}
pwn.colldge{Q07W0aO5gN4UwVMQnDH4R2XdaY_.0FM0MDOxvRM1EyNzEzW}
pwn.collegd{P08X0aO6gN5UwWLRoDH4R3YdaZ_.0FM0MDOxwRM0EyNzEzW}
pwn.collegd{Q08X0aN6gN4UwWLRnDG4Q3XdaY_.0FM0MDOxvSM0EyMzEzW}
pwn.collegd{Q08X0aO6gM5UwWMRoDG4R3YdaY_.0FM0LDNxwSM1EyNyEzW}
pwn.college{P08X0aN5gN5UwWLRoCH4R2YdaZ_.0FM0MDOxwSM1DzMzEzW}
pwn.college{P08X0aO6gN5UwVMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.college{P08X0aO6gN5UwWMRoDH4R3YcaZ_.0FM0MDOxwSM1EzMzEzW}
pwn.college{Q07X0aN6gN5UwWMRoDH4R3XcaZ_.0FL0MCOxwSM1EzNzEyW}
pwn.college{Q07X0aO6gN4UwWMRoDG3R3XdaZ_.0FM0MDOxwSM1DyNzDzV}
pwn.college{Q08W0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.college{Q08X0aO5gN5UwWMQoCH3R3YdaZ_.0EM0MDOxwSL1DzNzEzW}
pwn.college{Q08X0aO6gN5UwVMRoCH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.college{Q08X0aO6gN5UwVMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.college{Q08X0aO6gN5UwWLRoDH4R3YdaZ_.0EM0MDOxwSM1EyNzEzW}
pwn.college{Q08X0aO6gN5UwWMRoDH3R3YdaZ_.0FM0MDOxwSL1EzNzEyW}
pwn.college{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzDzW}
pwn.college{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
pwn.college{Q08X0aO6gN5UwWMRoDH4R3YdaZ_.0FM0MDOxwSM1EzNzEzW}
```

### New Learning 
Learnt how to sort files in shell using sort command and also various different argument that can be passed to sort as per your wish.
### Reference
-NA-