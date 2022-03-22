# morse-code 
## Problem: 
Morse code is well know. Can you decrypt this? 

Download the file https://artifacts.picoctf.net/c/235/morse_chal.wav

Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase. 
## Solution: 
After downloading, i see a morse_chal.wav file. 

I decrypt it by using this tool online https://morsecode.world/international/decoder

![morse1](https://user-images.githubusercontent.com/84562630/159509352-545be302-f163-4ff6-b25b-94811f5b90b1.PNG)

That is not the flag, beause at the request of the order post, spaces are replaced by underscore and letters are lowercase. 

So i use below code to find the flag: 
```python
s = "WH47 H47H 90D W20U9H7"
x = s.replace(" ","_")
print(x.lower())

```
## Flag
picoCTF{wh47_h47h_90d_w20u9h7}
