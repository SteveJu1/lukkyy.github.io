---
layout: post
title:  "MySQL"
categories: JavaScript
tags:  WebSocket 通信 协议
---

* content
{:toc}
增删查改

create 







**基于socket编写的C/S架构的软件**

#### MySQL的索引

可以快速检索，减少I/O次数



##### 分类

主键索引：**不允许重复，不允许空值**

唯一索引：**唯一的，允许空值**

普通索引（单列索引）：用一列构建索引，没限制，一个表可以有多个单列索引；

组合索引：是 一个索引有几个列

全文索引：用大文本对象的列构建的索引

note：索引也是一张表存储的，如果索引过多，在添加数据时要额外的更改索引表，造成效率低

**索引实现的原理**

不同数据库支持不同的存储引擎，不同存储引擎支持不同索引

MySQL支持 **哈希索引，全文索引，BTree索引，B+Tree索引**

**mysql的底层引擎是什么**

MySQL中最常见的两种存储引擎分别是MyISAM和InnoDB，分别实现了非聚簇索引和聚簇索引。

聚簇索引:索引的顺序就是数据的物理存储顺序

非**聚簇**索引:索引顺序与数据物理排列顺序无关