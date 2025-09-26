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

### Use grep to search in a stored result

**Flag:** `pwn.college{ISSXkuW9Xgud8gs42WYGFG3uAWP.QX4EDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run > /tmp/data.txt` and then `grep pwn  /tmp/data.txt` to obtain the flag.

## What I learnt
Syntax for grep: `grep searchText searchFile`

## References
No references used.



<br><br><br><br><br>



# Grepping Live Output

### Use `|` to grep live output

**Flag:** `pwn.college{4aDnsmf8Q01GPE9bBwKISHSvSsr.QX5EDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run | grep pwn` to get the flag.

## What I learnt
`|` can be used to redirect output of one command into input of other.

## References
No references used.



<br><br><br><br><br>


# Grepping Errors

### Use `>&` to convert data streams

**Flag:** `pwn.college{gYi0_-oEeDN0C4TV_yWHuYqbyra.QX1ATO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run 2>& 1 | grep pwn` to get the the flag.

## What I learnt
`>&` converts one data stream into another. In this case `2>& 1` converted the error stream into the output stream.

## References
No references used.



<br><br><br><br><br>


# Filtering With Grep -v

### Use `grep -v` to filter out decoys

**Flag:** `pwn.college{4GvjlI14vR4xgbtc4QIc1ncpLbB.0FOxEzNxwSN2EzNzEzW}`

## Process
Ran `/challenge/run | grep -v DECOY` to obtain the flag.

## What I learnt
`grep -v` to invert the output the grep. Instead of giving the matched statements, `grep -v` returns the unmatched statements.

## References
No references used.



<br><br><br><br><br>


# Duplicating Piped Data with Tee

### Use `tee` to debug command output

**Flag:** `pwn.college{whbOeGeUMJ3LDZZ1R9iUTorgSXp.QXxITO0wSN2EzNzEzW}`

## Process
Ran `/challenge/pwn | tee data | /challenge/college` and then ran `/challenge/pwn --secret whbOeGeU | /challenge/college` to get the flag.

## What I learnt
`tee` can be used with `|` to debug/intercept the input being sent to a comamnd.
Syntax:
  `command1 | tee debugFile | command2`

## References
No references used.



<br><br><br><br><br>


# Process Substitution for Input

### Use Process Substitution with diff

**Flag:** `pwn.college{UPd4qFSquUrgzWQu25j4bFUBIDw.0lNwMDOxwSN2EzNzEzW}`

## Process
Ran `diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)` to get the flag.

## What I learnt
`<(givenFile)` is a placeholder for the output of the file that is given to it.

## References
No references used.


<br><br><br><br><br>


# Writing to Multiple Programs

### Use `>()` to redirect input along with `tee`

**Flag:** `pwn.college{4gfnjANi2Sc1chLW-G4ENeA5A22.QXwgDN1wSN2EzNzEzW}`

## Process
Ran `/challenge/hack | tee >(/challenge/the) | /challenge/planet` to get the flag.
Initially I messed up the syntax of tee and thought it gives 2 files, but then I realised it takes one file and one command which solved the problem.

## What I learnt
While `<(command)` redirects output of given command, `>(command)` redirects input to given command.

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
