```note
```

<div id="Div1">
</div>
<pre id="Pre2">

JS生成数字下拉列表
https://www.cnblogs.com/haocool/archive/2012/06/27/2565716.html

<html>
<head>
<title></title>
<script language="javascript">
    //生成数字下拉列表（选中项，起始数字，结束数字）
    function CreateOption(str1, str2, str3) {
        var CreateOption = "";
        for (var i = str2; i <= str3; i++) {
            CreateOption += "<option value=" + i;
            if (str1 == i) {
                CreateOption += "\" selected>" + i + "</option>";
            }
            else {
                CreateOption += "\">" + i + "</option>";
            }
        }
        document.write(CreateOption);
    }
</script>
</head>
<body>
<select >
<script type="text/javascript">CreateOption('1','1','20')</script>
</select>
</body>
</html>

</pre>

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
