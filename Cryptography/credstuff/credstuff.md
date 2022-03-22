# credstuff 
## Problem: 
We found a leak of a blackmarket website's login credentials. Can you find the password of the user cultiris and successfully decrypt it?
Download the leak https://artifacts.picoctf.net/c/534/leak.tar
## Solution: 
After downloading, we decompress this file by using 'binwalk -e leak.tar' commad line on the terminal. 
I see a new folder after extracting, i access it and see two .txt files.

![credstuff2](https://user-images.githubusercontent.com/84562630/159506364-c8ef048b-027f-417f-a374-1d91202fd75e.PNG)

I find the user with cultiris name, the user is at 378th

![credstuff1](https://user-images.githubusercontent.com/84562630/159506972-70e51034-6aa6-492f-a68a-fc502b2b1003.PNG)

so the password is at 378 in the password.txt file. 

![ccredstuff4](https://user-images.githubusercontent.com/84562630/159507253-66851685-5020-4347-9360-14020590edb7.PNG)

I try some decode tools online, and i find the flag by using https://rot13.com/
## Flag
picoCTF{C7r1F_54V35_71M3}
