# Terminal multiplexing

## Launching screen

### Solve
**Flag:** `pwn.college{Yj1ThCItWjVXVx2vXIR7JhMI8Tb.0VN4IDOxwSM1EzNzEzW}`

In this i just had to type the screen command to receive the flag.

```bash
hacker@terminal-multiplexing~launching-screen:~$ screen
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{Yj1ThCItWjVXVx2vXIR7JhMI8Tb.0VN4IDOxwSM1EzNzEzW}
```

### New Learnings
I learnt we can mirror our existing terminal.
### References 
-NA-


## Deataching and attaching 

### Solve
**Flag:** `pwn.college{MQbp7iF8rrem3Zbu89bWz8U56v8.0lN4IDOxwSM1EzNzEzW}`

For this I had to run the screen command then detach the screen and the reattach it to find the flag.

```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 163.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 163.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{MQbp7iF8rrem3Zbu89bWz8U56v8.0lN4IDOxwSM1EzNzEzW}
Yes! Flag is: pwn.college{MQbp7iF8rrem3Zbu89bWz8U56v8.0lN4IDOxwSM1EzNzEzW}
Remove dead screens with 'screen -wipe'.
[screen is terminating]
```

### New Learnings
I learnt what is deattaching and reattaching
### References 
-NA-


## Finding Sessions

### Solve
**Flag:** `pwn.college{AyyMFh5au4JIbq_zajSMm9ikuxd.01N4IDOxwSM1EzNzEzW}`

For this i had to list all the sessions running using the "screen -ls" function then check each one of them to find the flag and I found the correct flag in the first screen itself.

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        173.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        162.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        144.session_52cc2dea0f931398    (Detached)
        147.session_da82f17d45a71902    (Detached)
        150.session_8bb52123845bdc6f    (Detached)
5 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_52cc2dea0f931398
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{AyyMFh5au4JIbq_zajSMm9ikuxd.01N4IDOxwSM1EzNzEzW}
pwn.college{AyyMFh5au4JIbq_zajSMm9ikuxd.01N4IDOxwSM1EzNzEzW}
```

### New Learnings
how to list multiple screen in the terminal.
### References 
-NA-


## Switching windows

### Solve
**Flag:** `pwn.college{siPePyh1Kmdsn9HwJFoSMwg3HkX.0FO4IDOxwSM1EzNzEzW}`

For this challenge I had to reattch the screen then use the ctrl A 0 to go to the 0th window where i found the flag.

```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -r
[screen is terminating]
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{siPePyh1Kmdsn9HwJFoSMwg3HkX.0FO4IDOxwSM1EzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{siPePyh1Kmdsn9HwJFoSMwg3HkX.0FO4IDOxwSM1EzNzEzW}
```

### New Learnings
i learnt about what are windows how to create them,delete them, jump to next or previous window etc.
### References 
-NA-


## Detaching and attaching(tmux)

### Solve
**Flag:** `pwn.college{UVyHLiwmeS1GclYZaE119n6UOCl.0VO4IDOxwSM1EzNzEzW}`

For this challenge instead of the "screen" function i had to use the "tmux" and "ctrl b" as the key combination to perform all the steps.

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{UVyHLiwmeS1GclYZaE119n6UOCl.0VO4IDOxwSM1EzNzEzW}
Congratulations, here is your flag: pwn.college{UVyHLiwmeS1GclYZaE119n6UOCl.0VO4IDOxwSM1EzNzEzW}
```

### New Learnings
i learnt about tmux which is similar to screen command.
### References 
-NA-


## Challenge Name

### Solve
**Flag:** `pwn.college{gHGkB73Vp2eBGyaWHmjDBx41z0x.0FM5IDOxwSM1EzNzEzW}`

For this challenge i entered the tmux windown then entered the windo0 and there with the help of arrow key i found the flag.

```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux
hacker@terminal-multiplexing~switching-windows-tmux:~$ Here is your flag: pwn.college{gHGkB73Vp2eBGyaWHmjDBx41z0x.0FM5IDOxwSM1EzNzEzW}
[detached (from session 1)]
```

### New Learnings
-NA-
### References 
-NA-