---
title:  "AngularJS vs React"
layout: post
tags:
    - angularjs
    - javascript

---

* [React/Flux from an AngularJS Perspective](http://blog.celerity.com/react/flux-from-an-angularjs-perspective)

> The community support backing React and Flux is huge right now, which may or may not be a good thing. When investigating Flux abstractions a simple search revealed 9 different implementation of Flux.

看來還是等到各種 flux 實作框架廝殺競爭之後，再來選一個成熟的勝出者。

> * React forces components to remain dumb and never manipulate state directly.
> * In Angular, it’s too easy to write directives that rely on the state of other components.

directives 盡量不要依賴其他組件，這點要注意。

> In cases where I have a lot of inter-component communication or manipulation, need server side rendering, or have to pass data to thousands of elements, I would prefer React and Flux.
> In cases where I need a single page app with a ton of two way interactions, I would prefer Angular.

angularjs 的應用規模不要太大。
