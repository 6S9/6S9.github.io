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

https://static6.hentai-cosplays.com/upload/20211215/257/262397/p=700/120.jpg
https://static5.hentai-cosplays.com/upload/20211208/249/254781/p=700/32.jpg
https://static5.hentai-cosplays.com/upload/20211208/249/254711/p=700/150.jpg
https://static5.hentai-cosplays.com/upload/20211208/249/254595/p=700/152.jpg
https://static5.hentai-cosplays.com/upload/20211209/251/256739/p=700/388.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

[水淼Aqua] 原神 优菈 - エロコスプレ
https://ja.hentai-cosplays.com/image/water-harajin-/

https://static6.hentai-cosplays.com/upload/20211215/257/262397/p=700/120.jpg

<font size="1" style="color:#DCDCDC">2022-07-27</font>

网红Coser@水淼aqua 黑白猫自拍 黑色内衣自拍 - エロコスプレ
https://ja.hentai-cosplays.com/image/coser-water-qua-aqua---color-innerwear-self-beat/

https://static5.hentai-cosplays.com/upload/20211208/249/254781/p=700/32.jpg

<font size="1" style="color:#DCDCDC">2022-04-29</font>

网红Coser@水淼aqua 愈合 - エロコスプレ
https://ja.hentai-cosplays.com/image/coser-water/

https://static5.hentai-cosplays.com/upload/20211208/249/254711/p=700/150.jpg

<font size="1" style="color:#DCDCDC">2022-04-29</font>

Coser@水淼Aqua Vol.091 黑兽2 - エロコスプレ
https://ja.hentai-cosplays.com/image/coser-water-basin-aqua-vol091-2/

https://static5.hentai-cosplays.com/upload/20211208/249/254595/p=700/152.jpg

<font size="1" style="color:#DCDCDC">2022-04-28</font>

水淼Aquaさんのコスプレ画像300枚 zg人コスプレイヤー 露出とテカテカの体がえちえちすぎ - エロコスプレ
https://ja.hentai-cosplays.com/image/300-images-of-mizuki-aquas-cosplay-images-chinese-cosplayer-exposure-and-tecatekas-body-are-too-cute/

https://static5.hentai-cosplays.com/upload/20211209/251/256739/p=700/388.jpg

<font size="1" style="color:#DCDCDC">2022-02-21</font>

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
