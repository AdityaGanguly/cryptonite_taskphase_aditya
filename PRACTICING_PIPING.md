# REDIRECTING OUTPUT
### Command:
```
1)
2)hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
```
### Explanation:
I created the COLLEGE file in the home directory.
Then i Redirected the input 'PWN' to the file COLLEGE by using the command and successfully obtaining the flag.
### flag:
>pwn.college{ccaccDMe6LbIwYvexg0g0gspqKR.dRjN1QDL0cDM1czW}
# REDIRECTING MORE OUTPUT
### Command:
```
1)hacker@piping~redirecting-more-output:~$ touch myflag
2)hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
3)hacker@piping~redirecting-more-output:~$ cat myflag
```
### Explanation:
Firstly i created the myflag file as the output of /challenge/run command has to be redirected to it.
Then i used command 2 to redirect the output of /challenge/run to the myflag file and got the the output that it has been successfully redirected.
Finally i used cat myflag command to view the contents of myflag file which displayed the flag.
### flag:
>pwn.college{EG1Acb9-NICe8fB6UiSeyX-ov8w.dVjN1QDL0cDM1czW}
# APPENDING OUTPUT
### Command:
```
1)hacker@piping~appending-output:~$ touch the-flag
2)hacker@piping~appending-output:~$ /challenge/run >> the-flag
3)hacker@piping~appending-output:~$ cat the-flag
```
### Explanation:
I created the the-flag file usint the touch command.
Then i used command 2 to append the second part of the flag to the first part by using the append mode.
Command 3 is now displays the entire flag as both parts have been appended.

### flag:
>pwn.college{AzD38zats8kv6fYZGhJV2m2EbeQ.ddDM5QDL0cDM1czW}
# REDIRECTING OUTPUT
### Command:
```
1)hacker@piping~redirecting-errors:~$ touch myflag
2)hacker@piping~redirecting-errors:~$ touch instructions
3)hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
4)hacker@piping~redirecting-errors:~$ cat instructions
5)hacker@piping~redirecting-errors:~$ cat myflag
```
### Explanation:
Created the myflag and instructions files using the touvh command.
Used command 3 to redirect the flag to the myflag file and the errors(instructions in this case) to the instructions file.
Used the cat command to view whether the instructions and flag got copied to their respective files, the cat myflag command gave the flag.
### flag:
>pwn.college{w5r69XrgnmY2YFE_ALLpEPk9UHh.ddjN1QDL0cDM1czW}
# REDIRECTING INPUT
### Command:
```
1)hacker@piping~redirecting-input:~$ touch PWN
2)hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
3)hacker@piping~redirecting-input:~$ /challenge/run < PWN
```
### Explanation:
Firstly i used the touvh command to create the PWN file
Used command 2 to redirect 'COLLEGE' to the PWN file
Used command 3 to redirect the input of PWN file to /challege/run which displayed the flag.
### flag:
>pwn.college{ACcFz-vJQ-hta0eX6BZDsqfMc2-.dBzN1QDL0cDM1czW}
