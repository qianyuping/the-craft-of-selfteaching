

## 环境配置



### 安装python 3.8



目前，Python有两个版本，一个是2.x版，一个是3.x版，这两个版本是不兼容的。由于3.x版越来越普及，我们的教程将以最新的Python 3.8版本为基础。请确保你的电脑上安装的Python版本是最新的3.8.x，这样，你才能无痛学习这个教程。

**在Mac上安装Python**

如果你正在使用Mac，系统是OS X>=10.9，那么系统自带的Python版本是2.7。要安装最新的Python 3.8，有两个方法：

方法一：从Python官网下载Python 3.8的[安装程序](https://www.python.org/downloads/)，下载后双击运行并安装；

方法二：如果安装了[Homebrew](https://brew.sh/)，直接通过命令`brew install python3`安装即可。

**在Windows上安装Python**

首先，根据你的Windows版本（64位还是32位）从Python的官方网站下载Python 3.8对应的[64位安装程序](https://www.python.org/ftp/python/3.8.0/python-3.8.0-amd64.exe)或[32位安装程序](https://www.python.org/ftp/python/3.8.0/python-3.8.0.exe)，然后，运行下载的exe安装包：

![](D:\B00-picture\python\python install 01.png)

特别要注意勾上`Add Python 3.8 to PATH`，然后点“Install Now”即可完成安装。

**运行Python**

安装成功后，打开命令提示符窗口，敲入python后，会出现两种情况：

情况一：

```ascii
┌────────────────────────────────────────────────────────┐
│Command Prompt                                    - □ x │
├────────────────────────────────────────────────────────┤
│Microsoft Windows [Version 10.0.0]                      │
│(c) 2015 Microsoft Corporation. All rights reserved.    │
│                                                        │
│C:\> python                                             │
│Python 3.8.x ...                                        │
│[MSC v... 64 bit (AMD64)] on win32                      │
│Type "help", "copyright", "credits" or "license" for mor│
│information.                                            │
│>>> _                                                   │
│                                                        │
│                                                        │
└────────────────────────────────────────────────────────┘
```

看到上面的画面，就说明Python安装成功！

你看到提示符`>>>`就表示我们已经在Python交互式环境中了，可以输入任何Python代码，回车后会立刻得到执行结果。现在，输入`exit()`并回车，就可以退出Python交互式环境（直接关掉命令行窗口也可以）。

情况二：得到一个错误：

```ascii
┌────────────────────────────────────────────────────────┐
│Command Prompt                                    - □ x │
├────────────────────────────────────────────────────────┤
│Microsoft Windows [Version 10.0.0]                      │
│(c) 2015 Microsoft Corporation. All rights reserved.    │
│                                                        │
│C:\> python                                             │
│'python' is not recognized as an internal or external co│
│mmand, operable program or batch file.                  │
│                                                        │
│C:\> _                                                  │
│                                                        │
│                                                        │
│                                                        │
└────────────────────────────────────────────────────────┘
```

这是因为Windows会根据一个`Path`的环境变量设定的路径去查找`python.exe`，如果没找到，就会报错。如果在安装时漏掉了勾选`Add Python 3.8 to PATH`，那就要手动把`python.exe`所在的路径添加到Path中。

如果你不知道怎么修改环境变量，建议把Python安装程序重新运行一遍，务必记得勾上`Add Python 3.8 to PATH`。



**小结**

学会如何把Python安装到计算机中，并且熟练打开和退出Python交互式环境。

在Windows上运行Python时，请先启动命令行，然后运行`python`。

在Mac和Linux上运行Python时，请打开终端，然后运行`python3`。



【参考文献】

1. 廖雪峰的官方网站：https://www.liaoxuefeng.com/wiki/1016959663602400/1016959856222624



### pip升级

第一步：首先检测一下我们电脑是否安装了python，打开命令提示框（win系统下，同时按win+R，启动运行对话框），输入python，如果安装了python就会提示出版本信息

第二步：执行exit()命令退出python运行环境

第三步：查看我们的python环境是否安装了pip，执行pip命令会出现如下信息

![](D:\B00-picture\python\python install 02.png)

第四步：查看我们目前pip版本的信息，执行pip show pip命令，会提出相信的版本信息

第五步：执行pip升级命令进行升级，命令是python -m pip install -U pip就行了，安装成功会提示你卸载了旧版本并且安装了最新版本的pip



【参考文献】

1. 百度经验：https://jingyan.baidu.com/article/08b6a591e068cc55a80922a8.html



### Jupyter lab 安装与配置



JupterLab 俗称“程序员的笔记本”。持续学习对于成为优秀的程序员来说至关重要，学习一定要做笔记，如果没钱买笔记本，强烈推荐使用JupterLab。

**jupyterlab 下载方式**

第一种：在cmd中输入命令：

`pip Install jupyterlab`



第二种：打开[pypi官网](https://pypi.org/)，搜索jupyterlab的wheel文件进行下载完成后，在cmd输入命令：

`jupyter lab`



添加桌面图标

该步可以根据需要进行，有以下两种方式
第一种：
在python文件夹中找到Scripts文件夹，在其中找到jupyter-lab.exe文件

创建快捷方式并放在桌面即可

第二种：
在桌面建立一个.txt文件，在文件中输入jupyter lab并保存，将该文件的后缀改为.bat

如果需要改变图标，可以通过以下方式改变（仅针对快捷方式），对于第二种方法生成的桌面图标，则需要再创建一个快捷方式
首先，右键点击快捷方式，打开属性，并点击“快捷方式”



第三种：Anaconda

1. 安装Anaconda，直接上官网 https://www.anaconda.com/，下载并安装与自己电脑匹配的版本，建议安装Python 3.7。

2. 配置JupyterLab，使用Anaconda Prompt进入Terminal，输入： `jupyter lab --generate-config 此时会在目录（C:\Users\Administrator\.jupyter）下生产jupyter_notebook_config.py文件。`
3. 打开jupyter_notebook_config.py,在最后加入以下代码段

```
import webbrowser
webbrowser.register('chrome',None,webbrowser.GenericBrowser(u'C:\Program Files(x86)\Google\Chrome\Application\chrome.exe'))
c.NotebookApp.browser = 'chrome'
```



![](D:\B00-picture\python\python install 04.png)



4. download GitHub开源项目，并用安装好的jupterlab进行阅读。通过Anconada Prompt 进入项目所在目录，然后输入: jupyter lab  即可。

![](D:\B00-picture\python\python install 05.png)



**jupyterlab 样式定制**



对中文用户来说，Jupyter 的默认字号有点过小，阅读起来不是很舒适。但最佳的方案不是去寻找合适的 themes，而是直接使用支持 [Stylus](https://github.com/openstyles/stylus) 这类终端 CSS 定制插件的浏览器，Chrome/Firefox/Opera 都支持 Stylus 插件。

我用的 Stylus 定制 CSS 是这样的：

```css
a {color: #2456A4 !important;}
strong {color:#6392BF;}
em {color: #A9312A; font-style: normal !important;}
table {font-size: 90% !important;}

#jp-main-dock-panel {background-color: #f9f9f9;}
.jp-RenderedHTMLCommon {font-family: "Yuanti SC"; font-size: 100%;}
.jp-Notebook {background-color: #fbfafa;}
.CodeMirror, .jp-RenderedHTMLCommon pre {font-size: 90%;}
.jp-RenderedHTMLCommon pre {
    padding: 10px 25px;
    background-color: #fafafa;
    border-left: 4px solid #dadada;
    border-radius: 10px;
}

.jp-RenderedHTMLCommon pre code {
    background-color: #fafafa;
}

.jp-RenderedHTMLCommon h1 code,
.jp-RenderedHTMLCommon h2 code,
.jp-RenderedHTMLCommon h3 code,
.jp-RenderedHTMLCommon h4 code,
.jp-RenderedHTMLCommon p code, 
.jp-RenderedHTMLCommon li code,
.jp-RenderedHTMLCommon blockquote p code, 
.jp-RenderedHTMLCommon blockquote li code,
.jp-RenderedHTMLCommon td code {
    background-color: #f6f6f6;
    font-size: 90%;
    color:#2e2e2e;
    padding: 4px 4px;
    margin: 0 8px;
    box-shadow: 0px 1px 2px 0px rgba(0,0,0,0.2);
    border-radius: 4px;
}
```

这样就相当于我把 JupyterLab Light 这个 Theme 稍微 Tweak 了一下。

另，我写的内容里，为了重点突出，特别定制了 `strong` 和 `em` 两个元素的显示，让它们以不同的颜色展示；又因为中文并不适合斜体展示，所以，把 `em` 的 `font-style` 设定为 `normal`……



**jupyterlab 安装插件**

Jupyter notebook 经过很多年的发展，现在有很多扩展插件，但也有其中一些并不兼容最新的 Jupyter lab。不过，刚开始的时候用不着那么多插件，你只用其中的两个就足够开始了：

> - [@jupyterlab/toc](https://github.com/jupyterlab/jupyterlab-toc)
> - [ryantam626/jupyterlab_sublime](https://github.com/ryantam626/jupyterlab_sublime)

首先在用快捷键 `⌘ ,` 打开 jupyter lab 的 Advanced Settings，在 Extension Manager 中，添加 User Overrides：

```json
{
    "enabled": true
}
```

而后在 Terminal 执行以下命令安装插件：

```bash
jupyter labextension install @jupyterlab/toc
jupyter labextension install @ryantam626/jupyterlab_sublime
jupyter lab build
```

toc 插件，自动将 ipynb 文件中的标题转换成目录。

jupyterlab_sublime 则可以让你在 Jupyter lab 的 cell 中，使用跟 SublimeText 一样的快捷键，比如 `⌘ D` 能够多选其它与当前选中内容一样的内容；比如 `⌘` 加鼠标点击，可以生成多个可编辑点……





【参考文献】

1. jupyterlab 简单功能与配置一览：https://blog.csdn.net/qq_45404676/article/details/104494123

2. 使用jupyterlab阅读Github开源项目：https://blog.csdn.net/aaeiepb3378/article/details/102013733

3. 安装jupyterlab及各种Extension扩展插件的记录：https://blog.csdn.net/watfe/article/details/108822625

4. 《自学是门手艺》关于 Jupyter lab themes



### git安装及设置



**安装准备**

  1. [廖雪峰老师Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000) ：推荐Git入门教程。

  2. 按照自己的系统版本下载Git软件，我的操作系统：Windows7 64位，安装版本为Git-2.18.0-64-bit.exe（截至2018.8.27最新版本）。
  [Git下载地址](https://git-scm.com/download/win)：国外网站，可确保为最新版本。

  [百度网盘下载](https://pan.baidu.com/s/194uzbJ9vB5lgi_TbxhRE1Q)：国内镜像，如果网速慢可以到网盘下载。
  
  3. 点击Next，默认选项和图中不一样，建议按照图中修改，Git Bash Here和Git GUI Here可以方便的在任意目录下打开git，建议选中，选中这两项后Additional icons->On the Desktop就按照自己心情了。

       ![](D:\B00-picture\python\python install 06.png)

  4. 这一步根据自己需要设置后，不爱折腾的小伙伴下面的步骤可以直接采用默认选项，当然也可以详细研究选择最适合自己的。

  5. 点击next,选择默认编辑器，我选择的是Notepad++。

       ![](D:\B00-picture\python\python install 07.png)

  6. 继续next,配置PATH环境。

       ![](D:\B00-picture\python\python install 08.png)

       

       Use Git from Git Bash only：这是最安全的选择，因为你的PATH根本不会被修改，你只能使用Git Bash的Git命令行工具。
       Use Git from the Windows Command Prompt：这个选项被认为是安全的，它只向PATH添加一些最小的Git包，以避免使用可选的Unix工具混淆环境。你将能够从Git Bash和Windows命令提示符中使用Git。建议选择此项。
       Use Git and optional Unix tools from the Windows Command Prompt：Git和可选的Unix工具都将添加到计算机的PATH中。警告：这将覆盖Windows工具，如“find”和“sort”，只有在了解其含义后才使用此选项。

  7. 继续next，**以下选项均为默认**。

  8. 点击Install开始安装，安装完成后点击Finish即可。
        在开始菜单里点击“Git“Git Bash”，弹出类似命令行的窗口，就说明Git安装成功！
               在任意目录下右击，可以看到右键菜单中有Git GUI Here和Git Bash Here两个选项。

  9. 安装后的设置
       安装完成后需要设置自己的git账号和邮箱，否则无法正确使用，但是到目前为止还没有申请git账号，下面就来说一下具体的账号申请和git设置过程。点击[账号申请网址](https://github.com/) ，出现如下界面。(略)

  10. 因为Git是分布式版本控制系统，所以，每个机器都必须自报家门：你的名字和Email地址。账号申请完成后，打开命令行或者Git Bash，输入
       `git config --global user.name “Your Name”`，之后回车，再输入
       `git config --global user.email email@example.com`

       其中Your Name和email@example.com替换成上面注册时的账户名和邮箱。

       命令行下输入和Git Bash下输入均可。
       命令行下输入如图：

       ![](D:\B00-picture\python\python install 09.png)

       

       Git Bash下输入如图：

       ![](D:\B00-picture\python\python install 10.png)





### git 教程



```bash
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit
```

`pwd`命令用于显示当前目录。在我的Mac上，这个仓库位于`/Users/michael/learngit`。



第二步，通过`git init`命令把这个目录变成Git可以管理的仓库：

```
$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/
```

瞬间Git就把仓库建好了，而且告诉你是一个空的仓库（empty Git repository），细心的读者可以发现当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的，没事千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。

如果你没有看到`.git`目录，那是因为这个目录默认是隐藏的，用`ls -ah`命令就可以看见。



现在我们编写一个`readme.txt`文件，内容如下：

```
Git is a version control system.
Git is free software.
```

一定要放到`learngit`目录下（子目录也行），因为这是一个Git仓库，放到其他地方Git再厉害也找不到这个文件。

和把大象放到冰箱需要3步相比，把一个文件放到Git仓库只需要两步。

第一步，用命令`git add`告诉Git，把文件添加到仓库：

```
$ git add readme.txt
```

执行上面的命令，没有任何显示，这就对了，Unix的哲学是“没有消息就是好消息”，说明添加成功。

第二步，用命令`git commit`告诉Git，把文件提交到仓库：

```
$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```

简单解释一下`git commit`命令，`-m`后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。

嫌麻烦不想输入`-m "xxx"`行不行？确实有办法可以这么干，但是强烈不建议你这么干，因为输入说明对自己对别人阅读都很重要。实在不想输入说明的童鞋请自行Google，我不告诉你这个参数。

`git commit`命令执行成功后会告诉你，`1 file changed`：1个文件被改动（我们新添加的readme.txt文件）；`2 insertions`：插入了两行内容（readme.txt有两行内容）。







> 所谓实用主义，就是掌握了以下知识就可以玩转 `Git`，轻松应对90%以上的需求。以下是实用主义型的Git命令列表，先大致看一下



- `git clone`
- `git config`
- `git branch`
- `git checkout`
- `git status`
- `git add`
- `git commit`
- `git push`
- `git pull`
- `git log`
- `git tag`



**工作区（*Working Directory*）**



![](D:\B00-picture\python\python study 04.png)



**本地版本库（*Local Repository*）**

> 工作区有一个隐藏目录 `.git`，这个不算工作区，而是 `Git` 的版本库。

**暂存区（*stage*）**

> 本地版本库里存了很多东西，其中最重要的就是称为 `stage`（或者叫index）的暂存区，还有`Git` 为我们自动创建的第一个分支 `master`，以及指向 `master` 的一个指针叫 `HEAD`。

![python study 05](D:\B00-picture\python\python study 05.png)



**远程版本库（*Remote Repository*）**

> 一般指的是 `Git` 服务器上所对应的仓库，本文的示例所在的`github`仓库就是一个远程版本库

![python study 06](D:\B00-picture\python\python study 06.png)



**以上概念之间的关系**

> `工作区`、`暂存区`、`本地版本库`、`远程版本库`之间几个常用的 `Git` 操作流程如下图所示：

![python study 07](D:\B00-picture\python\python study 07.png)



**分支（*Branch*）**

> 分支是为了将修改记录的整个流程分开存储，让分开的分支不受其它分支的影响，所以在同一个数据库里可以同时进行多个不同的修改



![python study 08](D:\B00-picture\python\python study 08.png)



**主分支（*Master*）**

> 前面提到过 `master` 是 `Git` 为我们自动创建的第一个分支，也叫主分支，其它分支开发完成后都要合并到 `master`

**标签（*Tag*）**

> 标签是用于标记特定的点或提交的历史，通常会用来标记发布版本的名称或版本号（如：`publish/0.0.1`），虽然标签看起来有点像分支，但打上标签的提交是固定的，不能随意的改动，参见上图中的`1.0` / `2.0` / `3.0`



![python study 09](D:\B00-picture\python\python study 09.png)



**HEAD**

> `HEAD` 指向的就是当前分支的最新提交

![](D:\B00-picture\python\python study 10.png)





【笔记】

> **如何用GitHub记录自己的学习过程**

> 你可以在本地建立一个分支（branch），例如，取名为 `study`：

```bash
git branch study
git checkout study
```

> 如此这般之后，你在本地工作目录中所做的任何修改，都可以提交到 `study` 这个分支之中。





创建本地分支：git branch dev

报错：fatal: Not a valid object name: 'master'.

原因：

 问题描述-一个非法的master,原因：本地还没有创建master，你可以执行以下git branch，会发现没有看到本地分支列表

解决方案：

 如果本地没有文件，添加一个文件

![](D:\B00-picture\python\python study 02.png)



此时本地仓库主干master 创建成功，使用git branch 查看本地分支列表，会查看到如下图所示

![](D:\B00-picture\python\python study 03.png)

可以创建本地分支：

 git branch dev





（为了便于理解，在桌面上演示）

```bash
cd Desktop
mkdir study
cd study
```

以上代码，在桌面创建了一个study的版本库，并将路径指向了study。

![](D:\B00-picture\python\python study 01.png)





查看当前分支、创建/转换分支

```bash
git branch
git branch study
git checkout study
```

关联远程仓库：

```bash
git remote add origin git@github.com:XXX（GitHub账号名）/XXX（GitHub远程仓库分支名）.git
git push -u origin XXX
```





【参考文献】

1. git 下载安装及设置详细教程：https://blog.csdn.net/sanxd/article/details/82624127

2. 廖雪峰git 教程：https://www.liaoxuefeng.com/wiki/896043488029600

3. 工作总结：Git的学习和使用，最详细的Git教程，从入门到精通：https://mp.weixin.qq.com/s/1IPy15Ywh7m2J6x0LFWhUQ