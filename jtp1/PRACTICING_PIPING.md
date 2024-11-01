# REDIRECTING OUTPUT
### Command:
```
1)hacker@piping~redirecting-output:~$ touch COLLEGE
2)hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
```
### Explanation:
I created the COLLEGE file in the home directory.
Then i Redirected the input 'PWN' to the file COLLEGE by using command 2 successfully obtaining the flag.
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
Firstly i used the touvh command to create the PWN file.
Used command 2 to redirect 'COLLEGE' to the PWN file.
Used command 3 to redirect the input of PWN file to /challege/run which displayed the flag.
### flag:
>pwn.college{ACcFz-vJQ-hta0eX6BZDsqfMc2-.dBzN1QDL0cDM1czW}
# GREPPING STORED RESULTS
### Command:
```
1)hacker@piping~grepping-stored-results:~$ touch /tmp/data.txt
2)hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
3)hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
```
### Explanation:
Used the touch command to create the file data.txt in /tmp directory.
Then used command 2 to redirect the output of /challenge/run to data.txt.
Since there are too many lines of text in data.txt we use the grep command to display the line that contains the flag(The flags start with pwn.college which is unique).
### flag:
>pwn.college{0BzjHCgJhHxxBucn_VqlZCsyKOy.dhTM4QDL0cDM1czW}
# GREPPING LIVE OUTPUT
### Command:
```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
```
### Explanation:
Used the pipe operator, the standard output of the command was on the left of the pipe and the input command was on the right of the pipe.
The grep command which was on the right side of the pipe searched in the output of /challenge/run for lines that began with pwn.college and displayed it thus giving the flag.
### flag:
>pwn.college{4Lgw86L_jak0j-vwmo7aAQP3gwJ.dlTM4QDL0cDM1czW}
# GREPPING ERRORS
### Command:
```
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
```
### Explanation:
Similar to the previous question,Using the pipe operator i kept the standard output of /challenge/run program on the left and the standard input of grep pwn.college on the right but this time we had to grep errors so i used the 2>&1 operator which redirects the standard error to standard output. The grep command searched for the line containing pwn.college in the standard errors and diaplayed the flag.
### Flag:
>pwn.college{Iny0wHEBPjYU9XKjoKSj0mPQoMW.dVDM5QDL0cDM1czW}
# DUPLICATING PIPED DATA WITH TEE
### Command:
```
1)hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | /challenge/college
2)hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee cmd_out | /challenge/college
3)hacker@piping~duplicating-piped-data-with-tee:~$ cat cmd_out
4)hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret YK6pHvYE | /challenge/college
```
### Explanation:
Used command 1 to pipe the contents of /challenge/pwn into /challenge/college.
It gave an output that the input to college does not contain a secret code that should be provided by the pwn command.
To find that secret code i used command 2 and used the tee command to figure out what the code should be and duplicate the piped in data from /challenge/pwn to a file named cmd_out.
Used command 3 to display the contents of cmd_out and obtained the secret code to be used.
Then finally ran command 4 and got the flag.
### flag:
>pwn.college{YK6pHvYE6Zl03DVZcHHHGiAiOBM.dFjM5QDL0cDM1czW}
# WRITING TO MULTIPLE PROGRAMS
### Command:
```
1)hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | /challenge/planet
2)hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | /challenge/the
3)hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the ) >(/challenge/planet)
output:
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
21957381787331661
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{osSXyCNoKkzLvkUDN9xv1QGlvvQ.dBDO0UDL0cDM1czW}
```
### Explanation:
Ran the commands as per the instructions given in the description and got the flag.(extremely sorry for the small right up i was low on time, will make up in the next taskphase).
### flag:
>pwn.college{osSXyCNoKkzLvkUDN9xv1QGlvvQ.dBDO0UDL0cDM1czW}

# SPLIT PIPING STDERR AND STDOUT
### Command:
```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
```
# Explanation:
I redirected the standard output and standard error to respective commands where > (i.e. 1>) was used to redirect standard output to /challenge/planet and 2> (i.e. standard error) was used to redirect standard error to /challenge/the which displayed the flag.
# Flag:
>pwn.college{I7v5sV_CsWGCGduL0O6YvtU7OEh.dFDNwYDL0cDM1czW}
