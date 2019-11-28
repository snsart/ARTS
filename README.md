# ARTS
Algorithm、Review、Technique、Share

## 第1期
date:2019.10.22

**A: 算法**

|#|Question|Status|Language|
|-|-|-|-|
|0001|Two Sum|Accepted|js|

**R: 阅读和点评**

[react:Getting Started](https://reactjs.org/docs/getting-started.html)

**T: 知识和技巧**

1. 使用map通过值找索引 
2. js垃圾回收

**S: 分享和输出**

垃圾回收的本质

---

## 第2期

date:2019.10.23

#### A: 算法

|#|Question|Status|Language|
|-|-|-|-|
|0002|Add Two Numbers|Accepted|js|


#### R: 阅读和点评

read:[Concurrency model and the event loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

![image](https://developer.mozilla.org/files/4617/default.svg)
1. understand the concept of eventloop,taskQuene and stack of frames
2. know the time when message be added to taskQuene
3. async task include settimeout/intervial dom event and es6 promise


#### T: 知识和技巧

###### 标准模型和IE模型设置
```
box-sizing:content-box//标准模型
box-sizing:border-box//IE模型
```

###### 盒模型重点:BFC(Block Formatting Context)的概念

BFC为块格式化上下文,主要为了解决父子级边距折叠等问题

* BFC特点如下:<br>

1. BFC兄弟元素之间正常折叠
2. 和float元素之间不会重叠
3. 大小包含内部的float元素大小
4. 大小包含内部元素外边距

###### BFC的实现

1. float不为none
2. display为flex或table相关
3. position不为static或relative
4. overflow不为visible，可设置为hidden或auto

上述四种满足任意一种块元素即变为BFC


###### html元素快捷输入

举例：
```
section.wrap>ul>li*3

<section class="wrap">
  <ul>
     <li></li>
     <li></li>
     <li></li>
  </ul>
</section>
```

#### S: 分享和输出

如何判断某个技术自己是否真正掌握了，学习新技术有三个阶段。阶段一： 根据操作文档一步步实现一遍；阶段二：熟练应用，理解该技术的优缺点；阶段三：深入理解技术背后的实现原理和思想，对同类技术有过交叉比较，内化为自己的思想。只有达到阶段三，才算真正掌握了该技术。

---

## 第3期

date:2019.10.24


#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0003|Longest Substring Without Repeating Characters|Accepted|js|

技巧:sliding window


#### R: 阅读和点评
read:[Separating Axis Theorem (SAT) Explanation](https://www.sevenson.com.au/actionscript/sat/)

SAT is use to resolve the collisions between convex polygons. how it works?
there is a visual sample to explain the principle:Imagine taking a torch and shining it on the two shapes you are testing from different angles. What sort of shadows would it cast on the wall behind it? if you never find a gap in the shadows then the objects must be touching.<br> 
From a programming point view,we only need to consider the angle from sides the two shapes we are testing have, due to the nature of the polygon.Eg. Two pentagons would require ten angles to be checked.<br>
the detail is explained in the article.


#### T: 知识和技巧

###### sliding window
通过两个下标跟踪一个字符串或数组的两个位置，这两个下标将字符串(数组)分为了三部分，中间部分即为sliding window。
所有涉及到两个下标跟踪一个字符串或数组的问题，都可以将其归结为滑动窗口的模式进行思维。比如在快速排序中，将数组分为三部分，就使用了sliding window(point)。在上例的Longest Substring Without Repeating Characters中，sliding window中是不含重复的字符的字符串。

###### http协议
1. 特点
2. 报文结构
3. 状态码说明
4. 方法
5. GET和POST的区别 
6. 持久连接
7. 管线化

###### 2D碰撞检测
1. 矩形包围盒
2. 圆形：距离检测
3. 凸多边形: SAT
4. 优化：两个阶段:Broad和Narrow，数据结构-四叉树


#### S: 分享和输出
前端性能优化的本质：减少不必要的渲染，减少不必要的请求，减少不必要的执行。不必要的渲染体现在：1. 暂时用不到的模块不渲染->模块延迟加载技术 2.减少DOM修改->渲染模板代替渲染结点->浏览器渲染原理；不必要的请求体现在：利用缓存；不必要的运算体现在：对需要大量js运算的代码拆成多帧执行，运用js异步执行原理。

---

## 第4期

date:2019.10.25


#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0005|Longest Palindromic Substring|Accepted|js|


#### R: 阅读和点评
read:[How to learn all programming languages](https://www.coderscat.com/how-to-learn-all-pl)

* 为什么会有各种编程语言

1. 需要更易用，表达力更强的语言（es6比es5表达力更强）
2. 问题域增多
3. 不同的语言有不同的思考模式

不同的语言在数学本质上是相同的，都是图灵完备的。这意味着所有语言都能实现任何算法。只所以产生新的语言，不是因为旧的语言不能解决某种问题，而是因为新语言有更好的解决方案。

* 不同语言包含共同的要素，主要体现在抽象层面

1. 数据类型和数据抽象
2. 控制流和控制抽象
3. 对底层实现的抽象
4. 对具体问题域的补充和抽象

* 不同的语言也有共同的概念和范式，我们只所以能够掌握所有语言，是因为这些语言中涉及的概念是有限的，下面是各种语言普遍都有的：

1. 过程化(Procedural)
2. 递归(Recursive)
3. 静态类型(Static type)
4. 动态类型(Dynamic type)
5. 类型推论(type inference)
6. 匿名函数(Lambda function)
7. 面向对象(Object-oriented）
8. 垃圾回收(Garbage collection)
9. 指针(Pointer)
10. 续延(Continuation)
11. 元编程(Meta-programming)
12. 宏(Macro)
13. 异常(Exception)

* 关注语言概念，而不是语法

学习概念的关键是要理解这个概念要解决的问题，它的优缺点和实现原理。

* 学习新语言的步骤

1. 理解语言的设计思想和一般特征
2. 跟着教程或书本学习语法并实践
3. 做项目，阅读和编写大量代码
4. 理解更多语言实现的细节


#### T: 知识和技巧
1. 对动态规划的深层理解：动态规划通过备忘录优化了暴力求解中对子问题的求解过程，设计动态规划时可先思考暴力求解。
2. 编程能力的体现是高产，把才智用在生产有价值的产品上，而不是做大量初级工程师即可完成的小玩意儿
3. 数组方法梳理，对方法更熟悉了
4. 知道了学习一门新语言需要关注的焦点
5. 了解浏览器渲染原理，了解重排和重绘

#### S: 分享和输出
好文章分享：如何学会所有编程语言

---

## 第5期

date:2019.10.28

#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0008|String to Integer (atoi)|Accepted|js|
|0009|Palindrome Number|Accepted|js|

#### R: 阅读和点评
read:[如何学习数据结构和算法](https://www.coderscat.com/how-to-learn-data-structures-and-algorithms)

* 暂没发现新技巧

#### T: 知识和技巧
1. 编程算法设计要先列出所有情况，然后先处理特殊情况，再处理一般情况
2. 学技术要深入理解概念和模式，不要死记硬背表面语法
3. 永远不要忘记初始化

#### S: 分享和输出
1. styled-component：
 为了避免css文件污染全局（一个父模块导入的css文件影响了子模块的html），其中一个方法是借助第三方模块styled-component，styled-component允许我们把css样式按某种规则写在js文件，然后在模块中导入此js，则js文件中的样式只对当前模块有效。<br>
通过styled-component中的styled模块可创建一个带样式的标签组件，然后将这个标签组件导出去，在jsx中就可以直接使用这个组件了。创建语法如下:

```javascript
export const ComponentDemo=styled.div`
  height:50px;
  background-color:green;
` 
```

2. 一个dom节点携带的信息有且只有三个：标签名，标签属性和标签内容。使用一个带有这三个属性的对象即可唯一的描述一个dom节点。react中的jsx语法本质上就是一个描述了dom对象这三个属性的js对象。react通过这个对象来判断要渲染的节点是否发生了改变，及根据这个对象上的信息来渲染dom，这个对象称为虚拟dom。


## 第6期

date:2019.10.29

#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0011|Container With Most Water |Accepted|js|
|0012|Integer to Roman |Accepted|js|
|0015|3Sum|Accepted|js|
|0018|4Sum|Accepted|js|

#### R: 阅读和点评
read:[编程书籍推荐](https://www.coderscat.com/best-cs-books)
###### 一般技能
1. 《程序员修炼之道——从小工到专家》
2. 《代码大全》
3. 《计算机程序的构造和解析》SICP 
###### 算法类
1. 《编程珠玑》
2. 《算法设计手册》
3. 《算法导论》
4. 《程序设计的艺术》
5. 练习网站：[leetcode](https://leetcode.com/problemset/all/)和[hackerrank](https://www.hackerrank.com/)
###### 编程语言和编译
关于编程语言应该学习语言的核心概念，包括语义，计算模型和编程元素。如果对编程元素有深入的理解，学习新语言是很容易的。
1. 《编程语言的本质》
2. 《程序设计语言——实践之路》
3. 《编译原理技术和工具》
* 项目<br>
1. [8cc](https://github.com/rui314/8cc)用c语言写的编译器
2. [BuildYourOwnLisp](https://github.com/orangeduck/BuildYourOwnLisp)用1000行c代码写一个lisp解析器
###### 系统
1. 《Advanced Programming in the UNIX Environment》
###### 计算机网络
1. 《计算机网路——至顶向下方法》
2. 《TCP-IP详解》1-3卷

#### T: 知识和技巧
1. 要取数组中的任意两个数，一般需要两重循环。为了优化性能，可考虑是否能设计两个指针，分别从头尾遍历数组，这样只需要一重循环即可拿到两个数。复杂度从O(n^2)降为O(n)。比如今日leetCode练习中的0011,0015和0018。另外一种方法是采用map，比如0001题：two Sum。
2. 从虚拟DOM到真实dom的构建流程


#### S: 分享和输出
创建好虚拟DOM之后，虚拟dom影响真实dom的流程如下：1. 构建虚拟dom 2.将虚拟dom通过reactDom的render函数挂载在真实dom上 3.通过调用setState等方法导致虚拟Dom发生变化 4. 通过diff算法找出改变后的虚拟DOM和原虚拟DOM的不同 5. 将不同点作用在真实dom上



## 第7期

date:2019.10.30

#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0013|Roman to Integer |Accepted|js|
|0026|Remove Duplicates from Sorted Array|Accepted|js|
|0027|Remove Element|Accepted|js|
|0031|Next Permutation|Accepted|js|
|0033|Search in Rotated Sorted Array|Accepted|js|
|0034|Find First and Last Position of Element in Sorted Array|Accepted|js|

#### R: 阅读和点评
[创建一个虚拟现实语言沙盒](https://developer.ibm.com/industries/gaming/patterns/create-a-virtual-reality-speech-sandbox#flow)

本文介绍了如何使用IBM Watson的语言识别系统和Watson Assistant创建一个虚拟现实语音系统，比如用声音控制生成一个盒子。工作流如下:
1. 虚拟现实玩家说一个语音命令
2. 虚拟现实应用程序从麦克风取得这个语音文件，并把语音发送给Watson语言识别系统
3. 语言识别系统把这个声音转文文本并发送回应用程序
4. 应用程序把文本发送给Waston辅助系统，辅助系统把文本识别为：意图+实体的模式，应用程序根据这个模式做出相应的反应，比如创建一个盒子。

#### T: 知识和技巧

###### 算法
今天做的算法练习主要是关于数组方面的，比如数组去重，全排列，折半查找等。对我来说大都比较简单，稍微复杂点的是全排列问题，给定一个排列生成下一个排列，是一个按字典序对数组进行排序的问题，思考方法：先搞懂一个实例，看其方法是否能应用至全局。关于折半查找要考虑到前提，即数组必须是有序的，然后针对不同的变体分类思考。<br>
思维模式总结:对于像数组字符串这类序列问题，通常可以使用双指针进行解决，双指针把序列分为了三个区间，每个区间代表不同的含义。

###### react哲学 
react项目开发思考模版
1. 根据设计图和功能将页面划分为组件层级
2. 针对划分好的每一个组件编写静态页面，即只有props属性的组件，在这一步只考虑页面呈现，不考虑任何逻辑和数据问题
3. 确定每个组件state 的最小（且完整）表示
4. 确定state 放置的位置。如果使用redux存数据，体现在如何划分数据
5. 添加反向数据流，即组件如何影响数据。使用redux框架体现在编写和发送action
以上就是react开发的整个流程，非常简单，只需要多练习熟悉一下即可。

#### S: 分享和输出
react哲学


## 第8期

date:2019.10.31

#### A: 算法
|#|Question|Status|Language|
|-|-|-|-|
|0035|Search Insert Position|Accepted|js|
|0039|Combination Sum|Accepted|js|
|0040|Combination Sum II|Accepted|js|

#### R: 阅读和点评


#### T: 知识和技巧

###### 算法

#### S: 分享和输出
react哲学






