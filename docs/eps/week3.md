# 学习小组第3周 | 共识层

第三周将深入探讨以太坊的共识层。

加入由[Alex Stokes](https://twitter.com/ralexstokes)在[周一，3月4日，UTC下午4点](https://savvytime.com/converter/utc-to-germany-berlin-united-kingdom-london-ny-new-york-city-ca-san-francisco-china-shanghai-japan-tokyo-australia-sydney/mar-04-2024/4pm)进行的演示。

流媒体链接将在此提供，并在[Discord群组](https://discord.gg/epfsg)中宣布。

## 预备阅读

在开始第3周内容之前，请熟悉[第2周](/eps/week2.md)中的资源。

此外，你可以通过阅读以下资源做好准备：

- [Ethereum.org关于权益证明的文档](https://ethereum.org/developers/docs/consensus-mechanisms/pos)及其子主题
- [信标链解释器](https://ethos.dev/beacon-chain)
- [权益证明和太阳能朋克未来，Dany Ryan 2022](https://www.youtube.com/watch?v=8N10a1EBhBc)，合并之前的讲话，对合并和信标链的开发和测试有很好的见解

## 大纲

- 区块链实现数字稀缺性，但需要确保其完整性的安全性
- 分布式网络处理拜占庭容错(BFT)
- 比特币首先通过PoW解决了BFT问题
- 以太坊转向权益证明，从系统内部切换到外部信号以保护 Sybil
- 使用BFT多数确定链的状态
  - 拜占庭故障可以被协议观察到，并且抵押品可以被 `减持`
  - 分叉选择规则总结为LMD-GHOST
  - 借助Casper确保活力
- 提供更多的加密经济安全性

## 更多阅读和练习

- [Gasper 论文](https://arxiv.org/pdf/2003.03052.pdf)
- [比特位LMD GHOST：一种高效的CBC Casper分叉选择规则](https://medium.com/@aditya.asgaonkar/bitwise-lmd-ghost-an-efficient-cbc-casper-fork-choice-rule-6db924e57d1f)
- [Eth2book，注释规范](https://eth2book.info/)
- [关于PoS的你应该知道的事情，由Domothy](https://domothy.com/proof-of-stake/)
- [Justin Drake关于信标链设计错误](https://www.youtube.com/watch?v=10Ym34y3Eoo)
- [来自Devcon 3的Casper和共识](https://archive.devcon.org/archive/watch/3/casper-and-consensus/?tab=YouTube)

在了解了 EL 和 CL 之后，运行一个客户端对。运行一个执行和一个共识客户端，阅读它们的日志以了解它们的操作方式。
