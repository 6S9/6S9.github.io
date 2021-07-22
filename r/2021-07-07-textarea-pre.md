### 2021-07-　

```note
```

{:.font-head}

```tip
```

{:.h4}

<div id="dv1">
</div>
<button onclick="toggleb()">toggle</button>
<pre id="pr2" style="display: none">
<!-- 🍅<br>　<hr>🍑 -->

How to add a new line in textarea element?
https://stackoverflow.com/questions/8627902/how-to-add-a-new-line-in-textarea-element

&#13;&#10;

<br>

\n

Creating a textarea with auto-resize
https://stackoverflow.com/questions/454202/creating-a-textarea-with-auto-resize

为什么div里面\n不能起到换行作用呢？
https://www.zhihu.com/question/273749104

white-space: 'pre-wrap'

使pre的内容自动换行
https://www.html.cn/archives/2422

CSS 属性篇(八)：word-wrap、word-break、white-space属性
https://juejin.cn/post/6844903798792519694

Javascript: Convert textarea into an array
https://stackoverflow.com/questions/2299604/javascript-convert-textarea-into-an-array

var textArea = document.getElementById("textAreaId");
var arrayFromTextArea = textArea.value.split(String.fromCharCode(10));

HTML 颜色名
https://www.w3school.com.cn/html/html_colornames.asp

CornflowerBlue
　#6495ED

DodgerBlue
　#1E90FF

<!-- 🍅<br>　<hr>🍑 -->
</pre>

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

setTimeout(function(){
  dv1.innerHTML = parseURL(pr2.innerHTML);
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

function toggleb() {
  var x = document.getElementById("pr2");
  if (x.style.display === "none") {
    x.style.display = "";
  } else {
    x.style.display = "none";
  }
}

</script>
