# 为Wiki协议做出贡献

协议 Wiki 是一个开放的协作项目。无论您是否是[学习小组](study-group.md)的成员，我们都欢迎您的贡献！帮助我们构建有关以太坊核心研发的文档并提高学习资源的可用性。  

*我们的目标不是重写其他现有的以太坊文档，而是为有抱负的核心开发人员和研究人员创建一个有凝聚力的技术资源集合。

创建贡献时，请考虑它是否在其他地方不以其他形式存在。使用它并在文本中引用它，但不要复制其内容。专注于将其添加到一个整体中，并将其与相关主题联系起来。

根据您一路上对协议的了解、您收集的经验以及遗漏的导致您放慢速度的部分来撰写贡献。将其视为向您的同行解释，反思您自己作为核心开发人员/学习人员的旅程。

## 贡献

在开始编辑之前，请阅读行为准则、遵循指南并熟悉整个 wiki 结构。 

wiki 源代码托管在 [github.com/eth-protocol-fellows/protocol-studies](https://github.com/eth-protocol-fellows/protocol-studies). 的 github 存储库中。镜像于//TODO

> 维基百科由`wiki-pages`分支提供服务。贡献时，打开 PR 到`main`分支（repo 默认分支）。一段时间后，所有更新都会集中到上游来`wiki-pages`更新网站。

您可以探索现有问题或针对缺失内容提出新问题，建议改进现有内容或 wiki 前端功能。如果您发现缺失或未完成的内容，请随时提出 PR。 

我们的目的不是重建其他现有的 wiki。如果相同的内容在其他地方得到了很好的解释，只需链接它并提供额外的上下文即可。 

### 什么（不）属于这里

本 wiki 的范围仅限于以太坊核心协议基础设施的技术资源。这意味着它的规范、实现、测试、研究或相关工具。 

它**不**涵盖链上协议/dapp、第 2 层/汇总或任何其他不依赖于核心基础设施的工具。换句话说，这些内容将由 EIP 涵盖，而不是 ERC 涵盖。

### 结构与协作

该维基应该涵盖以太坊核心协议及其开发的所有重要部分。协议架构和相关主题反映在 wiki 格式中。整个 wiki 都在下面`/docs/wiki`，[侧边栏]((_sidebar.md))定义了主要的文档结构。高层区域被抽象为包含所有子主题的目录。 

对于贡献者，我们建议关注相应文档中包含的特定主题。最好拥有一个主题并解决所有细节。创建一个新文档并将主题添加到侧边栏（如果尚不存在）。

加入[discord](https://discord.gg/epfsg)，让其他人知道您在群组频道中正在做什么，并与其他贡献者合作撰写相关主题。如果您与多人合作处理重要的内容，您可以在存储库中拥有一个专用分支，以便于协调。 

## 编辑维基

wiki 是常规 Markdown 文件的集合，可以使用 github 界面或您最喜欢的 Markdown 编辑器直接编辑。在做出承诺和开放 PR 时，请提供评论来解释您的贡献。

Web 文档版本由[Docsify](https://docsify.js.org/)生成 . 了解其[config](https://docsify.js.org/#/configuration) 和 [features](https://docsify.js.org/#/plugins)选项。配置和网页设计也欢迎改进或建议。 

要对配置进行更广泛的编辑或更改，请使用 Docsify 在本地预览网络。你只需要 git 和 node.js。

安装 docsify，克隆存储库并将其托管在本地。

```
npm i docsify-cli -g
git clone https://github.com/eth-protocol-fellows/protocol-studies.git
cd protocol-studies
docsify serve ./docs
```

## 样式指南

Wiki 页面遵循标准 Markdown，可以通过 Github 或 Docsify 呈现。有关使用它的详细信息，请参阅 Markdown [指南](https://www.markdownguide.org/). 

本 wiki 的受众是技术人员，内容应反映这一点。有许多关于技术和文档写作的指南可供您学习。以下是编写此 wiki 时需要遵循的一些准则:

- 以客观、清晰和解释性的语气写作
- 避免不必要的简化，描述技术现实
- 避免使用太长和复杂的句子或段落
    - 使用简洁明了的陈述
    - 使用块引用、项目符号或图像分解文本
- 始终链接您的资源并验证它们
- 对于需要枚举的主题使用要点或表格
- 突出显示关键字以支持扫描和浏览文章
- 提供可视化以更好地解释主题
- 使用首字母缩略词或技术术语时，请务必先介绍它
- 不要使用法学硕士来生成文本
    - 我们不接受完全由人工智能生成的文本，但我们建议使用它来修复语法或措辞
- 考虑创建实践指南或教程
- 在顶部添加推荐阅读，指向您依赖的主题

目标是产生一个可信的中性文本，该文本正式、结构良好，并保持清晰的思想进展。
内容应该是纯技术性的，不应该浪费空间来介绍高水平/众所周知的概念。
介绍性主题是必要的，可以使用比较、历史轶事和具体例子来使复杂的概念更容易理解。

### 内容标准化

维基百科使用美式英语而非英式拼写。所有页面的术语、大小写和命名法都应匹配。使用[Ethereum.org 指南](https://ethereum.org/contributing/style-guide/content-standardization)作为参考。 

鼓励使用图像和可视化。如果您使用第三方创建的图像，请确保其许可证允许并提供原始图像的链接。要创建您自己的可视化效果，我们建议您使用 [excalidraw.com](https://github.com/excalidraw/excalidraw). 

请随意使用合适的 [emojis](https://docsify.js.org/#/emoji?id=emoji)或 [icons](https://icongr.am/fontawesome)，例如在块引号中。

### 链接资源

添加外部链接时，您可以直接在正文中使用，也可以在页面底部的“资源”部分中使用。

链接资源时使用描述性名称，例如[inevitableeth.com](https://inevitableeth.com/)，而不是像[this wiki](https://inevitableeth.com/)这样的通用短语。

不要让文本中的太多资源让读者不知所措。

链接此 wiki 中的页面时，请使用相对路径，如果它引用页面中的特定主题，请使用标题 ID 的链接。 

对于其他重要链接，请在页面底部添加一个包含资源列表的部分。资源应该有一个名称或简短描述，并带有指向其存档镜像的链接和替代链接。我们强烈建议添加指向 archive.org 的最新快照的链接。资源部分中的链接示例： 

[JSON-RPC API 参考](https://ethereum.org/en/developers/docs/apis/json-rpc), [已存档](https://web.archive.org/web/20240117035335/https://ethereum.org/en/developers/docs/apis/json-rpc)


## 还要别的吗？

此页面也向贡献者开放！对 github [protocol-studies](https://github.com/eth-protocol-fellows/protocol-studies) 的风格和指南提出改进建议。如果您有任何问题，请随时在 [discord](https://discord.gg/epfsg) 上提问。 
