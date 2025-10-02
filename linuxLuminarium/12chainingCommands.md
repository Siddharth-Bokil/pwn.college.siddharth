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

### Desc

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

### Desc

**Flag:** `pwn.college{MPfVVkUUhM5Hio24en396ql_6NY.QX4ETO0wSN2EzNzEzW}`

## Process
Ran `bash x.sh | /challenge/solve` to get the flag. Since x.sh still had the same data, there was no need to change it.

## What I learnt
The output of a shell script can be redirected the same way of any command using piping methods.

## References
No references used.



<br><br><br><br><br>



# Executable Shell Scripts

### Desc

**Flag:** `pwn.college{05udjlZj9z6u6F3j3Anj8yBfdxS.QX0cjM1wSN2EzNzEzW}`

## Process
Ran `nano x.sh` to edit the shell script. Wrote `/challenge/solve` to the file. Made it exeecutable by running `chmod u+x x.sh` and then got the flag by running `./x.sh`

## What I learnt
Shell scripts can be ran without invoking bash by making them executable.

## References
No references used.



<br><br><br><br><br>



# Understanding Shebangs

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Scripting With Arguments

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Scripting With Conditionals

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Scripting With Default Cases

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Scripting With Default Cases

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Scripting With Multiple Conditions

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>



# Reading Shell Scripts

### Desc

**Flag:** ``


## Process


## What I learnt


## References
No references used.
