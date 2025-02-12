---
title: "重启"
date: 2022-01-06T16:13:27+08:00
weight: 40
description: >
    将处于运行中状态的虚拟机重启
---

该功能用于将处于运行中状态的虚拟机重启，重启过程中VNC连接会中断。批量重启操作支持选择不同平台上“运行中”状态的虚拟机。

**单个虚拟机重启**

1. 在左侧导航栏，选择 **_"主机/主机/虚拟机"_** 菜单项，进入虚拟机页面。
2. 单击“运行中”状态的虚拟机右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"实例状态-重启"_** 菜单项，弹出操作确认对话框。
2. 选择是否勾选强制重启，单击 **_"确定"_** 按钮。

**批量重启**

1. 在虚拟机列表中选择一个或多个“运行中”状态的虚拟机，单击列表上方 **_"重启"_** 按钮，弹出操作确认对话框。
2. 选择是否勾选强制重启，单击 **_"确定"_** 按钮。

{{% alert title="注意" color="warning" %}}
若勾选“强制重启”，虚拟机中未保存数据将会丢失。
{{% /alert %}}