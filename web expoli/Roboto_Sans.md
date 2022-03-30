# Roboto Sans.md
## Description 
The flag is somewhere on this web application not necessarily on the website. Find it.

Check http://saturn.picoctf.net:65352/ out. 
## Solution 
I open this website, let's show the source. I see a message: 

![image](https://user-images.githubusercontent.com/84562630/160781297-ce6ad27e-a335-413a-8455-32acbcde07c5.png)

I add "robots.txt" at the end of the URL: 

![image](https://user-images.githubusercontent.com/84562630/160781613-d1b3c9c5-b9de-44cb-b4f1-fb0aa59bbf05.png)

I see an encoded message, i try to decode it with base64. 

![image](https://user-images.githubusercontent.com/84562630/160781987-d43c11e0-2b87-401c-b52e-e3d700dc3d6c.png)

I will add "js/myfile.txt" at the end of the URL. 

![image](https://user-images.githubusercontent.com/84562630/160782329-27977dd7-32ae-4a0a-a12f-f6d2a529768e.png)

## Flag
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
