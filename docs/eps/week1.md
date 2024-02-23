# 学习小组 第1周 | 协议介绍

学习小组的第一周致力于介绍协议和研发生态。

## 录像

观看 Mario Havel 在 StreamEth 上的 *以太坊协议101* 演讲。[幻灯片](https://github.com/eth-protocol-fellows/protocol-studies/tree/main/docs/eps/presentations/week1_protocol_intro.pdf)

[录像](https://streameth.org/embed/?playbackId=9bc1ekw2jk5sz6c7&vod=true&streamId=&playerName=Intro+to+Ethereum+%7C+Mario+Havel+%7C+Week+1 ':include :type=iframe width=100% height=520 frameborder="0" allow="fullscreen" allowfullscreen')

要查看演讲期间的讨论存档，请查看[Discord 服务器](https://discord.gg/epfsg)的 `#study-group` 频道中的相应线程。

## 预先阅读

这是一个介绍性的演讲，不需要太多先前的知识。在[第0周](/eps/week0.md)检查一些一般要求。以下是一些更多的入门材料，以帮助您入门：
- [Inevitable Ethereum - 世界计算机](https://inevitableeth.com/home/ethereum/world-computer)
- [30分钟理解以太坊](https://www.youtube.com/watch?v=UihMqcj-cqc)
- [Ethereum.org 文档](https://ethereum.org/what-is-ethereum)

查看以下文本和额外阅读中的资源。所有资源将在第1周的演示中进行解释。

## 历史与哲学

要理解以太坊的设计，我们需要了解前辈和它所建立的文化。现代加密货币生态系统建立在几十年来计算机科学家、密码学家和活动家的工作之上。

从上世纪60年代开始，UNIX 是一种重新定义了整个计算范式的操作系统和哲学。这是我们使用了50多年的范式，从未真正改变过。其模块化的基本概念对以太坊的设计以及贝尔实验室的开放协作环境非常重要，而后者类似于今天的以太坊核心开发。

> 观看这部由丹尼斯·里奇和肯·汤普逊主演的纪录片，完美地捕捉了 UNIX 背后的精神和思想：[https://yewtu.be/watch?v=tc4ROCJYbm0](https://yewtu.be/watch?v=tc4ROCJYbm0)

自由软件运动对以太坊和所有加密货币都至关重要。以太坊的开放、独立和协作开发文化在自由软件和开源软件中深深扎根。以太坊需要以给予其用户完全自由的软件进行透明实现。使用任何自由软件都可以赋予每个用户和开发人员权力，但对以太坊的安全性、中立性和无信任性来说，这是必要的。

> 要了解其重要性，请观看自由软件和 GNU 项目的创始人理查德·斯托曼的演讲：
> - [https://yewtu.be/watch?v=Ag1AKIl_2GM](https://yewtu.be/watch?v=Ag1AKIl_2GM)
> - 更多阅读：[https://www.gnu.org/philosophy/free-sw.html](https://www.gnu.org/philosophy/free-sw.html)，*大教堂和集市* 一书：[http://www.catb.org/~esr/writings/cathedral-bazaar/](http://www.catb.org/~esr/writings/cathedral-bazaar/)

[非对称加密](https://www-ee.stanford.edu/~hellman/publications/24.pdf) 的发明标志着密码学应用的新范式的诞生。随后，密码学在普通公众的计算中的崛起使每个人都能够利用工具进行数字隐私、安全通信，并从根本上改变了网络安全。尽管国家并没有为这些新概念制定框架，但[密码战争](https://en.wikipedia.org/wiki/Crypto_Wars)导致了倡导和构建密码学工具的活动家运动。最终，这些人发明了成为现代加密货币基本构建模块的工具和思想。

> 从早期的 CipherPunks 获得灵感，他们构想了一个建立在无信任和无国界技术上的独立数字领域：
> - [https://activism.net/cypherpunk/manifesto.html](https://activism.net/cypherpunk/manifesto.html)
> - [https://activism.net/cypherpunk/crypto-anarchy.html](https://activism.net/cypherpunk/crypto-anarchy.html)
> - [https://www.eff.org/cyberspace-independence](https://www.eff.org/cyberspace-independence)

## 以太坊协议设计

最初在其[白皮书](https://ethereum.org/whitepaper#ethereum-whitepaper)中概述，以太坊从比特币及其上文（上文已解释）中汲取灵感，创建了一个基于区块链的通用计算平台。该设计在[黄皮书](https://ethereum.github.io/yellowpaper/paper.pdf)中进行了技术规定，并随着时间的推移不断发展。变更在[EIPs](https://eips.ethereum.org)的社区过程中进行跟

踪，当前规范在 Python 中实现为：

- [执行规范](https://github.com/ethereum/execution-specs)
- [共识规范](https://github.com/ethereum/consensus-specs)

该规范纯粹是技术性的，不为读者提供任何背景或解释。要了解共识，请查看[由 Ben 注释的版本](https://eth2book.info/capella/annotated-spec/)和[由 V 注释的版本](https://github.com/ethereum/annotated-spec)。

随着时间的推移，协议会发生变化，每次网络升级都会带来新的改进。尽管它不断变化，但架构演变反映了某些基本原则。这些原则可以总结如下：

- 简单性、普适性、模块化、非歧视性、灵活性

这些核心原则一直引导着以太坊的发展，并且在设计变更的每个决定中都应予以考虑。除此之外，它通过封装和/或夹层化来管理不断增长的复杂性。当前的网络架构是许多[网络升级历史](https://ethereum.org/history)的迭代结果。

> 在[存档](https://web.archive.org/web/20220815014507mp_/https://ethereumbuilders.gitbooks.io/guide/content/en/design_philosophy.html)中阅读更多有关以太坊设计原则的内容，并考虑将其重写为[此维基](/wiki/protocol/design-rationale.md)。

以太坊网络利用去中心化成为无需许可、可信中立和抗审查的。它不断发展以应对最新的研究和新的、始终存在的挑战。为了保持安全性和去中心化，区块链技术有一定的限制，主要是可扩展性。因为以太坊需要始终遵循其原则，这激励我们找到巧妙的方法解决这些问题，而不是接受权衡。

[路线图](https://twitter.com/VitalikButerin/status/1741190491578810445/photo/1)概述了当前的研究和开发，但可能不完全准确。以太坊研发没有单一路径，[路线图](https://ethroadmap.com/)只总结了其当前的格局。核心生态系统是一个不断增长的[无限花园](https://ethereum.foundation/infinitegarden)。然而，随着越来越多的进展，以太坊可能会逐渐走向其固化。

> 可在[节点架构](https://ethereum.org/developers/docs/nodes-and-clients/node-architecture)的文档和第1周的演示中找到当前以太坊设计的简化概述。

如上所示，以太坊的主要高层组件是执行层和共识层。这是两个相互连接且相互依赖的网络。执行层提供执行引擎，处理用户交易和所有状态（地址、合约数据），而共识则实现了保证安全性和[容错](https://inevitableeth.com/home/concepts/bft)的权益证明机制。

## 实现和开发

上述的所有想法、设计和规范最终都落实到这里的实际应用中。执行层（EL）或共识层（CL）的实现称为 *客户端*。运行此客户端并连接到网络的计算机称为 *节点*。因此，一个节点是一对 EL 和 CL 客户端，它们积极参与网络。

由于以太坊已经得到正式规定，因此可以以任何语言的不同方式实现。这导致多年来出现了各种实现，其中一些已经过时，一些正在开发中。当前的生产就绪实现列表可以在[节点和客户端文档](https://ethereum.org/en/developers/docs/nodes-and-clients#execution-clients)和第1周的演示中找到。

> 这种策略称为[客户端多样性](https://ethereum.org/developers/docs/nodes-and-clients/client-diversity)。以太坊不依赖于单一的“官方”实现，但用户可以选择任何客户端并确信它能够完成工作。如果在单个客户端实现中发生问题，它不会影响网络的其余部分。

### 测试

由于经常变更和多个客户端实现，测试对于网络安全至关重要。在任何网络升级之前都会广泛利用各种测试工具和场景。

测试是根据规范生成的，并创建各种场景。有些是单独测试客户端，有些是模拟具有所有客户端对的测试网络。不同的测试工具用于开发周期的不同部分和客户端的不同部分。这包括状态转换测试、模糊测试、影子分支、RPC 测试、客户端单元测试和 CI/CD 等。

> 这是一份专门用于测试的存储库的简短列表：
> - [https://github.com/ethereum/tests](https://github.com/ethereum/tests)
> - [https://github.com/ethereum/retesteth](https://github.com/ethereum/retesteth)
> - [https://github.com/ethereum/execution-spec-tests](https://github.com/ethereum/execution-spec-tests)
> - [https://github.com/ethereum/hive](https://github.com/ethereum/hive)
> - [https://github.com/kurtosis-tech/kurtosis](https://github.com/kurtosis-tech/kurt

osis)
> - [https://github.com/MariusVanDerWijden/FuzzyVM](https://github.com/MariusVanDerWijden/FuzzyVM)
> - [https://github.com/lightclient/rpctestgen](https://github.com/lightclient/rpctestgen)

### 协调

以太坊的开发与传统的企业项目非常不同。首先，它是开放和公开的，任何人都可以查看或贡献。其次，有许多不同的团队致力于不同的部分。总共有大约20个来自各种组织的不同团队在以太坊上工作。

与专有技术不同，以太坊开发人员并不竞争，而是共同合作。随着复杂性的不断增加，基本上没有人能够精通所有以太坊。相反，人们在特定领域发展专业知识，并与他人合作。这得益于以太坊的模块化，使开发人员可以专注于他们个人更喜欢的挑战。

> 新功能或更改的传统开发周期是 `想法 - 研究 - 开发 - 测试 - 采用`。然而，问题可能会在此周期的任何时刻出现，导致从头开始再次迭代。

要能够发布网络升级并就当前开发重点达成一致，需要进行一定的协调。所有这一切也都是公开的，任何对了解核心协议感兴趣的人都可以关注。协调主要通过定期电话会议进行，这些电话会议已在[PM 存储库](https://github.com/ethereum/pm)中安排。有不同类型的开发人员电话，其中最大的电话是 All Core Devs（ACD）。这是各个团队代表讨论共识或执行层当前开发的地方。

社区的想法和提议的变更使用[EIP 过程](https://eips.ethereum.org/EIPS/eip-1)进行协调。此外，还有一些讨论论坛。最大的一个讨论核心升级的是 [ethresear.ch](https://ethresear.ch)。另一个与 EIP 过程相关且用于讨论具体提案的论坛是[Ethereum Magicians](https://ethereum-magicians.org/)。许多重要的讨论也在 R&D Discord 服务器（在 EPFsg Discord 中 @我们以获得邀请）和客户端团队群组中进行。还有举办现场会议或研讨会，许多核心开发人员可以亲自会面，加速面对面的过程。

## 额外阅读和练习

要测试您对以太坊基础知识的了解程度，请尝试一下测验：
[https://ethereum.org/quizzes](https://ethereum.org/quizzes)

了解更多有关路线图的信息：
[https://ethereum.org/roadmap](https://ethereum.org/roadmap)

要探索以太坊协议的各个部分，请查看 EPF 中人们正在进行的工作：
[https://github.com/eth-protocol-fellows/cohort-three/tree/master/projects](https://github.com/eth-protocol-fellows/cohort-three/tree/master/projects)
[https://github.com/eth-protocol-fellows/cohort-four/tree/master/projects](https://github.com/eth-protocol-fellows/cohort-four/tree/master/projects)

[Devcon 存档](archive.devcon.org)充满了深入探讨以太坊各种技术和非技术方面的令人难以置信的演讲。

Alex 和 Mike 最近对路线图的[回顾性文件](https://notes.ethereum.org/@mikeneuder/rcr2vmsvftv)提供了有关以太坊开发、价值和目标的重要见解。

阅读更多关于 Unix 和贝尔实验室的历史：
[https://www.theregister.com/2024/02/16/what_is_unix/](https://www.theregister.com/2024/02/16/what_is_unix/)
[https://www.deusinmachina.net/p/history-of-unix](https://www.deusinmachina.net/p/history-of-unix)

我推荐的几本书：

如果您对以太坊的早期时期、其创始人和创造的故事感兴趣，请查看书籍[The Infinite Machine](https://www.camirusso.com/book)。另一本类似的书是[Out of the Ether](https://www.goodreads.com/book/show/55360267-out-of-the-ether)。 （向我索取 epub 文件）

提供全面洞察力的最新出版物是[以太坊的绝对必要性](https://www.routledge.com/Absolute-Essentials-of-Ethereum/Dylan-Ennis/p/book/9781032334189)。它涵盖了[各种主题](https://www.coindesk.com/consensus-magazine/2024/02/07/absolute-essentials-of-ethereum-by-paul-dylan-ennis-an-excerpt/)，我强烈推荐它。

[精通以太坊](https://github.com/ethereumbook/ethereumbook)是 aantop 撰写的一本伟大的区块链书籍，涵盖了从基础知识到技术细节的所有内容。虽然已经过时，但仍然可以提供很好的启发。
