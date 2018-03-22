# Highlight.js

[![Build Status](https://travis-ci.org/isagalaev/highlight.js.svg?branch=master)](https://travis-ci.org/isagalaev/highlight.js)

Highlight.js 是用JavaScript编写的语法高亮显示。它在浏览器和服务器上都能工作。它几乎适用于任何标记，不依赖于任何框架，并且具有自动语言检测功能。
![效果](https://raw.githubusercontent.com/hongmaju/light7Local/master/img/productShow/20170518152848.png)

## 如何使用

```html
<link rel="stylesheet" href="/path/to/styles/default.css">
<script src="/path/to/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
```

程序将会在`<pre><code>`中找到并突出显示代码;它试图自动检测语言。如果自动检测对您不起作用，您可以在类属性中指定语言

```html
<pre><code class="html">...</code></pre>
```

支持的语言类列表在类引用中可用。类也可以用语言或lang进行前缀。
要禁用高亮显示，请使用nohighlight类:

```html
<pre><code class="nohighlight">...</code></pre>
```

## 自定义初始化
如果你需要在自定义标签中实现代码高亮美化，此时需要自定义初始化，这里需要用到jquery配合jQuery，需要引入，别忘记了！

```javascript
$(document).ready(function() {
  $('pre code').each(function(i, block) {
    hljs.highlightBlock(block);
  });
});
```

## 相关

官网 <https://highlightjs.org/>.

接口
<http://highlightjs.readthedocs.io/>.

样式
<https://highlightjs.org/static/demo/>.
