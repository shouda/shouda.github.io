---
title:  "HWB Color Viewer by react.js & redux"
layout: post
tags:
    - reactjs
    - javascript

---

發覺用 [HWB Ｃolor](http://fettblog.eu/hwb-colors/) 調色還蠻直覺的，只要先選好色調，然後加減黑色或白色來調整。不過網路上幾乎找不到用 HWB 調色的工具，正好要學習 [Redux](http://redux.js.org/)，乾脆寫了一個 [HWB Color Space Viewer](http://shouda.github.io/demo/color-hwb-viewer/) 來練手。

程式直接拿 [eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb) 的規則來檢查 coding style，真的很嚴格，老的程式套用的話會改的很痛苦，airbnb 每次升級加規則後，也是要跟著重構。最近加了這條 [prefer-stateless-function](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/prefer-stateless-function.md)，改完後，發覺 [hot reloading](https://github.com/gaearon/react-transform-boilerplate) 爛掉了。

查了一下，發覺 hot reload 不支援 stateless function 這個問題，[一直沒有解決方法](https://github.com/gaearon/babel-plugin-react-transform/issues/57)，跟著追到了 redux 作者的新文章：[Hot Reloading in React](https://medium.com/@dan_abramov/hot-reloading-in-react-1140438583bf#.wxhvd4f12)，喔不，接下來又要大改了。

react + redux 真的不是心臟弱的人玩得起的，沒有時時跟著最新的變化，一升級半年前的專案，保證爛掉，而且要改的地方多到不知從何下手。

ref:

* [State of the Art JavaScript in 2016](https://medium.com/javascript-and-opinions/state-of-the-art-javascript-in-2016-ab67fc68eb0b#.k0p1p7c82)
