---
title: "NAS权限组"
date: 2021-11-26T15:36:58+08:00
weight: 40
description: >
    NAS权限组管理
---

NAS权限组用于设置指定IP地址或者网段访问文件系统，并给不同的IP地址或网段授予不同的访问权限。在文件系统添加挂载点时，需要选择NAS权限组。

初始情况下，每个阿里云账号会自动生成一个默认权限组，默认权限组允许任何IP地址以最高权限（可读写且不限制Linux系统用户对文件系统的访问权限）访问文件系统。默认权限组不支持删除或修改。一个阿里云账号最多可以创建10个权限组，一个权限组最多支持添加300个规则。即从阿里云平台上同步下来的Default权限组不支持删除。