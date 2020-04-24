此处主要是官方文档指路.

❗️ 据我观察webots从最开始到现在变化较大, 发布时间较早的教程参考价值不那么大.

## 语言

建议直接英文, 这个中文是阉割版的. 只有菜单栏里本来就能看懂的翻译过来了, 真正有点难理解的词并没有翻译... 文档也只有英文的, 如果软件语言中中文有时候可能并不能很快把文档说明和软件里的词对应上.

## 查看

<kbd>Alt</kbd> <kbd>5</kbd>

## 建议设置

![image-20200424152241305](webots/image-20200424152241305.png)

🔗 [官方文档偏好设置部分](https://cyberbotics.com/doc/guide/preferences)

- 启动模式建议设置为**Pause**, 这样不会每次打开一个世界就在运行仿真了.
- 如果使用了Python虚拟环境那么要注意在偏好中`Python command`这项设置为你需要的python解释器的路径

## 编辑流程

![image-20200424062307261](webots/image-20200424062307261.png)

![image-20200424062332371](webots/image-20200424062332371.png)

## 一个标准的webots项目文件结构

🔗 [官方文档](https://cyberbotics.com/doc/guide/the-standard-file-hierarchy-of-a-project?tab-language=python)

## 外部程序调试webots控制器

🔗 [官方文档配置使用Pycharm调试webots控制器教程](https://cyberbotics.com/doc/guide/using-your-ide?tab-language=python#pycharm) (对VSC同理)

## PRBAppearance

**P**hysics **R**ender **B**ased

## PROTO

**Proto**typing

## Troubleshooting

### 为什么闪退了

![image-20200424210003023](webots/image-20200424210003023.png)

### 为什么变得只有线了

![image-20200424153712413](webots/image-20200424153712413.png)

这个是勾选了`View` > `Wireframe Rendering`的效果, 如果选`View` > `Plain Rendering`就回到熟悉的感觉了.