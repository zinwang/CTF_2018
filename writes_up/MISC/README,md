<br />

# CTF:MICS

<br />

============================================

Breaking the PassWORd<br/><br/>
--------------------------------------------

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























