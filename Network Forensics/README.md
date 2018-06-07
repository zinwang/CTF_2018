<br />

# CTF: Forensics-Network

<br /><br />

=========================================

BITSCTF 2017 : woodstock-1-10<br /><br />
-----------------------------------------
萬能strings 
```
strings ws1_2.pcapng |grep CTF
```
<br />
==================================================

CSAW Quals CTF 2013: Networking 1<br /><br />
--------------------------------------------------

```
strings networkingOK.pcap 
```
<br />
===========================================================

Internetwache-CTF-2016:Network Forensic<br /><br />
-----------------------------------------------------------
1.用wireshark 打開<br />
2.尋找http<br />
發現東西了!

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/2018-05-20%2021-14-55%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />

3.右鍵>Follow>TCP Stream

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(183).png)

<br />

4.

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(185).png)

<br />

5.另存為flag.zip<br />
6.
```
unzip flag.zip
```
<br />
需要密碼

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/2018-05-20%2021-22-09%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />
7.往回找封包，一樣找http<br />
找到密碼!

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/2018-05-20%2021-25-37%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />
得到flag!!!

<br />

===========================================================

google-ctf-2016:Network Forensic<br /><br />
-----------------------------------------------------------

```
strings no-big-deal.pcap
```
注意到這行特別可疑
```
Q1RGe2JldHRlcmZzLnRoYW4ueW91cnN9
```
用base64試試<br />
flag就出來了!<br />
CTF{betterfs.than.yours}
<br />


===========================================================

PicoCTF_2017: Special Agent User<br /><br />
-----------------------------------------------------------
他要問的是user-agent<br />
所以封包裡找找
```
Mozilla/5.0 (X11; OpenBSD i386) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/36.0.1985.125 Safari/537.36
```
然後他有要求
```
 We're just looking for up to 3 levels of subversions for the browser version (ie. Version 1.2.3 for Version 1.2.3.4) and ignore any 0th subversions (ie. 1.2 for 1.2.0)
 ```
 所以flag是<br />
```
 Chrome 36.1985.125
```
<br />
===========================================================

hitcon-2017:Data & Mining<br /><br />
-----------------------------------------------------------

```
strings traffic-1b2b39e2c2231e6b98c77700da047b78.pcapng |grep hitcon
```

答案出現!
```
{"method":"login","params":{"login":"45duiDz79Y2AtSZH2pw9uV8YXmvtAT8tVNAYrfKTUnYiQZT5BMdRrGD4hbipmZ5DoaQXLak9ENEwYNC7kVk3ivDyMHyZCVV","pass":"hitcon{BTC_is_so_expensive_$$$$$$$}","agent":"xmr-stak-cpu/1.3.0-1.5.0"},"id":1}
```

<br /><br />









































































































