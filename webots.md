此处主要是官方文档指路. (因为偷懒下面摘自官方文档的中文是谷歌机翻)

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

🔗 [出处](https://cyberbotics.com/doc/guide/tutorial-1-your-first-simulation-in-webots#add-an-e-puck-robot)

![image-20200424062307261](webots/image-20200424062307261.png)

![image-20200424062332371](webots/image-20200424062332371.png)

## 一个标准的webots项目文件结构

🔗 [官方文档](https://cyberbotics.com/doc/guide/the-standard-file-hierarchy-of-a-project?tab-language=python)

## 外部程序调试webots控制器

🔗 [官方文档配置使用Pycharm调试webots控制器教程](https://cyberbotics.com/doc/guide/using-your-ide?tab-language=python#pycharm) (对VSC同理)

我已经试了可以配置VSC调试webots控制器.

(只是运行的话用终端就可以)

## 节点

🔗 [官方文档节点从属图](https://cyberbotics.com/doc/reference/node-chart) (这个图里的大部分节点是有超链接的)

## 外观

外观节点有`PBRAppearance`和`Appearance`两种.

🔗 [官方文档PBRAppearance部分](https://cyberbotics.com/doc/reference/pbrappearance)

![image-20200426162539849](webots/image-20200426162539849.png)

PBRAppearance的PBR指的是**P**hysically-**B**ased **R**endering. 从上面描述能看出PBRAppearance渲染效果必然比Appearance好. [这里](https://cyberbotics.com/doc/guide/tutorial-3-appearance#modify-the-appearance-of-the-walls)是一个Appearance和PBRAppearance的效果对比.

## PROTO

🔗 [官方文档PROTO部分](https://cyberbotics.com/doc/reference/proto)

官方并没有给出PROTO是什么含义, 不过我猜是**Proto**type, 即原型. PROTO机制允许用户利用webots内置节点和其他PROTO节点轻松创建新的PROTO节点类型.

## Troubleshooting

### 为什么闪退了

![image-20200424210003023](webots/image-20200424210003023.png)

🔗 [仅使用intel显卡可能导致崩溃](https://cyberbotics.com/doc/guide/general-bugs#intel-graphics-cards)

🔗 [为什么我的机器人/仿真炸了](https://cyberbotics.com/doc/guide/modeling#my-robotsimulation-explodes-what-should-i-do)

🔗 [提高仿真速度](https://cyberbotics.com/doc/guide/speed-performance#how-can-i-change-the-speed-of-the-simulation)

### 为什么变得只有线了

![image-20200424153712413](webots/image-20200424153712413.png)

这个是勾选了`View` > `Wireframe Rendering`的效果, 如果选`View` > `Plain Rendering`就回到熟悉的感觉了.

### 为什么机器人沉入地面了

🔗 [My Robot Sinks into the Ground, How to Remove This Effect?](https://cyberbotics.com/doc/guide/modeling#my-robot-sinks-into-the-ground-how-to-remove-this-effect)

### 为什么每次仿真结果不一样

🔗 [How to Make Replicable/Deterministic Simulations?](https://cyberbotics.com/doc/guide/modeling#how-to-make-replicabledeterministic-simulations)

