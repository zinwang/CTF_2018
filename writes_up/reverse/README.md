<br />

# CTF:Reverse

<br />


===========================================

Reverse-20<br /><br />
-------------------------------------------

```
strings reverse|grep CTF
```

<br />


===========================================

alexctf-2017: RE1: Gifted<br /><br />
-------------------------------------------

```
strings gifted|grep CTF
```

<br />

===========================================

HITCON CTF 2016 : welcome<br /><br />
-------------------------------------------
Python:
```
string_a="}FTC NOCTIH ot emocleW{noctih"
print(''.join(reversed(string_a)))
```
<br />

C++:
```
#include <iostream>
#include <cstring>

using namespace std;

int main(){
        char a[]="}FTC NOCTIH ot emocleW{noctih";

        for(int i=0;i<strlen(a)/2;i++){
                swap(a[i],a[strlen(a)-i-1]);
        }
        for(int i=0;i<strlen(a);i++){
                cout<<a[i];
        }
        return 0;

}

```


<br />

===========================================

Java! Java!<br /><br />
-------------------------------------------






