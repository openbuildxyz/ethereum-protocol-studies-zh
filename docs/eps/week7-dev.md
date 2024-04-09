# 学习小组 第7周 | 执行客户端架构

第7周的开发课程是对以太坊执行层客户端代码库的洞察，解释其架构并突出新颖的方法。

观看[Dragan](https://twitter.com/rakitadragan)在 StreamEth 或 Youtube 上的演示录像。幻灯片[在此可用](https://github.com/eth-protocol-fellows/protocol-studies/blob/main/docs/eps/presentations/week7-dev.pdf)。

<iframe width="560" height="315" src="https://www.youtube.com/embed/ibcsc5cv-vc?si=mTR7ReFUZo3vFtJD" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## 预先阅读

在开始第7周的开发内容之前，请熟悉前几周的资源，尤其是第2周。执行客户端介绍提供了关于执行客户端及其主要特性的重要知识，并通过来自 geth 代码库的示例进行了说明。本次讨论将深入探讨用 rust 编写并采用现代设计方法开发的 reth 客户端设计。

此外，您可以通过学习以下资源来阅读并做好准备：

- Reth 文档 https://paradigmxyz.github.io/reth/
- 由 Georgios 撰写的 Reth 简介 https://www.youtube.com/watch?v=zntRpCKHyDc
- 由 Dragan 提供的更深入的洞察 https://www.youtube.com/watch?v=pxhq7YrySRM

## 大纲

- Reth 客户端
- 设计和架构
- 代码库概述、示例
- 特性和亮点

## 额外阅读和练习

- Erigon 是 geth 的一个分支，开创了 reth 实现的设计方法。它在 geth 和 reth 之间有一定的折中，是关于新颖执行客户端设计的重要资源来源。
- 作为一个练习，运行 reth 并设置不同的 `DEBUG` 选项，以探索各种客户端组件在更低层上的操作方式。
