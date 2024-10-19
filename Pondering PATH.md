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

As seen in command 1 i blanked out this PATH variable so that /challenge/run woud'nt be able to search for the rm command.
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
