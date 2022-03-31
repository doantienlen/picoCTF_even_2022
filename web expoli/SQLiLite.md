# SQLiLite
## Description 
Can you login to this website? 
Try to login http://saturn.picoctf.net:51441/
## Solution 
I open this website. It asks for login username and password: 

![image](https://user-images.githubusercontent.com/84562630/160954350-54ae6005-ecf0-4779-997b-a5662e5e237c.png)

According to the title, username = "admin", so i only enter a password. I have a website  about the SQL security https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/

I try some password there

![image](https://user-images.githubusercontent.com/84562630/160954949-18faac17-66b4-4d11-94cd-3d1341a611b8.png)

The i open the source of this website 

![image](https://user-images.githubusercontent.com/84562630/160955011-f4e3758d-6340-4c9d-8a8d-f51011dd1143.png)
## Flag 
picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}
