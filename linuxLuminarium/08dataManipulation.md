# Translating Characters

### Use `tr` to switch character cases

**Flag:** `pwn.college{U82nc494YLC54nuZggyhzubgjCS.01MxEzNxwSN2EzNzEzW}`

## Process
Ran `challenge/run | tr abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz` to get the flag.

## What I learnt
`tr` can be used to replace characters and uses a one-to-one mapping to do so.

## References
No references used.



<br><br><br><br><br>



# Deleting Characters

### Use `tr` to delete specific characters

**Flag:** `pwn.college{UnXFaIQ07bwrxwmEBSgJjLliWoU.0FNxEzNxwSN2EzNzEzW}`

## Process
Ran ` /challenge/run | tr -d ^%` to get the flag.

## What I learnt
The `-d` flag in `tr` can be used to remove characters as `input | tr -d charToRemove`

## References
No references used.



<br><br><br><br><br>



# Deleting Newlines

### Use `tr` to delete newline characters 

**Flag:** `pwn.college{cs6RfJ3QPX0OP9HhbAk9XwxR_G-.0VNxEzNxwSN2EzNzEzW}`

## Process
Ran `/challenge/run | tr -d "\n"` to get the flag.

## What I learnt
`"\n"` can be used to mention newline character to `tr` command.

## References
No references used.



<br><br><br><br><br>



# Extracting the First Lines With Head

### Use `head` to extract specfic content

**Flag:** `pwn.college{gr7vFpvAJjEZ_dt-6MVLpSoeS4C.0lNxEzNxwSN2EzNzEzW}`

## Process
Ran ` /challenge/pwn | head -n 7 | /challenge/college` to get the flag.

## What I learnt
`head` can be used to extract the first few lines of any file. It takes the argument `-n` as the number of initial lines to extract. `input | head -n 7` extracts the first 7 lines of given input.

## References
No references used.



<br><br><br><br><br>



# Extracting Specfic Sections of Text

### Use `cut` to select specific data

**Flag:** `pwn.college{IQPgnb7viV3Eoit6j29a-G8PIJB.01NxEzNxwSN2EzNzEzW}`

## Process
Ran `echo $(/challenge/run)` to find the format of the input and then ran ` /challenge/run | cut -d ' ' -f2,4,6,8,10,12,14,16,18,20 | tr -d "\n"` to get the flag.

## What I learnt
`cut` takes `-d 'delimiter'` to get the input seperated and then `-fnum1,num2,num3..` to keep the columns num1,num2,num3.

## References
https://www.gnu.org/software/coreutils/manual/html_node/cut-invocation.html#cut-invocation
chatGPT conversation



<br><br><br><br><br>



# Sorting Data

### Use `sort` to get the flag

**Flag:** `pwn.college{4-Uhxf_bas1T2uuw2ORJ9XjmUnW.0FM0MDOxwSN2EzNzEzW}`

## Process
Ran `sort /challenge/flags.txt` and got the flag at the end.

## What I learnt
`sort` orders output alphabetically by default. 
Takes arguments-
  -r : Reverse alphabetical order
  -n : Numeric sort (for numbers)
  -u : Unique lines only (removes duplicates)
  -R : Random order

## References
No references used.
