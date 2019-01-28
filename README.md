源文档：https://github.com/awayings/mac-dev-setup/blob/master/README.md

# iTerm2安装
由于我们将在命令行中花费大量时间，让我们安装一个比默认终端更好的终端。下载并安装iTerm2（最新版本，即使它说的是“beta版”）。

在Finder中，将iTerm应用程序文件拖放到Applications文件夹中。

您现在可以通过Launchpad启动iTerm 。

让我们快速改变一些偏好。在iTerm>首选项...中，在常规选项卡下，取消选中确认关闭多个会话，并在结束部分下确认“退出iTerm2（Cmd + Q）”命令。

在选项卡“ 个人档案”中，使用“+”图标创建一个新的，然后将其重命名为您的名字。然后，选择其他操作...>设为默认值。最后，在Window部分下，将大小更改为更好的内容，例如Columns：125和Rows：35。

完成后，点击左上方的红色“X”（在OS X首选项窗格中自动保存）。关闭窗口并打开一个新窗口以查看大小更改。


# Consolas（可选）
我非常喜欢用于编码的Consolas字体。作为Microsoft（！）字体，默认情况下不会安装它。由于我们将要查看大量的终端输出和代码，现在让我们安装它。

我们可以通过两种方式安装它。如果您购买了Microsoft Office for Mac，请安装它，并安装Consolas。

如果您没有Office，请按照下列步骤操作：
`$ brew install cabextract
$ cd ~/Downloads
$ mkdir consolas
$ cd consolas
$ curl -O http://download.microsoft.com/download/f/5/a/f5a3df76-d856-4a61-a6bd-722f52a5be26/PowerPointViewer.exe
$ cabextract PowerPointViewer.exe
$ cabextract ppviewer.cab
$ open CONSOLA*.TTF`

然后单击安装字体。感谢Alexander Zhuravlev的发帖。


# 美丽的终端
由于我们在码头上花了这么多时间，我们应该努力使它成为一个更加愉快和多彩的地方。以下内容可能看起来很多，但相信我，它会让开发体验变得更好。

让我们继续，先改变字体。在iTerm>首选项...中，在选项卡配置文件，文本部分下，将两种字体更改为Consolas 13pt。

现在让我们添加一些颜色。我是Solarized配色方案的忠实粉丝。它应该是科学上最适合眼睛的。我发现它很漂亮。

向下滚动页面并下载最新版本。解压缩存档。在其中，您将找到iterm2-colors-solarized带有README.md文件的文件夹，但我将在此处引导您完成：

在iTerm2首选项中，在“ 配置文件和颜色”下，转到“ 加载预设...”>“导入...”，找到并打开我们下载的两个.itermcolors文件。
返回Load Presets ...并选择Solarized Dark来激活它。瞧！
注意：您不必这样做，但Solarized Dark预设中有一种我不同意的颜色，即Bright Black。你会发现它太接近黑色了。因此我将其更改为与亮黄色相同，即R 83 G 104 B 112。

还没有很多颜色。我们需要调整一下我们的Unix用户的配置文件。这是在OS X和Linux上完成的，在~/.bash_profile文本文件中（~代表用户的主目录）。

我们稍后会回过头来看详细信息，但是现在，只需将附加到此文档的文件.bash_profile，.bash_prompt，.aliases下载到您的主目录中（.bash_profile是加载的文件，我已经设置好了）打电话给其他人）：

`$ cd ~
$ curl -O https://raw.githubusercontent.com/awayings/mac-dev-setup/master/.bash_profile
$ curl -O https://raw.githubusercontent.com/awayings/mac-dev-setup/master/.bash_prompt
$ curl -O https://raw.githubusercontent.com/awayings/mac-dev-setup/master/.aliases`
然后，打开一个新的终端选项卡（Cmd + T）并查看更改！尝试列表命令：ls，ls -lh（别名ll），ls -lha（别名la）。

此时，您还可以更改计算机的名称，该名称显示在此终端提示符中。如果要执行此操作，请转至“ 系统首选项” >“ 共享”。例如，我将“Nicolas的MacBook Air”改为“MacBook Air”，因此它显示MacBook-Air在终端中。

现在我们有一个可以使用的终端！

（感谢Mathias Bynens的精彩dotfiles。）
