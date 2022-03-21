# Bloat.py
## Problem: 
Can you get the flag?
Run this https://artifacts.picoctf.net/c/428/bloat.flag.py in the same directory as this https://artifacts.picoctf.net/c/428/flag.txt.enc
## Solution: 
Code of the problem: 

I run bloat.flag.py code on the sumbtext. It reports some error: 

![bloat2](https://user-images.githubusercontent.com/84562630/159296632-30575477-7bc7-41bb-b708-173a98673b50.PNG)

After reading the code. I noticed that the funciton arg132 contains a flag, and the arg444 varible of the arg111 funtion is used for decoding. 
Below varrable arg444 has been signed to are132 funcion, now just need to call arg111 funcition to decode this code. 
```python
import sys
a = "!\"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ"+ \
            "[\\]^_`abcdefghijklmnopqrstuvwxyz{|}~ "
def arg133(arg432):
  if arg432 == a[71]+a[64]+a[79]+a[79]+a[88]+a[66]+a[71]+a[64]+a[77]+a[66]+a[68]:
    return True
  else:
    print(a[51]+a[71]+a[64]+a[83]+a[94]+a[79]+a[64]+a[82]+a[82]+a[86]+a[78]+\
a[81]+a[67]+a[94]+a[72]+a[82]+a[94]+a[72]+a[77]+a[66]+a[78]+a[81]+\
a[81]+a[68]+a[66]+a[83])
    sys.exit(0)
    return False
def arg111(arg444):
  return arg122(arg444.decode(), a[81]+a[64]+a[79]+a[82]+a[66]+a[64]+a[75]+\
a[75]+a[72]+a[78]+a[77])
def arg232():
  return input(a[47]+a[75]+a[68]+a[64]+a[82]+a[68]+a[94]+a[68]+a[77]+a[83]+\
a[68]+a[81]+a[94]+a[66]+a[78]+a[81]+a[81]+a[68]+a[66]+a[83]+\
a[94]+a[79]+a[64]+a[82]+a[82]+a[86]+a[78]+a[81]+a[67]+a[94]+\
a[69]+a[78]+a[81]+a[94]+a[69]+a[75]+a[64]+a[70]+a[25]+a[94])
def arg132():
  return open('flag.txt.enc', 'rb').read()
def arg112():
  print(a[54]+a[68]+a[75]+a[66]+a[78]+a[76]+a[68]+a[94]+a[65]+a[64]+a[66]+\
a[74]+a[13]+a[13]+a[13]+a[94]+a[88]+a[78]+a[84]+a[81]+a[94]+a[69]+\
a[75]+a[64]+a[70]+a[11]+a[94]+a[84]+a[82]+a[68]+a[81]+a[25])
def arg122(arg432, arg423):
    arg433 = arg423
    i = 0
    while len(arg433) < len(arg432):
        arg433 = arg433 + arg423[i]
        i = (i + 1) % len(arg423)        
    return "".join([chr(ord(arg422) ^ ord(arg442)) for (arg422,arg442) in zip(arg432,arg433)])
arg444 = arg132()
## 
print(arg111(arg444)) # print the flag
##
# arg432 = arg232()
# arg133(arg432)
# arg112()
# arg423 = arg111(arg444)
# print(arg423)

sys.exit(0)

```
![bloat3](https://user-images.githubusercontent.com/84562630/159299338-8f359b76-1408-4afe-a8cc-2743c5dd83be.PNG)
## Flag
picoCTF{d30bfu5c4710n_f7w_b8062eec}

