---
title: 页面置换算法详解
publishDate: 2025-01-22 19:00:00
description: '页面置换算法包括LRU-K，FIFO，LFU等。'
tags:
  - Disk Page
heroImage: { src: './thumbnail.jpg', color: '#B4C6DA' }
language: '中文'
---

## 什么是页面置换算法

进程运行时，若其访问的页面不在内存而需将其调入，但内存已无空闲空间时，就需要从内存中调出一页程序或数据，送入磁盘的对换区，其中选择调出页面的算法就称为页面置换算法。
好的页面置换算法应有较低的页面更换频率，也就是说，应将以后不会再访问或者以后较长时间内不会再访问的页面先调出。

## 常见页面置换算法

### 1.FIFO（先进先出算法）

（优先淘汰最早进入内存的页面）

FIFO 算法是最简单的页面置换算法。FIFO 页面置换算法为每个页面记录了调到内存的时间，当必须置换页面时会选择最旧的页面置换。

“FIFO 算法当进程分配到的页面数增加时，缺页中断的次数可能增加也可能减少。”

FIFO 算法基于队列实现，不是堆栈类算法
注意，并不需要记录调入页面的确切时间，可以创建一个 FIFO 队列，来管理所有的内存页面。置换的是队列的首个页面。当需要调入页面到内存时，就将它加到队列的尾部
FIFO 页面置换算法易于理解和编程。然而，它的性能并不总是十分理想：
其一，所置换的页面可以是很久以前使用过但现已不再使用的初始化模块
其二，所置换的页面可以包含一个被大量使用的变量，它早就初始化了，但仍在不断使用

### 2.OPT（最佳置换算法）
