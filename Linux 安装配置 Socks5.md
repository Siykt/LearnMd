# Linux 安装配置 _Socks5_

准备工具

> OS: CentOS7 等 Linux 环境
>
> common：wget

1. 下载官方 Socks 包

   `$wget http://downloads.sourceforge.net/project/ss5/ss5/3.8.9-8/ss5-3.8.9-8.tar.gz`

2. 安装依赖

   `$yum install pam-devel openldap-devel openssl-deve`

3. 解压 tar 压缩包

   `$tar -zxvf ss5-3.8.9-8.tar.gz`

   `$cd ss5-3.8.9`

4. 编译、安装

   `$./configure`

   `$make`

   `$make install`

5. 修改配置文件

   `$vim /etc/opt/ss5/ss5.conf`

   > ss5 默认使用 1080 端口，并允许任何人使用
   >
   > 在这里主要是修改对 ss5 开启用户验证
   >
   > ***
   >
   > auth 0.0.0.0/0 - - | auth 0.0.0.0/0 – **u**
   >
   > permit – 0.0.0.0/0 – 0.0.0.0/0 – – – – - | permit **u** 0.0.0.0/0 – 0.0.0.0/0 – – – – -

6. 添加用户验证

   `$vim /etc/opt/ss5/ss5.passwd`

   > 用户 密码
   >
   > test 123456

7. 修改端口（可选） => `$/usr/sbin/ss5 -t $SS5_OPTS -u root -b 0.0.0.0:port`
8. 启动 Socks

   > 默认情况 ss5 文件没有执行权限, chmod 加上 x 执行权限：
   >
   > `$chmod u+x /etc/rc.d/init.d/ss5`
   >
   > 或者将 /etc/sysconfig/ss5 中的 SS5_OPTS 取消注释:
   >
   > `$vim /etc/sysconfig/ss5`
   >
   > SS5_OPTS=” -u root”

   **start => /usr/sbin/ss5 -t \$SS5_OPTS -u root -b 0.0.0.0**

   **start => `/usr/sbin/ss5 -t $SS5_OPTS -u root -b 0.0.0.0`**

## 附加

> `$service ss5 status` _查询 Socks 运行状况_
>
> 一键安装脚本：
>
> `wget -q -N --no-check-certificate https://raw.githubusercontent.com/wyx176/Socks5/master/install.sh && bash install.sh`
