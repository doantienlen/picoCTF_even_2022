# patchme.py
## Problem: 
Can you get the flag? Run this https://artifacts.picoctf.net/c/386/patchme.flag.py in the same directory as this https://artifacts.picoctf.net/c/386/flag.txt.enc

First, i will download 2 that files in the same directory.
I run with python3 by python3 patchme.flag.py command on terminal.

![patch1](https://user-images.githubusercontent.com/84562630/159281667-cdf362c6-49c0-46d9-9398-48d0cc66da20.PNG)

It will request enter the password, so i thing i will open pathcme.flag.py on the sumbline text.
After reading the code i see the pass is 
```python 
user_pw == "ak98" + \
            "-=90" + \
            "adfjhgj321" + \
            "sleuth9000")
```
i will link them together:
                           password= ak98-=90adfjhgj321sleuth9000 
Then i will run code and enter pass this: 

![ptch3](https://user-images.githubusercontent.com/84562630/159283504-184b4c25-bda1-4131-910a-587119102590.PNG)

# Flag: 
picoCTF{p47ch1ng_l1f3_h4ck_c4a4688b}
