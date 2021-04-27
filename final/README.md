I Rania Ehsan (02408509) agree that the solutions presented below are my own. If I have used resources that are not my own,
I have included appropriate citations. 


Task 1.1: 
In theory the function system() asks shell not OS to execute commands. It may have root priviledges. 

Task 1.2:
The target must be running a vulnurable version shell. An outside source must be sent to the target as an environment variable. 

Task 1.3:
nl -l 7070 will evesdrop on 7070 for any incomingconnections on machine 1. The standard input that is to come from Machine 2
is to be redirected to the TCP connection for Machine1.

Task 1.4:
Because it is a computer protection method. What this does is, it will at random place the base address of an executable 
in the address space of the process. Randomly mixing the adresses will cause an attack not to know the address. 

Task 1.5: 
Root cause of this vulnurability is when a web application uses untrusted input without performing proper validation first. 

Task 1.6:
Stored XSS means that some persistant data (typically stored in a databse) are not sanitized in a page, which implies that 
everyone can be affected by the vulnerability. For example, imagine a forum where users' answers posted are not escaped. If someone
posts a topic with some HTML on it, everyone that goes to the topic page will be affected! The risks can generally be important, since 
it affects all users and can widespread rapidly (A typical example is Myspace XSS worm which impacted one million users in 20 hours).

Reflected XSS, on the contrary, means that non-persistent data (generally data provided by the client through form submission) are not escaped.
For instance, imagine a search engine where in the results list page, your search keywords are redisplayed (and not sanitized). You could then put html
on your research and it will be executed. While the risks of this vulnerability are less obvious, since it only affects the user who made the injection,
it can be a problem too. For example if a malicious user sends a link with the injection on it to a victim, and the victim clicks on the link. 

Task 1.7:
Alice will send the computed value of x to Bob and bob will send the computed value of y to alice. Alice will go (G^ymodp)^x mod p And bob will
do the same for y. And eventually it will be G^xymod p for both of them. 

Task 1.8:
Hybrid encryption is a mode of encryption that merges two or more encryption systems. It incorporates a combination of asymmetric and symmetric
encryption to benefit from the strengths of each form of encryption. These strengths are respectively defined as speed and security.
Hybrid encryption is considered a highly secure type of encryption as long as the public and private keys are fully secure.

Task 1.9:
In general, libraries are created from many library source files, and are either built as archive files (libmine.a) that are statically linked into 
executables that use them, or as shared object files (libmine.so) that are dynamically linked into executables that use them. To link in libraries
of these types, use the gcc command line options -L for the path to the library files and -l to link in a library (a .so or a .a).

There is a potential for security risks for using this approach. 

Task 1.10:
The three counter measures are: ASLR, where stack address keeps changing everytime program is executed. This makes it hard for attacker to 
figure out where to inject malicious code. Bounds checking is another counter measure. Avoid using standard library functions. And finally by
avoiding C and C++ becuase it is more vulnerable to buffer overflow attacks. Using Java or Python may help. 

Task 2.1:
I would limit database access to specific IP addresses. This will give tighter control on who can access our data and enable us to track and 
identify unfamiliar activities. We can also tie specific credentials to specific IP ranges to further limit access and track strange behavior
more closely. The cons of this approach is that, mapping out all the organizations that need access to our data is going to be a difficult 
task and may take a lot of time to do. 

Task 2.2:
Compliance means creating a program that establishes risk-based controls to protect the integrity, confidentiality, and accessibility
of information stored, processed, or transferred. Compliance is important because it helps us avoid fines and penalties. 
Compliance framework typically provides recommendations on implementing and managing the various aspects of a security program, such as
perimeter defense, access control, authentication, encryption, monitoring, reporting, incident response, and risk management. Examples of compliance are 
Mandatory employee cyber security training, Audit and Accountability processes, Conducting risk and vulnerability assesment. Doing these would ensure 
compliance becuase if employees are trained then they would know what the risks may be and would know how to avoid them. By audit and accountability 
process, a supervisor may keep track of things. By conduting risk and vulnerability assesment, we can be sure that things are in order and that 
risks are being avoided. 

Task 3.2:
We saw in class that using "suystem" the user is able to type in whatever command, then a semicolon and then add maliscious commands. The program
being SET-UID any instructions that are injected after the semicolon will be executed. This means that this person can do whatever they want 
because they have rights that they aren't supposed to which may be problematic. 

Task 3.3:
What more does is that, it looks for input from Standard Input Source. From this a program will read its input data if there aren't any given
file names. Read is used by software to request data transfers. 


Task 4.1:
To defeat SQL injection attacks, a web application has implemented a filtering scheme at the client side: basically, on the page where users type their data,
a filter is implemented using JavaScript.

Task 4.2:
The malicious employee, assuming the id being EID5000 provides the $name field in $sql as : update employee salary=90000 where EID80000. At this point
sql will become $sql= insert INTO employee(Name, EID, Password, Salary)
values ('a'); update employee SET salary= 90000 where 'EID5000'; #', 'EID600','Password',80000)"

Task 4.3:
 $result = $conn->query("SELECT id, name, eid, salary, ssn FROM credential WHERE name= '$input_uname' and password= '$hashed_pwd'"); if ($result->num_rows > 0) {"

Prepare the query $stmt = $conn->prepare("SELECT name, local, gender FROM USER_TABLE WHERE id = ? and password = ? ");

$stmt->bind_param("is", $id, $pwd); $stmt->execute(); $stmt->bind_result($bind_name, $bind_local, $bind_gender); $stmt->fetch(); "


Links used:
https://darkcubed.com/compliance

https://blog.finjan.com/cybersecurity-compliance-frameworks/

https://stackoverflow.com/questions/27461936/system-vs-execve/27461938

https://www.handsonsecurity.net/files/problems/Shellshock_ex.pdf

https://www.howtogeek.com/278056/what-is-aslr-and-how-does-it-keep-your-computer-secure/

https://resources.infosecinstitute.com/topic/cross-site-scripting-xss-vulnerabilities/

https://portswigger.net/web-security/cross-site-scripting

https://stackoverflow.com/questions/45952778/what-is-the-difference-between-stored-xss-and-reflected-xss

https://crypto.stackexchange.com/questions/31234/why-is-hybrid-encryption-more-effective-than-other-encryption-scheme#31235

Used lecture slides for task 1.7






