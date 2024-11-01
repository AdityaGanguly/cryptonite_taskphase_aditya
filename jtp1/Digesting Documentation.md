# LEARNING FROM DOCUMENTATION
### Command:
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
```
### Explanation:
Ran the /challenge/challenge program and gave it the required arguments to obtain the flag.
### Flag:
>pwn.college{wAYEXDwvO9maq_S1RfQ3Hz7VGY5.dRjM5QDL0cDM1czW}
# LEARNING COMPLEX USAGE
### Command:
```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
```
### Explanation:
Ran the /challenge/challenge program and gave it the argument of –printfile to which I gave the argument which was the path of the flag which displayed the flag.
### Flag:
>pwn.college{0cfmzsWdoeW4c3dk5jfyVAh_NPR.dVjM5QDL0cDM1czW}
# READING MANUALS:
### Command:
```
1)hacker@man~reading-manuals:~$ man challenge
2)hacker@man~reading-manuals:~$ /challenge/challenge --gugqdr 452
```
### Explanation:
Used the man command to view the man page of challenge and in the description, I saw that if we give the –gugqdr NUM  arguments to /challenge/challenge it would print the flag if NUM=452 so I ran command 2 and obtained the flag
### Flag:
>pwn.college{gZuTQgDEPRqKdr4dAE5IlJ_qt2S.dRTM4QDL0cDM1czW}
# SEARCHING MANUALS
### Command:
```
1) hacker@man~searching-manuals:~$ man challenge
2) hacker@man~searching-manuals:~$ /challenge/challenge –tlrsqtn
```
### Explanation:
Used the man challenge command to view the manpage of challenge. 
Then I searched the description for the right arguments by using the /flag to search for the word ‘flag’ in the description and used ‘n’ to travel to it. Found the arguments and used command 2 and got the flag.
### Flag:
>pwn.college{cG3bCf3ZDF6vM_xiI55sW2cHn_k.dVTM4QDL0cDM1czW}
# SEARCHING FOR MANUALS:
### Command:
```
1)hacker@man~searching-for-manuals:~$ man man
2)hacker@man~searching-for-manuals:~$ man -k challenge
3)hacker@man~searching-for-manuals:~$ man gvswiujmkg
4)hacker@man~searching-for-manuals:~$ /challenge/challenge --gvswiu 717
```
### Explanation:
Used the man man command to learn about the man command to find the hidden challenge man page.
I found out that -k searches for keywords in man pages and displays the result so I used command 2 to search for a man page containing the challenge keyword and got a result.
Used command 3 which opened the manpage for the challenge command and used command 4 as per the instructions in the man page and got the flag.
### Flag:
>pwn.college{g7vUU1A70sVwLOiujmkJG5g9fVo.dZTM4QDL0cDM1czW}
# HELPFUL PROGRAMS
### Command:
```
1)hacker@man~helpful-programs:~$ /challenge/challenge --help
2)hacker@man~helpful-programs:~$ /challenge/challenge --print-value
Output:
The secret value is: 819
3)hacker@man~helpful-programs:~$ /challenge/challenge -g 819
```
### Explanation:
Used the –help argument with /challenge/challenge to know how to run the /challenge/challenge program, as per the instructions command 2 gave the secret value to be used in command 3 which gave me the flag.
### Flag:
>pwn.college{8tqn-fe1eYL9RkDBiPb3xFnTBuM.ddjM4QDL0cDM1czW}
# HELP FOR BUILTINS:
### Command:
```
hacker@man~help-for-builtins:~$ help challenge
hacker@man~help-for-builtins:~$ challenge --secret IqeyiAvq
```
### Explanation:
Used the help command to view the help page of the challenge program(which is a shell builtin) and found out that the argument --secret gives the flag if it was given the right argument which was ‘IqeyiAvq’.
### Flag:
>pwn.college{IqeyiAvqxRPIvWK5uuVRjdwfCc1.dRTM5QDL0cDM1czW}

