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

https://static9.porn-images-xxx.com/upload/20210729/923/944418/p=700/41.jpg
https://static4.porn-images-xxx.com/upload/20190925/697/713521/p=700/31.jpg
https://static8.porn-images-xxx.com/upload/20210514/915/936197/p=700/147.jpg
https://static9.porn-images-xxx.com/upload/20210707/921/942177/p=700/82.jpg
https://static9.porn-images-xxx.com/upload/20210729/923/944419/p=700/36.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
Kocho Komachi 小丁こまち - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/kocho-komachi-kocho-komachi-1/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:23:57</b></font><br>

<font size="2"><b>
普通に乳首見せてるzgコスプレイヤーの小丁こまちさん - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/chinese-cosplayer-kocho-komachi-who-shows-nipples-normally/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:25:31</b></font><br>

<font size="2"><b>
キレイなピンクの乳首にパイパン！全裸になっちゃう露出系美人コスプレイヤー「小丁こまち」ヌード画像137枚 - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/shaved-on-beautiful-pink-nipples-exposed-beautiful-cosplayer-kocho-komachi-nude-image-137-pieces-that-become-naked/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:34:22</b></font><br>

<font size="2"><b>
「小丁こまち」透けてるセーラーコスプレでピンクのパイパンと乳首を見せつけ！露出ヌード画像 71枚 - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/show-off-pink-shaved-bread-and-nipples-in-sailor-cosplay-that-is-transparent-kocho-komachi-71-exposed-nude-images/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:35:15</b></font><br>

<font size="2"><b>
Kocho Komachi 小丁こまち - ３次エロ画像 - エロ画像</b></font><br>
https://ja.porn-images-xxx.com/image/kocho-komachi-kocho-komachi/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:35:51</b></font><br>

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
