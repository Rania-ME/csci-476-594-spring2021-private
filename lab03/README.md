Task 1.1:
Makefile is used to compile the code by typing make in the directory. Makefile produces two binaries.Running executables doesn't pose any errors. 
then we get access to the shell program. 



![task 1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%201.JPG)



![task 1.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%201.1.JPG)



Task 1.2:
The main() puts the code in the shell code.
Here we compile the vulnerable program into a 32 bit binary stack L1. To do this we used the Makefile, and upon using Makefile it handled all 
the files needed to run the attack. The gdb tool still needs to be used to find out the values needed for running a successful attack. 




Task 2.1:
Here we are to use the vulnerable SET-UID program to access root shell. For this the program needs to be debugged first and get values that may
help when running the attack. A breakpoint is set in the gdb on the bof function. When the program stops at the breakpoint the required numbers can be seen.
We need the edb and buffer values to figure out what is offset and return address that should be used. Hence we compile the debugger, but first we have to 
make sure that ASLR and counter measures are disabled for successfully running the attack. 




![task 2](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%202.JPG) 




Task 2.2:
Here we can use the edp and buffer values to determine what the offset we are supposed to use. When we get the values we need return address and offset
which we add to the exploit.py file. Using gdb gives a deeper stack hence we add 4^n. Also, we need to look out to see that there aren't any 0's in the 
return address because if there are strcopy would terminate it. Nops are used to make sure that the code has been hit correctly. 




![task 2.2](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%202.2.JPG)






Task 3: 




![task 3](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%203.JPG)




Task 4.1: 
First we change the real UID so that it is equal to the effective UID. Because call_shellcode.c is used to  compile the program, the code can be chaged there.
The code already exists within there but just needs ot be at the beginnign of the shellcode. Then we are able to get a root shell after shellcode is run. 
If assembly wasn't used to make the program into SET-UID(0) the root shell wouldn't be achieved. We don't get root shell for the countermeasure that checks
if EUID and RUID are same or not. If they aren't the same the priviledges would be dropped and we just get a normal shell. 




![task 4.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%204.1.JPG) 




Task 4.2:
Here we should be able to launch our attack and get a root shell. This could be done because the counter measures of dash can be defeated using setuid. 


![task 4.2](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%204.2.JPG) 




Task 5.1:
to turn on the address randomization we use the code sudo/sbin/sysctl -w kernel.randomize_va_space=2. This turns on ASLR for stack and heap. This makes the attack
more difficult everytime the program is run. When the ASLR was turned off the stack pointer started from the same place everytime. 



![task 5.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%205.1.JPG)




Task 5.2:
When running brute-force attack, it will run successfulyy regardless if the ASLR is is enabled or not. This just goes through all the possible addresses.



![task 5.2](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%205.2.JPG) 



Task 6.1:
First we turn on stack guard protection to launch the attack. We also turn off ASLR and compile the stack.c without using -fno-stack-protector. This prevents the 
attack. 



![task 6.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/task%206.1.JPG)




Task 6.2:
First we turn on the non-executable stack protection. We change the file and remove -z nonexecstack. Upon running call_shellcode after this we get a32.out
and a64.out. We get a segmenttation fault here because the stack isn't executable now. 
