<br />

# CTF:Reverse

<br />


===========================================

Reverse-20<br /><br />
-------------------------------------------

輕而易舉!
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

```
unzip tmpBPWe7T.zip
java Authenticator

```

```
java Authenticator
```


```
root@kalib:~/Download# java Authenticator 
Enter password:

```




```
jad Authenticator.class
cat Authenticator.jad
```

```
// Decompiled by Jad v1.5.8e. Copyright 2001 Pavel Kouznetsov.
// Jad home page: http://www.geocities.com/kpdus/jad.html
// Decompiler options: packimports(3) 
// Source File Name:   Authenticator.java

import java.io.Console;
import java.io.PrintStream;

class Authenticator
{

    public Authenticator()
    {
    }

    public static void main(String args[])
    {
        key = new char[10];
        key[0] = 'A';
        key[1] = 'o';
        key[2] = 'J';
        key[3] = 'k';
        key[4] = 'V';
        key[5] = 'h';
        key[6] = 'L';
        key[7] = 'w';
        key[8] = 'U';
        key[9] = 'R';
        Console console = System.console();
        for(String s = ""; !s.equals("ThisIsth3mag1calString4458"); s = console.readLine("Enter password:", new Object[0]));
        for(int i = 0; i < key.length; i++)
            System.out.print(key[i]);

        System.out.println("");
    }

    public static char key[];
}

```



```
root@kalib:~/Download# java Authenticator 
Enter password:ThisIsth3mag1calString4458
AoJkVhLwUR
```

<br />

