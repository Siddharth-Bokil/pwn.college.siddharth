# Changing File Ownership 

## Use `chown` to change file ownership

**Flag:** `pwn.college{4lFmvHZi4O-s4ne3W4V2Oco-p_Y.QXxEjN0wSN2EzNzEzW}`

## Process
Ran `chown hacker /flag` to make myself the owner. Then I ran `cat /flag` to get the flag.

## What I learnt
`chown` can be used to change ownership of a file.
Syntax: `chown newOwner fileName`

## References
No references used.



<br><br><br><br><br>



# Groups and Files 

## Desc

**Flag:** `pwn.college{EGM7KRLrUhcNJOyULrrjWJJaEhU.QXxcjM1wSN2EzNzEzW}`

## Process
Ran `chgrp hacker /flag` and then ran `cat /flag` to get the flag.

## What I learnt
`chgrp` can be used to change the group of a file. This is important because in most cases permissions are controlled on a group basis.
Syntax: `chgrp newGroup fileName`

## References
No references used.



<br><br><br><br><br>



# Fun With Groups Names 

## Find and chnage the group of a file

**Flag:** `pwn.college{0V9IfE4UD1xLQWBWUPnL0kU48sR.QXycjM1wSN2EzNzEzW}`

## Process
Ran `chgrp grp15397 /flag` and then `cat /flag` to obtain the flag. 

## What I learnt
`ls -al` can be used to see the permissions, owner. and group of files. The current users group can be seen by running `id`

## References
No references used.



<br><br><br><br><br>



# Changing Permissions 

## Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Execultable Files 

## Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Permission Tweaking Practice 

## Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Permissions Setting Practice 

## Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# The SUID Bit 

## Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.
