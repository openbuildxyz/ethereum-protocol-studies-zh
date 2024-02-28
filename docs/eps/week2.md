# 学习小组第二周 | 执行层

在第二周，我们将深入研究以太坊的执行层。

观看关于以太坊轻客户端内部的执行客户端(EL)的演示，请访问 [StreamEth](https://streameth.org/watch?event=&session=65dcdef0a6d370a1ab326de1) 或 [Youtube](https://www.youtube.com/watch?v=pniTkWo70OY)。介绍文档可在此处获取。

[录像](https://streameth.org/embed/?playbackId=70f6rq6un48dy74q&vod=true&streamId=&playerName=Execution+Layer+Overview+%7C+lightclient+%7C+Week+2 ':include :type=iframe width=100% height=520 frameborder="0" allow="fullscreen" allowfullscreen')

要查看讨论期间的存档，请查看我们[Discord服务器](https://discord.gg/epfsg)中的[这个线程](https://discord.com/channels/1205546645496795137/1210292746817110027/1210292751158222848)。

## 预读

在开始第二周内容之前，请熟悉[第一周](/eps/week1.md)的资源。

此外，您应该阅读以下文档以准备演示：

* [节点和客户端](https://ethereum.org/developers/docs/nodes-and-clients)
* [以太坊：机制](https://cs251.stanford.edu/lectures/lecture7.pdf)（基于这些幻灯片的讲座也可在YouTube上找到：[以太坊执行层概述 - Dan Boneh](https://www.youtube.com/watch?v=7sxBjSfmROc)）

## 大纲

### 执行层节点的概述

* 区块验证
  * 在过度简化的术语中，执行端(EL)处理状态转换
  * 每个交易由客户端验证、执行，并将其结果累积到状态trie中
  * 还有其他必须在每个区块中更新的机制，例如EIP-1559基础费用、EIP-4844多余的blob gas、EIP-4844信标根环形缓冲区、信标链提款等。
  * 新节点还必须能够在不造成太多摩擦的情况下加入网络，因此执行端(EL)提供了有效的同步机制来启动其他节点
* 区块构建
  * 执行端(EL)还根据它们在网络中看到的交易构建区块
  * 这需要一个基于p2p的tx池系统

### 状态转换函数

* 标头验证
  * 验证默克尔根
  * 验证gas限制
  * 验证时间戳
* 区块验证
  * 在 `state_processor.go` 中步行[`Process(..)`](https://github.com/ethereum/go-ethereum/blob/master/core/state_processor.go#L60)

### EVM高级

* 栈机介绍
* 查看简单的程序
* 复习不同类别的操作码：栈/内存操纵器、env获取器、以太坊系统操作等。

### p2p高级

* p2p提供三个主要功能
  * 历史数据
  * 待处理交易
  * 状态
* 讨论快速同步
  * 阶段1：下载快照瓦片
  * 阶段2：恢复

### JSON-RPC

* 与以太坊的“接口”
  * 愿景是所有客户端提供完全相同的API，用户可以运行任何选择的客户端，并与所有工具完美集成
  * 还没有完全实现，但我们已经非常接近
* 复习主要的 RPC 方法

## 额外阅读和练习

* <https://www.evm.codes/>
* <https://github.com/ethereum/go-ethereum>
* <https://github.com/ethereum/consensus-specs>
* <https://github.com/ethereum/execution-specs>
* <https://github.com/ethereum/devp2p>
* <https://github.com/ethereum/execution-apis>
* <https://blog.ethereum.org/2022/01/24/the-great-eth2-renaming>
* <https://blog.ethereum.org/2021/11/29/how-the-merge-impacts-app-layer>
* [执行客户端和共识客户端如何协同工作](https://www.youtube.com/watch?v=91-GArv6lKo)
* [引擎API：可视化指南](https://hackmd.io/@danielrachi/engine_api) 由 [Daniel Ramirez](https://hackmd.io/@danielrachi)

Lightclient 的 vim 和 shell 设置 <https://github.com/lightclient/dotfiles>
