# THE PATH VARIABLE
### Command:
```
1)hacker@path~the-path-variable:~$ PATH=""
2)hacker@path~the-path-variable:~$ /challenge/run
Output:
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
```
### Explanation:
There is a special shell variable, called PATH, that stores a bunch of directory paths in which the shell will search for programs corresponding to commands.

As seen in command 1 i blanked out this PATH variable so that /challenge/run woud'nt be able to use the rm command.
So i used command 2 to run /challenge/run and since the rm command is gone, it coudnt delete the flag and gave it to me.
### Flag:
>pwn.college{YHvU8RKhIYTZ3rnL-KDnmidl1_U.dZzNwUDL0cDM1czW}
# SETTING PATH
### Command:
```
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
```
### Explanation:
In this challenge /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH

So I used command 1 and added the /challenge/more_commands/ directory to the PATH variable as it contained the win command needed by /challenge/run.
Then i used command 2 to invoked the win command and got the flag
### Flag:
>pwn.college{AU_kR0MqdkgpiSv5OUlDl7AP1u0.dVzNyUDL0cDM1czW}
# ADDING COMMANDS
### Command:
```
1)hacker@path~adding-commands:~$ touch win
2)hacker@path~adding-commands:~$ PATH=$PATH:/home/hacker
3)hacker@path~adding-commands:~$ echo $PATH
Output:
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker
4)hacker@path~adding-commands:~$ ls /run/workspace/bin
5)hacker@path~adding-commands:~$ echo "cat /flag" > /home/hacker/win
6)hacker@path~adding-commands:~$ ls -l win
7rw-r--r-- 1 hacker hacker 0 Oct 19 17:10 win
8)hacker@path~adding-commands:~$ chmod a+x win
9)hacker@path~adding-commands:~$ ls -l win
Output:
-rwxr-xr-x 1 hacker hacker 10 Oct 19 17:14 win
10)hacker@path~adding-commands:~$ /challenge/run
```
### Explanation:
I used command 1 to create the win file.
I used command 2 to add the /home/hacker directory to the PATH variable.
I used command 3 to see what directories are present in the PATH variable and from command 4 found that cat is in /run/workspace/bin.
Used command 5 to put the cat /flag command in win.
Used chmod to make win executable as seen in command 8.
Used command 10 and got the flag.
### Flag:
>pwn.college{w3mLxFjE7vTeAHUk2eOkoM_lBbO.dZzNyUDL0cDM1czW}
# HIJACKING COMMANDS
### Command:
```
1)hacker@path~hijacking-commands:~$ touch rm
2)hacker@path~hijacking-commands:~$ echo "cat /flag" > rm
3)hacker@path~hijacking-commands:~$ echo cat /flag > rm
4)hacker@path~hijacking-commands:~$ PATH=/home/hacker:$PATH
5)hacker@path~hijacking-commands:~$ echo $PATH
Output:
/home/hacker:/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
6)hacker@path~hijacking-commands:~$ ls -l rm
Output
-rw-r--r-- 1 hacker hacker 10 Oct 19 19:14 rm
7)hacker@path~hijacking-commands:~$ chmod a+rwx rm
8)hacker@path~hijacking-commands:~$ ls -l rm
-rwxrwxrwx 1 hacker hacker 10 Oct 19 19:14 rm
9)hacker@path~hijacking-commands:~$ /challenge/run
Output:
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{E_ts2LiTIE-HIhQI2dbhU0ULORz.ddzNyUDL0cDM1czW}
```
### Explanation:
### Flag:
>pwn.college{E_ts2LiTIE-HIhQI2dbhU0ULORz.ddzNyUDL0cDM1czW}
