# teamwork

1. [开发规范](#开发规范)
   1. [文件命名](#文件命名)
   2. [文件编码格式](#文件编码格式)
   3. [代码](#代码)
      1. [语言及版本](#语言及版本)
      2. [虚拟环境管理器](#虚拟环境管理器)
      3. [代码风格](#代码风格)
      4. [结对编程](#结对编程)
      5. [调试信息](#调试信息)
      6. [各组应给出原理图](#各组应给出原理图)
2. [学习资料](#学习资料)
   1. [markdown](#markdown)
   2. [git和GitHub](#git和GitHub)
   3. [文档驱动开发](#文档驱动开发)
   4. [项目管理](#项目管理)
   5. [ssh](#ssh)
   6. [Python](#Python)
   7. [效率工具](#效率工具)
   8. [Zenhub](#Zenhub)

## 开发规范

### 文件命名

**文件名只应包含数字, 字母, 汉字, 下划线 ( _ ), 连字符 ( - ), 句点 ( . )**

💡 空格以下划线代替, 其他字符以连字符代替.

文件名包含其他字符容易导致程序出错. 为避免麻烦我们以这样的形式规范命名文件. 文件名包含其他字符可能造成的问题举例:

- `文件名里 有空格.jpg` 这样的文件名很可能让程序以为要处理的文件的名字是`文件名里`, 因而找不到文件或者处理了错误的文件. 而`有空格.jpg`会被当成无效参数, 多余字符.
- `文件名里/有左斜杠.avi` 这样的文件名在很多程序里会被认为是一个名为`文件名里`的文件夹下的`有左斜杠.avi`文件, 因此可能得到**没有"文件名里"这个文件夹**的报错
- `文件名里(有)括号.gif` 比如在markdown文档中用`![](文件名里(有)括号.gif)`来引用这个gif, 在有的markdown渲染器会被渲染为`)括号.gif`. 因为前一个\)被认为是markdown引用图片的`![]()`语法的结束符了.

### 文件编码格式

**请使用UTF-8作为程序, 文档文件的编码格式**

如果你用的是系统语言为简体中文的Win10系统, 那么你的系统默认编码格式是**cp936**, 也称**GBK** (不过大部分编程软件默认使用UTF-8作为文件编码格式). 如果用UTF-8编码格式打开实际编码格式为cp936的文件就会出现下图效果.

![image-20200227090637990](image-20200227090637990.png)

> 上图文字内容与上一段话一样.

![image-20200227091026869](image-20200227091026869.png)

> 如果你使用Visual Studio Code, 在状态栏里可以看到当前文件是以什么编码格式打开的. 点击它可以更改当前文件保存/读取时使用的编码格式.

🔗 [了解更多关于cp936](https://leojhonsong.github.io/zh-CN/2019/05/29/%E6%9C%89%E5%85%B3%E5%AD%97%E7%AC%A6%E9%9B%86%E4%B8%8E%E7%BC%96%E7%A0%81/#%E8%87%AA%E6%95%B4%E7%90%86%E7%9A%84%E4%B8%AD%E6%96%87%E5%AD%97%E7%AC%A6%E9%9B%86%E5%8F%91%E5%B1%95%E5%8F%B2)

### 代码

#### 语言及版本

因为以树莓派4为主板, 相关Python生态很好, 另外Python语法较为直观, 开发迅速, 除底盘组内容我们先统一以**Python3.7**为开发语言验证原型, 如果有必要后期再用C++重写需要算力部分.

#### 虚拟环境管理器

为避免大家环境冲突, 统一使用**conda**作为Python虚拟环境管理器.

#### 代码风格

建议统一使用[pycodestyle](http://pycodestyle.pycqa.org/en/latest/intro.html) (旧称pep8)作为Python代码样式检查器, [autopep8](https://pypi.org/project/autopep8/)作为Python代码自动格式化工具.

#### 结对编程

为利于结对编程请大家一定要写尽量详尽的**代码注释**, 同时要写**文档**, 方便其他组同学快速了解你们部分的原理及如何配合.

#### 调试信息

在关键处一定要打印彩色调试信息. 🔗 [参考](https://leojhonsong.github.io/zh-CN/2019/09/12/Linux%E7%BB%88%E7%AB%AF%E5%91%88%E7%8E%B0%E5%BD%A9%E8%89%B2%E8%BE%93%E5%87%BA/)

#### 各组应给出原理图

建议各组给出原理图/框架图, 方便debug, 组间交流, 展示.

## 学习资料

为方便大家了解各自在做什么, 相互学习, 方便后期报告写作, 我们把看到的好的相关资料整理到这里吧.

### markdown

你目前看到的这份文档就是一个markdown文件😏

因此markdown算是我们沟通的一大关键, 请大家学习一下🙏

🔗 [markdown教程](https://leojhonsong.github.io/zh-CN/2019/09/23/Markdown%E5%AE%89%E5%88%A9-Typora%E7%AE%80%E8%A6%81%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B/)

### git和GitHub

[详情](git和github.md)

### 文档驱动开发

🔗 [Readme Driven Development](https://tom.preston-werner.com/2010/08/23/readme-driven-development.html)

### 项目管理

🔗 [如何使用 Issue 管理软件项目](http://www.ruanyifeng.com/blog/2017/08/issue.html)

### ssh

小车在线调试前期远程连接小车的方式. 因为主板打算采用树莓派4, 因此只需要让树莓派和电脑在同一个WiFi下就可以通过访问树莓派ip来ssh连接. (树莓派自身开启热点/手机热点)

[详情](ssh.md)

### Python

🔗 [python速成-python图像处理体验](https://uestc-fury.com/2019/02/python%E9%80%9F%E6%88%90-python%E5%9B%BE%E5%83%8F%E5%A4%84%E7%90%86%E4%BD%93%E9%AA%8C/) 👈 Anaconda是什么&Anaconda安装教程&一些Python处理图像的内容

💡 这篇文章的内容稍有过时, [清华镜像源](https://mirror.tuna.tsinghua.edu.cn/help/anaconda/)已恢复且因为版权问题国内目前只有这一个Anaconda源

💡 如果即便你给Anaconda换了国内源用conda下载东西速度还是很慢, 或者你更喜欢用pip安装python包, 也可以给pip换[清华源](https://mirror.tuna.tsinghua.edu.cn/help/pypi/) (速度很快). ⚠️ 减少conda与pip混用.

🔗 [Python语法速成](https://leojhonsong.github.io/zh-CN/2019/09/12/Python%E5%9F%BA%E7%A1%80%E8%AF%AD%E6%B3%95/)

💡 这个网站的表格是熊猫色, 没设置好, 白底白字看不大清可以选中来看清. 大家将就一下😅

🌟 [Python Tutor](http://pythontutor.com/) 是一个强烈推荐的可视化你的Python代码运行具体过程的网页工具

### 效率工具

鉴于大家用的都是Windows系统我们就只讨论Windows系统的好工具吧.

[详情](效率工具.md)

### Zenhub
[详情](Zenhub.md)