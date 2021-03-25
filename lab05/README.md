Task 1: 

![Task01_Working](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task01_Working.png


Task 2:

Here we do the same as before but instead of displaying an alert we will display user cookies. We change the JS that has been used before. 


![Task02_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task02_Payload.png)



![Task02_Working](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task02_Working.png)


If done correctly any visitor of the profile would get an alert showing their cookies. 


Task 3: 

![Task03_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task03_Payload.png)



![Task03_Working](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task03_Working.png)


In here we want to send cookies to somewhere that can access information from. For this, JS needs to send HTTP request to the attacker 
with cookies append to request. After getting the URL that is used to send cookies to we need to inject it along some some JS code to 
our profile to be able to steal cookies from any visitor of the profile. The JS code needs to be injected about me field. If done correctly 
we will be able to steal the cookies from the visitor of the profile. 



Task 4: 

Here we try to become the victims friend. We need to know how the add friend reqest works. So we send a friend request, observe how HTTP 
request works. When we know that we create a JS code to do that to any visitor of the profile. 


![Task04.1_After_Visiting](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04.1_After_Visting.png)


After knowing the parameters we can start creating the payload. Now anyone who visits the profile will be add us as friends. 

![Task04.1_Before_visiting](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04.1_Before_Visting.png)


Now that we were able to successfully launch our attack, we will try to do the same thing in text mode. This will not be 
successful because text editor will change a few things. 



![Task04.2_Not_Working(1)](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04.2_Not_Working(1).png)



![Task04.2_Not_Working](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04.2_Not_Working.png)




![Task04.2_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04.2_Payload.png)




![Task04_Finding_ID_NUmber](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04_Finding_ID_Number.png)



![Task04_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task04_Payload.png)


Task 5: 

Here we will trybto create a payload that makes changes to the profiles of anyone who visited our profile. We go to our profile and make changes to 
description field and see the HTTP request. 




![Task05.1_Visiting_Samy](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05.1_Visting_Samy.png)





![Task05.1_After_Visiting_Samy](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05.1_After_Visting_Samy.png)





![Task05_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05_Payload.png)




![Task05.2_Payload](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05.2_Payload.png)





![Task05.2_Without_If_Statement(1)](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05.2_Without_If_Statment(1).png)






![Task05.2_Withou_If_Statement](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task05.2_Without_If_Statment.png)







The JS code obtains curent session's values and stores a string name in the about me section. If we comment out line 1 as soon as the changes
are saved the JS code will be executed. It would replace the JS code we had with the string which means that the attack would not work. 




Task 6:

We want to see if we can have our code to copy itself into other people's profiles once they view our profile. We will try to implement self propagating 
scripting worm which would modify the victims profile. This attack will spread from one user to the next whenever an infected user is visited, much like 
a plague rat. 






![Task06_After_The_Attack(1)](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task06_After_The_Attack(1).png)





![Task06_After_The_Attack](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task06_After_The_Attack.png)






![Task06_After_Visiting_Infected(1)](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task06_After_Visiting_Infected(1).png)











