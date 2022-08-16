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

https://static10.hentai-cosplays.com/upload/20220722/307/314063/p=700/452.jpg
https://static5.hentai-cosplays.com/upload/20210913/238/243706/p=700/76.jpg
https://static5.hentai-cosplays.com/upload/20211007/241/246502/p=700/54.jpg
https://static7.hentai-cosplays.com/upload/20220218/290/295994/p=700/30.jpg
https://static7.hentai-cosplays.com/upload/20220218/290/295993/p=700/42.jpg
https://static7.hentai-cosplays.com/upload/20220218/290/296017/p=700/49.jpg
https://static7.hentai-cosplays.com/upload/20220218/290/296016/p=700/30.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

[どてちん販売所 (岡田ゆい)] アナルなんて覚えるんじゃなかった・・・。アナルファキングマシーン開封 (東方Project) - エロコスプレ
https://ja.hentai-cosplays.com/image/dotechin-sales-office-yui-okada-i-didnt-remember-anal-anal-fucking-machine-opening-dongfang-project/

https://static10.hentai-cosplays.com/upload/20220722/307/314063/p=700/452.jpg

(Okada Yui) のれんおっぱいエロすぎてバイブで潮！止まらない_画像? (Okada Yui) のれんおっぱいエロすぎてバイブで潮！止まらない_画像? - エロコスプレ
https://ja.hentai-cosplays.com/image/okada-yui-_-okada-yui-_/

https://static5.hentai-cosplays.com/upload/20210913/238/243706/p=700/76.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

(Okada Yui) Genshin Impact - Kujou Sara - エロコスプレ
https://ja.hentai-cosplays.com/image/okada-yui-genshin-impact-kujou-sara/

https://static5.hentai-cosplays.com/upload/20211007/241/246502/p=700/54.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

[岡田ゆい] ピストンマシーンだいちゅきホールド♥ [岡田ゆい] ピストンマシーンだいちゅきホールド♥ - エロコスプレ
https://ja.hentai-cosplays.com/image/----133/

https://static7.hentai-cosplays.com/upload/20220218/290/295994/p=700/30.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

[岡田ゆい] 実は追い追オナニーしてたんだよね? [岡田ゆい] 実は追い追オナニーしてたんだよね? - エロコスプレ
https://ja.hentai-cosplays.com/image/----132/

https://static7.hentai-cosplays.com/upload/20220218/290/295993/p=700/42.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

[岡田ゆい] 2日目♡最強ピストンマシンとふぇら、パイ擦り♡♡ - エロコスプレ
https://ja.hentai-cosplays.com/image/okada-yui-day--2-strongest-piston-machine-and-fura-pie-rubbing-/

https://static7.hentai-cosplays.com/upload/20220218/290/296017/p=700/49.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

[岡田ゆい] 3日目♥横撮じっくりアナル♥ピストン♥ - エロコスプレ
https://ja.hentai-cosplays.com/image/okada-yui-day-3--side-view-carefully--piston-/

https://static7.hentai-cosplays.com/upload/20220218/290/296016/p=700/30.jpg

<font size="1" style="color:#DCDCDC">2022-07-29</font>

</textarea>
</pre>

<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/@fancyapps/ui/dist/fancybox.css"
/>
<script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@4.0/dist/fancybox.umd.js"></script>

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
