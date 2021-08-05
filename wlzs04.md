# 谷歌云连接FinalShell配置方法

---

### [官方网址](https://www.hostbuf.com/)
[Windows版下载地址](https://fox.didousun.workers.dev/finalshell_install.exe?rootId=0APzwBjv73RCPUk9PVA)

[MacOS版下载地址](https://fox.didousun.workers.dev/finalshell_install.pkg?rootId=0APzwBjv73RCPUk9PVA)
#### 准备新的谷歌云VPS主机一台
>1、使用gcp自带的浏览器shell登录vm实例
>
>2、首先切换用户为root用户 `sudo -i`
>
>3、为root用户设置密码passwd root输入两次root用户密码
 
Enter new UNIX password: 
 
Retype new UNIX password:
 
控制台会提示设置成功
>
>4、修改配置文件`vim /etc/ssh/sshd_config` 
>
>需要修改的配置项目如下，在32行和56行：PermitRootLogin yesPasswordAuthentication yes
>
>若使用centos则执行vim /etc/ssh/sshd_config 输入`vi` 修改PermitRootLogin yesPasswordAuthentication yes按`esc` 退出，输入`:wq`保存并退出vim执行重启服务器的操作`reboot`可生效，并且无需执行`/etc/init.d/ssh restart`这个命令
>
>5、重启服务

