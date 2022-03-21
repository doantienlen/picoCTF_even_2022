# File-run2 
## Problem: 
Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"?
Download the program https://artifacts.picoctf.net/c/351/run

## Solution: 

I will download that file. i have tried a few ways as string, binwalk, exiftool, but it doesn't work. 
I use to chmod +x run command and then use ./run, but it doesn't work. 
The question has a hint that "if you try to run it on the command line input "Hello!"". So i will run it with ./run Hello! command line. 

![run2](https://user-images.githubusercontent.com/84562630/159240286-1dd9e288-6246-4bc4-b3c6-aa8a4b98db6e.PNG)

## Flag: 
picoCTF{F1r57_4rgum3n7_be0714da}  
