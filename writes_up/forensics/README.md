======================

CTF:Forensics
----------------------


#Practice 1.#

#sCTF 2016 Q1 : banana-boy-20

solution 1: binwalk&&dd

`
binwalk carter.jpg
`






ABCTF 2016 : best-ganondorf-50

xxd ezmonay.jpg |head -5

檢查file signature

`
printf '\xdd\xd8\xff' | dd of=ezmonay.jpg seek=0 bs=1 conv=notrunc
`
xxd ezmonay.jpg |head -5
在檢查一次

