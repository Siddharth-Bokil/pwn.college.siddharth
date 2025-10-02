# Chaining With Semicolons

### Chain commands using `:`

**Flag:** `pwn.college{Il_W6bIw4krZnwgSLB6fyAzxO6O.QX1UDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/pwn; /challenge/college` to get the flag.

## What I learnt
Commands can be chained, executed one after the other using `;`.

## References
No references used.



<br><br><br><br><br>



# Building On Success

### Chain commands using `&&`

**Flag:** `pwn.college{o8be0lHYP7_K3GZdFOIpY-baQDT.0lM0MDOxwSN2EzNzEzW}`

## Process
Ran `/challenge/first-success && /challenge/second` to get the flag.

## What I learnt
`&&` can be used to chain commands given that the first one succeds.
`command1 && command2` means if command1 succeeds, then execute command2.

## References
No references used.



<br><br><br><br><br>



# Handling Failure

### Chain commands using `||`

**Flag:** `pwn.college{8CJJV-RbGHRsjnEXjd87fII9uBs.01M0MDOxwSN2EzNzEzW}`


## Process
Ran `/challenge/first-success && /challenge/second` to get the flag.

## What I learnt
`||` runs a command if the first one fails.
`command1 || command2` means if command1 fails, execute command2.

## References
No references used.



<br><br><br><br><br>



# Your First Shell Script

### Make a shell script

**Flag:** `pwn.college{gmf5of8Py_YRL-1rXR88DUWn9_-.QXxcDO0wSN2EzNzEzW}`

## Process
Ran `nano x.sh` to create and edit the shell script. Wrote
```
/challenge/pwn
/challenge/college
```
in the script and then ran it using `bash x.sh` to get the flag.

## What I learnt
Shell scripts can be used to execute a bunch of commands for a common purpose. They have the extension of `.sh` and are ran using `bash fileName.sh`

## References
No references used.



<br><br><br><br><br>



# Redirecting Script Output

### (title)

**Flag:** `pwn.college{MPfVVkUUhM5Hio24en396ql_6NY.QX4ETO0wSN2EzNzEzW}`

## Process
Ran `bash x.sh | /challenge/solve` to get the flag. Since x.sh still had the same data, there was no need to change it.

## What I learnt
The output of a shell script can be redirected the same way of any command using piping methods.

## References
No references used.



<br><br><br><br><br>



# Executable Shell Scripts

### Make a shell script an executable

**Flag:** `pwn.college{05udjlZj9z6u6F3j3Anj8yBfdxS.QX0cjM1wSN2EzNzEzW}`

## Process
Ran `nano x.sh` to edit the shell script. Wrote `/challenge/solve` to the file. Made it exeecutable by running `chmod u+x x.sh` and then got the flag by running `./x.sh`

## What I learnt
Shell scripts can be ran without invoking bash by making them executable.

## References
No references used.



<br><br><br><br><br>



# Understanding Shebangs

### Add #! to a file to identify it as a shell script

**Flag:** `pwn.college{YbC753spXdrEgQ3gvxi-ZKKTMAc.0VOzMDOxwSN2EzNzEzW}`

## Process
Ran `nano solve.sh` in the /home/hacker directory. Wrote
```
#!/bin/bash
echo "hack the planet"
```
in the shell script and made it executable by running `chmod a+x ./solve.sh` and then ran `/challenge/run` to get the flag.

## What I learnt
`#!` is called a shebang. `#1/bin.bash` is for bash scripts. It is appended in the beginning to tell that it is to be run as a shell script as the extensions is not looked at.

## References
No references used.



<br><br><br><br><br>



# Scripting With Arguments

### Reverse arguments given to a shell script

**Flag:** `pwn.college{0LNwBgwvN8ZAqSWmSSbyLyM05FK.0VNzMDOxwSN2EzNzEzW}`

## Process
Ran `nano solve.sh` and wrote `echo "$2 $1"` to reverse the arguments.
Then ran `/challenge/run` to get the flag.

## What I learnt
The first argument can be accessed by `$1` second by `$2` and so on inside the shell script.

## References
No references used.



<br><br><br><br><br>



# Scripting With Conditionals

### Use if conditions in the shell script

**Flag:** `pwn.college{8xMQtJuiRcL8Utbc8cgw9zAP6UE.0lNzMDOxwSN2EzNzEzW}`

## Process
Ran `nano solve.sh` to edit the script. Wrote 
```
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
fi
```
Then ran `/challenge/run` to get the flag.

## What I learnt
Conditions can be applied to shell scripts using if statements but the syntax is more strict.
Syntax:
  ```
  if [ cond ]
  then
    codeToRun
  fi
  ```
All spaces must be just as they are.

## References
No references used.



<br><br><br><br><br>



# Scripting With Default Cases

### Use else condition in shell script

**Flag:** `pwn.college{QvyHAqc7Rck4PqQ_tHgpRqKT-ID.01NzMDOxwSN2EzNzEzW}`

## Process
Ran `nano solve.sh` to edit the script. Wrote
```                             
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
else
        echo "nope"
fi
```
Then ran `/challenge/run` to get the flag.

## What I learnt
else conditions can be used in shell scripts. They do not have a "then" statement.

## References
No references used.



<br><br><br><br><br>



# Scripting With Multiple Conditions

### Use if, elif and else conditions

**Flag:** `pwn.college{Qir0w1KBdP8dy6zTXeQ1h8yRlZg.0FOzMDOxwSN2EzNzEzW}`

## Process
Ran `nano solve.sh` to edit the shell script. Wrote
```
#!/bin/bash

if [ "$1" == "pwn" ]
then
        echo "college"
elif [ "$1" == "hack" ]
then
        echo "the planet"
elif [ "$1" == "learn" ]
then
        echo "linux"
else
        echo "unknown"
fi
```
and then ran `/challenge/run` to get the flag.

## What I learnt
elif conditions can be applied to bash scripts. They have a "then statement" just as if did.

## References
No references used.



<br><br><br><br><br>



# Reading Shell Scripts

### Read `challenge/run`

**Flag:** `pwn.college{s2vw9a1Qt9J-gGZ059Fnq_4LDve.0lMwgDOxwSN2EzNzEzW}`


## Process
Ran `cat /challenge/run` to read the challenge file and found the password. Then ran the file, `/challenge/run` and gave the password as "hack the PLANET" to get the flag.

## What I learnt
All challenges in this module are implemented as shell scripts and can be catted out.

## References
No references used.
