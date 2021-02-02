fork() is used for creating a new process called the child process which runs concurrently with the process that makes the fork() call. After a new child process is created both processes will execute the next instruction following the fork() system call. A child process uses the same program counter same CPU registers same open files which use in the parent process. \

exec() is used ot execute a file which is residing in an active process. when exec is called the previous executable file is replaced and a new file is executed. 



main is located in the heap. it is in a part of memory that is designated as executable. 
printf is located in the stack
argv is located in the stack
environ is located in the stack
