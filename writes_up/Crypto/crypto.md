<br/>

# CTF:Crypto


<br />

===================================================

ABCTF 2016 : ceasar-salad-10<br />
angstromCTF 2017:The Beginning<br /><br />
---------------------------------------------------

C++:
```
#include <iostream>
#include <cstring>
using namespace std;

int main()
{
		char a[1000];
		cin.getline(a,sizeof(a));
		for(int i=0;i<26;i++){
			char b[strlen(a)];
			for(int j=0;j<int(strlen(a));j++){
				if(a[j]>=97&&a[j]<=122){
					b[j]=char(122-(122-int(a[j])+i)%26);
				}
				else
					b[j]=a[j];
				cout<<b[j];
			}
			cout<<endl<<endl;

		}
	return 0;
}
```

<br />

===================================================

EasyCTF-2014:A Simple Cipher<br /><br />
---------------------------------------------------

C++:
```
#include <iostream>
#include <cstring>
using namespace std;

int main()
{
		char a[1000];
		cin.getline(a,sizeof(a));
		for(int i=0;i<26;i++){
			char b[strlen(a)];
			for(int j=0;j<int(strlen(a));j++){
				if(a[j]>=65&&a[j]<=90){
					b[j]=char(90-(90-int(a[j])+i)%26);
				}
				else
					b[j]=a[j];
				cout<<b[j];
			}
			cout<<endl<<endl;
		}
	return 0;
}
```

<br />


===================================================

angstromCTF 2017: Substitution Cipher<br />
angstromCTF 2016 : artifact-20<br />
Pico CTF 2014 : Substitution<br /><br />
---------------------------------------------------
超快線上解!<br />

[https://quipqiup.com](https://quipqiup.com)

<br />

===================================================

Vigenère cipher<br /><br />
---------------------------------------------------

因為題目提示"caesar is everything. But he took it to the next level."<br />
所以猜想KEY是caesar

C++:
```
#include <iostream>
#include <cstring>

using namespace std;

int main()
{
	char cipher[]="vhixoieemksktorywzvhxzijqni";
	char key[]="caesar";
	for(int i=0;i<int(strlen(cipher));i++){
		cipher[i]=char(122-(122-int(cipher[i])+int(key[i%strlen(key)])-97)%26);
		cout<<cipher[i];
	}
	return 0;
}
```

<br />
或者線上解!<br />

[https://www.guballa.de/vigenere-solver](https://www.guballa.de/vigenere-solver)

<br />


===================================================

RC3 CTF 2016 : salad-100<br /><br />
---------------------------------------------------

Python3:
```
#!/usr/bin/python3

import string

a=string.ascii_lowercase+string.ascii_uppercase+string.digits

c="7sj-ighm-742q3w4t"

for x in range(62):
    b=''
    for ch in c:
        if ch in a:
            b+=a[(a.index(ch)+x)%62]
        else:
            b+=ch
    print (b)

```


<br />




===================================================

AlexCTF2017: Fore1-Hit_the_core<br /><br />
---------------------------------------------------

strings 先看看

```
strings fore1.core
```
<br />
結果發現了這串，但不是答案

```
cvqAeqacLtqazEigwiXobxrCrtuiTzahfFreqc{bnjrKwgk83kgd43j85ePgb_e_rwqr7fvbmHjklo3tews_hmkogooyf0vbnk0ii87Drfgh_n kiwutfb0ghk9ro987k5tfb_hjiouo087ptfcv}
```

隱約可發現前面的ALEXCTF，而且間格都是5<br />
所以拿掉前三個字母，並且每間格5個字母打印出來


Python3:

```
#!/usr/bin/python3

a="AeqacLtqazEigwiXobxrCrtuiTzahfFreqc{bnjrKwgk83kgd43j85ePgb_e_rwqr7fvbmHjklo3tews_hmkogooyf0vbnk0ii87Drfgh_n kiwutfb0ghk9ro987k5tfb_hjiouo087ptfcv}"

b=''

for x in range(len(a)):
    if x%5==0:
        b+=a[x]
print(b)

```



<br />




C++:
```
#include <iostream>
#include <cstring>
using namespace std;


int main()
{
	char a[]="AeqacLtqazEigwiXobxrCrtuiTzahfFreqc{bnjrKwgk83kgd43j85ePgb_e_rwqr7fvbmHjklo3tews_hmkogooyf0vbnk0ii87Drfgh_n kiwutfb0ghk9ro987k5tfb_hjiouo087ptfcv}";
	for(int i=0;i<int(strlen(a));i+=5){
		cout<<a[i];
	}
	return 0;
}
```














