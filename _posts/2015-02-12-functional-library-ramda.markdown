---
title:  "Functional Library: Ramda"
layout: post
tags:
    - book
    - javascript

---

研究 [lodash](https://lodash.com/) 的時候，發現另一種用 Functional 模式寫的 [Ramda](http://ramdajs.com/)，酷！

看了這一本 [Functional JavaScript](http://jcouyang.gitbooks.io/functional-javascript/content/zh/higher_order_function/currying.html) 後，發覺稍微有點明白 Functional 是啥了：

> 用已有的函数组合出新的函数，而柯里化每消费一个参数，都会返回一个新的部分配置的函数，这为函数组合提供了更灵活的手段，并且使得接口更为流畅⋯⋯。由于 Eweda/Ramda 的函数都是自动柯里化，而且数据总是最后一个参数，因此可以随意组合，最终将需要处理的数据扔给组合好的函数就好了。这才是函数式的思想，<strong>先写好一个公式，再把数据扔给公式，而不是算好一部分再把结果给另一个公式</strong>。

ref:

* [Why Ramda?](http://fr.umio.us/why-ramda/)
* [Practical Functional JavaScript with Ramda](http://developer.telerik.com/featured/practical-functional-javascript-ramda/)
* [Lodash to Ramda example](http://bahmutov.calepin.co/lodash-to-ramda-example.html)
