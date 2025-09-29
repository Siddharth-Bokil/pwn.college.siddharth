# Listing Processes

### Use `ps` along with arguments to list processes

**Flag:** `pwn.college{Ak-SIpp8Cj3MdVDuKetBSRaIC_Q.QX4MDO0wSN2EzNzEzW}`

## Process
Ran `ps aux` to know the running command. Ran `/challenge/14210-run-21903` to get the flag.

## What I learnt
`ps` is used to list process. By default it prints the processes running in the terminal. It can take many arguments, some are:
  `ps -e` : Every process
  `ps -f` : Full format
  `ps -ef` : Every process in full format
  `ps aux` : a - all users, u - user readable, x - not in terminal.
  

## References
No references used.



<br><br><br><br><br>



# Killing Processes

### Use `kill` to kill processes

**Flag:** `pwn.college{YNkMfXwE8DLBEesLyp7RtnpWu1o.QXyQDO0wSN2EzNzEzW}`

## Process
Ran `ps aux | grep dont_run` which gave me the PID as 316 and then ran `kill 136` followed by `/challenge/run` which gave me the flag.

## What I learnt
`kill` can be used to stop processes from running. It takes the PID of the process.

## References
No references used.



<br><br><br><br><br>



# Interrupting Processes

### Desc

**Flag:** `pwn.college{sB5g_O4IJr7_KVKGzeoGjfQHst0.QXzQDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run` and then hit ctrl+c to get the flag.

## What I learnt
Ctrl + C can be used to stop a process clogging the terminal.

## References
No references used.



<br><br><br><br><br>



# Killing Misbehaving processes

### Kill interruptive processes

**Flag:** `pwn.college{0p3CY9kEnn2-d1KjPvROnxKYEZQ.0FNzMDOxwSN2EzNzEzW}`

## Process
Ran `ps aux`, then ran `kill 142`. After this, `/challenge/run` followed by `cat /tmp/flag_fifo` gave me the flag.

## What I learnt
`kill` can be used to stop processes based on their PID's.

## References
No references used.



<br><br><br><br><br>



# Suspending processes

### Suspend a process using ctrl+z

**Flag:** `pwn.college{Q4SEOVf0i8twjJrDzkPd6mMIKll.QX1QDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run` and then hit Ctrl+Z. Ran `/challenge/run` again to get the flag.

## What I learnt
Ctrl+Z can be used to suspend programs.

## References
No references used.



<br><br><br><br><br>



# Resuming Processes

### Resume processes using the `fg` command

**Flag:** `pwn.college{IcwKXduuTBWnx2mOWQcS2sOIhy_.QX2QDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run` and then suspended it by pressing Ctrl+Z. After that I resumed it by running the `fg` command.

## What I learnt
`fg` command brings back suspended processes.

## References
No references used.



<br><br><br><br><br>





# Backgrounding Processes

### Desc

**Flag:** `pwn.college{sNeUUy_SkgmpfdVWXTnEhN98k6y.QX3QDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run`, then suspended it by pressing Ctrl+Z. After this I background-ed it by running `bg` and then ran it again to get the flag.

## What I learnt
`bg` can be used to rerun a suspended task.

## References
No references used.



<br><br><br><br><br>



# Foregrounding Processes

### Use `fg` to itneract with a backgrounded process

**Flag:** `pwn.college{Q0O1FHx_uC1PE9kAS3m8UiSFv8J.QX4QDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run` followed by `bg`. Then I ran `fg` and hit Enter to get the flag.

## What I learnt
`fg` can be used to further interact with a backgrounded process.

## References
No references used.



<br><br><br><br><br>



# Starting Backgrounded Processes

### Start a process in the background

**Flag:** `pwn.college{sM3yjufKRwnTOGpJmjPRiH68Lhk.QX5QDO0wSN2EzNzEzW}`

## Process
Ran `/challenge/run &` to get the flag.

## What I learnt
Appending an `&` to a command automatically starts it in the background.

## References
No references used.



<br><br><br><br><br>



# Process Exit Codes

### Desc

**Flag:** `pwn.college{ItCU4N4iJxCpTjbsbXidO4avZmb.QX5YDO1wSN2EzNzEzW}`

## Process
Ran `/challenge/get-code`. For its exit code, I ran `echo $?` to get it as 137. Then, `challenge/submit-code 137` gave me the flag.

## What I learnt
The exit code of the last executed command is stored in the `?` variable. It can be accessed by running `echo $?`.
`?` :
  Holds 0 for successful programs
  Holds most commonly 1 or specific error codes for incorrectly ran programs.

## References
No references used.
