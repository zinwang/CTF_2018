
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
dd command<br />

`
dd if=carter.jpg of=carter87.jpg skip=140147 bs=1
`

<br />

![](https://github.com/zinwang/ctf/blob/master/writes_up/forensics/pics/2018-05-18%2021-11-35%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

result:<br />
![](https://github.com/zinwang/ctf/blob/master/writes_up/forensics/pics/carter87.jpg)






<br />
solution 2: foremost

`
foremost carter.jpg
`
<br /><br />

=====================================================

BITSCTF 2017 : black-hole-10<br /><br />
-----------------------------------------------------
strings指令
```
strings black_hole.jpg
```
會發現
UQklUQ1RGe1M1IDAwMTQrODF9
這段特別長特別令人起疑<br />
於是假設他是base64<br />
因為這是BITSCTF<br />
所以試試base64加密BITSCTF<br />
結果QklUU0NURg==<br />
由此可知此段base64從Q開始，U是多餘的<br />
即QklUQ1RGe1M1IDAwMTQrODF9<br />
base64解碼:<br />
BITCTF{S5 0014+81}


=====================================================

CSAW Quals CTF 2013: Black & White<br /><br />
-----------------------------------------------------

stegslove隱寫分析神器: [http://kmb.ufoctf.ru/stego/stegsolve/main.html](http://kmb.ufoctf.ru/stego/stegsolve/main.html)

install:
```
wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
chmod +x stegsolve.jar
```
use:
```
java -jar stegslove.jar
```



=====================================================

CSAW QUALS 2015: keep-calm-and-ctf<br /><br />
-----------------------------------------------------

exiftool:[http://owl.phy.queensu.ca/~phil/exiftool](http://owl.phy.queensu.ca/~phil/exiftool)<br />

```
exiftool img.jpg
```

```
ExifTool Version Number         : 10.77
File Name                       : img.jpg
Directory                       : /root
File Size                       : 92 kB
File Modification Date/Time     : 2018:04:22 23:59:22+08:00
File Access Date/Time           : 2018:05:18 22:33:10+08:00
File Inode Change Date/Time     : 2018:04:23 00:01:43+08:00
File Permissions                : rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
X Resolution                    : 72
Y Resolution                    : 72
Exif Byte Order                 : Big-endian (Motorola, MM)
Resolution Unit                 : inches
Y Cb Cr Positioning             : Centered
Copyright                       : h1d1ng_in_4lm0st_pla1n_sigh7
Image Width                     : 600
Image Height                    : 700
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 600x700
Megapixels                      : 0.420
```








=====================================================

CSAW QUALS 2015: keep-calm-and-ctf<br /><br />
-----------------------------------------------------
strings指令
```
strings just_open_it.jpg |grep CTF
```



=====================================================

ABCTF 2016 : gz-30<br /><br />
-----------------------------------------------------

```
mv flag flag.gz #把flag改成gz檔
gzip -d flag.gz #解壓gz
```



ABCTF 2016 : best-ganondorf-50













































ABCTF 2016 : best-ganondorf-50

xxd ezmonay.jpg |head -5

檢查file signature

`
printf '\xdd\xd8\xff' | dd of=ezmonay.jpg seek=0 bs=1 conv=notrunc
`
xxd ezmonay.jpg |head -5
在檢查一次

