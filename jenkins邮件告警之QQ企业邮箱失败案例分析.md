# jenkins邮件告警 -- QQ企业邮箱失败案例分析
## 目录
    1、问题分析
    2、jenkins邮件告警的基本设置
    3、qq邮箱的基本设置
    4、jenkins邮件告警关于qq邮件的设置分析
    5、jenkins邮件告警 -- qq邮件的设置
    6、问题小结
    
## 问题分析：
* 1、jenkins邮件告警的基本设置
* 2、关于qq邮箱的基本设置
* 3、jenkins邮件告警关于qq邮件的设置分析
* 4、jenkins邮件告警 -- qq邮件的设置
* 5、问题小结

## jenkins邮件告警的基本设置
经过设置126邮箱的成功经验得知，主要是三个方面：
* 1、jenkins location的管理员邮件配置。
* 2、触发邮件邮件通知配置。
* 3、邮件设置部分。
    * 输入smtp服务器
    * 点击 advanced
    * 点击使用 Use SMTP Authentication
    * 输入需要的信息

涉及到邮箱的部分内容都要使用一致qq邮箱账号

## qq邮箱的基本设置
关于qq邮箱的基本设置主要涉及到三个方面：
* 1、qq账号的账户设置
* 2、客户端开启POP/SMTP服务设置
* 3、qq邮箱 授权码的安装设置

## jenkins邮件告警关于qq邮件的设置分析

关于qq邮件设置，很重要的一点就是，授权码的设置，在第三方软件上登录qq邮箱，或者使用qq邮箱发送信息，一定要使用授权码作为登录密码，使用QQ账号自己的登录密码是不成功的。
## jenkins邮件告警 -- qq邮件的设置
* 1、jenkins location 设置

系统管理 -- 系统设置 -- jenkins location
![](http://i.imgur.com/9CVeZOu.png)
* 2、Extended E-mail Notification 设置 

系统管理 -- 系统设置 -- Extended E-mail Notification

![](http://i.imgur.com/0kQkIot.png)

![](http://i.imgur.com/Yf1D0x7.png)

![](http://i.imgur.com/dcmDaa2.png)
* 3、邮件告警设置

系统管理 -- 系统设置 -- 邮件告警

![](http://i.imgur.com/PQp6LYv.png)

* 4、邮箱告警测试

系统管理 -- 系统设置 -- 邮件告警 -- 通过发送测试邮件测试配置

![](http://i.imgur.com/EdHPAih.png)


## 问题小结
### qq邮箱基本设置成功后，测试发送不成功
原因分析：
* 1、管理员账号和默认发送账号不一致。
* 2、smtp服务器设置不正确。
    * qq企业邮箱和普通qq邮箱的smtp服务器不一样。
* 3、qq邮箱设置的第三方软件登录的授权码输入错误。
    * 1、授权码过期。
    * 2、授权码手工输入错误。
    * 3、授权码复制携带多余空格。
    * 4、Extended E-mail Notification 和 邮件通知处关于密码的设置不一致。
* 4、其他原因。

## 参考资料
[1] [配置jenkins发送邮件](http://liuhongjiang.github.io/hexotech/2015/12/04/jenkins-send-email-after-build/)

[2] [客户端设置](http://service.exmail.qq.com/cgi-bin/help?id=28)

[3] [Jenkins进阶系列之邮件配置](http://www.cnblogs.com/zz0412/p/jenkins_jj_01.html)

[4] [jenkins配置QQ邮箱服务器](http://jingyan.baidu.com/article/e3c78d647d32bc3c4c85f5e5.html)
