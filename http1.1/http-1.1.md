# http1.1 share
* author：pighead
* time：2017/1/21
* version：1.0.0
* email：zhuhuanhuan@qccr.com
---
## 说明
* HTTP使用的是可靠的数据传输协议，因为基于TCP
* HTTP的无状态
* web服务器是web资源的宿主，HTTP的方法
* Internet的多媒体信使，因为它包含不同的数据类型
* URI：URL和URN
* 状态码
* 各种Header
* web的结构组件：代理，缓存，网关，隧道

---
## HTTP报文格式
* 请求报文
* 响应报文
---
## Cookie
* 解决HTTP访问的无状态问题，能够识别用户，跟踪用户
* 域名的问题
* 服务端，客户端对Cookie的设置与使用
* 自身的问题
---
## web缓存
---
## DNS
* DNS的网络流量和DNS的平均时延
---
## P2P
---
## SPDY与Http2做了哪些改进
* 降低延迟
* 头部压缩：user-agent,cookie膨胀
* server push

---
## android端的问题
* 对于使用webview的app来说，需要基于chrome内核的webview才能支持spdy和http2.0，而android系统的webview是从android4.4（KitKat）才改成基于chrome内核的。

* 对于使用native api调用的http请求来说，okhttp是同时支持spdy和http2.0的可行方案。如果使用ALPN，okhttp要求android系统5.0+(实际上，android4.4上就有了ALPN的实现，不过有bug，知道5.0才正式修复)，如果使用NPN，可以从android4.0+开始支持，不过NPN也是属于将要被淘汰的协议。