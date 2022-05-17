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

https://static6.hentai-cosplays.com/upload/20211214/256/261288/p=700/30.jpg
https://static5.hentai-cosplays.com/upload/20211209/250/255971/p=700/72.jpg
https://static5.hentai-cosplays.com/upload/20211208/248/253371/p=700/20.jpg
https://static5.hentai-cosplays.com/upload/20211209/250/255891/p=700/42.jpg
https://static5.hentai-cosplays.com/upload/20211209/250/255774/p=700/22.jpg
https://static6.hentai-cosplays.com/upload/20211218/259/264283/p=700/45.jpg
https://static4.hentai-cosplays.com/upload/20210424/223/227778/p=700/45.jpg
https://static6.hentai-cosplays.com/upload/20220108/274/280246/p=700/35.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

Yoshinobi – Riamu Yumemi Lingerie - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi--riamu-yumemi-lingerie/

https://static6.hentai-cosplays.com/upload/20211214/256/261288/p=700/30.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

Yoshinobi – Ilulu Bunny Suit - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi--ilulu-bunny-suit/

https://static5.hentai-cosplays.com/upload/20211209/250/255971/p=700/72.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

Yoshinobi - Satanya 2 - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi-satanya-2/

https://static5.hentai-cosplays.com/upload/20211208/248/253371/p=700/20.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

Yoshinobi – Pumpkin Milf - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi--pumpkin-milf/

https://static5.hentai-cosplays.com/upload/20211209/250/255891/p=700/42.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

Yoshinobi – Young Mommy - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi--young-mommy/

https://static5.hentai-cosplays.com/upload/20211209/250/255774/p=700/22.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

Yoshinobi - Riko Sakurauchi 2 - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi-riko-sakurauchi-2/

https://static6.hentai-cosplays.com/upload/20211218/259/264283/p=700/45.jpg

<font size="1" style="color:#DCDCDC">2022-03-07</font>

Yoshinobi - Riko Sakurauchi - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi-riko-sakurauchi/

https://static4.hentai-cosplays.com/upload/20210424/223/227778/p=700/45.jpg

<font size="1" style="color:#DCDCDC">2022-02-21</font>
Yoshinobi - Kokomi - エロコスプレ
https://ja.hentai-cosplays.com/image/yoshinobi-kokomi/

https://static6.hentai-cosplays.com/upload/20220108/274/280246/p=700/35.jpg

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
