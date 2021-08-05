# SSL TLS 证书申请

---

### 准备工作
>域名注册([点击这里](https://www.freenom.com))
>
>托管域名到 Cloudflare，提前做好解析（[点击这里](https://dash.cloudflare.com)）
>
>后面 ACME 脚本申请证书，需要安装以后才可以进行使用，禁止直接使用 ACME 目录下面的证书文件

### Acme 脚本申请证书
Acme 脚本申请证书，是我们用到的最常见的一种证书的申请方式，它有很多的申请方法，大家只需要找到一种适合自己的也就好了。

不管用下面的何种方式申请，都需要安装 Acme，有一部分的申请场景需要用到相关的插件，所以我们需要提前安装。

下面环境的安装方式，大家根据自己的系统选择命令安装就好了。
>```
>apt update -y          #Debian/Ubuntu 命令
>```
>```
>apt install -y curl    #Debian/Ubuntu 命令
>```
>```
>apt install -y socat    #Debian/Ubuntu 命令
>```
>```
>yum update -y          #CentOS 命令
>```
>```
>yum install -y curl    #CentOS 命令
>```
>```
>yum install -y socat    #CentOS 命令
>```
### 安装 Acme 脚本
>```
>curl https://get.acme.sh | sh
>```

### 重要申明

2021 年 6 月 17 日更新：

从 acme.sh v 3.0.0 开始，acme.sh 使用 Zerossl 作为默认 ca，您必须先注册帐户（一次），然后才能颁发新证书。

具体操作步骤如下：

1、安装 Acme 脚本之后，请先执行下面的命令（下面的邮箱为你的邮箱）
`~/.acme.sh/acme.sh --register-account -m xxxx@xxxx.com`

2、其他的命令暂时没有变动

### 80 端口空闲的验证申请
如果你还没有运行任何 web 服务, 80 端口是空闲的, 那么 Acme.sh 还能假装自己是一个 WebServer, 临时监听在 80 端口, 完成验证
>```
>~/.acme.sh/acme.sh  --issue -d mydomain.com   --standalone
>```

![](https://i.imgur.com/Q76QuLs.png)

### 安装证书到指定文件夹
注意, 默认生成的证书都放在安装目录下: ~/.acme.sh/, 请不要直接使用此目录下的证书文件。
正确的使用方法是使用 --install-cert 命令,并指定目标位置, 然后证书文件会被copy到相应的位置，比如下面的代码
>```
>~/.acme.sh/acme.sh --installcert -d mydomain.com --key-file /root/private.key --fullchain-file /root/cert.crt
>```
![](https://i.imgur.com/dA0OnBz.png)

上面的 /root/private.key 以及 /root/cert.crt 是把密钥和证书安装到 /root 目录，并改名为 private.key 和 cert.crt

### 更新 Acme 脚本
* **升级 Acme.sh 到最新版本**
>```
>~/.acme.sh/acme.sh --upgrade
>```

* **如果你不想手动升级, 可以开启自动升级:**
>```
>~/.acme.sh/acme.sh  --upgrade  --auto-upgrade
>```
之后, acme.sh 就会自动保持更新了.

### 更新证书
目前证书在 60 天以后会自动更新, 你无需任何操作. 今后有可能会缩短这个时间, 不过都是自动的, 你不用关心.

