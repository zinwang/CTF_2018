
# CTF:Forensics


=====================================================

sCTF 2016 Q1 : banana-boy-20<br /><br />
-----------------------------------------------------



solution 1: binwalk&&dd

```
binwalk carter.jpg
```

<br />
output:

```
DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01
382           0x17E           Copyright string: "Copyright (c) 1998 Hewlett-Packard Company"
3192          0xC78           TIFF image data, big-endian, offset of first image directory: 8
140147        0x22373         JPEG image data, JFIF standard 1.01
140177        0x22391         TIFF image data, big-endian, offset of first image directory: 8

```

<br/>
dd command

`
dd if=carter.jpg of=carter87.jpg skip=140147 bs=1
`

<br />

![](https://github.com/zinwang/ctf/blob/master/writes_up/forensics/pics/2018-05-18%2021-11-35%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)








































































ABCTF 2016 : best-ganondorf-50

xxd ezmonay.jpg |head -5

檢查file signature

`
printf '\xdd\xd8\xff' | dd of=ezmonay.jpg seek=0 bs=1 conv=notrunc
`
xxd ezmonay.jpg |head -5
在檢查一次

