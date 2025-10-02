# Launching Screen

### Launch screen

**Flag:** `pwn.college{MTkGALQ2QATw0TyQDTwmWU39zG-.0VN4IDOxwSN2EzNzEzW}`

## Process
Ran `screen` to get the flag.

## What I learnt
`screen` is a program used to create virtual terminals inside the current terminal.

## References
No references used.



<br><br><br><br><br>



# Detaching and Attaching

### Detach and rettach a screen session

**Flag:** `pwn.college{oS-VrysP3CLg9-G2Pp4qZVg1Xj7.0lN4IDOxwSN2EzNzEzW}`

## Process
Ran `screen` and then detached by pressing Ctrl-A followed by d. Then ran `/challenge/run` and then `screen -r` to reattach and get the flag.

## What I learnt
A screen session can be detached by pressing Ctrl-A followed by d and can be reattached by running `screen -r`

## References
No references used.



<br><br><br><br><br>



# Finding Sessions

### Find sessions in screen using `screen -ls`

**Flag:** `pwn.college{krZbXvHKXcGmibPAG0sUn1RtEjf.01N4IDOxwSN2EzNzEzW}`

## Process
Ran `screen -ls` to list all currently detached screen processes. Accesed each one by running `screen -r PID` and found the flag in one of the 3.

## What I learnt
Multiple detached screen sessions can be lsited out by running `screen -ls`

## References
No references used.



<br><br><br><br><br>



# Switching Windows

### Switch windows in screen

**Flag:** `pwn.college{AHEClhLm0ig6Nkpf6MXRwxN5NOV.0FO4IDOxwSN2EzNzEzW}`

## Process
Ran `screen -r` and then pressed Ctrl-A followed by p to go to winodw 0 and got the flag,

## What I learnt
There can be multiple windows within a screen sessions. They can be accessed by the following shortcuts. ALl the shortcuts start with Ctrl-A.
c - Create new window
n - Next window
p - Previous window
0-9 - Access windows 0,1,2,...,9
'' - Bring up a selection menu of all the windows

## References
No references used.



<br><br><br><br><br>



# Detaching and Attaching (tmux)

### Detach and rettach to a tmux session

**Flag:** `pwn.college{AIj_vC3yEtNaCO8iXo_w1F5UE3C.0VO4IDOxwSN2EzNzEzW}`

## Process
Ran `tmux` and then hit Ctrl-B follwed by d to detach. Ran `tmux a` to rettach and get the flag.

## What I learnt
tmux is an alternate to screen and uses Ctrl-B instead of Ctrl-A in place of the main shrotcut key. Some shorcuts also differ:
    `tmux ls` - List all sessions
    `tmux attach` or `tmux a` - Rettach to sessions

## References
No references used.



<br><br><br><br><br>



# Switching Windows (tmux)

### Switch windows in a tmux session

**Flag:** `pwn.college{wOc5WIBIuyYbGxWgl2SZLnpRiYr.0FM5IDOxwSN2EzNzEzW}`

## Process
Ran `tmux a` to reattach to the session and then hit Ctrl-B followed by p to get the flag.

## What I learnt
tmux has the same shortcuts as screen when it comes to switching windows. The only difference is the Ctrl-B instead of Ctrl-A.

## References
No references used.
