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

## Use `chgrp` to change file group

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
Ran `chgrp grp27192 /flag` and then `cat /flag` to obtain the flag. 

## What I learnt
`ls -al` can be used to see the permissions, owner. and group of files. The current users group can be seen by running `id`

## References
No references used.



<br><br><br><br><br>



# Changing Permissions 

## Use `chmod` to change permissions of a file

**Flag:** `pwn.college{wSxbhJMyJGrz-ngWT0K5mAXCNzZ.QXzcjM1wSN2EzNzEzW}`

## Process
Ran `chmod o+r /flag` to change file permissions, and then ran `cat /flag` to get the flag.

## What I learnt
`chmod` can be used to change file permissions.
It has the following syntax:
  `chmod owner(u)/group(g)/others(o)/all(a) addPerm(+)/removePerm(-) read(r)/write(w)/execute(x)`

## References
No references used.



<br><br><br><br><br>



# Execultable Files 

## Use `chmod` to make a file executable

**Flag:** `pwn.college{MfLMJF572rn-puf12Y8i7yADQ7h.QXyEjN0wSN2EzNzEzW}`

## Process
Ran `ls -l /challenge` to see that the file was in the hacker group and user. Ran `chmod u+x /challenge/run` to give myself permissions, then `/challenge/run` gave me the flag.

## What I learnt
Sometimes the file might be owned by you, so you must change permissions for the user.

## References
No references used.



<br><br><br><br><br>


# Permission Tweaking Practice 

## Practice using `chmod`

**Flag:** `pwn.college{4nz6wDn31Ly3TMJFe-9Vftvw2vu.QXwEjN0wSN2EzNzEzW}`

## Process
Ran
```
/challenge/run
chmod o+w /challenge/pwn
chmod u+x /challenge/pwn
chmod u-rx,g-r /challenge/pwn
chmod g+rw /challenge/pwn
chmod u-w /challenge/pwn
chmod u+w /challenge/pwn
chmod g+x /challenge/pwn
chmod uo-w /challenge/pwn
chmod ugo+r /flag
cat /flag
```
to complete all 8 levels and get the flag.

## What I learnt
To change permissions of 2 categories, they must be sepereated by ",".

## References
No references used.



<br><br><br><br><br>



# Permissions Setting Practice 

## Practice using `chmod`

**Flag:** `pwn.college{k4NRy5TDU9KCrjk2ztM7qyzSAE-.QXzETO0wSN2EzNzEzW}`

## Process
Ran
```
/challenge/run
chmod u-rw,g+wx,o=w /challenge/pwn
chmod u=w,g-x,o=rx /challenge/pwn
chmod u=rx,g=x,o=x /challenge/pwn
chmod u=-,g=rwx,o=- /challenge/pwn
chmod u=rx,g=w,o=wx /challenge/pwn
chmod u=wx,g=rwx,o=rwx /challenge/pwn
chmod u+r,g=r,o-x /challenge/pwn
chmod u-x,o+x /challenge/pwn
chmod a=r /flag
cat /flag
```
to complete all 8 levels and obtain the flag.

## What I learnt
`chmod category=perm fileName` can be used to overwrite the old permission with the new ones.
`chmod cateogry=- fileName` can be used to remove all permissions of that category.

## References
No references used.



<br><br><br><br><br>



# The SUID Bit 

## Desc

**Flag:** ``

## Process
Ran `chmod u+s /challenge/getroot` to set SUID bit. Ran `/challenge/getroot` to get access to the root shell and then ran `cat /flag` as root to get the flag.

## What I learnt
The SUID bit allows any user to run a certain file as the root. The bit comes in place of the executable permission. `chmod u+s fileName`

## References
No references used.
