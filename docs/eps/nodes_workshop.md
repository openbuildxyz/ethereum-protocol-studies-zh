# 学习小组第五周 | 使用以太坊客户端

在第五周，除了[常规演示](https://epf.wiki/#/eps/week5)之外，我们还准备了一个研讨会，让你亲身体验使用以太坊客户端。我们将学习如何通过运行执行和共识客户端来启动以太坊节点。

观看 [Mario](https://twitter.com/TMIYChao) 在 StreamEth 或 Youtube 上的研讨会录像。

[录像](https://www.youtube.com/embed/KxXowOZ2DLs?si=yLpNoczrUmxj4kE4 ':include :type=iframe width=100% height=560 frameborder="0" allow="fullscreen" allowfullscreen encrypted-media gyroscope picture-in-picture web-share')

确保准备好你的环境并学习理解该过程所必需的基础知识：

## 先决条件

熟悉以太坊客户端架构，如第1周所述，并且你可以查看第2周和第3周以更好地理解工作坊执行的内容。该工作坊默认使用geth+lighthouse，但如果你有其他首选客户端要尝试，请熟悉其文档。

- <https://ethereum.org/en/developers/docs/nodes-and-clients/node-architecture/>
- <https://ethereum.org/en/developers/docs/nodes-and-clients/run-a-node/>
- 你首选客户端的客户端文档
- 基本的 bash/cli shell 技能
  - <https://btholt.github.io/complete-intro-to-linux-and-the-cli/>, <https://ubuntu.com/tutorials/command-line-for-beginners>

准备你的环境，更新系统并安装依赖项，以便在工作坊期间不会受到阻碍。

- 工作坊环境将是一个全新的Debian 12实例，但你可以使用任何首选的发行版。在其他基于Unix的系统（如Mac）上，该过程可能非常相似，但你始终可以设置一个虚拟机来复制该环境。
- 安装我们将需要的基本工具，如curl、git、gpg、docker、编译器

我们将只在测试网上运行一个客户端，因此硬件要求很低 - 该工作坊的目标不是同步链的顶端，而仅仅是演示节点的工作原理。默认客户端对将是 geth+lighthouse，但如果时间充足，我们可以演示如何切换对。

## 大纲

- 运行节点简介
  - 选择客户端对和环境
- 获取客户端
  - 下载和验证二进制文件
  - 编译客户端？
  - Docker设置？
- 客户端对设置
  - 在Holesky上运行EL+CL客户端
  - 在Ephemery上使用自定义起源运行
  - 切换CL或EL客户端
    - Nimbus？
    - Erigon？
- 使用客户端
  - 访问RPC
    - http，控制台，钱包
    - 添加验证器
- 如果有时间，还有其他练习
  - Systemd服务
  - 监控节点
- 在直播结束后，我们可以切换到 [jitsi](meet.ethquokkaops.io/EPFsgWorkshop) 进行进一步讨论和故障排除

## 更多阅读和练习

在工作坊期间，我们将不会演示一堆事情，因此你可以随后自行尝试。

- 使用 Grafana 仪表板设置监控，该仪表板显示各种客户端参数和功能的详细信息
- 启用更高详细程度的日志，阅读客户端调试日志以了解其低级别进程
- 使用钱包、开发工具、web3.py 或 JS 控制台连接到你的节点
- 将你的节点连接到 [crawler](https://www.ethernets.io/help/) 并检查它了解到的细节，发现新的网络节点
- <https://github.com/eth-educators/ethstaker-guides/blob/main/holesky-node.md>
- <https://notes.ethereum.org/@launchpad/node-faq-merge>
- <https://www.coincashew.com/coins/overview-eth/guide-or-how-to-setup-a-validator-on-eth2-mainnet/part-i-installation/monitoring-your-validator-with-grafana-and-prometheus>
