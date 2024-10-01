---
title: "Docker"
date: 2024-08-19T00:13:04+08:00
draft: true
---

# docker获取镜像
从 Docker 镜像仓库获取镜像的命令是 `docker pull`，其命名格式为：
```shell
$ docker pull [选项] [Docker Registry 地址[:端口号]/]仓库名[:标签]
```
例如：
```shell
 docker pull ubuntu:16.04
```