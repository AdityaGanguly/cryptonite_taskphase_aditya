# CHAINING WITH SEMICOLONS
### Command:
```
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Output:
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
```
### Explanation:
I used the semicolon to chain /challenge/pwn and /challenge/college and got the flag.
### Flag:
>pwn.college{E6X7rLr6JBxO7VjZOKMY7CtGgZN.dVTN4QDL0cDM1czW}
# YOUR FIRST SHELL SCRIPT
### Command:
```
In x.sh shell script:
/challenge/pwn
/challenge/college
On Ubuntu terminal:
hacker@chaining~your-first-shell-script:~$ bash x.sh
Output:
Great job, you've written your first shell script! Here is the flag:
```
### Explanation:
In this challenge I had to run /challenge/pwn and /challenge/college on the x.sh shell script. 
Since we dont have the knowledge of how to use the text editor from the terminal yet, for this challenge i used the vs code workspace to create the x.sh shell script.
On that script i ran the /challenge/pwn and /challenge/college commands.
Now i went back to the linux terminal and ran the command bash.sh and it gave me the output that i have successfully written to the shell scipt and gave me the flag.

NOTE: i realised way too late that i coud've done this by an alternate method purely on the linux terminal by using echo and output redirection:
```
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~your-first-shell-script:~$ echo "/challenge/pwn;/challenge/college" > x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
```
### Flag:
>pwn.college{8779lN9VD_6ooUktNiesaD2HP2c.dFzN4QDL0cDM1czW}
# REDIRECTING SHELL OUTPUT
### Command:
```
In x.sh shell script:
/challenge/pwn
/challenge/college
On linux terminal:
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
```
### Explanation:
Firstly i created the shell script x.sh which cointains the /challenge/pwn and /challenge/college commands.
Then on the terminal i used the piping operator to pipe the output of the script to the /challenge/solve command as seen above.
Since the redirection was correct i got the flag through the standard output.

NOTE:
Similar to the previous problem here's the alternate method without using vs code:
```
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~redirecting-script-output:~$ echo "/challenge/pwn;/challenge/college" > x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve
```
### Flag:
>pwn.college{MBLXxdEiHUu1IsJ-wBVbeWoIn7Q.dhTM5QDL0cDM1czW}
# EXECUTABLE SHELL SCRIPTS
### Command:
```
1)hacker@chaining~executable-shell-scripts:~$ touch x.sh
On x.sh shell script:
/challenge/solve
2)hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
Output:
-rw-r--r-- 1 hacker hacker 16 Oct 19 06:15 x.sh
3)hacker@chaining~executable-shell-scripts:~$ chmod u+x x.sh
4)hacker@chaining~executable-shell-scripts:~$ /home/hacker/x.sh
Congratulations on your shell script execution! Your flag:
```
### Explanation:
I used the touch command to create the x.sh shell script.
In the shell script i added the /challenge/solve command.
Then back in the terminal i used ls -l x.sh to see what permissions are enabled.
In this challenge i had to make the shell script executable by the user(me) so i used the chmod command with arguments u+x as seen in command 3.
Then i used command 4 to run the shell script which invoked the /challenge/solve command(without using bash) and gave me the flag.

NOTE : ALTERNATE METHOD:(used > to redirect the output of echo command which was "/challenge/solve" to x.sh) 
```
hacker@chaining~your-first-shell-script:~$ touch x.sh
hacker@chaining~executable-shell-scripts:~$ echo "/challenge/solve" > x.sh
hacker@chaining~executable-shell-scripts:~$ ls -l x.sh
output : -rw-r--r-- 1 hacker hacker 17 Oct 19 12:24 x.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+x x.sh
hacker@chaining~executable-shell-scripts:~$ /home/hacker/x.sh
```
### Flag:
>pwn.college{M-mzRDUfWVDIS6mky-btnmLENH9.dRzNyUDL0cDM1czW}
