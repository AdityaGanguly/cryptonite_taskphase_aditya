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
