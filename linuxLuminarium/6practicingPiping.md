# Redirecting Output

### Use > to redirect output to a file

**Flag:** `pwn.college{0ju3PxbdKMshW3JLJlRCFqsdS0p.QX0YTN0wSN2EzNzEzW}`

## Process
Ran `echo PWN > COLLEGE` to get the flag.

## What I learnt
`>` can be used to redirect output to files

## References
No references used.


<br><br><br><br><br>


# Redirecting More Output

### Use > to redirect output to a file

**Flag:** `pwn.college{AZUn_BNDt-hX2pITq0IvMK8sgvm.QX1YTN0wSN2EzNzEzW}`

## Process
Ran `/challenge/run > myflag` and then `cat myflag` to get the flag.

## What I learnt
`>` can be used to redirect output from commands as well.

## References
No references used.



<br><br><br><br><br>


# Appending Output

### Redirect out to a file in append mode

**Flag:** `pwn.college{wAhP6PNM1LZN6bN3tWHYexWGSYX.QX3ATO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run >> ~/the-flag` and then ran `cat ~/the-flag` to get the flag.

## What I learnt
`>>` writes data to a file in append mode whereas `>` overwrites it.

## References
No references used.



<br><br><br><br><br>


# Redirecting Erros

### Use File Descriptors to redirect specific data streams

**Flag:** `pwn.college{MMl06-NHw-OcDzq2Ye47z6WAuwD.QX3YTN0wSN2EzNzEzW`

## Process
Ran `/challenge/run > myflag 2> instructions` and then ran `cat myflag` to get the flag.

## What I learnt
File descriptors can be used to direct different data streams:
  FD 0: Standard Input
  FD 1: Standard Output
  FD 2: Standard Error
This can be used by specifying the number before `>` to redirect the specfic stream. If no number is mentioned, Standard Output(FD 1) is redirected.

## References
No references used.



<br><br><br><br><br>


# Redirecting Input

### Use < to redirect input

**Flag:** `pwn.college{EzqgCrXGL2_O1EqC3WgM_LSuu0H.QXwcTN0wSN2EzNzEzW}`

## Process
Ran `echo COLLEGE > PWN` and then `/challenge/run < PWN`

## What I learnt
`<` can be used to redirect input to a command.

## References
No references used.



<br><br><br><br><br>


# Grepping Stored Results

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Greppinng Stored Results

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Grepping Live Output

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Grepping Errors

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Filtering With Grep -v

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Duplicating Piped Data with Tee

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Process Substitution for Input

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.


<br><br><br><br><br>


# Writing to Multiple Programs

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.


<br><br><br><br><br>


# Split-piping Stderr and Stdout

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br><br>


# Named Pipes

### Desc

**Flag:** ``

## Process


## What I learnt


## References
No references used.
