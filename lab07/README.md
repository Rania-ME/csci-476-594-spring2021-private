Task 1: 

Here we are supposed do generate two diffenrent files with the same MD5 hash values. This can be done by using md5collgen. 

the code used is: md5collgen -p prefix.txt out2.bin. Then we use a different command to see if the output files are different 
or not. 

diff out1.bin out2.bin

md5collgen uses padding if the files was not a multiple of 64 then it adds a 0 to fill spots 
till the next multiple of 64 is hit. 

when a file of size 64 is used there isn't going to be any padding. 



![Task1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task1.png)



![Task1.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task1.1.png)




![Task_1.1](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task_1.1.png)





Task 2: 

If the same vaule was used to edit the file we end up having the same hash value. 



![Task2](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task2.png)





Task 3:


Here we are using the provided the C program to create out file.

code used: gcc print_array.c -o task3.out

we can use any hex editor to figure out the vlues needed to use for the head and tail. We need a value which is a 
multiple of 64. 

Code used: 
head -c 12402 task3.out > task3-prefix
tail -c +12530 task3.out > task3-suffix
md5collgen -p task3-prefix -o task3-out1.bin task3-out.bin

whe then get p and q values to create new files. 

Code used: 
tail -c 128 task3-out.bin > p
tail -c task3-out.bin > q

then we create new files
cat task3-prefix p task3-suffix > task-new-1.out
cat task3-prefix q task3-suffix > task3-new-2.out

chomd u+x task3-new-1.out task3-new-2.out



![Task3](https://github.com/Rania-ME/csci-476-594-spring2021-private/blob/main/Task3.png)
