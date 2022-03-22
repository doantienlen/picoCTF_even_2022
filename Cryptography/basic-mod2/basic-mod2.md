# basic-mode2
## Problem: 
There is an encrypted message with mod 41 and find the modular inverse for the result. 
Then map to the following character set: 
  * 1-26 are the alphabet 
  * 27-36 are the decimal digits, 
  * 37 is an underscore
Download the message: https://artifacts.picoctf.net/c/499/message.txt
## Solution: 
After downloading, i open this file with strings command line. 

![base2-1](https://user-images.githubusercontent.com/84562630/159462391-c21df038-4655-43c0-b757-8fff74bf235c.PNG)

Now, i must find the modular inverse. i use a tool online (https://www.dcode.fr/modular-inverse)
This method is not the most optimal method, because i am not good at cryptography, but this method still finds the flag.
After finding modul inverse, i will run the following code python. 
```python
def  find_flag():
	array_1 = [28  ,14   ,22  ,30 ,18  ,32  ,30  ,12  ,25  ,37  ,8   ,31   ,18  ,4 , 37 ,3  ,33  ,35   ,27  ,2   ,4 , 3   , 28 ]
	array = [ 'A','B','C','D','E','F','G','H','I','J','K' ,'L' ,'M' ,'N' ,'O', 'P','Q','R','S','T' ,'U','V' ,'W' ,'X' ,'Y' ,'Z' ,
		  '0' ,'1' , '2' ,'3' ,'4' ,'5' ,'6' ,'7' ,'8' ,'9' ,'_' ]
	lst = []
	for i in array_1: 
		lst.append(array[i-1])
	return "".join(lst)
print(find_flag())
```
![base2-2](https://user-images.githubusercontent.com/84562630/159465585-46936b89-8fd5-466e-9ae7-bb9df8c5ea74.PNG)
## Flag: 
picoCTF{1NV3R53LY_H4RD_C680BDC1}


