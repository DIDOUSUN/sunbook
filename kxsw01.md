# 最新v2rayN windows 详细使用教程

  #### V2rayNG WIN客户端APP下载

 >客户端目前支持 Xray Vmess Vless XTLS

 >V2rayN项目：[GitHub 链接](https://github.com/2dust/v2rayN)

 >4.20 v2rayN windows：[点击下载](https://github.com/2dust/v2rayN/releases/download/4.20/v2rayN-Core.zip)

#### win10安装V2rayN后续设置

#### 自由切换和更新 v2ray ｜ Xray内核

 >检查更新—更新v2rayN 客户端版本、v2Ray核心/Xray核心即相关geo规则集文件（geosite、geoip）

 >![](https://i.imgur.com/s5jY1hE.jpg)
 
 >* **完成上述更新**

 #### **自由切换** v2ray 核心和Xray 核心，但默认是使用v2ray核心和v2ray核心自带Geo规则集文件
 
 <font size="3" color="red"><b>P.S：如果你的Geo文件已经是最新或者最满意，在更新核心的适合，可以勾选“更新Core是忽略Geo文件”，即不更新Geo文件;</b></font>

![](https://i.imgur.com/51e5dXA.jpg)

#### **自定义和切换多个路由规则集**
 
 >需要手动选择“基础规则”，否则 成功启用 v2rayN  客户端后，所有入站数据都走代理出站（可以理解为全局代理模式）
 
 >“基础规则“=绕过大陆IP 模式：在Geo规则集中的国内IP/网址/服务走本地直连；国外的IP/网址/服务走代理出站（通过客户端添加的节点访问）

 >![](https://i.imgur.com/f6Gmdz4.jpg)
 使用“启用路由高级功能”，使用默认的绕过大陆路由规则集或者按自己不同的需求，增加多个路由规则集并切换使用
 >* **启用默认的“绕过大陆路由规则集“（推荐使用）**

 >![](https://i.imgur.com/XulniFp.jpg)

 >* **根据自身需求，添加"多个路由规则集"没有可以不用添加**

 >![](https://i.imgur.com/dDtEcTE.jpg)
 
 >* **点击客户端图标，可以“随意切换并使用不同路由规则集”**

 >![](https://i.imgur.com/xAHHj9P.jpg)

#### 系统代理

**系统代理的功能是把windows系统部分软件(比如浏览器)流量转到v2ray的http入口**

* 清除系统代理:每次启动/重启服务的时候,强制把windows系统(ie)的代理清除掉

* 自动配置系统代理:每次启动/重启服务的时候,强制设定windows系统(ie)的代理 （推荐使用）

* 不改变系统代理:每次启动/重启服务的时候,什么都不做.作用就是保留其他软件设定的代理


