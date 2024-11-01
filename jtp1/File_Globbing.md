# MATCHING WITH *
### Command:
```
1)hacker@globbing~matching-with-:~$ cd /cha*
2)hacker@globbing~matching-with-:/challenge$ /challenge/run
```
### Explanation:
Used globbing by matching with * in command 1 to cd to the challenge directory and once successfully executed used command 2 to obtain the flag.
### flag:
>pwn.college{sVQZtxPP7nNrdtAxc8TbSUQbz9R.dFjM4QDL0cDM1czW}
# MATCHING WITH ?
### Command:
```
1)hacker@globbing~matching-with-:~$ cd /?ha??enge
2)hacker@globbing~matching-with-:/challenge$ /challenge/run
```
### Explanation:
Used globbing by matching with ? in command 1 to cd to the challenge directory.
As per the instructions of the challenge I replaced c and l with ? and then used the cd command.
After successfully changing to the /challenge directory I used /challenge/run (command 2) to obtain the flag.
### flag:
>pwn.college{scR75iGPTBK9n9F9KCtK5KvCsn5.dJjM4QDL0cDM1czW}
# MATCHING WITH []
### Command:
```
1)hacker@globbing~matching-with-:~$ cd /challenge/files
2)hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
```
### Explanation:
Used the cd command to change to the /challenge/files directory and then ran the /challenge/run command with arguments of file_[absh] to bracket glob into file_a,file_b,file_s,file_h thus using globbing by matching with [] and obtaining the flag.
### flag:
>pwn.college{E0ZVRJCp3leUa2nsRyhUUNgJFEK.dNjM4QDL0cDM1czW}
# MATCHING PATHS WITH []
### Command:
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
```
### Explanation:
Ran the /challenge/run command and gave it a single argument of /challenge/files/file_[bash] which contains the absolute path (/challenge/files) thus matching the path to file_a,file_b,file_c.
### flag:
>pwn.college{YVXBF6aMb90ZEM90C06CI5MLURd.dRjM4QDL0cDM1czW}
# MIXING GLOBS
### Command:
```
1)hacker@globbing~mixing-globs:~$ cd /challenge/files
2) hacker@globbing~mixing-globs:/challenge/files$ ls
3)hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [ecp]*
```
### Explanation:
Firstly I used the cd command to change the directory to /challenge/files.
Then I used the ls command to view all the files present in that directory. 
Then I saw that the files "challenging", "educational", and "pwning"  have unique beginnings ,i.e, no other files begin with c,e,p so I used command 2 to use the square bracket glob along with the * glob(to search for any pattern after c,e,p) to get the flag.  
### flag:
>pwn.college{If5hWNMg6CA79z11pflxvqlHAY-.dVjM4QDL0cDM1czW}
# EXCLUSIONARY GLOBBING
### Command:
```
1)hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
2) hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
```
### Explanation:
Firstly I used the cd command to change the directories to /challenge/files.
Then I used the bracket glob as seen in command to with [!pwn]*  to ignore all the files that start with p,w,n and runs the /challenge/run with all the files that don’t start p,w,n.
### flag:
>pwn.college{o7FM75nl4d-pS9jWSSPYoMoFiP_.dZjM4QDL0cDM1czW}


