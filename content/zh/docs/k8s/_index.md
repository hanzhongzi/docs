---
title: "多云Kubernetes"
date: 2019-07-19T20:56:33+08:00
weight: 80
description: >
  在多云环境下部署和管理多Kubernetes集群
---

多云Kubernetes支持管理已有的Kubernetes集群，同时也支持基于{{<oem_name>}}的虚拟机资源，无论是本地IDC还是多云的虚拟机资源，搭建部署 kubernetes 集群，目前支持在以下平台部署：

- 内置私有云
- 阿里云
- AWS

此外，当在{{<oem_name>}}上添加了公有云账号后，若云账号下有kubernetes集群，则集群也将同步到平台上，暂只支持只读同步，不支持管理，目前支持同步的kubernetes集群如下：

- 阿里云 EKS
- 腾讯云 TKE
- Azure AKS
