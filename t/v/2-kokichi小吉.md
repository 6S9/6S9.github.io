<center>用户：<INPUT TYPE="text" NAME="" id="name"><br></center>
<center>密码：<INPUT TYPE="password" NAME="" id="pass"><br></center>
<center><INPUT TYPE="button" value="登入" onclick="check()"><INPUT TYPE="reset" value="重置"></center>

<div style="display: none" id="mdm" name="dmd">
  <button onclick="location.reload()">Cover 0</button>
</div>

<button style="display: none" name="dmd" onclick="toggleb()">toggle</button>
<button onclick="loadparse()">loadparse</button>

<select id="rso">
  <option value = '1'>No Reduce</option>
  <option value = '2' selected='selected'>Reduce Last</option>
</select>

<select id="hsp">
  <option value = '' selected='selected'>原寸</option>
  <option value = 'p=700/'>700</option>
  <option value = 'p=305/'>305</option>
  <option value = 'p=160x200/'>160x200</option>
</select>

<br>
<div style="display: none" id="mdc" name="dmd">
</div>

<pre style="display: none" id = "raw">
<!-- 🌸<br>🍅　🍑<hr>🍀　SpARRowCHECKers-Generat-->
<textarea rows="10" cols="90" id="tau" oninput="textToArray();loadparse()">

https://static7.hentai-cosplays.com/upload/20220224/290/296817/p=700/31.jpg
https://static7.hentai-cosplays.com/upload/20220224/290/296812/p=700/24.jpg
https://static7.hentai-cosplays.com/upload/20220224/290/296819/p=700/31.jpg
https://static6.hentai-cosplays.com/upload/20211222/262/267465/p=700/13.jpg
https://static7.hentai-cosplays.com/upload/20220224/290/296815/p=700/51.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

[爆机少女喵小吉] 尼尔 机械纪元 花嫁 1 - エロコスプレ
https://ja.hentai-cosplays.com/image/bakusakusaku-shoujo-kokichi-1/

https://static7.hentai-cosplays.com/upload/20220224/290/296817/p=700/31.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

[爆机少女喵小吉] 骸骨少女 - エロコスプレ
https://ja.hentai-cosplays.com/image/baku-desk-girl-kokichi-skeleton-girl/

https://static7.hentai-cosplays.com/upload/20220224/290/296812/p=700/24.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

[爆机少女喵小吉] Reゼロから始める異世界生活 - エロコスプレ
https://ja.hentai-cosplays.com/image/baku-desk-girl-kokichi-life-in-a-different-world-starting-from-re-zero/

https://static7.hentai-cosplays.com/upload/20220224/290/296819/p=700/31.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

【爆机少女喵小吉】尼尔机械纪元-人形兵器 - エロコスプレ
https://ja.hentai-cosplays.com/image/--776/

https://static6.hentai-cosplays.com/upload/20211222/262/267465/p=700/13.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

[爆机少女喵小吉] 永恒魅魔 - エロコスプレ
https://ja.hentai-cosplays.com/image/bakusakusune-girl-kokichi/

https://static7.hentai-cosplays.com/upload/20220224/290/296815/p=700/51.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

</textarea>
</pre>

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png|webp)$/i;

textToArray();
loadparse();

function parseURL($string){

    var exp = __urlRegex;
    return $string.replace(exp,function(match){
            __imgRegex.lastIndex=0;
            if(__imgRegex.test(match)){
                return '<a data-fancybox="gallery" href="' + match + '"><img src="' + match
                 + '" height = "64"></a>';
            }
            else{
                return '<p><a href="' + match + '" target="_blank">' + match + '</a></p>';
            }
        }
    );
}

function textToArray(){
  var textArea = document.getElementById("tau");
  var arrayFromTextArea = textArea.value.split(String.fromCharCode(10));
  for ( var i = 0; i < arrayFromTextArea.length; i++ ) {
    generateM(arrayFromTextArea[i]);
  }
}

function generateM(url) {
  mdm.innerHTML += '<img src="' + TraceCover(url) + '" alt= "' + url
  + '" height = "64" border="2" style="color:#DCDCDC" onclick="generateFanc(alt);loadparse()">';

}

function TraceCover(url) {
  var SegmentArr = url.split('/');

  var Extens = SegmentArr.slice(-1).join().split('.').pop();
  var SegmentCount = SegmentArr.length - 2;

  var TopHalf = SegmentArr.slice(0,SegmentCount).join('/');

  return TopHalf + '/p=160x200/1.' + Extens + '\n';

}

function generateFanc(url) {
  var SegmentArr = url.split('/');
  var GeneratCount = SegmentArr.slice(-1).join().split('.').shift();
  var Extens = SegmentArr.slice(-1).join().split('.').pop();
  var SegmentCount = SegmentArr.length;
  var ReduceSegments = document.getElementById('rso').value;
  var HentaiSizeP = document.getElementById('hsp').value;
  var TopHalf = SegmentArr.slice(0,SegmentCount - ReduceSegments).join('/');
  tar.innerHTML = '';

  for (var j = 1; j <= GeneratCount; j++) {
    tar.innerHTML += TopHalf + '/' + HentaiSizeP + j + '.' + Extens + '\n';
  }
}

function loadparse() {
  mdc.innerHTML = parseURL(tar.value);
}

function check(){
  var name=document.getElementById("name").value;
  var pass=document.getElementById("pass").value;
  if(name==!/[^\s]/.test(new Date().getTime()) && pass==String.fromCharCode(window.atob("MTIx"))){
    var nd = document.getElementsByName("dmd");
    for (var i = 0; i <= nd.length; i++) {
      nd[i].style.display = "";
      }
      }else{
      }
}

function toggleb() {
  var x = document.getElementById("raw");
  if (x.style.display === "none") {
    x.style.display = "";
  } else {
    x.style.display = "none";
  }
}

</script>
