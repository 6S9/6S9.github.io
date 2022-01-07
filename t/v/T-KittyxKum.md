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

https://static6.hentai-cosplays.com/upload/20211215/256/261994/p=700/31.jpg
https://static5.hentai-cosplays.com/upload/20210906/238/243142/p=700/55.jpg
https://static5.hentai-cosplays.com/upload/20210729/233/238294/p=700/128.jpg
https://static5.hentai-cosplays.com/upload/20210908/238/243347/p=700/80.jpg
https://static8.porn-images-xxx.com/upload/20210521/916/936997/p=700/82.jpg
https://static7.porn-images-xxx.com/upload/20200623/827/846051/p=700/48.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
Ankha - PB - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/ankha-pb/

https://static6.hentai-cosplays.com/upload/20211215/256/261994/p=700/31.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:55:24</b></font><br>

<font size="2"><b>
KittyxKum - Kanao Sling Bikini - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/kittyxkum-kanao-sling-bikini/

https://static5.hentai-cosplays.com/upload/20210906/238/243142/p=700/55.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:44:54</b></font><br>

<font size="1"><b>
KittyxKum - Kanao Tsuyuri - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/kittyxkum-kanao-tsuyuri/

https://static5.hentai-cosplays.com/upload/20210729/233/238294/p=700/128.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:45:50</b></font><br>

<font size="2"><b>
KittyxKum - Zero Two - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/kittyxkum-zero-two/

https://static5.hentai-cosplays.com/upload/20210908/238/243347/p=700/80.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:47:06</b></font><br>

<font size="2"><b>
アナル大好きw アヘ顔でマ○コ見せてる、黒髪ツインテールのちっぱい合法□リ美少女 ヌード画像まとめ Vol.2 - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/love-w-im-showing-ma--co-with-an-ahe-face-black-hair-twin-tails-cute-legal--beautiful-girl-nude-image-summary-vol2/

https://static8.porn-images-xxx.com/upload/20210521/916/936997/p=700/82.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:48:32</b></font><br>

<font size="2"><b>
アヘ顔でマ○コ見せてる、黒髪ツインテールのちっぱい合法□リ美少女 ヌード画像＆Twitter動画まとめ - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/ma--co-is-showing-in-the-face-black-hair-twin-tails-of-the-little-legal--ri-pretty-nude-image-amp-twitter-video-summary/

https://static7.porn-images-xxx.com/upload/20200623/827/846051/p=700/48.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:49:40</b></font><br>

</textarea>
</pre>

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png)$/i;

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
