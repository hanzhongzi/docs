---
title: "公有云资源归属"
weight: 5
description: 介绍公有云平台上资源如何同步到var_oem_name平台
---

公有云平台上的资源与 {{<oem_name>}} 平台的项目对应关系由以下几个因素决定的。

## 资源归属项目

在添加云账号时，不勾选自动创建项目，并选择资源归属项目，则公有云上的资源都将同步到资源归属项目中。公有云上的项目都将对应到 {{<oem_name>}} 平台的资源归属项目。

## 自动创建项目

在添加云账号时，勾选自动创建项目，将会按照公有云的项目在{{<oem_name>}} 平台创建一一对应的同名项目，公有云上若存在不归属于项目的资源，该资源将同步到资源归属项目。

## 同步策略

同步策略即设置标签与项目的对应关系，将公有云上的资源按照策略规则同步到指定项目中。同步策略优先级最高，当配置同步策略后，资源将按照同步策略中的规则进行同步。不符合同步策略的资源，仍然云上项目与本地项目的对应关系同步资源。