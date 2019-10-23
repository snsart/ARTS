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


## 第2期

date:2019.10.23

#### A: 算法

|#|Question|Status|Language|
|-|-|-|-|
|0001|Two Sum|Accepted|js|


#### R: 阅读和点评

read:[Concurrency model and the event loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)

![image](https://developer.mozilla.org/files/4617/default.svg)
1. understand the concept of eventloop,taskQuene and stack of frames
2. know the time when message be added to taskQuene
3. async task include settimeout/intervial dom event and es6 promise


#### T: 知识和技巧

**标准模型和IE模型设置**
```
box-sizing:content-box//标准模型
box-sizing:border-box//IE模型
```

**盒模型重点:BFC(Block Formatting Context)的概念**

BFC为块格式化上下文,主要为了解决父子级边距折叠等问题

* BFC特点如下:<br>

1. BFC兄弟元素之间正常折叠
2. 和float元素之间不会重叠
3. 大小包含内部的float元素大小
4. 大小包含内部元素外边距

**BFC的实现**

1. float不为none
2. display为flex或table相关
3. position不为static或relative
4. overflow不为visible，可设置为hidden或auto

上述四种满足任意一种块元素即变为BFC


**html元素快捷输入**

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
