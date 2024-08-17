---
title:  ELK日志分析平台
description: ElasticSearch 介绍与安装
date: 2020-09-09
slug: ELK
categories:
    - Elasticsearch
    - Logstash
    - Kibana
---
---

## 什么是ELK

ELK 是三个开源项目的首字母缩写，这三个项目分别是：Elasticsearch、Logstash 和 Kibana 。
* **Elasticsearch** 是一个搜索和分析引擎。
* **Logstash** 是服务器端数据处理管道，能够同时从多个来源采集数据，转换数据，然后将数据发送到诸如 Elasticsearch 等存储库中。
* **Kibana** 则可以让用户在 Elasticsearch 中使用图形和图表对数据进行可视化。

简单来说，ELK是一个日志收集分析的技术栈。Logstash从多个数据源采集数据，Elasticsearch作为搜索引擎去查询数据，Kibana作为可视化工具显示图表和统计记录。那么就从核心的Elasticsearch开始学起来吧。

## 初识Elasticsearch
