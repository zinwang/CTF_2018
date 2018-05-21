<br />

# CTF:Web101

<br /><br />


============================================

Web-1:source code<br /><br />
--------------------------------------------

右鍵>檢查原始碼或者F12
```

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <meta name="description" content="">
    <meta name="author" content="">
    <link rel="icon" href="images/favicon.ico">

    <title>BreakALL CTF</title>

    <link href="css/bootstrap.min.css" rel="stylesheet">

    <link href="css/signin.css" rel="stylesheet">
  </head>

  <body>

    <div class="container">

      <form class="form-signin"  method="post" action="index.html">
        <h3 class="form-signin-heading">BreakALL CTF</h3>
        <input type="text" id="inputUsername" class="form-control" name="name" placeholder="Username" >

        <input type="password" id="inputPassword" class="form-control" name="pw" placeholder="Password">
		
        <button class="btn btn-lg btn-primary btn-block" type="submit">登入</button>
	
      </form>

    </div> 

	<!-- BreakALLCTF{3xjVYR8dMetWQbwzYsLJ} -->

    <script src="js/ie10-viewport-bug-workaround.js"></script>
  </body>
</html>
```

<br />

============================================

web-2:Robots.txt<br /><br />
--------------------------------------------
網址後面加/robots.txt
```
120.114.62.89:2001/robots.txt
```

<br />
result:

```
User-agent: *
Disallow: /images
Disallow: /secret
```

所以就是120.114.62.89:2001/secret啦!<br />
找到flag.txt!<br />

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/2018-05-21%2021-16-17%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />





是一串16進位<br />

```
516e4a6c595774425445784456455a374e31463053304979546a5655624846425155563651334a36546b3939
```

轉成字串後是一串base64<br />

```
QnJlYWtBTExDVEZ7N1F0S0IyTjVUbHFBQUV6Q3J6Tk99
```

base64解碼<br />
BreakALLCTF{7QtKB2N5TlqAAEzCrzNO}<br />
答案出來了!<br />



============================================

web-3:Curl-1<br /><br />
--------------------------------------------

在GO按鈕的地方按右鍵>Copy Link Location

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(188).png)

<br />

使用curl

```
curl http://120.114.62.89:2014/index.php
```





<br />




============================================

Web-6:Burp Suite<br /><br />
--------------------------------------------

1.首先設定瀏覽器proxy<br />
Preferences>Advanced>Network>Settings

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/2018-05-21%2020-56-14%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/2018-05-21%2020-56-28%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />
2.確認Intercept is off
<br />
3.隨意輸入帳號密碼

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/2018-05-21%2020-58-48%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/2018-05-21%2020-58-57%20%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

<br />
4.Burp Suite
<br />
在POST發現東西了!
<br />
右鍵>Sent to Repeater

![](https://github.com/zinwang/CTF_write_ups/blob/master/writes_up/Web/pics/%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%20(186).png)

<br />
5.修改






