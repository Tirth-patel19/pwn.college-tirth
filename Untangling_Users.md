# Module Name

## Becoming root with su

### Solve
**Flag:** `pwn.college{cNdglAA7jPwy4qqqBqF9zy3VQGa.QX1UDN1wSM1EzNzEzW}`

TO clear this challenge I first had to open the root shell using the "su" command and provide the password once in i had to read the flag file using the cat command to obtain the flag.

```bash
hacker@users~becoming-root-with-su:~$ su 
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{cNdglAA7jPwy4qqqBqF9zy3VQGa.QX1UDN1wSM1EzNzEzW}
```

### New Learnings
I learnt what is root, how to access, difference between "su" and "sudo".
### References 
-NA-


## Other user with su

### Solve
**Flag:** `pwn.college{QhfDGUFKsjWskHUfjLRBqIXMp_V.QX2UDN1wSM1EzNzEzW}`

For this challenge I first logged in as zardus and then had to run the command to obtain the flag.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{QhfDGUFKsjWskHUfjLRBqIXMp_V.QX2UDN1wSM1EzNzEzW}
```

### New Learnings
We can use su not just to enter as root but also to enter as other user.
### References 
-NA-


## Cracking password.

### Solve
**Flag:** `pwn.college{UQwLrO8YRupYNHHesa-jHzfMVe1.QX3UDN1wSM1EzNzEzW}`

At first i had trouble understanding the syntax and logic of how to use John the ripper then after referring to the documentation and some youtube tutorial i got the logic and gave the file name as the argumnet to the command "john" and received the password for the zardus user and then i entered it and run the command.

```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04914g/s 286.1p/s 286.1c/s 286.1C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{UQwLrO8YRupYNHHesa-jHzfMVe1.QX3UDN1wSM1EzNzEzW}
```

### New Learnings
I learnt about John the ripper and how to use it.
### References 
https://www.openwall.com/john/ \
https://youtu.be/rioBjLN4FyY?si=sXovnRo8k0lsAjuB 


## Using sudo

### Solve
**Flag:** `pwn.college{sdJBzWMSJ4dywFTGEsvWs7DeutV.QX4UDN1wSM1EzNzEzW}`

To complete this challenge I needed to run the cat command as a root user to obtain the flag.


```bash
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{sdJBzWMSJ4dywFTGEsvWs7DeutV.QX4UDN1wSM1EzNzEzW}
```

### New Learnings
I learnt that sudo is different from su because sudo allows you to run commands as root user rather actually making u the root user.
### References 
-NA-