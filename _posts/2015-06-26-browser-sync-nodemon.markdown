---
title:  "browser-sync with nodemon"
layout: post
tags:
    - angularjs
    - javascript
    - node

---

用 [gulp-angular](https://github.com/Swiip/generator-gulp-angular) 產生新網站後，除了監視網頁變化外，用 node 跑的 api server 也可以用 [nodemon](https://github.com/remy/nodemon) 來監視，兩者的整合修改如下：

在 gulp/server.js 這個檔案裡頭，將

```javascript
gulp.task('serve', ['watch'], function () {
```

修改成

```javascript
gulp.task('serve', ['watch', 'nodemon'], function () {
```

最後再加上一段

```javascript
gulp.task('nodemon', function (cb) {
  var nodemon = require('gulp-nodemon');
  var BROWSER_SYNC_RELOAD_DELAY = 500;

  var called = false;
  return nodemon({
    execMap: { js: 'node --harmony' },
    script: 'server.js',
    watch: ['server.js', 'server/**/*.*']
  })
  .on('start', function onStart() {
    if (!called) { cb(); }
    called = true;
  })
  .on('restart', function onRestart() {
    setTimeout(function reload() {
      browserSync.reload({
        stream: false
      });
    }, BROWSER_SYNC_RELOAD_DELAY);
  });
});
```

順便把預設瀏覽器改成 chrome

```javascript
function browserSyncInit(baseDir, browser) {
  browser = browser === undefined ? 'google chrome' : browser;
```

ref: [browser-sync + nodemon + expressjs](https://github.com/sogko/gulp-recipes/tree/master/browser-sync-nodemon-expressjs)

註：browser-sync 裡頭沒有用 proxy，因為不是要把網頁導到 express，網頁仍然在 src/ 下面，只是將 express server 當成拉 api 資料的地方，在開發 angularjs 又同步開發 api 時，可以監測兩者的變動。
