# LISTING PROCESSES
### Command:
```
1)hacker@processes~listing-processes:~$ ps aux
2)hacker@processes~listing-processes:~$ /challenge/13077-run-15055
```
### Explanation:
I used the ps aux command to list all the running processes to search for /challenge/run which was also running(but renamed).
After going through all the running processes i saw a program named /challenge/13077-run-15055 that was running.
So i used command 2 and it gave me the flag.
### Flag:
>pwn.college{Y2E3mc8KzL9v86HnLX4Z6WZayT8.dhzM4QDL0cDM1czW}
# KILLING PROCESSES
### Command:
```
1)hacker@processes~killing-processes:~$ ps aux
2)hacker@processes~killing-processes:~$ kill 73
3)hacker@processes~killing-processes:~$ /challenge/run
```
### Explanation:
I used the ps aux command to see all the running processes to find the PID for the /challenge/dont_run process( which is 73).
Then i used the kill command as seen in command 2 to kill the dont_run process in order to run the /challenge/run process.
Finally i used command 3 and got the flag.
### Flag:
>pwn.college{0i9VT2Q7S_ZpMEvHAyE8wDhFvcX.dJDN4QDL0cDM1czW}
# INTERUPPTING PROCESSES
### Command:
```
hacker@processes~interrupting-processes:~$ /challenge/run
Output:
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
Output after ctrl+c:
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{Q12f9TKbo3oY0bpuPZHSkkfDQOi.dNDN4QDL0cDM1czW}
```
### Explanation:
Used the /challenge/run command to check whether it needs to be interrupted or not. Then i used ctrl+c to interuppt this process allowing it to cleanly exit which gave me the flag.
### Flag:
>pwn.college{Q12f9TKbo3oY0bpuPZHSkkfDQOi.dNDN4QDL0cDM1czW}
# SUSPENDING PROCESSES
### Command:
```
1)hacker@processes~suspending-processes:~$ /challenge/run
Output:
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 18:10 pts/0    00:00:00 bash /challenge/run
root          84      82  0 18:10 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
2)hacker@processes~suspending-processes:~$ /challenge/run
Output:
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 18:10 pts/0    00:00:00 bash /challenge/run
root          89      65  0 18:11 pts/0    00:00:00 bash /challenge/run
root          91      89  0 18:11 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
```
### Explanation:
Used the /challenge/run command to see what output it gives and from there i saw that there's only one program running.
As per the challenge i had to make a copy of the run program so i suspended it by using ctrl+z and launched another copy while the first one is suspended which gave me the flag.
### Flag:
>pwn.college{4Y8Lg6J8i_zv5PXmNJAA9XlxJh_.dVDN4QDL0cDM1czW}
# RESUMING PROCESSES
### Command:
```
1)hacker@processes~resuming-processes:~$ /challenge/run
Output:
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
2)hacker@processes~resuming-processes:~$ fg
```
### Explanation:
Used command 1 to try to run /challenge/run program and then pressed ctrl+z to suspend it.
Then i used the fg command to resume the /challenge/run program which gave me the flag
### Flag:
>pwn.college{AHXTx9lfQj9jGn4SNO7oLGhBMqj.dZDN4QDL0cDM1czW}
# BACKGROUNDING PROCESSES
### Command:
```
1)hacker@processes~backgrounding-processes:~$ /challenge/run
2)hacker@processes~backgrounding-processes:~$ bg
3)hacker@processes~backgrounding-processes:~$ /challenge/run
```
### Explanation:
I used command 1 to try to run the /challenge/run program but it failed since another copy wasnt running.
Then i used ctrl+z to suspend the process and then used the bg command to send it to the background.
Now /challenge/run was running in the background so i launched another copy of it in the terminal and received the flag.
### Flag:
>pwn.college{sMh8ysep1f_D8FDBsNsEAOR9Jhv.ddDN4QDL0cDM1czW}
# FOREGROUNDING PROCESSES
### Command:
```
1)hacker@processes~foregrounding-processes:~$ /challenge/run
2)hacker@processes~foregrounding-processes:~$ bg
3)hacker@processes~foregrounding-processes:~$ fg
Output:
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!
```
### Explanation:
Used command 1 to try running the /challenge/run program which gave an output containing the necessary instructions for the challenge.
As per the instructions firstly i suspended the process by pressing ctrl+z and then used the bg command to resume it in the background.
Then i used the fg command to resume it in the foreground which gave me an output to press 'enter' to receive the flag.
I pressed enter and got the flag. 
### Flag:
>pwn.college{YwMq8nQaaLVEweHWlncOmwKX_sn.dhDN4QDL0cDM1czW}
# STARTING BACKGROUND PROCESSES
### Command:
```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
```
### Explanation:
I used the above command to run the /challenge/run process in the backgroung without suspendind it using ctrl+z which gave me the output that the process has successfully started in the background and gave me the flag.
### Flag:
>pwn.college{IN7XxAntXfoeca0fn7Vwrhrym3Y.dlDN4QDL0cDM1czW}
# PROCESS EXIT CODES
### Command:
```
1)hacker@processes~process-exit-codes:~$ /challenge/get-code
Output:
Exiting with an error code!
2)hacker@processes~process-exit-codes:~$ echo $?
Output:
87
3)hacker@processes~process-exit-codes:~$ /challenge/submit-code 87
```
### Explanation:
Used the /challenge/get-code command which gave me an output that the process exited with an error code.
Then in used command 2 to get the value of the error code from the ? variable which gave me the value 87.
Then i used the command 3 and gave 87 as an argument to /challenge/submit-code which gave me the flag.
### Flag:
>pwn.college{ceFwN95002CSaSyLiNSFQzt_pgf.dljN4UDL0cDM1czW}
