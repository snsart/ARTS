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
















