# readme
# 标题相关
----
 
```
# 一级标题  
## 二级标题  
### 三级标题  
#### 四级标题  
##### 五级标题  
###### 六级标题  
```

 # 横线相关
-----------
`***` `---` `___` 可以显示横线效果

> 三个* 
> 三个- 
> 三个_

***
---
___
# 文本相关
------
## 普通文本

这是一段普通的文本
## 单行文本

    Hello I'm 星矢.
在一行开头加入1个Tab或者4个空格。

#星矢的见解
> 讲真的一点也不好看
## 文本块

语法1
在连续几行的文本开头加入1个Tab或者4个空格
 
    欢迎到访
    很高兴见到您
    祝您，早上好，中午好，下午好，晚安
 
语法2
使用一对各三个的反引号：
```
这是一段文本
用来测试换行
好不好使的
```
该语法也可以实现代码高亮，见[代码高亮](#代码高亮)
## 文字高亮
文字高亮功能能使行内部分文字高亮，使用一对反引号。
语法：
```
`linux` `网络编程` `socket` `epoll` 
```
效果：`linux` `网络编程` `socket` `epoll`
 
也适合做一篇文章的tag(才知道我下面这东西就叫tag)

#星矢的见解
>**这里感觉是根据你的markdown的默认高亮颜色而有区别的 就比如我这就是单纯的灰色- -**

![[Pasted image 20241121165505.png]]
### 换行

直接回车不能换行，  
可以在上一行文本后面补两个空格，  
这样下一行的文本就换行了。

或者就是在两行文本直接加一个空行。
 
也能实现换行效果，不过这个行间距有点大。

#星矢的见解
>**话说这俩行间距好像是一样的...**
### 斜体、粗体、删除线(实用)

| 语法                  | 效果                |
| ------------------- | ----------------- |
| `*斜体1*`             | *斜体1*             |
| `_斜体2_`             | _斜体2_             |
| `**粗体1**`           | **粗体1**           |
| `__粗体2__`           | __粗体2__           |
| `这是一个 ~~删除线~~`      | 这是一个 ~~删除线~~      |
| `***斜粗体1***`        | ***斜粗体1***        |
| `___斜粗体2___`        | ___斜粗体2___        |
| `***~~斜粗体删除线1~~***` | ***~~斜粗体删除线1~~*** |
| `~~***斜粗体删除线2***~~` | ~~***斜粗体删除线2***~~ |
 
> 斜体、粗体、删除线可混合使用
 
# 图片
------
## 基本格式
```
![alt](URL title)
```
alt和title即对应HTML中的alt和title属性（都可省略）：

- alt表示图片显示失败时的替换文本
- title表示鼠标悬停在图片时的显示文本（注意这里要加引号）
> **这两个属性和 `html` 里面的 `img` 标签的属性效果完全一致 学过前端的话 应该不难理解**
## 引用图片

1. 相对路径引用图片
`![这是百度logo](./assets/baidu.png "百度")`
![baidulogo](baidu.png "图片")
 2. 网页地址引用
![](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png)
3. `html` 写法
```
<img src="./assets/baidu.png" alt="不知道为啥就是不显示这个图片..." title="wenben"/>
```
<img src="./imgs/baidu.png" alt="不知道为啥就是不显示这个图片..." title="wenben"/>

4. ![][baidu-logo]` ![][baidu-logo]`
这个例子用到了**URL标识符** 在[图片链接](#图片链接)有讲
5. 还有绝对路径引图片 但是有局限性 不能分享md给别人 就不具体写了

# 链接
------
## 链接外部URL

| 例子  | 语法                                             | 效果                                           |
| --- | ---------------------------------------------- | -------------------------------------------- |
| 1   | `[我的Github](https://github.com/Jctsy/ "点击前往")` | [我的GitHub](https://github.com/Jctsy/ "点击前往") |
| 2   | `[跳转知乎][zhihu] `                               | [跳转知乎][zhihu]                                |


例子2由两部分组成：
- 第一部分使用两个中括号，[ ]里的标识符（本例中zhihu），可以是数字，字母等的组合，标识符上下对应就行了（**姑且称之为URL标识符**）
- 第二部分标记实际URL。

>使用URL标识符能达到复用的目的，一般把全文所有的URL标识符统一放在文章末尾，这样看起来比较干净。
>>URL标识符是我起的名字，不知道是否准确。囧。。(原作者大大的话 就保留了囧 _ _ _)


#星矢的见解
>个人小见解：这东西有点像编程语言里面的的***变量名与变量值***，定义了一个变量在下面 变量名:链接也就是变量值(一般是放在.md文章末尾) 然后通过变量名(也就是这个例子里面的zhihu) 然后使用的时候 直接写变量名就行了

> 个人感觉这么写是的md**更容易维护了** 比如这个链接失效了，去文章中找很麻烦 但是如果链接统一写成这种形式的话 可以在文章末尾快速定位 进行修改


## 链接本仓库里的URL
 
|                                     语法                                     | 效果                                                                       |
| :------------------------------------------------------------------------: | ------------------------------------------------------------------------ |
| `[Blog简介](https://github.com/Jctsy/Jctsy.github.io/blob/master/README.md)` | [Blog简介](https://github.com/Jctsy/Jctsy.github.io/blob/master/README.md) |
|                           `[example](./example)`                           | [example](./example)                                                     |
 
## 图片链接
给图片加链接的本质是混合图片显示语法和普通的链接语法。普通的链接中[ ]内部是链接要显示的文本，而图片链接[ ]里面则是要显示的图片。  
直接混合两种语法当然可以，但是十分啰嗦，为此我们可以使用URL标识符的形式。
 
| 数字  |                                        语法                                        |                                     效果                                     | 备注                                           |
| :-: | :------------------------------------------------------------------------------: | :------------------------------------------------------------------------: | -------------------------------------------- |
|  1  |                ```[![](imgs/baidu.png)](http://www.baidu.com)```                 |              [![baidu](imgs/baidu.png)](http://www.baidu.com)              | 经典写法 复杂 但是好理解                                |
|  2  |                    ```[![](imgs/baidu.png  "百度一下")][baidu]```                    |                    [![](imgs/baidu.png  "百度一下")][baidu]                    | 简化了跳转链接 定义链接引出去了                             |
|  3  |                        ```[![](imgs/csdn.png) ][csdn]```                         |                        [![](imgs/csdn.png) ][csdn]                         | 同上 然后和上面的区别就是没有""里面的内容 那是鼠标悬停的时候显示的内容        |
|  4  | ```[![](https://www.baidu.com/img/flexible/logo/pc/result.png "百度一下")][baidu]``` | [![](https://www.baidu.com/img/flexible/logo/pc/result.png "百度一下")][baidu] | 可能上面感觉相对路径也没多写多少东西 来看这个的 网络图片地址 是不是就一大坨 不好看了 |
|  5  |         ```[![csdn-logo]][csdn]```<br>![CDSN](imgs/csdn.png "手动添加这个图片吧")         |                            [![csdn-logo]][csdn]                            | 这是相对路径的图片但不知道为啥就是显示不出来呢 一样的很简洁               |
|  6  |                           ```[![baidu-logo]][baidu]```                           |                           [![baidu-logo]][baidu]                           | 这样看起来很简洁了，但是也是引得网络图片不过也是和链接一样的处理方式 看起来简洁了许多  |
|     |                                                                                  |                                                                            |                                              |


因为图片本身和链接本身都支持URL标识符的形式，所以图片链接也可以很简洁（见数字5 6）。  

#星矢的见解 
>但是我没捣鼓明白这个图片的链接简化 - -
>然后所有的URL标识符都在文末了


 
## 锚点
其实呢，每一个标题都是一个锚点，和HTML的锚点（`#`）类似，比如我们 
 
| 语法                | 效果              |
| ----------------- | --------------- |
| `[回到顶部](#readme)` | [回到顶部](#readme) |
| `[标题](#标题相关)`     | [标题](#标题相关)     |
 
不过要注意，标题中的英文字母都被转化为**小写字母**了。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦！
 
## 列表
### 无序列表

 语法
```
* 昵称：星矢
* 英文名：Xingshi
```

效果
* 昵称：星矢
* 英文名：Xingshi
 
### 多级无序列表

语法 

#星矢的见解 
就是一级 然后 回车`Enter` 再 `Tab` 键然后第二级就有了

```
* 编程语言
    * 脚本语言
        * JavaScript
```

效果

* 编程语言
    * 脚本语言
        * JavaScript
 
### 一级有序列表

语法

就是在数字后面加一个点，再加一个空格。不过看起来起来可能不够明显。 
```
面向对象的三个基本特征：
 
1. 封装
2. 继承
3. 多态
```
 
效果

面向对象的三个基本特征：
 
1. 封装
2. 继承
3. 多态
 
 
### 多级有序列表
和无序列表一样，有序列表也有多级结构。

语法
```
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
```
 
效果
 
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
	 

一二三

1. 一级
	1.  二级
		1. 三级
### 复选框列表

语法
```
- [x] 数据采集
- [x] 数据清洗
- [x] 数据预处理
- [ ] 数据分析
- [ ] 数据可视化
```

效果
 
- [ ] 数据采集
- [ ] 数据清洗
- [ ] 数据预处理
- [x] 数据分析
- [x] 数据可视化
 
您可以使用这个功能来标注某个项目各项任务的完成情况。
> Tip:
>> 在GitHub的**issue**中使用该语法是可以实时点击复选框来勾选或解除勾选的，而无需修改issue原文。

#星矢的见解 
**是好用哈这个法 做那种选择题的md文档或者选项式的时候很好使**
## 块引用
 
### 常用于引用文本
##### 文本摘自《深入理解计算机系统》P27
　令人吃惊的是，在哪种字节顺序是合适的这个问题上，人们表现得非常情绪化。实际上术语“little endian”（小端）和“big endian”（大端）出自Jonathan Swift的《格利佛游记》一书，其中交战的两个派别无法就应该从哪一端打开一个半熟的鸡蛋达成一致。因此，争论沦为关于社会政治的争论。只要选择了一种规则并且始终如一的坚持，其实对于哪种字节排序的选择都是任意的。
　
> **“端”（endian）的起源**  
以下是Jonathan Swift在1726年关于大小端之争历史的描述：  
“……下面我要告诉你的是，Lilliput和Blefuscu这两大强国在过去36个月里一直在苦战。战争开始是由于以下的原因：我们大家都认为，吃鸡蛋前，原始的方法是打破鸡蛋较大的一端，可是当今的皇帝的祖父小时候吃鸡蛋，一次按古法打鸡蛋时碰巧将一个手指弄破了，因此他的父亲，当时的皇帝，就下了一道敕令，命令全体臣民吃鸡蛋时打破较小的一端，违令者重罚。”

#星矢的见解 
**这个Obsidian的默认引用样式是真丑 - -**
### 块引用有多级结构

语法
```
> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树
```
效果

> 数据结构
>> 树
>>> 二叉树
>>>> 平衡二叉树
>>>>> 满二叉树
代码高亮
----------
 
### 高亮指定编程语言(实用)
在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号。
 效果
#星矢的见解 

**适合做花里胡哨的文档使**

```Java
System.out.println("Hello World"); //Java
```
```c
printf("Hello World\n"); //C
```
```Bash
echo "hello GitHub" #Bash
```
```javascript
console.log('Hello World'); //javascipt
```
```python
print("Hello World")//python
```
# 表格
--------
 
表头1  | 表头2|
--------- | --------|
表格单元  | 表格单元 |
表格单元  | 表格单元 |
 
| 表头1  | 表头2  |
| ---- | ---- |
| 表格单元 | 表格单元 |
| 表格单元 | 表格单元 |
 
### 对齐
表格可以指定对齐方式

```
| 左对齐           |       居中        |   右对齐 |
| :------------ | :-------------: | ----: |
| col 3 is      | some wordy text | $1600 |
| col 2 is      |    centered     |   $12 |
| zebra stripes |    are neat     |    $1 |
```

| 左对齐           |       居中        |   右对齐 |
| :------------ | :-------------: | ----: |
| col 3 is      | some wordy text | $1600 |
| col 2 is      |    centered     |   $12 |
| zebra stripes |    are neat     |    $1 |
 
### 混合其他语法
表格单元中的内容可以和其他大多数GFM语法配合使用，如：  
##### 使用普通文本的删除线，斜体等效果
 
| 名字    | 描述                           |
| ----- | ---------------------------- |
| Help  | ~~Display the~~ help window. |
| Close | _Closes_ a window            |
 ~~删除线~~
##### 表格中嵌入图片（链接）
其实前面介绍图片显示、图片链接的时候为了清晰就是放在在表格中显示的。
 
| 图片                     | 描述  |
| ---------------------- | --- |
| [![baidu-logo]][baidu] | 百度  |
|                        |     |
 
# 表情
----------
Github的Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情😀

比如`:blush:`，可以显示:blush:。

具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。
 
但是这个网页每次都打开**奇慢**。。所以我整理到了本repo中，大家可以直接在此查看[emoji](https://github.com/pcsAndRcx/README/blob/master/emoji.md)。

#星矢的见解 
>**但是现在好像不行了，只能直接复制他的表情下来用了**
 
# diff语法
---------
版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。
GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。
#### 语法
其语法与代码高亮类似，只是在三个反引号后面写diff，
并且其内容中，以 `+ `开头表示新增，`- `开头表示删除。
 
#### 效果
 
```diff
+ 人闲桂花落，
- 夜静春山空。
! 月出惊山鸟，
# 时鸣春涧中。
```

# 常用HTML语法
markdown是支持HTML语法的，虽然不鼓励大量使用HTML语法，毕竟那样就丧失了markdown的意义，但是有一些HTML语法在写README的时候是很少的补充。

#星矢的见解 
**但是html是真的好使呀！**
### 折叠
```
<details>
<summary>Linux环境</summary>

##### 编译
xxxx

##### 安装
xxxx
</details>
```
<details>
<summary>Linux环境</summary>

##### 编译
xxxx

##### 安装
xxxx

</details>

### 居中

很多地方都会用到居中的效果，比如如下内容将会把一个表格在页面中居中展示：

```
<div align="center">

| 表头1  | 表头2|
| ---------- | -----------|
| 表格单元   | 表格单元   |
| 表格单元   | 表格单元   |

</div>
```

<div align="center">

| 表头1  | 表头2|
| ---------- | -----------|
| 表格单元   | 表格单元   |
| 表格单元   | 表格单元   |

</div>

其他任意需要居中展示的语法，都可以放在其中。

# 其他
还有一些非markdown语法，但是在README文件中也很实用的组件。
### 徽章
绘制徽章，首选就是[shields.io](https://shields.io/)  具体语法去官网探索。

![LICENSE](https://img.shields.io/badge/license-MIT-green)

其次有些第三方平台也提供方便的徽章，比如gitter：

[![Join the chat at https://gitter.im/guodongxiaren/README](https://badges.gitter.im/guodongxiaren/README.svg)](https://gitter.im/guodongxiaren/README?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

#星矢的见解 
**我真的很get这个呀！一个个的小图标 感觉真的很好玩**
### star历史
star历史可以使用这个网站[star-history.com](https://star-history.com/)
```
[![Star History Chart](https://api.star-history.com/svg?repos=guodongxiaren/README&type=Date)](https://star-history.com/#guodongxiaren/README&Date)
```
这段代码的显示效果如下：
这是这个大佬的项目：[果冻虾仁](https://github.com/guodongxiaren)

[![Star History Chart](https://api.star-history.com/svg?repos=guodongxiaren/README&type=Date)](https://star-history.com/#guodongxiaren/README&Date)


---
引用图片(需要在查看源码格式查看)

[baidu]: https://www.baidu.com/ "百度一下"
[csdn]: https://www.csdn.net "点击跳转到CSDN"
[zhihu]: https://www.zhihu.com
[csdn-logo]:./assets/csdn.png "点击跳转CSDN"
[baidu-logo]: http://www.baidu.com/img/bdlogo.gif "百度baidu"

# 参考：

[Markdown 语法大全详解_markdown语法-CSDN博客](https://blog.csdn.net/w11111xxxl/article/details/140783343)

[pcsAndRcx/README: README文件语法解读，即Github Flavored Markdown语法介绍](https://github.com/pcsAndRcx/README)

[gitHub里面的README.MD编辑器的使用手册_readme编辑器-CSDN博客](https://blog.csdn.net/QQ826688096/article/details/89440483)

[创建README.md文件_readmemd文件怎么打开-CSDN博客](https://blog.csdn.net/zhao_jing_bo/article/details/68063070)

[怎么使表格内容垂直居中啊 - 疑问解答 - Obsidian 中文论坛](https://forum-zh.obsidian.md/t/topic/28753/3)

[Github表情包官方网站](https://www.webfx.com/tools/emoji-cheat-sheet/)

[表情包 大佬果冻虾仁Download版 (github.com)](https://github.com/pcsAndRcx/README/blob/master/emoji.md)

[制作徽章的网站](https://shields.io/)

[可视化stars的网站](https://star-history.com/)