---
title: "账号"
date: 2021-06-23T08:22:33+08:00
weight: 20
description: >
   RDS实例账号
---


支持为RDS实例创建多个账号并分配不同权限，从而更加灵活的管理RDS实例。

- 华为云的RDS实例创建成功后默认会创建root用户，root用户拥有实例下所有数据库的所有权限，不可删除和修改等。
- 阿里云目前只支持创建普通权限的用户，不支持在{{<oem_name>}}平台创建root权限的用户。
- 谷歌云目前只支持创建root权限的用户。