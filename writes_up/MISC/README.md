<br />

# CTF:MICS

<br />


============================================

Secret@Scratch<br/><br/>
--------------------------------------------

[Dialga1234 - Johnny Boy](https://scratch.mit.edu/projects/108998724/#editor)

觀看改編樹>觀看程式頁面
仔細找找答案就出來了!

<br />







============================================

Breaking the PassWORd<br/><br/>
--------------------------------------------
分析一下

[bitwise.py](http://120.114.62.89/files/90ee4d3a57d1c15f79e4efa0f2d88f67/bitwise.py)

<br />

python建表,要考慮大小寫和數字<br />
一開始沒考慮到數字，花了一點時間

Python3:
```
#!/usr/bin/python3

import string

a=string.ascii_lowercase+string.ascii_uppercase+string.digits
verify_arr=[193, 35, 9, 33, 1, 9, 3, 33, 9, 225]

b={}

for x in range(len(a)):
    b[a[x]]=((((ord(a[x])<<5)|(ord(a[x])>>3))^111)&255)

d=''

for l in range(len(verify_arr)):
    for m in range(len(a)):
        if verify_arr[l]==b[a[m]]:
            d+=a[m]
print(d)

```























