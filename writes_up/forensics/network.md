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
1.用wireshark 打開
2.尋找http
發現東西了!

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/2018-05-20%2021-14-55%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />

3.右鍵>follow>tcpstream

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/forensics/pics/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(183).png)

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
用base64試試
flag就出來了!
CTF{betterfs.than.yours}
<br />


===========================================================

PicoCTF_2017: Special Agent User<br /><br />
-----------------------------------------------------------


Mozilla/5.0 (X11; OpenBSD i386) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/36.0.1985.125 Safari/537.36

<br />
===========================================================

hitcon-2017:Data & Mining<br /><br />
-----------------------------------------------------------

```
strings traffic-1b2b39e2c2231e6b98c77700da047b78.pcapng |grep hitcon
```

```
{"method":"login","params":{"login":"45duiDz79Y2AtSZH2pw9uV8YXmvtAT8tVNAYrfKTUnYiQZT5BMdRrGD4hbipmZ5DoaQXLak9ENEwYNC7kVk3ivDyMHyZCVV","pass":"hitcon{BTC_is_so_expensive_$$$$$$$}","agent":"xmr-stak-cpu/1.3.0-1.5.0"},"id":1}
```

<br /><br />









































































































