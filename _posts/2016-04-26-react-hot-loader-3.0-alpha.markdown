---
title:  "React Hot Loader 3.0 alpha"
layout: post
tags:
    - reactjs
    - javascript

---

* [React Hot Loader 3.0 alpha demo](https://github.com/gaearon/react-hot-boilerplate/pull/61)
* [Hot reloading react stateless components](https://thesabbir.com/hot-reloading-react-stateless-components/)

要配合 react-router 使用的話，先把 routes 設定抽出來，寫成 [plain JS object](https://github.com/shouda/color-hwb-viewer/blob/master/src/routes/configureRoute.js)，不要用 JSX 的格式寫 routes，還要多傳一個 key 給 Router，這樣 hot reload 才會動，試了好久才找到這個方法。

```javascript
import React from 'react';
import { Provider } from 'react-redux';
import { Router } from 'react-router';
import { configureRoute } from './routes/configureRoute';

const hmrKey = Math.random();

const Main = ({ store, history }) => (
  <Provider store={store}>
    <Router key={hmrKey} history={history} routes={configureRoute} />
  </Provider>
);

Main.propTypes = {
  history: React.PropTypes.object.isRequired,
  store: React.PropTypes.object.isRequired,
};

export default Main;
```
[source code](https://github.com/shouda/color-hwb-viewer/blob/master/src/main.jsx)

終於可以 hot reload stateless components 了，又回到爽快開發的節奏。
