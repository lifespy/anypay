ssrpanel多域名/回调域名与网站访问域名不一致 的修改方法：

找到`app/Services/Gateway/YftPay.php`文件第82行

```
$notify_url = $request->getUri()->getScheme() . "://" . $request->getUri()->getHost() . "/payment/notify";
```



将其修改为

```
$notify_url = "http://yourdomain.com/payment/notify"; 
```

上面代码中http或https根据自己实际情况修改，且该域名必须在易付通后台入网过，配置文件里面的授权码也要与此域名对应
