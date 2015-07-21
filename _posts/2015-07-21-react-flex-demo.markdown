---
title:  "flexbox demo by react.js"
layout: post
tags:
    - reactjs
    - javascript

---

看到這一篇 [Flex 布局教程：实例篇](http://www.ruanyifeng.com/blog/2015/07/flex-examples.html)，正好在學寫 [React](https://facebook.github.io/react/)，就參考了幾個 flexbox playground ( [Flexy Boxes](http://the-echoplex.net/flexyboxes/) 和 [flexboxDemo](http://codepen.io/justd/pen/yydezN) )，寫了個展示骰子點子排列方式的網頁，放在 [CSS Flexbox Demo](http://shouda.github.io/demo/react-flex-dice/) 。

除了學習 react 之外，也試著用 [webpack](http://webpack.github.io/) 搭建開發工作流，還有新的 es6 語法來寫 code，在 atom 上搭配 [ESLint](http://eslint.org/) 檢查語法錯誤與 coding style，整體來說很順暢。

這次用 react 最新的 0.14 beta，因此 react-router 或 react-bootstrap 是無法安裝的，這讓我重新思考套件依賴的問題，為何 router 或是 css 要依賴於某套件的版本呢？為何不各自獨立發揮功能就好，將它們整合運作是我們開發者的責任，要等待一個套件升級，才能去嘗試新版本的語法，這真是很糟糕的事。

grunt, gulp, bower 這些工具都不用了，npm + webpack 就搞定。

sass, scss 和 bootstrap 也一起拋棄掉，選了 [Basscss](http://www.basscss.com/) 和 [cssnext](http://cssnext.io/)，實際用下來發覺這種小型模組化的 css 很適合用在 react，除非必要，不太需要去重新創造新的 class，有些微小的改動，善用 react 的 [Inline Styles](https://facebook.github.io/react/tips/inline-styles.html) 會更直覺，少數真的會重用的樣式再去寫 class 就好。

ref:

* [Solved by Flexbox — Cleaner, hack-free CSS](http://philipwalton.github.io/solved-by-flexbox/)
