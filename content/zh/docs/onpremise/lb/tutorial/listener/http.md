---
title: "新建HTTP监听"
date: 2021-12-17T17:05:56+08:00
weight: 30
description: >
    新建HTTP协议的监听
---

HTTP协议适用于需要对请求的内容进行识别的应用，如Web应用、App服务等。用户可创建HTTP监听来转发开自客户端的HTTP请求。

1. 在左侧导航栏，选择 **_"网络/负载均衡/负载均衡实例"_** 菜单项，进入负载均衡实例页面。
2. 单击{{<oem_name>}}平台的实例名称项，进入实例详情页面。
2. 单击“监听”页签，进入监听页面。
3. 单击列表上方 **_"新建"_** 按钮，弹出新建负载均衡监听对话框，配置协议&监听相关参数。 
    - 名称：设置监听的名称。
    - 监听端口：用来接收请求并向后端服务器转发请求的端口，端口范围为1-65535。
    - 协议：支持监听TCP、UDP、HTTP、HTTPS协议，协议选择为“HTTP”。
    - 重定向：当用户发起HTTP访问请求时，配置重定向后将HTTP访问重定向到用户配置的重定向后的URL地址。当启用重定向后，无需配置后端服务器组以及健康检查以及与后端服务器相关的参数等。
    - 重定向方式：包括永久重定向（301）、临时重定向（302）、临时重定向（307）。
        - 永久重定向（301）：当用户请求的网址资源永久的迁移到了新的网址，可以使用永久重定向（301），使得用户访问旧网址时直接替换成重定向网址。
        - 临时重定向（302）：当用户请求的网址资源临时改变了位置，可以使用临时重定向，但是302只能实现GET到GET的重定向，非GET请求可能会重定向为GET请求。
        - 临时重定向（307）：当用户请求的网址资源临时改变了位置，可以使用临时重定向，307可以保持请求方法不变，如POST请求仍旧重定向为POST请求。
    - 重定向至：设置重定向后的URL地址。修改HTTP协议、域名（IP或IP+端口）、URL路径任意一项即可。例如，将HTTP请求强制通过HTTPS协议访问，此时将重定向至修改为HTTPS协议，其他留空即可。

    **高级设置**：默认隐藏，可根据需求进行配置。

    - 调度算法：设置负载均衡的调度算法。
        - 轮询(RR)：按照访问顺序依次将外部请求分发到后端服务器组。
        - 加权轮询(WRR)：权重值越高的后端服务器，被轮询到的次数（概率）也越高。
        - 加权最小连接数(WLC)：除了根据每台后端服务器设定的权重值来进行轮询，同时还考虑后端服务器的实际负载（即连接数）。当权重值相同时，当前连接数越小的后端服务器被轮询到的次数（概率）也越高。
        - 源IP一致性哈希(SCH)：基于源IP地址的一致性hash，相同的源地址会调度到相同的后端服务器。
    - 开启会话保持：选择是否开启会话保持，开启会话保持后，负载均衡监听会把来自同一客户端的请求分发到同一台服务器上。
        - Cookie处理方式：包括植入Cookie和重写Cookie。当选择“植入Cookie”时，需要设置会话超时时间，客户端在第一次访问时，负载均衡会在返回请求中植入Cookie，下次客户端会携带此Cookie访问，负载均衡服务将会将请求重定向给之前记录到的后端服务器上。当选择“重写Cookie”时，需要在后端服务器上配置Cookie，并设置Cookie名称，负载均衡服务发现用户自定义了Cookie，将会对原来的Cookie进行重写，下次客户端携带新的Cookie访问，负载均衡服务会将请求定向转发给之前记录到的后端服务器。
        - 会话超时时间（植入Cookie设置此参数）：当超过设置时间后，连接内无新的请求，将会自动断开会话保持。
        - Cookie名称（重写Cookie设置此参数）：设置cookie名称为后端服务器上配置的Cookie名称。
    - 启用访问控制：设置是否启用访问控制，如勾选启用访问控制后，需要设置访问控制方式以及访问策略控制组。
        - 访问控制方式：白名单即允许访问控制策略组中的IP访问负载均衡；黑名单即禁止访问控制策略组中的IP访问负载均衡。
        - 访问控制策略组：选择访问控制策略组，请先在访问控制页面创建策略组。
    - 后端连接超时时间：转发节点收到客户端请求后，请求后端服务器的超时时间。
    - 后端连接空闲时间：设置转发节点与后端服务器的连接空闲时间。
    - 连接空闲超时时间：连接会话建议后允许的空闲时间，在超时时间内一直没有访问请求，将会暂时中断当前连接。
    - 连接请求超时时间：在超时时间内，服务器一直没有响应，负载均衡将放弃等待。
    - 限定接收请求速率：限定监听接收请求的最大速率，0为默认值，表示不限速。
    - 限定同源IP请求速率：限定每个源IP对此监听发送请求的最大速率，0为默认值，表示不限速。
    - Gzip数据压缩：是否启用Gzip数据压缩，开启后将会对特定的文件类型进行压缩，目前Gzip支持压缩的类型包括：text/xml、text/plain、text/css、application/javascript、application/x-javascript application/rss+xml、application/atom+xml、application/xml。
    - 设置Proxy协议：通过Proxy协议获取客户端真实IP。一般常用V2版本。       
    - 附加HTTP头部字段：选择是否通过X-Forwarded-For获取客户端真实IP。
4. 单击 **_"下一步：后端服务器组"_** 按钮，选择后端服务器组，如无后端服务器组，可新建。   
5. 单击 **_"下一步：健康检查"_** 按钮，配置健康检查相关参数。
    - 开启健康检查：选择是否开启健康检查，若勾选开启健康检查，配置以下参数。
    - 健康检查协议：选择健康检查协议，包括TCP和HTTP，TCP协议健康检查通过发送SYN握手报文来检测服务器端口是否存活；HTTP协议健康检查通过发送HEAD/GET请求模拟浏览器的访问行为来检查服务器应用是否健康。
    - 健康检查路径（仅支持HTTP）：设置健康检查的URL地址的路径。
    - 健康检查域名（仅支持HTTP）：设置健康检查的请求域名。
    - 正常状态码（仅支持HTTP）：设置健康检查正常的HTTP状态码。
    - 健康检查响应超时时间：健康检查响应的最大超时时间，如在响应时间内未响应，则判定健康检查异常。
    - 健康检查间隔时间：负载均衡进行健康检查的时间间隔。
    - 健康检查健康阈值：连续n（n为设置的值）次收到健康检查的结果为成功，则显示状态为健康。
    - 健康检查不健康阈值：连续n（n为设置的值）次收到健康检查的结果为识别，则显示状态为异常。
6. 单击 **_"确定"_** 按钮，完成操作。
