+++
title = '1Panel使用体验'
date = 2024-03-24T10:54:03-07:00
draft = false
+++

有 2 个闲置的小服务器，想用一个建一个博客网站，但是我实在不想折腾命令行界面了，有点费劲。于是搜索一番，找到了`1Panel`，确实很不错，有很多优点，但也有一些缺点。

**优点**

优点自然是大家比较常说的：

- UI 界面，方便操作
- 功能丰富，常用的服务器管理功能都有，而且也有很多应用可以一键安装，真的非常好
- 可以连接远程数据库，这个不错

**缺点**

我使用下来的缺点就是：

- 太占硬盘空间了，我的 10GB 硬盘，这刚建了一个 wordpress 和 mysql，就只剩下 1GB 了
- 占硬盘的原因，是他们使用了 docker，其实 1panel 就是一个管理 docker 的 UI，任何一个应用，都是 docker image，自然就很占硬盘
- 而且我折腾半天，找不到怎么清理 docker image
