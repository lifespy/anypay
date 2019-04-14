zfaka对接易付通教程(https://pay.anypay.me)

！以下所有操作都假设你已经去易付通后台注册过账户并且使用你的网址成功入网。

1.首先下载文件：

链接: https://pan.baidu.com/s/1Jmgqn4hNb9AyJ8Gi07eGUA   提取码: tksq

2.打开mysql控制台，执行数据库语句：

    INSERT INTO `faka`.`t_payment` (`id`, `payment`, `payname`, `payimage`, `alias`, `sign_type`, `app_id`, `app_secret`, `ali_public_key`, `rsa_private_key`, `configure3`, `configure4`, `overtime`, `active`) VALUES ('12', '易付通(支付宝)', '支付宝', '/res/images/pay/alipay.jpg', 'anypayalipay', 'MD5', '', '', '', '', '', '', '0', '0');
    

3.进入zfaka后台:

a.设置中心-->配置中心

切换到第三页左右，找到参数名为【weburl】的配置项，点击编辑，将值修改为你当前 网站的地址，然后点击确认修改。

b.设置中心-->支付设置

找到支付渠道为【易付通(支付宝)】，点击编辑，修改里面的【secret】和【accesskey】为易付通后台对应网址的配置。

然后将异步通知地址设置为你想通知的地址，如果只有一个域名，则直接填写当前域名。注意带上http或者https协议头，例如http://fk.dev.pi.do/

是否激活选择为激活状态。

然后确认修改。就可以正常使用了
