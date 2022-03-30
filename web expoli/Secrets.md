# Secrets 
## Description 
We have several pages hidden. Can you find the one with the flag?

The website is running http://saturn.picoctf.net:61481/
## Solution 
I open the source of this website

![image](https://user-images.githubusercontent.com/84562630/160881133-ed862f01-9af1-42f5-8c8c-b23069a8cd7b.png)

I will add the "/secret" at the end of home URL 

![image](https://user-images.githubusercontent.com/84562630/160881376-ce267b9f-8879-49f7-9c2e-824321015c75.png)

I open the source of this web 

![image](https://user-images.githubusercontent.com/84562630/160881590-c77504c8-7a74-4b65-b9c6-17d048fbc418.png)

I will add the "/hidden" at the end of the home URL 

![image](https://user-images.githubusercontent.com/84562630/160881879-049a2c45-d16e-4794-a447-8cd9c2051afd.png)


I continue open the source 

![image](https://user-images.githubusercontent.com/84562630/160882062-7324732b-513f-4fe1-9e81-476852f3d420.png)

Finally, i add "/superhidden" at the end of the home URL. 

![image](https://user-images.githubusercontent.com/84562630/160882688-193a21ac-af53-428f-9cbd-ed109b2bcfd3.png)

Then i open the source of it and get flag

![image](https://user-images.githubusercontent.com/84562630/160882816-8d8ea400-d2e0-4efd-8a52-d9dd4867195f.png)

## Flag
picoCTF{succ3ss_@h3n1c@10n_39849bcf}
