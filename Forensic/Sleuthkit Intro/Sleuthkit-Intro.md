# Sleuthkit Intro
## Problem: 
Download the disk image and use mmls on it find the size of the linux partion. 

  * https://artifacts.picoctf.net/c/114/disk.img.gz
  * Access checker program: nc saturn.picoctf.net 52279

## Solution: 
After downloading, i see a disk.img.gz file so i have to extract this file with "binwalk -e disk.img.gz " command line on the terminal. 

![sleuth2](https://user-images.githubusercontent.com/84562630/159443341-1ceee448-b71f-48cd-9d8a-4c02ee75b2c2.PNG)

It will have a new folder after unzipping. 

![sleuth3](https://user-images.githubusercontent.com/84562630/159443698-7abe4951-eaac-44d1-8612-95a7a2fd0b81.PNG)

i open that folder and see two file. 

![sleuth4](https://user-images.githubusercontent.com/84562630/159443932-d6c4fe58-1929-4b90-8965-7f73eca349f8.PNG)

i use a 'mmls -r disk.im' command line on the terminal and find size of the linux partion: 

![sleuth5-a](https://user-images.githubusercontent.com/84562630/159444379-5fd381a1-bcd6-40cc-b963-4aba60277098.PNG)

then i access to " nc saturn.picoctf.net 52279" and enter size on the above. 


![sleuth6](https://user-images.githubusercontent.com/84562630/159444782-cf8a43d3-864e-4189-b95b-ae4abddc1349.PNG)

## Flag: 
picoCTF{mm15_f7w!}

