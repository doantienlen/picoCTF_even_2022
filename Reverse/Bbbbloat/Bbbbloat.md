# Bbbbloat 
## Description 
Can you get the flag? 

Reverse engineer this https://artifacts.picoctf.net/c/301/bbbbloat
## Solution 
I will chomd to extract bbbloat file with "chmod +x bbbloat" on the terminal. 
I use Ghidra to disassemble this binary:
```code

undefined8 FUN_00101307(void)

{
  char *__s;
  long in_FS_OFFSET;
  int local_48;
  undefined8 local_38;
  undefined8 local_30;
  undefined8 local_28;
  undefined8 local_20;
  long local_10;
  
  local_10 = *(long *)(in_FS_OFFSET + 0x28);
  local_38 = 0x4c75257240343a41;
  local_30 = 0x3062396630664634;
  local_28 = 0x65623066635f3d33;
  local_20 = 0x4e326560623535;
  printf("What\'s my favorite number? ");
  __isoc99_scanf();
  if (local_48 == 0x86187) {
    __s = FUN_00101249(0,(char *)&local_38);
    fputs(__s,stdout);
    putchar(10);
    free(__s);
  }
  else {
    puts("Sorry, that\'s not it!");
  }
  if (local_10 != *(long *)(in_FS_OFFSET + 0x28)) {
                    /* WARNING: Subroutine does not return */
    __stack_chk_fail();
  }
  return 0;
}


```
From the decompiled code, we can see after it was for favorite number
```code 
  if (local_48 == 0x86187) {
    __s = FUN_00101249(0,(char *)&local_38);
    fputs(__s,stdout);
    putchar(10);
    free(__s);
  }
  else {
    puts("Sorry, that\'s not it!");
  }

```
I will convert "0x86187" to Decimal with https://www.hexadecimaldictionary.com/hexadecimal/ .Then i will run "./bbboat" with on the terminal and enter that Decimal. 

![image](https://user-images.githubusercontent.com/84562630/161197398-626678ff-b8ac-411c-a351-d8d48bc2ea3c.png)

## Flag 
picoCTF{cu7_7h3_bl047_36dd316a}


