---
title:  "React Router V4"
layout: post
tags:
    - reactjs
    - javascript

---

* [React Router: Declarative Routing for React.js](https://react-router.now.sh/)
* [Upgrading to react-router v4](http://broonix-rants.ghost.io/upgrading-to-react-router-v4/)
* [ReactRouter 4 前瞻](https://undefinedblog.com/reactrouter-4-foresee/)

又大改了，[試著把之前的程式升級上去](https://github.com/shouda/color-hwb-viewer/commit/61bbebec2e1a4acd034d65a3b1e734c61a78841e)，覺得是往好的方向走，搭建起來有比以前清楚一些。

跟 redux 的連接參考了 [這篇的做法](https://github.com/ReactTraining/react-router/blob/7f6706dab4827afc1c26a58418f8ef8c8ab40125/website/examples/Redux.js)，不再使用 [react-router-redux](https://github.com/reactjs/react-router-redux)，少包了一層東西，感覺較省心。

[Redirect 可以用 pushState 的方式](https://github.com/ReactTraining/react-router/pull/3912)，改了很久才搞定。
