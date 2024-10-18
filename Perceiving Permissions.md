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
Firstly i used command 1 to check the ownership of the /flag file and found out that its owned by the root user.
Then i used the chown command as seen in command 2 and changed the ownership of the file to the hacker user.
Then i again used ls -l /flag command to check whether i successfully changed the user to hacker and the used the cat /flag command to display the contents of the /flag file and got the flag.
### Flag:
>pwn.college{MI9TQNC3vyTISC4atY1XLEd41Rl.dFTM2QDL0cDM1czW}
# GROUPS AND FILES
### Command:
```
1)hacker@permissions~groups-and-files:~$ ls -l /flag
output:
-r--r----- 1 root root 58 Oct 17 16:28 /flag
2)hacker@permissions~groups-and-files:~$ chgrp hacker /flag
3)hacker@permissions~groups-and-files:~$ ls -l /flag
output:
-r--r----- 1 root hacker 58 Oct 17 16:28 /flag
3)hacker@permissions~groups-and-files:~$ cat /flag
```
### Explanation:
Used command 1 to check the group of the /flag file and found oyt that it belonged to the root group so i coudnt open it without changing its group to hacker.
Then i used the chgrp command as seen in command 2 to change the group from root to hacker.
Then i used command 3 to check whether the group has been successfully changed or not.
Then i used the cat /flag command and got the flag.
### Flag:
>pwn.college{8K18ezaZ1veNKnsIufIBD-yG8Ty.dFzNyUDL0cDM1czW}
# FUN WITH GROUP NAMES
# Command:
```
1)hacker@permissions~fun-with-groups-names:~$ id
output:
uid=1000(hacker) gid=1000(grp6896) groups=1000(grp6896)
2)hacker@permissions~fun-with-groups-names:~$ chgrp grp6896 /flag
3)hacker@permissions~fun-with-groups-names:~$ cat /flag
```
### Explanation:
I used the id command to check what group i belong to and found that my group name is grp6896.
Then i used the chgrp command and changed the group of /flag file to grp6896.
Finally i used the cat command and got the flag.
### Flag:
>pwn.college{UKwKAI4nlMi60s5rPnIRKqLhXVU.dJzNyUDL0cDM1czW}
# CHANGING PERMISSIONS
### Command:
```
1)hacker@permissions~changing-permissions:~$ ls -l /flag
output:
-r-------- 1 root root 58 Oct 18 11:21 /flag
2)hacker@permissions~changing-permissions:~$ chmod o+r /flag
3)hacker@permissions~changing-permissions:~$ ls -l /flag
output:
-r-----r-- 1 root root 58 Oct 18 11:21 /flag
4)hacker@permissions~changing-permissions:~$ cat /flag
```
### Explanation:
Firstly i used ls - /flag command to check the permissions of /flag file and according to the output found out that only the root user could read it.
I realised that i would have to use the chmod command and manipulate the permissions.
Since i am the hacker user i coudnt use 'u' , 'g' along with chmod to get the flag. I would have to use 'o' which is for other users and groups and hacker comes into this category. So i used command 2 and use o+r to give read access to other groups/users for the /flag file.
I used the ls -l /flag command to check whether the changes i made were successful and upon getting the output used the catr /flag command which gave me the flag.
### Flag:
>pwn.college{MSBiLzN1Bpb-fGaG7xbPIPOg5IE.dNzNyUDL0cDM1czW}
