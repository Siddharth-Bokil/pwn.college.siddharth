# The PATH Variable

### Change the PATH variable

**Flag:** `pwn.college{U9SPVfNUuEoN7ymHSwbRsaa3ggW.QX2cDM1wSN2EzNzEzW}`

## Process
Ran `PATH=""` and then `/challenge/run` to get the flag.

## What I learnt
The `PATH` variable is what makes the builtin commands run properly. if this variable is changed, the commands are searched for in the new path and are thus not found.

## References
No references used.



<br><br<br><br><br>




### Setting PATH

**Flag:** `pwn.college{oMjQqoNo6pM4ZXnYtpreiWLbvXA.QX1cjM1wSN2EzNzEzW}`

## Process
Ran `PATH=/challenge/more_commands/` to change the path and then ran `/challenge/run` to get the flag.

## What I learnt
The PATH variable can be used to access directory-specfic programs in an easier way.

## References
No references used.



<br><br><br><br><br>




### Finding Commands

**Flag:** `pwn.college{I4lBPRRR35GFHik0YQfWAzpVsVs.01NzEzNxwSN2EzNzEzW}`

## Process
Ran `which win` to find the path of the win command. Then ran `cat /challenge/paths/31140/flag` to get the flag.

## What I learnt
The `which commandName` command looks at each directory in the PATH variable in order and prints the first file it finds whose name matches the command name.

## References
No references used.



<br><br<br><br><br>




### Adding Commands

**Flag:** `pwn.college{oLDnyEwTKk1dkWriZ1A8dvfqW-o.QX2cjM1wSN2EzNzEzW}`

## Process
Ran `nano win` and entered
```
#!/bin/bash

cat /flag
```
Then I ran `chmod ugo+x ./win` and then `echo $PATH` to copy the currents directories.
Then, I ran `PATH="/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker"` as win was in /home/hacker. Finally, `/challenge/run` gave me the flag.

## What I learnt
PATH stores a collection of directories and new directories can be added to it. 

## References
No references used.



<br><br><br><br><br>



### Hijacking Commands

**Flag:** `pwn.college{IJY2EXWoTNUkXSMSlkzXI8ofvHR.QX3cjM1wSN2EzNzEzW}`

## Process
Inspected the /challenge/run command by running `cat /challenge/run` to realise I had to replicate the rm command.
Ran `nano rm` and wrote
```                                
#!/bin/bash

/run/dojo/bin/cat /flag
```
Gave the required permissions by running `chmod ugo+x rm` and changed the PATH variable as `PATH="/home/hacker/"` and then ran `/challenge/run` to get the flag.

## What I learnt
Catting a program can be of great use in understanding what it does without running it.

## References
No references used.
