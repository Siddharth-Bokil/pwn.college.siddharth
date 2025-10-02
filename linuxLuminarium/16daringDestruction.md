# The Fork Bomb

## Make a process call itself over and over again

**Flag:** `pwn.college{UmGmL9Xr59ercjn6rvmQMa3S6dL.0VMyEzNxwSN2EzNzEzW}`


## Process
In the first window, I ran `/challenge/check` and in the other I ran nano `script.sh` and wrote
```
#!/bin/bash
echo helloWorld!
ls -al /
ls -al ~
./script.sh &
./script.sh
```
Then I ran `./script.sh` to eventually get the flag in the first window.


## What I learnt
It works, but it takes a lot of time and patience.

## References
No references used.



<br><br><br><br><br>



# Disk-Space Doomsday

## Clog up the disk space 

**Flag:** `pwn.college{QrdVCd1NWm03M6NzNorjYZb9UoE.0lMyEzNxwSN2EzNzEzW}`


## Process
Ran
```
touch clog.txt
yes > clog.txt
/challenge/check
rm clog.txt
/challenge/check
```
to get the flag.

## What I learnt


## References
No references used.



<br><br><br><br><br>



# rm -rf /

## Remove everything

**Flag:** `pwn.college{MAvo2j0OuUIjMZZcl6yK3oROdJL.0lMzEzNxwSN2EzNzEzW}`


## Process
Ran `/challenge/check` and then in another window, ran `rm -rf / --no-preserve-root` to get the flag.

## What I learnt
`rm -rf /` is used to remove everything in a system.
rm - remove
-r - recursively
-f - forcefully
/ - root directory

## References
No references used.



<br><br><br><br><br>



# Life after rm -rf /

## Reading without cat

**Flag:** `pwn.college{caOrLmFnrij3gfT5wKMHpeYrdwD.01MzEzNxwSN2EzNzEzW}`


## Process
Ran `/challenge/check` on the first window. On the other window I ran
```
rm -rf /
read flag < /flag
$flag
```
and got the flag.

## What I learnt
Since read is a builtin, it still works after `rm -rf /`.

## References
No references used.



<br><br><br><br><br>



# Finding meaning after rm -rf /

## Listing files without ls

**Flag:** `pwn.college{AsO8ai5JuA5rF_FWtsPc89Ofv08.0FNzEzNxwSN2EzNzEzW}`


## Process
Ran `challege/check` in the first teminal, in the second terminal I ran
```
rm -rf / --no-preserve-root
cd /
echo *
read flag < d4c356fd
$flag
```
to obtain the final flag.

## What I learnt
echo and cd are also builtin commands.

## References
No references used.
