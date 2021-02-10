Task 1: Learning about environment details. 
Task 2: The program is its own process and makes a child process.
Which environment variables get printed depends on what is commented out.
The only difference in environment variables between parent and child
were GNOME_TERMILAN_SERVICE and GNOME_TERMINAL_SCREEN
Task 3: the third argument of execve passes the current environment variables
to the new program.
Task 4: As expected, it prints the environment variables of the current environment.

https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/CSec_Lab_01_T4.JPG 

Task 5: Unsurprisingly, the variables that I set were still changed within the
child process

https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/CSec_Lab_01_T51.JPG

Task 6: It ran my code with root privileges. This is dangerous because people can
do things with higher privileges.
Task 7: It doesn't print anything. It just sleeps for a bit. When a set UID program takes 
the lead/runs it provides the user with priviledges depending on the program's owner. So, if the owner
is root anyone running the program gains the roots priviledges. However, because of countermeasurements 
that is implimented by the dynamic linker any of the manipulations of LD_PRELOAD environment variables 
done by set UID programs is ignored unless it is done by the real user ID. 
  Experiment: We can copy the "env" variables which is already there in usr/bin that prints all environment
  variables to my directory. Changeing variables that has no threat to Set-UID program would be executed in both files. 
  One in usr/bin another in current directory. While changing other variables that can cause vulnerabilities to 
  Set_UID programs would be ignored unless it is done by the real UID from the root account. These kinds of changes takes
  place only in file in usr/bin not the one directory. 
  
 Task 8: In theory the function system() asks shell not the OS to execute commands. It may have root priviledges,
 hence Bob can remove files. 


