```tip
### 2022-03-Pharaoh
```

<table id="tbc" style="white-space:pre-wrap">
</table>
<button onclick="toggleb()">toggle</button>
<button onclick="loadparse()">loadparse</button>
<br>
<!-- 🌸<br>🍅-　-🍑<hr>🍀 -->
<pre>
<textarea rows="30" cols="100" style="display: none" id="tar">

e罗斯嘻哈歌手法老——дико например_哔哩哔哩_bilibili
https://www.bilibili.com/video/av50934361/

<font size="1" style="color:#DCDCDC">2022-03-25</font>

e罗斯修x后，普京为何指责苏g，到底有何深层用意？_网易订阅
https://www.163.com/dy/article/FRD3DPJU0515CCN3.html

其中eg领导久加诺夫就站出来反对，他认为e罗斯x法修正案，是e罗斯要出现沙皇、法老等独裁领导人。

<font size="1" style="color:#DCDCDC">2022-03-25</font>

久加诺夫：普j现在的q力比法老还大，必须被监督，不能像叶利钦_腾讯新闻
https://new.qq.com/rain/a/20201110a087up00

<font size="1" style="color:#DCDCDC">2022-03-25</font>

</textarea>
</pre>
<!-- 🍀<br>🍑-　-🍅<hr>🌸 -->

```note
```

<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/@fancyapps/ui/dist/fancybox.css"
/>
<script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@4.0/dist/fancybox.umd.js"></script>

<script type="text/javascript">

var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png|webp)$/i;

loadparse();

function parseURL($string){

    var exp = __urlRegex;
    return $string.replace(exp,function(match){
            __imgRegex.lastIndex=0;
            if(__imgRegex.test(match)){
                return '<a data-fancybox="gallery" href="' + match.replace("/p=700", "")
                 + '"><img src="' + match.replace("/p=700", "/p=160x200")+'" width="64"></a>';
            }
            else{
                return '<a href="' + match + '" target="_blank">' + match + '</a>';
            }
        }
    );
}

function loadparse() {
  tbc.innerHTML = parseURL(tar.value);
}

function toggleb() {
  var x = document.getElementById("tar");
  if (x.style.display === "none") {
    x.style.display = "";
  } else {
    x.style.display = "none";
  }
}

</script>
