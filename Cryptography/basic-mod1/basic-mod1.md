# basic-mod1
## Problem: 
There is an encryted message with mod 37 and map it is the following character set: 
    
    * 0-25 is the alphabet( uppercase) 
    * 26-35 are the decimal digits 
    * 36 is an underscore 
Download the message: https://artifacts.picoctf.net/c/393/message.txt
## Solution: 
After downloading, i open message.txt file with strings command line. 

![base1-1](https://user-images.githubusercontent.com/84562630/159448305-75ccac1e-e99c-49ba-8566-d878c280134c.PNG)

The message is encrypted by the numbers, and i decrypt it with code python: 
```python 
def  find_flag():
	array_1 = [54 ,396, 131, 198, 225, 258, 87, 258, 128, 211, 57, 235, 114, 258, 144, 220, 39, 175, 330, 338, 297, 288]
	array = [ 'A','B','C','D','E','F','G','H','I','J','K' ,'L' ,'M' ,'N' ,'O', 'P','Q','R','S','T' ,'U','V' ,'W' ,'X' ,'Y' ,'Z' ,
		  '0' ,'1' , '2' ,'3' ,'4' ,'5' ,'6' ,'7' ,'8' ,'9' ,'_' ]
            
	lst = []
	for i in array_1: 
		x = i % 37
		lst.append(array[x])
	return "".join(lst)
print(find_flag())
```
After running the code,the result is:

![base1-2](https://user-images.githubusercontent.com/84562630/159452922-7ef9fcda-fe96-47f5-8ad7-8636c8648bd0.PNG)

## Flag: 
picoCTF{R0UND_N_R0UND_79C18FB3}

