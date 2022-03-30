# SQL Direct
## Description 
Connect to this PostgreSQL sever and find the flag! 

psql -h saturn.picoctf.net -p 62502 -U postgres pico

Password: postgres
## Solution 

After accessing the server, i use "\?" command to see help. 

![image](https://user-images.githubusercontent.com/84562630/160799566-0a2ce936-028e-4e9c-b828-37a8f807d226.png)

I see the "\l" command to list databases. 

![image](https://user-images.githubusercontent.com/84562630/160799800-f848e90c-2c78-476f-9d2f-d8c49d8cadb2.png)

![image](https://user-images.githubusercontent.com/84562630/160800444-2b7d4eb8-9c8d-4e8d-b8c8-584f5d5b7cd8.png)

I use "\dt" command to list tables. Then, i use "SELECT * FROM flags" command to find the flag. 

![image](https://user-images.githubusercontent.com/84562630/160800740-509e67d2-2bb2-4bb2-bb98-4538479889e7.png)

## Flag
picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
