### 2021-07-　

```note
```

<table id="tbc" style="white-space: pre-wrap">
</table>
<button onclick="toggleb()">toggle</button>
<pre id="prr" style="display: none">
<!-- 🍅<br>　<hr>🍑 -->

搞笑动图GIF：伤敌一千自损一千二
https://www.163.com/dy/article/GDC0Q7OR05373FZT.html

http://dingyue.ws.126.net/2021/0625/d430ed8bg00qv978z02t7c0006o007fc.gif
http://dingyue.ws.126.net/2021/0625/a78bfff4g00qv978z01fqc000460046c.gif
http://dingyue.ws.126.net/2021/0625/d40e619bg00qv978z00suc0007v007jc.gif

以其人之道还治其人之身
https://www.bilibili.com/video/BV1th411r7GT

弹幕：伤敌一千，自损一万二
蚊子：我tm犯天条了？！

徐锦j这铁头功厉害了，伤敌一千自损一万
http://k.sina.com.cn/article_6778180643_m19402d423001010sqf.html

不要和股票谈恋爱，可怕的不是股票被套，而是死心塌地
http://s3.pfp.sina.net/ea/ad/12/7/b1069055f8d7c1559cb84efd394552d8.gif

<!-- 🍅<br>　<hr>🍑 -->
</pre>

```tip
```

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

setTimeout(function(){
  tbc.innerHTML = parseURL(prr.innerHTML);
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
                return '<a href="' + match + '" target="_blank">' + match + '</a>';
            }
        }
    );
}

function toggleb() {
  var x = document.getElementById("prr");
  if (x.style.display === "none") {
    x.style.display = "";
  } else {
    x.style.display = "none";
  }
}

</script>
