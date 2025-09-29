# Becoming Root With su

### Use `su` to become root

**Flag:** `pwn.college{83s4rZ0ijqwNK0jyV3hohrJM93g.QX1UDN1wSN2EzNzEzW}`

## Process
Ran `su` and entered the password as "hack-the-planet". Then, ran `ls /` to find a flag file in `/` and read the flag using `cat /flag`.

## What I learnt
`su` is the older way of becoming root. It is obsolete since it asks for a root password.

## References
No references used.



<br><br><br><br><br>



# Other Users With su

### Use su to become other users

**Flag:** `pwn.college{Q--KnbHUn1jH03-T8Bq56aI4KZ3.QX2UDN1wSN2EzNzEzW}`

## Process
Ran `su zardus` and then authenticated with the password "dont-hack-me". Then I obtained the flag by running `/challenge/run`

## What I learnt
`su` by default makes you the root, but it can take an argument of the particular user's name whom you want to switch to.

## References
No references used.



<br><br><br><br><br>



# Cracking Passwords

### Use john-the-ripper to crack hashed passwords

**Flag:** `pwn.college{wQb7PU2Foz05XnntgbmlXn8vcHP.QX3UDN1wSN2EzNzEzW}`

## Process
Ran `john /challenge/shadow-leak` to get the password for zardus as "aardvark". Ran `su zardus` and authenticated with that password. Then I ran `challenge/run` to get the flag.

## What I learnt
`john fileToDecrypt` can be used to obtain original text from one-way hashed files.

## References
No references used.



<br><br><br><br><br>



# Using sudo

### Use sudo

**Flag:** `pwn.college{c2yOD5KXyrlHNP3yCKdaUfLkcpq.QX4UDN1wSN2EzNzEzW}`

## Process
Ran `sudo cat /flag` to get the flag.

## What I learnt
`sudo` can be prepended to any command to gain access to executing the command as the root, without any passwords.

## References
No references used.
