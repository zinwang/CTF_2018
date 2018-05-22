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

int main(int argc, char const *argv[])
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















































