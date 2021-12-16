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

https://static5.hentai-cosplays.com/upload/20211210/254/259398/p=700/3.jpg
https://static2.hentai-cosplays.com/upload/20190906/135/137249/p=700/266.jpg
https://static5.hentai-cosplays.com/upload/20211210/254/259397/p=700/3.jpg
https://static5.hentai-cosplays.com/upload/20211210/254/259402/p=700/3.jpg
https://static5.hentai-cosplays.com/upload/20211210/254/259401/p=700/3.jpg
https://static5.hentai-cosplays.com/upload/20210812/236/240790/p=700/424.jpg
https://static3.hentai-cosplays.com/upload/20201231/197/201550/p=700/50.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
2021 Summer Set - SM Police - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/2021-summer-set-sm-police/

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:41:01</b></font><br>

<font size="2"><b>
SAKU AYAKA DANGEROUS BEAST - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/saku-ayaka-dangerous-beast/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:39:55</b></font><br>

<font size="2"><b>
2021 Summer Set - Saku Saku Succubus 2 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/2021-summer-set-saku-saku-succubus-2/

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:41:50</b></font><br>

<font size="2"><b>
2021 Summer Set - Daemon 1 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/2021-summer-set-daemon-1/

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:43:05</b></font><br>

<font size="2"><b>
2021 Summer Set - Daemon 2 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/2021-summer-set-daemon-2/

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:42:57</b></font><br>

<font size="2"><b>
(C87) [Shooting Star's (サク)] 潜駆 (艦隊これくしょん -艦これ-) - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/c87-sakuing-stars-submarine-fleet-collection-ship-this-/

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:43:44</b></font><br>

<font size="2"><b>
2021 Summer Set - Mid Summer Pink 1 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/2021-summer-set-mid-summer-pink-1/

https://static5.hentai-cosplays.com/upload/20211210/254/259399/p=700/3.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:48:28</b></font><br>

<font size="2"><b>
Saku サク, Fate day night, Toosaka Rin凜 , Shooting Star's True Set 1 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/saku--fate-day-night-toosaka-rin--shooting-stars-true-set-1/

https://static3.hentai-cosplays.com/upload/20201231/197/201550/p=700/7.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/14 下午1:50:04</b></font><br>

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
