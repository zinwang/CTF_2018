<br />

# CTF:編碼

=================================================

Base64<br /><br />
-------------------------------------------------

```
echo "QnJlYWtBTExDVEZ7NTN1c1pRM2hXVzI1ZGNoWjdkWGV9" |base64 -d
```


<br />
=================================================

Ascii<br /><br />
-------------------------------------------------

線上解:[https://www.dcode.fr/ascii-code](https://www.dcode.fr/ascii-code)
<br />


=================================================

Base32<br /><br />
-------------------------------------------------


```
echo "IJZGKYLLIFGEYQ2UIZ5TS6BUHA2VMUZXO5UWS5CCLJMFKVLIJVSX2===" | base32 -d
```

<br />

=================================================

Morse code<br /><br />
-------------------------------------------------

線上工具:[https://morsecode.scphillips.com/translator.html](https://morsecode.scphillips.com/translator.html)

<br />


=================================================

angstromCTF 2016 : what-the-hex<br /><br />
-------------------------------------------------

```
echo "6236343a20615735305a584a755a58526659323975646d567963326c76626c3930623239736331397962324e72" | xxd -r -p
```

`
b64: aW50ZXJuZXRfY29udmVyc2lvbl90b29sc19yb2Nr
`

```
echo "aW50ZXJuZXRfY29udmVyc2lvbl90b29sc19yb2Nr" | base64 -d
```

<br />



=================================================

alexctf-2017: CR1: Ultracoded<br /><br />
-------------------------------------------------

[zero_one.txt](http://120.114.62.89/files/eaffd1f3c51a013ef637b0c27c274963/zero_one.txt)

C++:
```

```












































