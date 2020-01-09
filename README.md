# IPv4转IPv6隧道& BYRBT使用及utorrent配置

使用IPv4网络访问纯IPv6的网站，比如某些校园网BT站。

## I. 创建隧道

1. 注册Tunnel Broker并登陆
   注册tunnel broker账号，注册页 https://www.tunnelbroker.net/
   ![login](/pic/login.jpg)
   
   用邮箱里收到的用户名和密码登录


2. 点击Create Regular Tunnel
   ![Create Regular Tunnel](/pic/create.jpg)

3. 百度搜索“ip地址”，将本机IP地址填入ipv4 endpoint，下方选择最近的节点   
   ![IP地址](/pic/ip.jpg)
   ![Create Regular Tunnel](/pic/create2.jpg)


## II. 本地配置

1. 选择Example Configurations

   ![Example Configurations](/pic/Configurations.png)

2. 选择你的操作系统类型，可以看到配置指令
   注意如果使用了路由器，要将外网IP换为内网IP
   
   > windos内网IP查看方式：<br/>
   > 1. WIN键(windows键)+R键,输入"cmd"，确定，调出命令提示符<br/>
   > 2. 在命令提示符里输入“ipconfig"回车，"IPv4地址"即是本机的内网IP地址
   
   ![Example Configurations](/pic/system.png)

3. 在本机上执行上面的命令
   > windos下：<br/>
   > 1.WIN键(windows键)+R键,输入"cmd"，确定，调出命令提示符<br/>
   > 2.输入对应系统的配置指令

## III. 使用BYRBT

1. 配置完成后应该就可以登陆到BYRBT的网站 https://bt.byr.cn/
2. 使用utorrent下载种子时可能无法下载，因为DNS无法解析
   > 需要手动在hosts文件("c:\windows\system32\drivers\etc\hosts")中添加 <br/>
   > 2001:da8:215:4078:250:56ff:fe97:654d tracker.byr.cn
