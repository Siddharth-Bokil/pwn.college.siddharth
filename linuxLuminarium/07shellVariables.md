# Printing Variables

### Print a shell variable

**Flag:** `pwn.college{suOvaOsBeUahBjYRAQtIGEhTh_i.QX3UTN0wSN2EzNzEzW}`

## Process
Ran `echo $FLAG` to get the flag.

## What I learnt
Variables can be printed out with echo by appending a `$` before the variable name.

## References
No references used.


<br><br><br><br><br>


# Setting Variables

### Assign a value to a variable

**Flag:** `pwn.college{8yvHU1P5G74hhYub3h31NS-iOeG.QX5UTN0wSN2EzNzEzW}`

## Process
Ran `PWN=COLLEGE` to get the flag.

## What I learnt
Variable names and values are case sensitive. No spaces should be used while assigning variable values. `$` is only used to access the value of a variable.

## References
No references used.


<br><br><br><br><br>


# Multi-Word Variables

### Assign a multi-word value to a variable

**Flag:** `pwn.college{AlZhfcKstqA0gfFSQ0CPF0Xaynp.QXwYTN0wSN2EzNzEzW}`

## Process
Ran `PWN="COLLEGE YEAH` to get the flag.

## What I learnt
Double quotes can be used to set a variable to a multi word value.

## References
No references used.


<br><br><br><br><br>


# Exporting Variables

### Export the value of a variable

**Flag:** `pwn.college{MpI1AXPZADFqxky8TiFqKhbuUoe.QXyYTN0wSN2EzNzEzW}`

## Process
Ran
```
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run
```
to get the flag.

## What I learnt
Shell variables must be exported before they are used by commands or other child shells. They cna also be set and exported in the same line by `export var=value`

## References
No references used.


<br><br><br><br><br>


# Printing Exported Variables

### Use `env` to print exported variables

**Flag:** `FLAG=pwn.college{QaEhgwzLpSECh8g34d-pXzRGu-V.QX4UTN0wSN2EzNzEzW}`

## Process
Ran `env | grep FLAG` to get the flag.

## What I learnt
`env` prints out all the variables that have been exported along with their values.

## References
No references used.


<br><br><br><br><br>


# Storing Command Output

### Store the output of a command into a variable

**Flag:** `pwn.college{sdBsQy_D3Ij6xUUHyz0lbCuE0kC.QX1cDN1wSN2EzNzEzW}`

## Process
Ran `PWN=$(/challenge/run)` and then `echo $PWN` to get the flag.

## What I learnt
`var=$(command)` can be used to store the output of a command in a shell variable.

## References
No references used.


<br><br><br><br><br>


# Reading Input

### Store input from the user using the `read` command

**Flag:** `pwn.college{gX7TBfpdtNYS9jGW_e0IYtD6mEI.QX4cTN0wSN2EzNzEzW}`

## Process
Ran `read -p "Enter: " PWN` to get the flag.

## What I learnt
`read` command can be used to take input from the user. `-p` flag can be used to provide text as a prompt to get input from the user.

## References
No references used.


<br><br><br><br><br>


# Reading Files

### Store input from a file using `read` command

**Flag:** `pwn.college{0kH5PFkfVFWEGE1zR4LsVAif9bI.QXwIDO0wSN2EzNzEzW}`

## Process
Ran `read PWN < /challenge/read_me` to redirect the output of `/challenge/read_me` as input to `PWN` and then got the flag.

## What I learnt
`<` redirection can also be used to provide input to the read command.

## References
No references used.
