# CHANGING FILE OWNWESHIP
### Command:
```
1)hacker@permissions~changing-file-ownership:~$ ls -l /flag
output:
-r-------- 1 root root 58 Oct 16 14:51 /flag
2)hacker@permissions~changing-file-ownership:~$ chown hacker /flag
3)hacker@permissions~changing-file-ownership:~$ ls -l /flag
output:
-r-------- 1 hacker root 58 Oct 16 14:51 /flag
4)hacker@permissions~changing-file-ownership:~$ cat /flag
```
### Explanation:
Firstlt i used command 1 to check the ownership of the /flag file and found out that its owned by the root user.
Then i used the chown command as seen in command 2 and changed the ownership of the file to the hacker user.
Then i again used ls -l /flag command to check whether i successfully changed the user to hacker so i used the cat /flag command to display the contents of the /flag fine and got the flag.
### Flag:
>pwn.college{MI9TQNC3vyTISC4atY1XLEd41Rl.dFTM2QDL0cDM1czW}
