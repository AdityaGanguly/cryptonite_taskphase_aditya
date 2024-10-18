# BECOMING ROOT WITH SU
### Command:
```
1)hacker@users~becoming-root-with-su:~$ su
Password:
2)root@users~becoming-root-with-su:/home/hacker# cat /flag
```
### Explanation:
Used the su command to become the root user. Upon using command 1 it asked for a password.
I entrered the given password 'hack-the-planet' and since it was correct it opened another shell where i was the root user to i used the cat /flag command and got the flag.
### Flag:
>pwn.college{cguE766TmHkummsw7xjb2pR-ik4.dVTN0UDL0cDM1czW}
# OTHER USERS WITH SU
### Command:
```
1)hacker@users~other-users-with-su:~$ su zardus
Password:
2)zardus@users~other-users-with-su:/home/hacker$ /challenge/run
output:
Congratulations, you have become Zardus! Here is your flag:
```
### Explanation:
Used the su command as seen in command 1 to switch th zardus user and entered the password 'dont-hack-me'.
The command was successful and now i was the zardus user.
Now i the /challenge/run program as seen in command 2 and got the flag. 
### Flag:
>pwn.college{kFgSnC9Ypr5BwZaLNa0m668GlkE.dZTN0UDL0cDM1czW}
