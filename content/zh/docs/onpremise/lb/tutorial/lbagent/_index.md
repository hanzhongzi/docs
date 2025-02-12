---
title: "负载均衡节点"
date: 2021-12-20T16:42:13+08:00
weight: 20
description: >
    负载均衡节点用于监听负载均衡实例，并将客户端的请求根据监听和转发规则将其转发给后端服务器。
---

负载均衡集群中的节点用于监听负载均衡实例，并将客户端的请求根据监听和转发规则转发给后端服务器。

同一个集群下可以有多个转发节点，但同一时刻只有一个节点作为Master节点提供转发服务。属于一个集群的节点的VRRP路由ID必须相同。

节点生命周期管理：

1. 新建节点：设置节点的配置参数。
2. 部署节点：将节点的配置文件下发到指定机器，提供转发功能的机器可称为转发实例，当节点状态为Master时，表示集群中的节点可正常提供负载均衡转发服务。
3. 下线节点：当不需要节点提供服务时，可下线节点，将配置文件从转发实例上删除。
4. 删除节点：删除节点的配置文件信息等。

