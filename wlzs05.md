# R2S 详细安装教程

---

<img src="https://i.imgur.com/1Tbelyg.png" title="source: imgur.com" />

### 固件写盘工具

官网下载：[点击下载](http://rufus.ie/)&nbsp;&nbsp;&nbsp;Windows

官网下载：[点击下载](https://www.balena.io/etcher/)&nbsp;&nbsp;&nbsp;MAC <font size="3" color="red"><b>推荐使用</b></font>

### 骷髅头编译固件

2021.07.29 NanoPi R2S FusionWrt_稳定精简:[点击下载](https://github.com/DHDAXCW/NanoPi-R2S-2021/releases/download/2021.07.29-Lean3/openwrt-rockchip-armv8-friendlyarm_nanopi-r2s-squashfs-sysupgrade.img.gz)

[Github项目](https://github.com/DHDAXCW/NanoPi-R2S-2021)

版本默认后台192.168.2.1默认密码<mark>password</mark>

<img src="https://gblobscdn.gitbook.com/assets%2F-MOj4TndW1aJFvpWDOor%2F-M_-9_QIieEbr61l2c-W%2F-M_-9ytG8oxCEcKxUuO_%2F20%20(1).jpg?alt=media&token=a01908b6-e7bd-439f-87c1-f15f65437868
" height="auto" width="75%"/>

### 安装流程
  - 固件/写盘工具下载
  - 安装写盘工具
  - 固件写入TF卡
  - R2S 后台设置

<font size="3" color="red"><b>P·S：固件后缀名是<mark>img.gz</mark>不用解压直接可以用</b></font>

<img src="https://i.imgur.com/6JV2DPU.png" height="auto" width="75%"/>

- 打开写盘工具

<img src="https://i.imgur.com/2iGHSPQ.png" height="auto" width="75%"/>

<img src="https://i.imgur.com/Dd8A7al.png" height="auto" width="75%"/>

<img src="https://i.imgur.com/Wg41CkA.png" height="auto" width="75%"/>

<img src="https://i.imgur.com/ErcVQ1K.png" height="auto" width="75%"/>

- MAC系统需要输入管理员密码

<img src="https://i.imgur.com/TA7Sf38.png" height="auto" width="75%"/>

<img src="https://i.imgur.com/utSHsZM.png" height="auto" width="75%"/>

- 固件写入完成后，<mark>弹窗千万不要点格式化，</mark>点忽略就可以

<img src="https://i.imgur.com/mRy0mAa.png" height="auto" width="75%"/>

---

### R2S 设置

<img src="https://i.imgur.com/miCOD6c.jpg" height="auto" width="75%"/>

- 把刷写好OpenWrt固件的TF卡插入R2S，给R2S通电，SYS灯正常闪烁说明进入系统正常，如果常亮说明固件有问题，建议重新刷写。<font color="red">(温馨提示：不要热拔插TF卡，会导致系统崩溃) </font>

<img src="https://i.imgur.com/FyKK2ez.png" height="auto" width="75%"/>

- 用网线把R2S的LAN口与电脑的网口相连接，进入R2S的后台进行设置，初始默认后台：192.168.2.1 默认密码：password

<img src="https://i.imgur.com/jW8mJO3.png" height="auto" width="75%"
/>

<img src="https://i.imgur.com/DZSYA5q.png" height="auto" width="95%"/>

<font size="3" color="red"><b>P·S：如果默认后台进不去不要着急，可以找到电脑上的网络配置属性查看默认网关是多少</b></font>

<img src="https://i.imgur.com/7S5s9Qr.png" height="auto" width="75%"/>

- 进去后台就是OpenWrt的操作系统，首先进入系统左边栏的网络-接口进行设置
在接口总览里面，删除默认的WAN6接口(不删也没有关系，一般都是删掉不要)

<img src="https://i.imgur.com/4ha52km.png" height="auto" width="100%"/>

- 随后进如WAN口进行设置

<img src="https://i.imgur.com/mnlxz7i.png" height="auto" width="100%"/>

- 在WAN口的基本设置里面，如果你是<mark>光猫拨号</mark>的话一切都不用修改，默认协议就是DHCP

<img src="https://i.imgur.com/tcVXvGp.png" height="auto" width="100%"/>

- 如果你是光猫做桥接,可以参考[2021最新中国电信光猫超级密码获取方法](wlzs02.md)，<mark>软由器做拨号</mark>的话就要把协议改成PPPoE，填入自己的宽带账号和宽带密码，保存应用，注意：需要重启光猫。

<img src="https://i.imgur.com/uUL9y2W.png" height="auto" width="100%"/>

<img src="https://i.imgur.com/6mmRvrJ.png" height="auto" width="100%"/>

- 进去LAN口的高级设置，把默认的内置ipv6的钩给去掉，别的什么都不变。

<img src="https://i.imgur.com/K2K7HVh.png" height="auto" width="100%"/>

##### 完成以上所有设置后把R2S的LAN口网线连接电脑的那一端拔掉，再用网线连接光猫的千兆口到R2S的WAN口，进去R2S后台的接口总览查看WAN口是否有数据在动，判断是否可以正常上网。

<img src="https://i.imgur.com/xYJ5lN5.png" height="auto" width="100%"/>












