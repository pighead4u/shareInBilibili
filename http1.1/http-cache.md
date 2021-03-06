# http-cache
* author: pighead4u
* time: 2017/02/13
* version: 1.0.0
* ![from disk cache](./image/fromdiskcache.png)
---
## 优点：
* 减少了冗余的数据传输
* 缓解了网络瓶颈的问题
* 降低了对原始服务器的要求
* 降低了距离时延
---
## 问题
* 过期
---
## Cache-Control（缓存存储策略）
*  Public：会缓存文件数据
*  Private：会缓存文件数据
*  no-cache：“不建议使用本地缓存”，其仍然会缓存数据到本地
*  max-age：会缓存文件数据，使用的是相对时间
*  no-store：不会在客户端缓存任何响应数据
### Pragma
*
## Expires（缓存过期策略）
* 用来确认存储在本地的缓存数据是否已过期，进而决定是否要发请求到服务端获取数据
* 指名了缓存数据有效的绝对时间，告诉客户端到了这个时间点（比照客户端时间点）后本地缓存就作废了，在这个时间点内客户端可以认为缓存数据有效，可直接从缓存中加载展示
## 缓存对比策略
* If-Modified-Since：对应响应头 Last-Modified
* If-None-Match：对应响应头 Etag

---
## 参考文章：
* 《HTTP权威指南》
* 彻底弄懂 Http 缓存机制：http://mp.weixin.qq.com/s/qOMO0LIdA47j3RjhbCWUEQ
* 浅谈浏览器http的缓存机制：http://www.cnblogs.com/vajoy/p/5341664.html
* web浏览器的缓存机制：http://www.alloyteam.com/2012/03/web-cache-2-browser-cache/
* https的七个误解：http://www.ruanyifeng.com/blog/2011/02/seven_myths_about_https.html
* MDN对http-cache的文档：https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching
* 官方文档：https://tools.ietf.org/html/rfc7234#section-5.3