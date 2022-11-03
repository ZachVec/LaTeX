# LaTex 模板

## 使用方法

这个仓库里的内容是个人使用的 LateX 模板，使用时直接拉取仓库，然后在模板上填充内容。

使用方法：

1. 在 **Windows** 下安装 Texlive；
2. 将 Texlive 的二进制文件夹`{Texlive 安装路径}\bin\win32`加入环境变量；
3. 安装 vscode，并安装 texstudio 插件。
4. 拉取本仓库到本地，并使用 vscode 打开。
5. 切换到期望的分支（`essay`, `presentation` 等）。
6. 开始填充内容，然后编译。

## Beamer 相关内容

### 关于主题 —— theme

Beamer 的主题有五个部分。

1. 主题 `beamertheme<name>.sty`: 包含以下四个内容。
2. 内主题 `beamerinnertheme<name>.sty`: 定义 `frame` 内部的各种样式，如 *无序列表* 等。
3. 外主题 `beameroutertheme<name>.sty`: 定义 `frame` 外部的各种样式，如 *页首页脚* 等。
4. 字体主题 `beamerfonttheme<name>.sty`: 决定各个地方的字体都是什么。
5. 颜色主题 `beamercolortheme<name>.sty`: 决定各个地方的配色都是什么。

写完这五个主题文件，在自己的 beamer 文档中使用 `\usetheme{name}` 来使用主题。

> Beamer 文档最终读取的内容是从 *主题文件* 中读取的。即必须要在 *主题文件* 中声明使用
> 什么 *内主题*、*外主题*、*字体主题*、*颜色主题*，否则即使写了其他文件也不使用，如下：
>
> ```latex
> % this is beamerthemefoo.sty
> \mode<presentation>
> \usefonttheme{default}
> \usecolortheme{default}
> \useinnertheme{default}
> \useoutertheme{default}
>
> \mode
> <all>
> ```
>
> 已经有一些现成的主题以供挑选，可以在 [Beamer Gallery](https://hartwork.org/beamer-theme-matrix/) 中看看。

### 如何写自己的主题？

- 参考 [Beamer 用户手册](https://tug.ctan.org/macros/latex/contrib/beamer/doc/beameruserguide.pdf) 。
- 参考[知乎专栏](https://www.zhihu.com/column/c_1241818411526680576)。
- 在 [Beamer Gallery](https://hartwork.org/beamer-theme-matrix/) 中挑选合适的模板，改一改。
