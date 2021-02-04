1)fork() is used for creating a new process called the child process which runs concurrently with the process that makes the fork() call. After a new child process is created both processes will execute the next instruction following the fork() system call. A child process uses the same program counter same CPU registers same open files which use in the parent process. \

exec() is used ot execute a file which is residing in an active process. when exec is called the previous executable file is replaced and a new file is executed. 

2)stack is located under the OS kernel and above the heap. Heap is memory is dynamically allocated. If one is to use calloc or malloc they can dynamically allocate memory to heap. In uniinitialized block segment the data is initialized to zero by kernel before executing the program. In initialized segement data can be found which is already initialized. It can be clasiified as read only or write only. 

3) Fundamentally there is no difference in code and data but for real software infrastructure there can be a big difference. Code most definitely cannot be changeable so anything that needs to be changed needs to be factored out and made configuration data so that changing it becomes palatable those whose job it is to ensure that a release works. 
4) Variables are stored in the stack and anyone access to the stack can see those. This could lead to data being stolen or manipulated. This could make the program crash or could cause data to leak. 
5) A trust boundary is a boundary where program data or execution changes its level of trust or where two principals with different capabilities exchange data or commands. The term refers to any distinct boundary where within a system all sub systems have equal trust. 
6) The major elements of a stack frame discussed in class is the return address. It gives the program instructions on what to do next and stores the values and arguments to be passed. 

7)main is located in the heap. it is in a part of memory that is designated as executable. 
printf is located in the stack
argv is located in the stack
environ is located in the stack
