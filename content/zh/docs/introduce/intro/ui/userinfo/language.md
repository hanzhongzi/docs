---
title: "语言设置"
date: 2022-02-09T16:06:58+08:00
weight: 30
description: >
    切换 var_oem_name 平台的显示语言，目前仅支持中、英文
---

### 设置界面语言

1. 单击顶部区域右上角用户图标，在弹出的对话框中选择“简体中文”或“English”，即可切换云管平台的语言。

### 设置平台发送信息的默认语言

平台向用户发送的语言根据用户的属性"lang"决定，因此即使将平台切换成英文显示，平台上发送的报警消息等内容可能也是中文显示，如需将其修改为英文内容，请修改对应用户的“lang”属性，目前界面暂不支持修改，请使用climc命令行修改。操作命令如下：

```bash
# 将用户接收的消息设置为英文
$ climc user-update --lang en <user_id>
#
$ climc user-update --lang zh-CN <user_id>
```
