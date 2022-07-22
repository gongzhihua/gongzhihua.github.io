Dock like code
===================

# Dock like code 

## 1.1 What Dock like code 

Docs Like Code 不是一个工具，而是一种理念。这种理念决定了一套写文档的完整流程和工具链，即：写文档与写代码的流程和工具链保持一致。

##  Why Dock like code 

据 Stack Overflow（著名开发者问答社区）2016 年的调查 [2] 显示，文档质量差是软件工程师们在工作中最常抱怨的三大问题之一。**文档不完整、文档找不到、文档过时**逐渐成为软件工程师们面临的“三堵高墙”。

**文档必须紧跟代码，迅速迭代优化**
## Docs Like Code 运动

Write the Docs 2014 会议 [3] 上，来自 Twitter 的 Simeon Franklin 和 Marko Gargenta 做了 Docs Like Code 的实践分享，台下来自 Google 的 Riona MacNamara 备受鼓舞。
次年 Write the Docs 会议 [4] 上，Riona 分享了在 Google 进行 Docs Like Code 实践的成功经验。

Docs Like Code 慢慢成为了 Google 司软件文档开发的一项事实标准。

## Docs Like Code 的优势

1. **文档任务能更早地融入到软件版本发布的流程**
2. **文档持续、即时发布**

# Sphinx

## 第一个Sphinx项目

### Sphinx介绍
Sphinx 是一种文档工具，它可以令人轻松的撰写出清晰且优美的文档, 由 Georg Brandl 在BSD 许可证下开发. 新版的Python文档就是由Sphinx生成的

- 丰富的输出格式: 支持 HTML (包括 Windows 帮助文档), - LaTeX (可以打印PDF版本), manual pages（man 文档）, 纯文本
- 完备的交叉引用: 语义化的标签,并可以自动化链接函数,类,引文,术语及相似的片段信息
- 明晰的分层结构: 可以轻松的定义文档树,并自动化链接同级/父级/下级文章
- 美观的自动索引: 可自动生成美观的模块索引
- 精确的语法高亮: 基于 Pygments 自动生成语法高亮

创建Sphinx项目 

Sphinx 提供了一个快速创建 Sphinx 项目的脚本 `sphinx-quickstart`
这样一个简单的SPhinx项目就已经创建完成了

导出创建的Sphinx项目 `make html`
Powershell（Windows 下 VS Code 的默认终端）需要使用 .\make html，.\ 不可省略 。

### 修改配置

使用sphinx-quickstart 脚本自动创建的 conf.py 文件存储了SPhinx项目的配置主要包括项目信息、一般配置项以及 HTML 输出选项三大类：

**项目信息配置**

 -- Project information -----------------------------------------------------

from importlib_metadata import version


project = 'learn-sphinx'  
copyright = '2022, gzh'  
author = 'gzh'  
version = '1.0.0'

The full version, including alpha/beta/rc tags
release = '1.0.0rc1'

**一般配置项 (General configuration)**

- extensions: 配置 Sphinx 的扩展，内容是 extensions 模块下的字符串列表。

- source_suffix: 定义源文件的文件扩展名，该值可以是字典映射文件扩展名到文件类型，默认为 source_suffix = {'.rst': 'restructuredtext'}。

- language: 文档编写的语言代码，Sphinx自动生成的任何文本都将使用该语言。目前 Sphinx 支持的语言及其代码可在 Sphinx 官方文档上查询到，我们平时比较常用的有英文和简体中文两种，其语言代码分别是en 与zh_CN。

为 Sphinx 项目添加 Markdown 支持








