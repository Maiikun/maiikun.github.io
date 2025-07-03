---
title: MVCC
date: 2024-11-27 18:11:58 +0800
categories: [MySQL]
tags: [MySQL] # TAG names should always be lowercase
media_subpath: /_posts/images
---

多版本并发控制,实现了MYSQL的事务隔离性;
**隔离性：通过加锁（当前读）&MVCC（快照读）实现。**
**在读已提交和可重复读隔离级别下的快照读，都是基于MVCC实现的**

mvcc的实现，基于**undolog**、**版本链**、**readview**。
![](Pasted image 20250703220016.png)
