```note
```

<div id="Div1">
</div>
<pre id="Pre2" style="display: none">

```note
```

如何用链接替换普通URL
https://qa.1r1g.com/sf/ask/2637911/

Regex to match URL's not ending in jpg or png
https://stackoverflow.com/questions/25274463/regex-to-match-urls-not-ending-in-jpg-or-png

.jpg、.png、または.gifで終わる有効なURLかどうかを確認する正規表現
https://www.it-swarm-ja.com/ja/regex/jpg%E3%80%81png%E3%80%81%E3%81%BE%E3%81%9F%E3%81%AFgif%E3%81%A7%E7%B5%82%E3%82%8F%E3%82%8B%E6%9C%89%E5%8A%B9%E3%81%AAurl%E3%81%8B%E3%81%A9%E3%81%86%E3%81%8B%E3%82%92%E7%A2%BA%E8%AA%8D%E3%81%99%E3%82%8B%E6%AD%A3%E8%A6%8F%E8%A1%A8%E7%8F%BE/958376661/

How to match file extensions?
Matching files that do not have a specific extension
https://www.phpliveregex.com/learn/system-administration/how-to-match-file-extensions/

```note
```

{:.font-head}
JavaScript expressions and replacement rules
https://stackoverflow.com/questions/21505434/javascript-expressions-and-replacement-rules

PYTHON 正则表达式的中括号[]和竖线 | 的详细讲解
https://blog.csdn.net/nixiang_888/article/details/106469305

正则的深奥由实战而来，它总会有意想不到的无穷组合方式

Regular expressions
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

{:.h4}
Replace multiple strings at once
https://stackoverflow.com/questions/5069464/replace-multiple-strings-at-once

Match any/all of multiple words in a string
https://stackoverflow.com/questions/30114238/match-any-all-of-multiple-words-in-a-string

Javascript regex pattern match multiple strings ( AND, OR, NEAR/n, P/n
https://stackoverflow.com/questions/48829958/javascript-regex-pattern-match-multiple-strings-and-or-near-n-p-n/48830410

{:.h4}
JavaScript 正则表达式
https://www.w3school.com.cn/js/js_regexp.asp

JavaScript 正则表达式
https://www.runoob.com/js/js-regexp.html

正则表达式 - 简介
https://www.runoob.com/regexp/regexp-intro.html

正则表达式 - 教程
https://www.runoob.com/regexp/regexp-tutorial.html

{:.font-head}
正则表达式 - 语法
https://www.runoob.com/regexp/regexp-syntax.html

```tip
```

Getting parts of a URL (Regex
https://stackoverflow.com/questions/27745/getting-parts-of-a-url-regex/12470263#12470263

{:.font-head}
How TO - Toggle Hide and Show
https://www.w3schools.com/howto/howto_js_toggle_hide_show.asp

{:.h4}
原生js实现toggle的显示与隐藏的切换功能（demo
https://blog.csdn.net/llrg222/article/details/83687778

</pre>
<!-- 🍅🍑 -->

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

setTimeout(function(){
  Div1.innerHTML = parseURL(Pre2.innerHTML);
},0);

var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png)$/i;

function parseURL($string){

    var exp = __urlRegex;
    return $string.replace(exp,function(match){
            __imgRegex.lastIndex=0;
            if(__imgRegex.test(match)){
                return '<a data-fancybox="gallery" href="' + match.replace("/p=700", "")
                 + '"><img src="' + match.replace("/p=700", "")+'" width="64"></a>';
            }
            else{
                return '<br><a href="' + match + '" target="_blank">' + match + '</a><br><br>';
            }
        }
    );
}

</script>
