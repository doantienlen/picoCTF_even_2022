# unpackme
## Description 
Can you get the flag? 

Reverse engineer this https://artifacts.picoctf.net/c/365/unpackme-upx

Hints: What is the UPX? 
## Solution 
I use the 'strings unpackme-upx' command. I can't find the flag but i do see the 'UPX!' at the end! 

![image](https://user-images.githubusercontent.com/84562630/162611465-bad1e41b-442b-4495-9433-43cd335487ba.png)

I have to decompress it using the upx command. 

![image](https://user-images.githubusercontent.com/84562630/162611540-a4bec4ed-656c-48db-b87f-e69592218fcf.png)

I use the 'chomd +x file name' to run the unpackme-upx. After running, it asks " What's my favorite number?". 
So i will use the Ghidra to disassemble the binary: 
```ghira

undefined8
main(undefined8 param_1,undefined4 param_2,undefined4 param_3,undefined4 param_4,undefined4 param_5,
    undefined4 param_6,undefined4 param_7,undefined4 param_8)

{
  undefined8 in_RCX;
  ulong uVar1;
  undefined8 extraout_RDX;
  undefined8 extraout_RDX_00;
  undefined8 extraout_RDX_01;
  undefined8 uVar2;
  undefined in_SIL;
  int *piVar3;
  char *pcVar4;
  mbstate_t in_R8;
  mbstate_t in_R9;
  long in_FS_OFFSET;
  undefined4 extraout_XMM0_Da;
  int local_44;
  char *local_40;
  undefined8 local_38;
  undefined8 local_30;
  undefined8 local_28;
  undefined4 local_20;
  undefined2 local_1c;
  ulong local_10;
  
  local_10 = *(ulong *)(in_FS_OFFSET + 0x28);
  local_38 = 0x4c75257240343a41;
  local_30 = 0x30623e306b6d4146;
  local_28 = 0x3532666630486637;
  local_20 = 0x36665f60;
  local_1c = 0x4e;
  printf((undefined4)param_1,"What\'s my favorite number? ");
  piVar3 = &local_44;
  __isoc99_scanf(extraout_XMM0_Da,param_2,param_3,param_4,param_5,param_6,param_7,param_8,
                 &DAT_004b3020,piVar3,extraout_RDX,in_RCX,in_R8,in_R9,in_SIL);
  if (local_44 == 0xb83cb) {
    local_40 = rotate_encrypt(0,(char *)&local_38);
    piVar3 = (int *)stdout;
    fputs(local_40,(FILE *)stdout);
    putchar(10);
    pcVar4 = local_40;
    free(local_40);
    uVar2 = extraout_RDX_00;
  }
  else {
    pcVar4 = "Sorry, that\'s not it!";
    puts("Sorry, that\'s not it!");
    uVar2 = extraout_RDX_01;
  }
  uVar1 = local_10 ^ *(ulong *)(in_FS_OFFSET + 0x28);
  if (uVar1 != 0) {
                    /* WARNING: Subroutine does not return */
    __stack_chk_fail(pcVar4,piVar3,uVar2,uVar1,in_R8,in_R9);
  }
  return 0;
}


```
From the decompiled code, we can see after it was for favorite number,
```ghidra
if (local_44 == 0xb83cb) {
    local_40 = rotate_encrypt(0,(char *)&local_38);
    piVar3 = (int *)stdout;
    fputs(local_40,(FILE *)stdout);
    putchar(10);
    pcVar4 = local_40;
    free(local_40);
    uVar2 = extraout_RDX_00;
  }
```

Now i will covert "0xb83cb" to dcimal by https://www.hexadecimaldictionary.com/hexadecimal

Then  i use "chmod +x unpackme-upx" on the terminal to be able to run it. 

![image](https://user-images.githubusercontent.com/84562630/161234640-8b7353a7-a97e-48df-909a-842ddc5f70b1.png)

## Flag 
picoCTF{up><_m3_f7w_77ad107e}
