# transposition-trail 
## Problem 
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message. 
Download the corrupted message: https://artifacts.picoctf.net/c/456/message.txt
## Solution
After downloading. I open this file, i see an encoded message. 

![transpotion1](https://user-images.githubusercontent.com/84562630/159620916-6b8bb3c6-d95a-4494-943f-c6b526749cb9.PNG)

I use some online decoding tools, but it can't find the flag. 

As the title suggests, the code is slip into three parts and let's see what the first part encodes. 

I see that, if change position of the 2th character to the front of the 0th and 1st positions, the word "The" will be obtained. 

![transpotio2](https://user-images.githubusercontent.com/84562630/159621821-024a7a86-fe3e-433d-ae1c-527fcb16177a.PNG) ---> ![transposition4](https://user-images.githubusercontent.com/84562630/159623020-2e508efc-2c0b-4636-8edf-85e0eb5d0dff.PNG)

Now, i will present my solution as follows: 

I will number each charater, and only three numbers are 0,1,2. 

![transpotion3](https://user-images.githubusercontent.com/84562630/159622218-1a0f9873-1712-42fc-8759-b455938663fa.PNG)

then i will change the position of the number 2 in front of the position of the two numbers 0 and 1. 

![transpertion7](https://user-images.githubusercontent.com/84562630/159625243-75d19723-05f9-4714-a3c0-48a5dc1767d1.PNG)

Keep doing this until the en of the string. And i got the flag: 

![transpiton6](https://user-images.githubusercontent.com/84562630/159625158-d9d1e05b-387e-4535-bb8b-5c2750a7ac29.PNG)

## Flag
picoCTf{7R4N5P051N6_15_3XP3N51V3_56E6924A}
