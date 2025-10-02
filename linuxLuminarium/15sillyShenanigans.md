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



<br><br><br><br><br>




# Overshared Directories

### Rewrite a file in an opened up directory


**Flag:** `pwn.college{gK-rwkpnIfR2Hxd2J_wvqRMDtOi.0FM0EzNxwSN2EzNzEzW}`

## Process
Ran `rm /home/zardus/.bashrc` and then `nano /home/zardus/.bashrc` and wrote the previous code into the file. Then, on running `/challenge/victim` I got the flag.

## What I learnt
Files can be accessed if in an opened up directory.

## References
No references used.



<br><br><br><br><br>



# Tricky Linking

### Make a symlink to a file to get the flag


**Flag:** `pwn.college{M_u0IvXnGpPUjB3lWAA8TnlhiIJ.0VM0EzNxwSN2EzNzEzW}`

## Process
Ran `rm /tmp/collab/evil-commands.txt` and then `ln -s /home/zardus/.bashrc /tmp/collab/evil-commands.txt` to create the symbolic link. Ran `nano /home/zardus/.bashrc` and then ran `/challenge/victim` twice to get the flag.

## What I learnt
Anything in .bashrc is ran as the root and is therefore allowed. So making a sym link to .bashrc is a great idea.

## References
No references used.



<br><br><br><br><br>



# Sniffing Process Arguments

### 

**Flag:** `pwn.college{0iGLkNiAjRiYgwfLnA3yXGo5biF.0FOzEzNxwSN2EzNzEzW}`

## Process
Ran `ps aux` to see arguments passed to the automation script. Ran `su zardus` and entered the password when prompted to login as zardus and then ran `sudo cat /flag` to get the flag.

## What I learnt
`ps aux` does not show the whole output in a minimized window.

## References
No references used.



<br><br><br><br<br>




# Snooping on Configuratiins

### Read .bashrc to find a key

**Flag:** `pwn.college{Y2JpXi2Spf9JBu3AuZ6nl8k_kRF.0lM0EzNxwSN2EzNzEzW}`

## Process
Ran `cat /home/zardus/.bashrc` to read the api key and then ran `flag_getter --key sk-2640723931` to get the flag,

## What I learnt
.bashrc is world-readable by default.

## References
No references used.
