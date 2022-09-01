---
title: "规则配置"
weight: 3
description: 规则配置即根据系统内影响资源安全的条件设置相应的规则，如安全组的规则设置等，当资源匹配规则则表示资源的安全性较低，需要用户进行处理等。
---

规则配置即根据系统内影响资源安全的条件设置相应的规则，如安全组的规则设置等，当资源匹配规则则表示资源的安全性较低，需要用户进行处理等。

**入口**：在云管平台单击左上角![](../../../images/intro/nav.png)导航菜单，在弹出的左侧菜单栏中单击 **_"优化建议/安全检查/规则"_** 菜单项，进入规则配置页面。

![](../../../images/suggest/securitysuggestsyrule.png)

## 修改规则配置

该功能用于修改规则配置，目前仅支持修改时间范围。时间范围将会影响扫描结果，即超过时间范围内闲置的资源才会被扫描出来。仅具有周期性使用规律的主机支持修改。

1. 在规则配置页面，单击规则右侧操作列 **_"修改"_** 按钮，弹出修改规则配置对话框。
2. 修改时间范围，单击 **_"确定"_** 按钮，完成操作。

## 启用规则

该功能用于启用"禁用"状态的规则。禁用状态的规则不生效。

**单个启用**

1. 在规则配置页面，单击"禁用"状态的规则右侧操作列 **_"启用"_** 按钮，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，启用规则。

**批量启用**

1. 在规则列表中选择一个或多个规则，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"启用"_** 菜单项，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，启用规则。

## 禁用规则

该功能用于禁用"启用"状态的规则，禁用状态的规则不生效。

**单个禁用**

1. 在规则配置页面，单击"启用"状态的规则右侧操作列 **_"禁用"_** 按钮，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

**批量禁用**

1. 在规则列表中选择一个或多个规则，单击列表上方 **_"批量操作"_** 按钮，选择下拉菜单 **_"禁用"_** 菜单项，弹出操作确认对话框。
2. 单击 **_"确定"_** 按钮，完成操作。

## 查看规则详情

该功能用于查看规则的详细信息。

1. 在规则配置页面，单击规则名称项，进入规则详情页面。
2. 查看规则的云上ID、ID、名称、状态、域、项目、启用状态、规则、上一次执行时间、创建时间、更新时间、备注。

### 查看操作日志

该功能用于查看规则相关操作的日志信息。

1. 在规则配置页面，单击规则名称项，进入规则详情页面。
2. 单击“操作日志”页签，进入操作日志页面。
    - 加载更多日志：列表默认显示20条操作日志信息，如需查看更多操作日志，请单击 **_"加载更多"_** 按钮，获取更多日志信息。
    - 查看日志详情：单击操作日志右侧操作列 **_"查看"_** 按钮，查看日志的详情信息。支持复制详情内容。
    - 查看指定时间段的日志：如需查看某个时间段的操作日志，在列表右上方的开始日期和结束日期中设置具体的日期，查询指定时间段的日志信息。
    - 导出日志：目前仅支持导出本页显示的日志。单击右上角![](../../../images/system/download.png)图标，在弹出的导出数据对话框中，设置导出数据列，单击 **_"确定"_** 按钮，导出日志。