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
# CRACKING PASSWORDS:
### Command:
```
1)hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Output:
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04921g/s 286.5p/s 286.5c/s 286.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
2)hacker@users~cracking-passwords:~$ su zardus
Password:
3)zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
```
### Explanation:
In this challenge the leak of /etc/shadow was in /challenge/shadow-leak.
I used john the ripper to crack the password of zardus as seen in commad 1 and it gave me his password in the output.
Now i used the su command and typed the password as seen in command 2 and became zardus, successfully hacking in.
Once in i used /challenge/run to get the flag as seen in command 3.
### Flag:
>pwn.college{oDVwTfQG6bKO7ZxVBsOUwmtePDg.ddTN0UDL0cDM1czW}
# USING SUDO
### Command:
```
1)hacker@users~using-sudo:~$ cat /flag
cat: /flag: Permission denied
2)hacker@users~using-sudo:~$ sudo cat /flag
```
### Explanation:
In this challenge we use sudo instead of su to get the flag.
Initially i used cat /flag command just to see what output im getting and it shows permission denied which means i will have to use sudo to get the flag as it will give me allow me to run this command as the root user.
So in command 2 i used sudo to run the same command and got the flag.
### Flag:
>pwn.college{4O4aFncYqK3embn553bPSdqLSwc.dhTN0UDL0cDM1czW}
