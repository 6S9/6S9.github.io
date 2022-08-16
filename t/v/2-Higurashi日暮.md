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

https://static.hentai-cosplays.com/upload/20140822/15/15215/p=700/64.jpg
https://static.hentai-cosplays.com/upload/20140920/15/15245/p=700/67.jpg
https://static4.porn-images-xxx.com/upload/20190418/656/671306/p=700/53.jpg
https://static.hentai-cosplays.com/upload/20150531/6/5495/p=700/440.jpg
https://static2.hentai-cosplays.com/upload/20180607/82/83106/p=700/86.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

日暮りんさんのパンツから透けるパイパンがエロいナースメイド姿の画像 - 7 - エロコスプレ
https://ja.hentai-cosplays.com/image/nippori-froms-panties-see-through-shaved-pussy-erotic-or-nursemaid-sight-picture/page/7/

<font size="1" style="color:#DCDCDC">2022-08-03</font>

日暮りんさんのほとんど隠せていないパイパンがエロすぎる十六夜咲夜画像 - 7 - エロコスプレ
https://ja.hentai-cosplays.com/image/izayoi-sakuya-paipan-nipporis-almost-no-roof-too-erotic-images/page/7/

<font size="1" style="color:#DCDCDC">2022-08-03</font>

【コスプレエロ画像】人気レイヤー日暮りんの最新の過激コスプレ画像はコチラw - ３次エロ画像 - エロ画像
https://ja.porn-images-xxx.com/image/cosplay-erotic-image-popular-layer-nippori-rins-latest-extreme-cosplay-image-is-here-w/

https://static4.porn-images-xxx.com/upload/20190418/656/671306/p=700/53.jpg

<font size="1" style="color:#DCDCDC">2022-07-07</font>

<font size="2"><b>
[Higurashi Kikaku (Higurashi Rin)] “DEKO” [日暮企画 (日暮りん)] 凸 DEKO - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/higurashi-kikaku-higurashi-rin-deko----deko/

https://static.hentai-cosplays.com/upload/20150531/6/5495/p=700/440.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/18 下午3:37:20</b></font><br>

<font size="3"><b>
[日暮企画] お肉たっぷり高シコリティ水着図鑑vol.3 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/higurashi-planning-meat-cicolity-swimsuit-vol-3/

https://static2.hentai-cosplays.com/upload/20180607/82/83106/p=700/86.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/18 下午3:35:35</b></font><br>

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
