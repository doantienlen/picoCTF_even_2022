# Forbidden Paths
## Decription 
Can you get the flag? 

Here's the http://saturn.picoctf.net:53864/

We know that the website files live in /usr/share/nginx/html/ and the flag is at /flag.txt but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solution 
I try to enter divine-comedy.txt, but it doesn't work. I enter again with "../../../../flag.txt" 

![image](https://user-images.githubusercontent.com/84562630/160774804-ba8f7534-5a47-4375-b7a8-d628229fe225.png)

## Flag
 picoCTF{7h3_p47h_70_5ucc355_6db46514}
