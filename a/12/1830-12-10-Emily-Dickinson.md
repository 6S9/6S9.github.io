```note
```

<table id="tbc" style="white-space: pre-wrap">
</table>
<button onclick="toggleb()">toggle</button>
<pre id="prr" style="display: none">
<!-- ð<br>ã<hr>ð -->

1830å¹´12æ10-è¾ç±³èÂ·çéæ£®
https://zh.wikipedia.org/wiki/%E5%9F%83%E7%B1%B3%E8%8E%89%C2%B7%E7%8B%84%E6%9B%B4%E7%94%9F

è¾ç±³èÂ·ä¼ä¸½èç½Â·çéæ£®ï¼è±è¯­ï¼Emily Elizabeth Dickinsonï¼åè¯è¾å¼¥èâ§çç¾èªæåç±³èÂ·çæ´çï¼ï¼1886å¹´5æ15

https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Black-white_photograph_of_Emily_Dickinson2.png/835px-Black-white_photograph_of_Emily_Dickinson2.png

è¾å¼¥èÂ·è¿ªæ´ç
https://zh.wikiquote.org/wiki/%E8%89%BE%E5%BD%8C%E8%8E%89%C2%B7%E8%BF%AA%E6%9B%B4%E7%94%9F

æ²¡æä¸èå¤§å¸è¹åä¸å·ä¹¦ï¼è½å°æä»¬éå°æé¥è¿çå¼ä¹¡ï¼ä¹æ²¡æä»»ä½éªé©¬åä¸é¡µå¥è¾è·³è·çè¯ç¯ï¼è½è½½çæä»¬å¥é©°åè¾½éçæ°ä¸çï¼æè´«ç©·çäººä»¬ä¹è½å°½æç¿±æ¸¸ï¼èä¸ä¼è¢«é¼ç´¢æè¡è´¹ã

å¦ææä¸æ¾è§è¿å¤ªé³ï¼ææ¬å¯ä»¥å¿åé»æã

å¦ææè½è®©ä¸é¢å¿ä¸åç¼çï¼æå°±æ²¡æç½æ´»è¿ä¸çã

å ä¸ºæä¸è½åä¸æ¥ç­æ­»ç¥ï¼æä»¥ä»æ¸©æå°åä¸æ¥ç­æã

å¦æä½ è½å¨ç§å¤©å°æ¥ï¼æä¼æå¤å¤©æ¸æãåå«è½»èï¼åå«å¾®ç¬ï¼åç®¡å®¶å¦å¥³æèèèµ¶è·ã

æä»¬èå¼±çæå®ï¼æ¿åä¸äºççè¿ååç¾çå®ä¼ã

å°±åé·å£°ä¸­æ¶æä¸å®çå­©å­ï¼éè¦æ¸©åå®æ°çè¯è¯­ï¼çççåä¹åªè½æ¢æ¢å°éå°ï¼å¦åäººäººé½ä¼å¤±æã

ç­å¾ä¸å°æ¶ï¼å¤ªä¹ãå¦æç±ï¼æ°å¥½å¨é£ä¹åãç­ä¸ä¸å¹´ï¼ä¸é¿ã

çé¾ä¸åï¼äººä¸èå¹»ï¼æä¸ä¸çãè¯·è®°ä½ï¼ææ¾ç»æ¥è¿ã

å¸æé¿æç¿èï¼æ äºå¿çµä¹ä¸ï¼åå±æ²è°ï¼æ éè¨è¡¨ï¼å¤©é³è¢è¢ï¼å§ç»ç¯ç»ã

çå¥¹æ¯ä¸å¹å¾ç»ï¼å¬å¥¹æ¯ä¸æ²ä¹é³ï¼æå¥¹æ¯ä¸ç§æ¾çºµï¼å°±åå­æä¸æ ·å¤©çï¼ä¸æå¥¹æ¯âç§æç£¨ã

å¤å½è¯æ­ï½è¾ç±³èÂ·çéæ£®è¯æ­ç²¾éå­é¦
https://baijiahao.baidu.com/s?id=1689370731492985454&wfr=spider&for=pc

çå ââå è½ââæ»ç£ââæéââ
éå¦é½ç²ââå¨éªçåç

<!-- ð<br>ã<hr>ð -->
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
