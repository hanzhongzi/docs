---
title: "合并/分割IP子网"
weight: 35
description: >
  介绍如何合并或分割IP子网。
---

## 分割IP子网

该功能用于分割IP子网范围，将一个子网分成两个子网。仅{{<oem_name>}}平台支持。

1. 单击IP子网右侧操作列 **_"更多"_** 按钮，选择下拉菜单 **_"分割IP子网"_** 菜单项，弹出分割IP子网对话框。
2. 输入新IP子网名称、新IP子网起始IP（原IP子网地址范围：原IP子网起始IP至新IP子网起始IP末位-1；新IP子网地址范围：新IP子网起始IP至原IP子网结束IP）。
3. 单击 **_"确定"_** 按钮。

## 合并IP子网

该功能用于将分割的IP子网，合并为一个IP子网，仅{{<oem_name>}}平台支持。

1. 在IP子网列表中选择两个IP地址段连续的IP子网，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"合并IP子网"_** 菜单项，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，将两个IP子网合并为一个，IP子网名称为IP地址大的IP子网名称。