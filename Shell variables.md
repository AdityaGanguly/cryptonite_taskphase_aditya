# PRINTING VARIABLES
### Command:
```
hacker@variables~printing-variables:~$ echo $FLAG
```
### Explanation:
In this challenge the flag has been put in a variables called FLAG. I printed the flag from the variable by prepending the varialble name with '$' ($FLAG). 
### Flag:
>pwn.college{Ej6_yvdo955kNQCEe3P_L73eJha.ddTN1QDL0cDM1czW}
# SETTING VARIABLES
### Command:
```
hacker@variables~setting-variables:~$ PWN=COLLEGE
```
### Explanation:
In this challenge we need to set the value of a variable named PWN to COLLEGE. I did this using the assignment operator(=) as seen in the command and got the flag.
### Flag:
>pwn.college{4PAcQNO5AxGb_EFlr6MDkvhXnJx.dlTN1QDL0cDM1czW}
# MULTI-WORD VARIABLES
### Command:
```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
```
### Explanation:
In this challenge we have to assign the value COLLEGE YEAH to the variable PWN.
We cant use the command PWN=COLLEGE YEAH as it contains a space so it will end the variable assignment after COLLEGE so we use quoting to include spaces.
I used the above command to successfully assign "COLLEGE YEAH" to the PWN variable and got the flag.
### Flag:
>pwn.college{MA0I38T2afMSeFDcuRvvWIf-7H3.dBjN1QDL0cDM1czW}
# EXPORTING VARIABLES
### Command:
```
1)hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
2)hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
3)hacker@variables~exporting-variables:~$ /challenge/run
```
### Explanation:
I used command 1 to set the value of the PWN variable to COLLEGE and exported it using the 'export' command.
Then i used command 2 to sed the value of COLLEGE variable to PWN but did not export it.
Both commands gave me the output that i have assigned the correct values so i used command 3 and got thr flag.
### Flag:
>pwn.college{k3LUcXAaO4HY4b6TTkrZYnCvSZF.dJjN1QDL0cDM1czW}
# PRINTED EXPORTED VARIABLES
### Command:
```
hacker@variables~printing-exported-variables:~$ env
```
### Explanation:

### Flag:
>pwn.college{QkCPY5AdtErw6y-BOLyc-D5lTDy.dhTN1QDL0cDM1czW}
