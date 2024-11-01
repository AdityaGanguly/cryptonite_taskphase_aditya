# CAT NOT THE PET, BUT THE COMMAND!
### Command:
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
```
### Explanation:
cat is used for reading out files.
So i used then cat flag command to read out the flag from the flag file.
### flag:
>pwn.college{o3pctzOY4Bt09qMrDpN_5yzCGDh.dFzN1QDL0cDM1czW}
# CATTING ABSOLUTE PATHS
### Command:
```
hacker@commands~catting-absolute-paths:~$ cat /flag
```
### Explanation:
The flag lies in the / directory so we use the cat /flag command thereby using the absolute path to read the flag file from that directory to obtain the flag.
### flag:
>pwn.college{4EAbVtKUg2i0AsF2bCyFjaak47U.dlTM5QDL0cDM1czW}
# MORE CATTING PRACTICE
### Command:
```
hacker@commands~more-catting-practice:~$ cat /lib/x86_64-linux-gnu/blas/flag
```
### Explanation:
In this challenge, The flag lies in the /lib/x86_64-linux-gnu/blas/flag file.
We use the cat /lib/x86_64-linux-gnu/blas/flag command to display the key from that file by using the absolute path since we cant use cd.
### flag:
>pwn.college{8zJn2g-Tr8vIuQAA1PBywczrMeF.dBjM5QDL0cDM1czW}
# GREPPING FOR A NEEDLE IN A HAYSTACK
### Command:
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
```
### Explanation:
The grep command is used to search a file for the specified lines to get the lines we need.
In this case we need to find the flag from the file /challenge/data.txt.
We know that the flag always starts from pwn.college so we use the grep command to search for the line containing pwn.college in the /challenge/data.txt file thus obtaining the flag.
### flag:
>pwn.college{owu1di_n8w4aNWhUeVhneJnmq87.ddTM4QDL0cDM1czW}
# LISTING FILES
### Command:
```
1) hacker@commands~listing-files:~$ ls /challenge
Output:
8426-renamed-run-25787  DESCRIPTION.md
2) hacker@commands~listing-files:~$ /challenge/8426-renamed-run-25787
```
### Explanation:
Used the ls command to list all the files present in /challenge directory.
From the output I came to know that there are 2 files.
one is the run program which has been renamed to 8426-renamed-run-25787   and a file named DESCRIPTION.md.
So I used command 3 and finally got the flag.
### flag:
>pwn.college{IBEhD67dFQiFtIS14etprBeWrbR.dhjM4QDL0cDM1czW}
# TOUCHING FILES
### Command:
```
1)hacker@commands~touching-files:~$ cd /tmp
2)hacker@commands~touching-files:/tmp$ touch pwn
3)hacker@commands~touching-files:/tmp$ touch college
3)hacker@commands~touching-files:/tmp$ ls
4)hacker@commands~touching-files:/tmp$ /challenge/run
```
### Explanation:
First I used the cd command to change the directory to /tmp as the files specified are to be made in that directory.
Then I used the ‘touch pwn’ and ‘touch college’ commands to create the pwn file and college files respectively.
Then Used the ls command to check whether my files have been created or not and after seeing the output I got the confirmation that my files have been successfully created so I used the /challenge/run command to get the flag.
### flag:
>pwn.college{APpr7Oi34ZStg1iRZ4qgOupTEMI.dBzM4QDL0cDM1czW}
# REMOVING FILES
### Command:
```
1)hacker@commands~removing-files:~$ ls
output:
 Desktop   delete_me  '~'
2)hacker@commands~removing-files:~$ rm delete_me
3)hacker@commands~removing-files:~$ ls
output:
 Desktop  '~'
4)hacker@commands~removing-files:~$ /challenge/check
```
### Explanation:
Used the ls command first to check whether the delete_me file was present in the home directory or not.
Upon seeing the output and getting confirmation I used the rm delete_me command to delete the file and then used ls command again to check and found out that It has been successfully deleted.
So then I used the /challenge/check command and obtained the flag.
### flag:
>pwn.college{oPXJ4BP9am83suprt6-meV46Jp7.dZTOwUDL0cDM1czW}
# HIDDEN FILES
### Command:
```
1)hacker@commands~hidden-files:~$ cd /
2)hacker@commands~hidden-files:/$ ls -a
3)hacker@commands~hidden-files:/$ cat .flag-275981801224686
```
### Explanation:
As the hidden file is in / directory, firstly I used the cd command to change to that directory.
Then I used the ls -a command to display all the hidden files(that start with .) present in that directory.
There I saw a file named .flag-275981801224686  and upon seeing it I was pretty sure that the flag might be in there and used the cat command to display its contents and obtained the flag.
### flag:
>pwn.college{gk5MLaqAIq7Szf2ZkVvHOgAuXXR.dBTN4QDL0cDM1czW}
# AN EPIC FILE SYSTEM QUEST
### Command:
```
1)hacker@commands~an-epic-filesystem-quest:~$ cd /
2)hacker@commands~an-epic-filesystem-quest:/$ ls -a
3)hacker@commands~an-epic-filesystem-quest:/$ cat DISPATCH
4)hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/help
5)hacker@commands~an-epic-filesystem-quest:/usr/share/help$ ls -a
6)hacker@commands~an-epic-filesystem-quest:/usr/share/help$ cat .ALERT
7)hacker@commands~an-epic-filesystem-quest:/usr/share/help$ cd /usr/local/lib/python3.8/dist-packages/jupyterlab/tests/mock_packages/test-hyphens/test_hyphens/__pycache__
8)hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyterlab/tests/mock_packages/test-hyphens/test_hyphens/__pycache__$ ls -a
9)hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyterlab/tests/mock_packages/test-hyphens/test_hyphens/__pycache__$ cat .GIST
10)hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/jupyterlab/tests/mock_packages/test-hyphens/test_hyphens/__pycache__$ cd /usr/lib/python3/dist-packages/scipy/signal/windows/__pycache__
11)hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/signal/windows/__pycache__$ ls -a
12)hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/signal/windows/__pycache__$ cat CLUE
13)hacker@commands~an-epic-filesystem-quest:/usr/lib/python3/dist-packages/scipy/signal/windows/__pycache__$ cd /usr/share/zsh/help
14)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ ls -a
15)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ cat POINTER
16)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ ls /usr/lib/python3/dist-packages/twisted/web/_auth
17)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ cat /usr/lib/python3/dist-packages/twisted/web/_auth/EVIDENCE-TRAPPED
18)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ ls /opt/busybox/busybox-1.33.2/examples/var_service
19)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ cat /opt/busybox/busybox-1.33.2/examples/var_service/SPOILER-TRAPPED
20)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ ls /opt/pwndbg/.venv/lib/python3.8/site-packages/pip/_internal/resolution -a
21)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ cat /opt/pwndbg/.venv/lib/python3.8/site-packages/pip/_internal/resolution/.SECRET
22)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ ls /opt/busybox/busybox-1.33.2/include/config/feature/del/user/from
23)hacker@commands~an-epic-filesystem-quest:/usr/share/zsh/help$ cat /opt/busybox/busybox-1.33.2/include/config/feature/del/user/from/BLUEPRINT-TRAPPED
```
### Explanation:
Used the cd command to change to the / directory which was the first hint.
Then Used ls -a to display all the files(including the hidden ones).
Saw a file named DISPATCH and thought that the next hint might be in there so i used the cat command to display its contents and got the next hint.
As per the next hint I had to go to the /usr/share/help directory to I used the cd command and went there.
There I used the ls -a command again to see all the files and saw a file named .ALERT and used the cat command to display its contents and got the next hint.
As per the next hint I had to go the /usr/local/lib/python3.8/dist-packages/jupyterlab/tests/mock_packages/test-hyphens/test_hyphens/__pycache__ directory so I used the cd command again and went there.
Then I used the ls -a command to display all the files in the directory.
There I saw a file named .GIST and used cat command to display its contents and got the next hint.
According to the next hint the file was in /usr/lib/python3/dist-packages/scipy/signal/windows/__pycache__ directory so I used the cd command and went there this time.
I used the ls -a command again to display all its contents.
There I saw a file named POINTER and used the cat command to display its contents and got the next hint.
According to the next hint the file was in /usr/lib/python3/dist-packages/twisted/web/_auth directory but I cant cd to it else it will self destruct so used the $ ls /usr/lib/python3/dist-packages/twisted/web/_auth command to display the files present in that directory without using cd.
Then I saw a file named EVIDENCE-TRAPPED and used the cat /usr/lib/python3/dist-packages/twisted/web/_auth/EVIDENCE-TRAPPED command to display its contents without going into that directory and go the next hint.
Similar to the previous hint this time as well the file was in /opt/busybox/busybox-1.33.2/examples/var_service directory and I had to get the hint without using cd.
I used the ls /opt/busybox/busybox-1.33.2/examples/var_service command to display the files present in this directory without using cd and saw a file named SPOILER-TRAPPED so I used the cat command and got the next hint.
According to the next hint the file was in /opt/pwndbg/.venv/lib/python3.8/site-packages/pip/_internal/resolution directory and it was hidden as well.
So I used the ls /opt/pwndbg/.venv/lib/python3.8/site-packages/pip/_internal/resolution -a command to display all the files present in that directory (without using cd) and saw a file named .SECRET so I used the cat command again and got the next hint.
According to this hint the file was in  /opt/busybox/busybox-1.33.2/include/config/feature/del/user/from directory and I coudnt use cd again so I used the ls command without cd’ing into the directory and saw a file named BLUEPRINT-TRAPPED and used the cat command and finally obtained the flag completing the quest.
### flag:
>pwn.college{cw-eg1I32_i59jVj8WTQABkFoiX.dljM4QDL0cDM1czW}
# MAKING DIRECTORIES
### Command:
```
1)hacker@commands~making-directories:~$ cd /tmp
2)hacker@commands~making-directories:/tmp$ mkdir pwn
3)hacker@commands~making-directories:/tmp$ ls
4)hacker@commands~making-directories:/tmp$ cd /tmp/pwn
5)hacker@commands~making-directories:/tmp/pwn$ touch college
6)hacker@commands~making-directories:/tmp/pwn$ /challenge/run
```
### Explanation:
Firstly I  used the cd command to go into /tmp directory ad I had to create the /pwn directory inside it. 
Then I used the mkdir command to create the pwn directory. I used the ls command to check whether the directory had been successfully created or not.
Upon seeing that pwn directory has been created successfully I used the cd command and went to that directory.
Then I made the college file using the touch command and then used the /college/run command to obtain the flag.
### Flag:
>pwn.college{0SySTeVg9eMvpWb42eS4yvz7Xxt.dFzM4QDL0cDM1czW}
# FINDIND FILES
### Command:
```
1)hacker@commands~finding-files:~$ find / -name flag
2)hacker@commands~finding-files:~$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/flag
3)hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls
4)hacker@commands~finding-files:~$ cd /usr/local/share/radare2/5.9.5/flag
5)hacker@commands~finding-files:/usr/local/share/radare2/5.9.5/flag$ ls
6)hacker@commands~finding-files:~$ cd /usr/lib/python3/dist-packages/networkx/algorithms/tree/flag
output:
ssh-entrypoint: cd: /usr/lib/python3/dist-packages/networkx/algorithms/tree/flag: Not a directory
7)hacker@commands~finding-files:~$ cat /usr/lib/python3/dist-packages/networkx/algorithms/tree/flag
```
### Explanation:
Used the find command and filtered by name to search the entire filesystem for the flag file and got a bunch of directories/files in output
I searched in them one by one starting with /usr/local/lib/python3.8/dist-packages/pwnlib/flag Directory to which I went by using cd and used ls to search for the flag but coud’nt find it.
Then I tried to used the cd command on /usr/local/lib/python3.8/dist-packages/pwnlib/flag but it gave and error saying that It wasn’t a directory so I directly used the cat command on it and obtained the flag.
### Flag:
>pwn.college{0VnkxZnZ60hlW3s431_C8iich2l.dJzM4QDL0cDM1czW}
# LINKING FILES
### Command:
```
1)hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
2)hacker@commands~linking-files:~$ /challenge/catflag
```
### Explanation:
Initially i ran command 2 and saw that it was trying to open a file named not-the-flag but it didnt exist.
so i created a symbolic link to /flag using command, i named the linked file not-the-flag(as it was getting diaplayed by command 2) and then used command 2 to trick the system and got the flag through the link.

### Flag:
>pwn.college{k7GF8P23XWooYadjPSmRut9XK7_.dlTM1UDL0cDM1czW}





