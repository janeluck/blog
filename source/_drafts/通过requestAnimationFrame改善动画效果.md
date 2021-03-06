---
title: 通过requestAnimationFrame改善动画效果
tags: JavaScript
---



#### 平滑的动画效果

    平滑动画最佳间隔为16ms,(1000ms/60)。

#### 传统的实现方式

    通过setTimeout, setInterval定时器这种办法来实现动画效果。
    缺点是setTimeout和setInterval的运行机制导致了回调函数运行的时间点可能受到其他任务干扰。
    动画效果因为间隔时间的不合适导致过度绘制或者卡顿。


#### requestAnimationFrame

    requestAnimationFrame采用系统时间间隔，并且浏览器内部会集中处理，使动画效果有一个统一的刷新机制。
    对于隐藏或者不可见元素, requestAnimationFrame将不会进行重绘或回流，节省资源




#### 参考链接

- [requestAnimationFrame for Smart Animating](https://www.paulirish.com/2011/requestanimationframe-for-smart-animating/)
- [浅析 requestAnimationFrame](http://taobaofed.org/blog/2017/03/02/thinking-in-request-animation-frame/)
- [Javascript高性能动画与页面渲染](http://www.infoq.com/cn/articles/javascript-high-performance-animation-and-page-rendering)
- [渲染主循环（main loop)和requestAnimationFrame](https://blog.csdn.net/milado_nju/article/details/8101188)