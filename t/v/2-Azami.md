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

https://static6.hentai-cosplays.com/upload/20211215/257/262158/p=700/11.jpg
https://static9.hentai-cosplays.com/upload/20220506/298/304290/p=700/12.jpg
https://static12.porn-images-xxx.com/upload/20220406/1181/1208523/p=700/36.jpg
https://static8.hentai-cosplays.com/upload/20220401/294/300868/p=700/20.jpg
https://static6.hentai-cosplays.com/upload/20211225/264/269891/p=700/27.jpg
https://static6.hentai-cosplays.com/upload/20211224/263/269073/p=700/19.jpg
https://static8.hentai-cosplays.com/upload/20220327/294/300263/p=700/22.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

Azami - Amelia Watson 3 - エロコスプレ
https://ja.hentai-cosplays.com/image/azami-amelia-watson-3/

https://static6.hentai-cosplays.com/upload/20211215/257/262158/p=700/11.jpg

<font size="1" style="color:#DCDCDC">2022-07-27</font>

Azami – Jinx - エロコスプレ
https://ja.hentai-cosplays.com/image/azami--jinx/

https://static9.hentai-cosplays.com/upload/20220506/298/304290/p=700/12.jpg

<font size="1" style="color:#DCDCDC">2022-05-17</font>

「サキュバスな保健医」という童貞即射精な有名Vtuberの露出エロコスプレがめちゃ卑猥 - ３次エロ画像 - エロ画像
https://ja.porn-images-xxx.com/image/exposed-erotic-cosplay-of-a-famous-vtuber-who-ejaculates-immediately-as-a-virgin-called-succubus-health-doctor-is-very-obscene/

https://static12.porn-images-xxx.com/upload/20220406/1181/1208523/p=700/36.jpg

<font size="1" style="color:#DCDCDC">2022-04-27</font>

Azami - Nero Swimsuit Fate Extra - エロコスプレ
https://ja.hentai-cosplays.com/image/azami-nero-swimsuit-fate-extra/

https://static8.hentai-cosplays.com/upload/20220401/294/300868/p=700/20.jpg

<font size="1" style="color:#DCDCDC">2022-04-25</font>

Azami - Siege 2 - エロコスプレ
https://ja.hentai-cosplays.com/image/azami-siege-2/

https://static6.hentai-cosplays.com/upload/20211225/264/269891/p=700/27.jpg

<font size="1" style="color:#DCDCDC">2022-04-04</font>

Azami - Lisa (Genshin Impact) 2 - エロコスプレ
https://ja.hentai-cosplays.com/image/azami-lisa-genshin-impact-2/

https://static6.hentai-cosplays.com/upload/20211224/263/269073/p=700/19.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

Azami – Cyber Bunny - エロコスプレ
https://ja.hentai-cosplays.com/image/azami--cyber-bunny/

https://static8.hentai-cosplays.com/upload/20220327/294/300263/p=700/22.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

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
