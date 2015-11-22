---
title:  "Sublime Text 3 Setup"
layout: post
tags:
    - editor
    - workflow

---

碰到了 sublime text 3 cpu 狂飆的狀況，似乎是有個 index 的程序一直在跑，沒辦法，只好依照這篇 [Reverting to a freshly installed state](https://www.sublimetext.com/docs/3/revert.html) 的做法，回到最剛開始安裝的狀態，重新設定一遍。

* 安裝 Package Control ( [Installation - Package Control](https://packagecontrol.io/installation) )
* 安裝 Theme ( [Theme - Cobalt2](https://packagecontrol.io/packages/Theme%20-%20Cobalt2) )
* 回復舊的設定檔 ( [Preferences.sublime-settings](https://gist.github.com/shouda/183040a0d5d13d7e6a31) )

然後一一把其餘的 packages 裝回去

* [SideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements)
* [Git](https://packagecontrol.io/packages/Git)
* [GitGutter](https://packagecontrol.io/packages/GitGutter)
* [Markdown Extended](https://packagecontrol.io/packages/Markdown%20Extended)
* [Markdown Preview](https://packagecontrol.io/packages/Markdown%20Preview)

```javascript
// keybind:
{ "keys": ["ctrl+shift+g"], "command": "markdown_preview", "args": {"target": "browser", "parser":"github"} }

// setting:
{
    "parser": "github",
    "enabled_parsers": ["github"],
    "strip_yaml_front_matter": true,
}
```

* [Emmet](https://packagecontrol.io/packages/Emmet)
* [CSS3](https://packagecontrol.io/packages/CSS3)
* [SCSS](https://packagecontrol.io/packages/SCSS)
* [Color Highlighter](https://packagecontrol.io/packages/Color%20Highlighter)
* [JavaScriptNext - ES6 Syntax](https://packagecontrol.io/packages/JavaScriptNext%20-%20ES6%20Syntax)
* [JavaScript Completions](https://packagecontrol.io/packages/JavaScript%20Completions)
* [AngularJS](https://packagecontrol.io/packages/AngularJS)
* [Ionic Framework Snippets](https://packagecontrol.io/packages/Ionic%20Framework%20Snippets)
* [GoSublime](https://packagecontrol.io/packages/GoSublime)

```javascript
// setting:
{
    "env":
    {
        "GOPATH": "/Users/shouda/Golang"
    },
    "fmt_cmd": [
        "goimports"
    ],
    "on_save": [{
        "cmd": "gs9o_open", "args": {
            "run": [
                "sh",
                //"go build . errors && go test -i && go test && go vet && golint ."
                "go build . errors && go vet && golint ."
            ],
            "focus_view": false
        }
    }],
    "autocomplete_closures": true,
    "autocomplete_builtins": true,
    "autocomplete_suggest_imports": true
}
```

* [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter)
* [SublimeLinter-jshint](https://packagecontrol.io/packages/SublimeLinter-jshint)
* [SublimeLinter-json](https://packagecontrol.io/packages/SublimeLinter-json)
* [SublimeLinter-ruby](https://packagecontrol.io/packages/SublimeLinter-ruby)
* [SublimeLinter-shellcheck](https://packagecontrol.io/packages/SublimeLinter-shellcheck)
* [BracketHighlighter](https://packagecontrol.io/packages/BracketHighlighter)
* [Unquote](https://packagecontrol.io/packages/Unquote)
* [DashDoc](https://packagecontrol.io/packages/DashDoc)

有兩個 packages 暫時放著，先不裝回去：

* [Alignment](https://packagecontrol.io/packages/Alignment)
* [All Autocomplete](https://packagecontrol.io/packages/All%20Autocomplete)

ref:

* [Sublime Text 3 Guide: Tips, Tricks, and Shortcuts](https://blog.generalassemb.ly/sublime-text-3-tips-tricks-shortcuts/)
* [Top tips (for Sublime Text, Sass, CSS, Terminal and more)](http://benfrain.com/top-tips-selection-unrelated-front-end-developer-tips/)
* [How I use Sublime Text 3](http://perso.crans.org/besson/sublimetext.en.html)
* [Sublime Text for Front End Developers](http://css-tricks.com/sublime-text-front-end-developers/)
