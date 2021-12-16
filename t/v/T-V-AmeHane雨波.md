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

https://static5.hentai-cosplays.com/upload/20211028/245/250070/p=700/101.jpg
https://static5.hentai-cosplays.com/upload/20211027/245/250055/p=700/22.jpg
https://static5.hentai-cosplays.com/upload/20211212/254/259513/p=700/47.jpg
https://static5.hentai-cosplays.com/upload/20211012/242/247016/p=700/13.jpg
https://static4.hentai-cosplays.com/upload/20210701/228/232987/p=700/268.jpg
https://static5.hentai-cosplays.com/upload/20210726/231/235802/p=700/10.jpg
https://static5.hentai-cosplays.com/upload/20210725/230/235251/p=700/38.jpg
https://static5.hentai-cosplays.com/upload/20211109/246/251102/p=700/45.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
Hane Ame - Nyotengu Photobook - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hane-ame-nyotengu-photobook/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:08:57</b></font><br>

<font size="2"><b>
Hane Ame - Nyotengu Neko - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hane-ame-nyotengu-neko/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:09:36</b></font><br>

<font size="2"><b>
Hane Ame - Mushoku Tensei Elinalise - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hane-ame-mushoku-tensei-elinalise/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午5:19:01</b></font><br>

<font size="2"><b>
雨波HaneAme - 2B Wedding suit - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/haneame-2b-wedding-suit/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:24:51</b></font><br>

<font size="2"><b>
[HaneAme] Azur Lane Collection - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/haneame-azur-lane-collection/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:19:51</b></font><br>

<font size="2"><b>
(COS Benefits) Hane Ame Rain wave - Bremerton - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/cos-benefits-hane-ame-rain-wave-bremerton/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午10:32:33</b></font><br>

<font size="2"><b>
Hane Ame - 2B Bride (White) - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hane-ame-2b-bride-white/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:15:04</b></font><br>

<font size="2"><b>
Hane Ame - Raiden Shogun - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hane-ame-raiden-shogun/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:11:12</b></font><br>

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
