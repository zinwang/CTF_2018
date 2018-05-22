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

angstromCTF 2016 : artifact-20<br />
Pico CTF 2014 : Substitution<br /><br />
---------------------------------------------------
超快線上解!<br />

[https://quipqiup.com](https://quipqiup.com)

<br />

===================================================

Vigenère cipher<br /><br />
---------------------------------------------------

C++:
```
#include <iostream>
#include <cstring>

using namespace std;

int main()
{
	char cipher[200];
	cin>>cipher;
	char key[30];
	cin>>key;
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

















