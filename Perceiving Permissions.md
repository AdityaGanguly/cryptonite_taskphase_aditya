
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
### useful tips:
 - r - user/group/other can read the file (or list the directory)
 - w - user/group/other can modify the files (or create/delete files in the directory)
 - x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
 - '-' - nothing 
# EXECUTABLE FILES
### Command:
```
1)hacker@permissions~executable-files:~$ ls -l /challenge/run
output:
-r--r--r-- 1 hacker hacker 32 Jul  4 06:37 /challenge/run
2)hacker@permissions~executable-files:~$ chmod u+x /challenge/run
3)hacker@permissions~executable-files:~$ ls -l /challenge/run
output:
-r-xr--r-- 1 hacker hacker 32 Jul  4 06:37 /challenge/run
4)hacker@permissions~executable-files:~$ /challenge/run
```
### Explanation:
I used command 1 to see what permissions are enabled for the /challenge/run program.
There i saw that this program is already owned by the hacker user(no need worry about users now lol) and is present in the hacker group so used the chmod command along with the arguments u+x to make it executable by the hacker user.(since in this challenge we need to run the program to get the flag)
Then i used command 3 and saw that /challenge/run is now executable by the hacker user so i used command 4 and got the flag.
### Flag:
>pwn.college{YbHOfsL1vQBYiIM7tZ7dwYkwIjh.dJTM2QDL0cDM1czW}
# PERMISSION TWEAKING PRACTICE
### Command:
```
1)hacker@permissions~permission-tweaking-practice:~$ chmod u+x /challenge/pwn
output:
You set the permissions incorrectly! Restarting the game!
2)hacker@permissions~permission-tweaking-practice:~$ ls -l /challenge/pwn
output:
-rw-r--r-- 1 hacker hacker 0 Oct 18 12:06 /challenge/pwn
3)hacker@permissions~permission-tweaking-practice:~$ chmod go+w /challenge/pwn
4)hacker@permissions~permission-tweaking-practice:~$ chmod g-w /challenge/pwn
5)hacker@permissions~permission-tweaking-practice:~$ chmod g+w /challenge/pwn
6)hacker@permissions~permission-tweaking-practice:~$ chmod a-r /challenge/pwn
7)hacker@permissions~permission-tweaking-practice:~$ chmod ug+x /challenge/pwn
8)hacker@permissions~permission-tweaking-practice:~$ chmod g+r /challenge/pwn
9)hacker@permissions~permission-tweaking-practice:~$ chmod g-r /challenge/pwn
10)hacker@permissions~permission-tweaking-practice:~$ chmod o-w /challenge/pwn
output:
You set the correct permissions!
You've solved all 8 rounds! I have changed the ownership
of the /flag file so that you can 'chmod' it. You won't be able to read
it until you make it readable with chmod!
11)hacker@permissions~permission-tweaking-practice:~$ chmod u+r /flag
12)hacker@permissions~permission-tweaking-practice:~$ cat /flag
```
### Explanation:
Initially since i didnt know(and wasnt told) what permissions to set for the /challenge/pwn program i tried using chmod with u+x to try and make it executable but it showed that the permissions are incorrect and the game has restarted.The good thing that came out of this is now along with the output showing that my command was incorrect it also showed the instructions of what to do.
I used ls -l /flag command to check if the permissions have been restarted or not.
Ok so i finally start with the quest:
As per the instructions i needed to give the world and the groups write permissions so i used the chmod command as seen in command 3 and did so and the output showed that i was correct.
As per the next instructions i needed to remove the write permissions from all the groups which i did as seen in command 4.
Next i needed to add the write permissions back to the groups which i did in command 5.
According to the next instructions i needed to remove the read permissions from everything which i did in command 6.
Then i needed to give the user and the group the execute permission which i did in command 7.
After this i needed to give the group read permissions which i did as seen in command 8.
The next instructions needed me to remove the read permissions from groups as seen in command 9.
The final set of instructions told me to remove the write permissions from other users/groups which i did in command 10.
Now it gave the output that i solved all the 8 rounds correctely and now i can use cmod on the /flag file.
So i used the cmod command as seen in commans 11 and made the file readable by the user(me).
Then i used the cat /flag command and got the flag.

### Flag:
>pwn.college{Ic3L04bB4g893vAcEy-6JEc8tVv.dBTM2QDL0cDM1czW}
