# unpackme.py
## Problem: 
Can you get the flag? Reverse engineer this https://artifacts.picoctf.net/c/464/unpackme.flag.py
## Solution: 
After downloanding, i try to run unpackme.flag.py code on the terminal. What is the password?
i open that file by sumbtext. 
```python 
import base64
from cryptography.fernet import Fernet



payload = b'gAAAAABiMD04m0Z6CohVV7ozdwHqtgc2__CuAFGG8rWhZBTL0lhfzp-mhu9LYNMnMQMGO-7tEwy3DJ2Y8yjogvzyojFETwN9YEIPXTnO9F1QnkPypWTgjISGve4gcSerJMs694oKcIdKHuVaSxOg1MMNs5k9iPaBIPU7xOKQqCyhnf_f4yUvLdMcer38BqRptocJNvKlyWN8h7ikoWL0zlssxd8OJyPujMz78HZaefvUouvq6LDtPVqRBJFPgSJYf1nHpHKFa1O0zJ6UpTe6ba3PPAxCVXutNg=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())
f = Fernet(key_base64)
plain = f.decrypt(payload)
exec(plain.decode())
```
if you don't know about Fernet in python. You can watch it here https://www.geeksforgeeks.org/fernet-symmetric-encryption-using-cryptography-module-in-python/
then i run the below code which i edited it. 
```python 
import base64
from cryptography.fernet import Fernet



payload = b'gAAAAABiMD04m0Z6CohVV7ozdwHqtgc2__CuAFGG8rWhZBTL0lhfzp-mhu9LYNMnMQMGO-7tEwy3DJ2Y8yjogvzyojFETwN9YEIPXTnO9F1QnkPypWTgjISGve4gcSerJMs694oKcIdKHuVaSxOg1MMNs5k9iPaBIPU7xOKQqCyhnf_f4yUvLdMcer38BqRptocJNvKlyWN8h7ikoWL0zlssxd8OJyPujMz78HZaefvUouvq6LDtPVqRBJFPgSJYf1nHpHKFa1O0zJ6UpTe6ba3PPAxCVXutNg=='

key_str = 'correctstaplecorrectstaplecorrec'
key_base64 = base64.b64encode(key_str.encode())
# 
# print(key_base64)
#
f = Fernet(key_base64)
plain = f.decrypt(payload)
print(plain)
#exec(plain.decode())
```
i saw the flowing flag when i ran: 

![unpakme2](https://user-images.githubusercontent.com/84562630/159293903-f0ecee4b-4a4c-44c2-9bb1-aacf88b46879.PNG)
## Flag: 
picoCTF{175_chr157m45_5274ff21}

