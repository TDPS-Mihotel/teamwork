1. [git](#git)
   1. [Commit message](#Commit-message)
   2. [图形化软件](#图形化软件)
      1. [GitHub Desktop](#GitHub-Desktop)
      2. [Tower](#Tower)
      3. [开发工具集成的git管理](#开发工具集成的git管理)
2. [GitHub](#GitHub)

先有git, 许久后才有了GitHub等代码托管平台. git是一个软件而GitHub是一个网站. 他们的关系是你可以通过git将你的代码托管给GitHub (就是把你的代码存到GitHub的服务器上)

## git

git是一个**分布式版本控制**软件. 与它齐名的另一个版本控制软件是**SVN**.

🔗 [为什么要版本控制及分布式版本控制原理](https://blog.csdn.net/xiaoqiangyonghu/article/details/78400313)

[git安装教程](/git安装教程.md)

🔗 [git命令行常用命令](https://leojhonsong.github.io/zh-CN/2019/02/27/Git%E6%9D%82%E8%AE%B0/)

💡 因为我们的代码托管在GitHub (这意味着服务器在美国), 因此可能下载/上传速度很慢. 如果你知道你的翻墙工具的代理端口那么你可以设置git使用这个端口, 速度会好很多. (如果你的翻墙工具是直接全局代理了所有流量那么不需要这一步)

```shell
# 比如我知道自己VPN的http代理端口为: 127.0.0.1:1234,
# socks代理端口为: 127.0.0.1:5678

# 设置git使用http代理端口
git config --global http.proxy http://127.0.0.1:1234

# 设置git使用socks代理端口
git config --global http.proxy socks5://127.0.0.1:5678

# 取消git使用代理
git config --global --unset http.proxy
```

### Commit message

🔗 [Commit message 和 Change log 编写指南](http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)

### 图形化软件

虽然有人仍喜欢用纯命令行并且有的命令只能在命令行输入, 但我更喜欢使用图形化软件来操作git. 此处推荐三款软件.

#### GitHub Desktop

🔗 [下载地址](https://desktop.github.com/)

GitHub官方客户端. 我自己也在用. 它的特点是**只能管理托管在GitHub的git仓库**. (不过我们仓库都在GitHub所以没影响) 它很有用的一点是**能在一个面板上看到你每个仓库的更新情况**. (我经常忘记哪个仓库有没有上传)

❗️ 要打开软件等它检测一会才会显示出来状态.

![image-20200227141011525](git和github/image-20200227141011525.png)

> 仓库名字后有蓝色点表示有本地更改未提交, 有向上箭头表示有本地提交未上传, 有向下箭头表示有远程端有比本地更新的提交需要拉取.

🔗 [GitHub Desktop使用帮助](https://help.github.com/cn/desktop/contributing-to-projects)

#### Tower

🔗 [下载地址](https://www.git-tower.com)

这个软件看起来比GitHub Desktop功能强大些, 并且不像后者只能管理托管在GitHub的git仓库. 这个软件只能免费试用, 但申请了这个[GitHub学生大礼包](https://education.github.com/pack)的话可以免费用一年.

#### 开发工具集成的git管理

实际上这是我最常使用的方式

![](git和github/image-202002271546.png)

这是装了**GitLens**插件的**Visual Studio Code**的源代码控制面板和编辑窗口截图. 可以看到左下角显示了当前分支及同步状态, 编辑窗口里有颜色条标示文件更改情况, 右上角有可以对文件进行的一些git操作, etc...

## GitHub

🌟🌟🌟 我新建了一个[仓库](https://github.com/TDPS-Mihotel/fuckme)给大家尝试git和GitHub, 请随意蹂躏 👍

🔗 [GitHub中文帮助文档-快速入门](https://help.github.com/cn/github/getting-started-with-github/set-up-git)

🔗 [GitHub中文帮助文档-如何从GitHub克隆仓库](https://help.github.com/cn/github/creating-cloning-and-archiving-repositories/cloning-a-repository)

🔗 [https克隆与ssh克隆的具体区别](https://help.github.com/en/github/using-git/which-remote-url-should-i-use)

💡 推荐使用https克隆, 速度会比ssh克隆快许多. https克隆导致的每次上传需要输入用户名及密码问题可以通过下面命令解决.

```shell
# 永久保存用户名及密码
git config --global credential.helper store
```

🔗 [知乎-你真的会高效的在GitHub搜索开源项目吗?](https://zhuanlan.zhihu.com/p/55294261)