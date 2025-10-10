# Level 13

### Login as bandit14 to cat the password

**Password:** `MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS`

## Process
Ran
```
ls
ssh -i sshkey.private -p 2220 bandit14@localhost
cat /etc/bandit_pass/bandit14
```
and got the password.

## What I Learnt
`ssh` takes the `-i` flag to provide the key seperately.

## References
-