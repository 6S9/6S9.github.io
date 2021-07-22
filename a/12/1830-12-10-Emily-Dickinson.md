```note
```

<table id="tbc" style="white-space: pre-wrap">
</table>
<button onclick="toggleb()">toggle</button>
<pre id="prr" style="display: none">
<!-- 🍅<br>　<hr>🍑 -->

1830年12月10-艾米莉·狄金森
https://zh.wikipedia.org/wiki/%E5%9F%83%E7%B1%B3%E8%8E%89%C2%B7%E7%8B%84%E6%9B%B4%E7%94%9F

艾米莉·伊丽莎白·狄金森（英语：Emily Elizabeth Dickinson，又译艾弥莉‧狄瑾荪或埃米莉·狄更生，－1886年5月15

https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Black-white_photograph_of_Emily_Dickinson2.png/835px-Black-white_photograph_of_Emily_Dickinson2.png

艾弥莉·迪更生
https://zh.wikiquote.org/wiki/%E8%89%BE%E5%BD%8C%E8%8E%89%C2%B7%E8%BF%AA%E6%9B%B4%E7%94%9F

没有一艘大帆船像一卷书，能将我们送到最遥远的异乡；也没有任何骏马像一页奔腾跳跃的诗篇，能载着我们奔驰向辽阔的新世界；最贫穷的人们也能尽情翱游，而不会被逼索旅行费。

如果我不曾见过太阳，我本可以忍受黑暗。

如果我能让一颗心不再疼痛，我就没有白活这一生。

因为我不能停下来等死神，所以他温柔地停下来等我。

如果你能在秋天到来，我会把夏天掸掉。半含轻蔑，半含微笑，像管家妇女把苍蝇赶跑。

我们脆弱的感官，承受不了真理过分华美的宏伟。

就像雷声中惶恐不安的孩子，需要温和安慰的话语，真理的光也只能慢慢地透射，否则人人都会失明。

等待一小时，太久。如果爱，恰好在那之后。等一万年，不长。

烟雾与光，人与虚幻，我与世界。请记住，我曾经来过。

希望长有翅膀，栖于心灵之上，吟唱曲调，无需言表，天音袅袅，始终环绕。

看她是一幅图画，听她是一曲乐音，懂她是一种放纵，就像六月一样天真，不懂她是—种折磨。

外国诗歌｜艾米莉·狄金森诗歌精选六首
https://baijiahao.baidu.com/s?id=1689370731492985454&wfr=spider&for=pc

王冠——坠落——总督——投降——
静如齑粉——在雪的圆盘

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
