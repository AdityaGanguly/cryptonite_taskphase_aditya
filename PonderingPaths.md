# THE ROOT
### Command:
```
hacker@paths~the-root:~$ /pwn
```
### Explanation:
a file system/path starts with '/'. pwn is a program in / which is the root directory, pwn program is invoked by using the absolute path. /pwn is called the absolute path(since its in the root directory) which gives us the flag.
### flag:
>pwn.college{I3wVbgIl_qkgPJ8XZkvqlwvRrZ9.dhzN5QDL0cDM1czW}
# PROGRAM AND ABSOLUTE PATHS
### Command:
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
```
### Explanation:
the run program is in the /challenge directory and the challenge directory is in the '/' directory(root directory). Therefore the absolute path is /challenge/run which gives us the flag.
### flag:
>pwn.college{wvLMv7VI3ur3soDpAmJotE1KNcp.dVDN1QDL0cDM1czW}
# POSITION THY SELF
### Command:
```
1) hacker@paths~position-thy-self:~$ /challenge/run
Output:
Incorrect...
You are not currently in the /etc directory.
Please use the `cd` utility to change directory appropriately.
2) hacker@paths~position-thy-self:~$ cd /etc
3) hacker@paths~position-thy-self:/etc$ /challenge/run

```
### Explanation:
Tried invoking the run program from the root directory but it gave an error since the program is located in the /etc directory so we use cd command to change directory to /etc and then execute /challenge/run which invokes the run program correctly and gives us the flag.
### flag:
>pwn.college{kTGuW4fRJZOVPEduRO-Lcfxhmd9.dZDN1QDL0cDM1czW}
# POSITION ELSEWHERE
### Command:
```
1) hacker@paths~position-elsewhere:~$ /challenge/run
Output:
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
2) hacker@paths~position-elsewhere:~$ cd /tmp
3) hacker@paths~position-elsewhere:/tmp$ /challenge/run
```
### Explsnation:
Same as the previous problem. Tried invoking the run program from the root directory again but it showed error as this time its located in the /tmp directory. So we use the cd command to change to that directory and then run the /chanllenge/run command which successfully invokes the run program and gives us the flag.
### flag:
>pwn.college{0Q6L6hDKDqpBj4yqEWehTjlEk4d.ddDN1QDL0cDM1czW}
# POSITION YET ELSEWHERE
### Command:
```
1) hacker@paths~position-yet-elsewhere:~$ /challenge/run
Output:
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
2) hacker@paths~position-yet-elsewhere:~$ cd /
3) hacker@paths~position-yet-elsewhere:/$ /challenge/run
```
### Explanation:
Similar to the previous problem, we try to run the run program from the root directory as seen in command 1 but this time the program is located in the / directory. So we use the cd command to change to that directory as seen in command 2 and the use the /challenge/run command as in command 3 to invoke the run program and get the flag.
### flag:
>pwn.college{AmttC1_lUb8DyZ97o380VOxSAsV.dhDN1QDL0cDM1czW}
# IMPLICIT RELATIVE PATHS, FROM /
### Command:
```
1) hacker@paths~implicit-relative-paths-from-:~$ cd /
2) hacker@paths~implicit-relative-paths-from-:/$ challenge/run
```
### Explanation:
Fiirst we use the cd command to change to the / directory. Current working directory is / therefore the relative path to invoke the run program is challenge/run.
### flag:
>pwn.college{09CcJ54P-u1gZUWaKhbM4Jel1CK.dlDN1QDL0cDM1czW}
# EXPLICIT RELATIVE PATHS, FROM /
### Command:
```
3) hacker@paths~explicit-relative-paths-from-:~$ cd /
4) hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
```
### Explanation:
Firstly we use the cd command to change to the / directory where the program is located. Then we use the ./challenge/run to explicitely invoke the run program. ./challenge/run is the relative path.
### flag:
>pwn.college{AQbNhl73vyKFcyHukeFQq3K5QWq.dBTN1QDL0cDM1czW}
# IMPLICIT REPATIVE PATH
### Command:
```
1) hacker@paths~implicit-relative-path:~$ cd /challenge
2) hacker@paths~implicit-relative-path:/challenge$ ./run
```
Firstly we will change the directory to /challenge as specified, by using the cd command. We use the relative path ./run to tell linux how to explicitely execute the run program from the correct directory.
### flag:
>pwn.college{8n5gJ6sRqQy8HKdlA7WBNtWEP3H.dFTN1QDL0cDM1czW}
# HOME SWEET HOME
### Command:
```
 1) hacker@paths~home-sweet-home:~$ /challenge/run ~
output:
Writing the file to /home/hacker!
/challenge/run: line 29: /home/hacker: Is a directory
... and reading it back to you:

 2) hacker@paths~home-sweet-home:~$ /challenge/run ~/~
output:
Writing the file to /home/hacker/~!
... and reading it back to you:
pwn.college{Y4kVMD8G4gHcWiS12HlA-RImJ0R.dNzM4QDL0cDM1czW}
```
### Explanation:
expalsion of ~ is an absolude path(/home/hacker). 
~/~ will be expanded to /home/hacker/~. 
Tried running command 1 but failed to receive the flag. 
Running command 2 will copy the flag into a file present in the home directory and allow us to view it
### flag:
>pwn.college{Y4kVMD8G4gHcWiS12HlA-RImJ0R.dNzM4QDL0cDM1czW}
