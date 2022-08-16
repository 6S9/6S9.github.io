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

https://static8.hentai-cosplays.com/upload/20220329/294/300440/p=700/156.jpg
https://static7.hentai-cosplays.com/upload/20220226/291/296984/p=700/130.jpg
https://static6.hentai-cosplays.com/upload/20220121/283/289104/p=700/90.jpg
https://static6.hentai-cosplays.com/upload/20211223/262/268243/p=700/81.jpg
https://static5.hentai-cosplays.com/upload/20211121/246/251854/p=700/68.jpg
https://static8.hentai-cosplays.com/upload/20220324/293/299987/p=700/143.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

[Cosplayer] Sameki - 16 - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-16/page/16/

<font size="1" style="color:#DCDCDC">2022-08-01</font>

[Cosplayer] Sameki - 13 - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-13/page/13/

<font size="1" style="color:#DCDCDC">2022-08-01</font>

[Cosplayer] Sameki - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-10/

https://static6.hentai-cosplays.com/upload/20220121/283/289104/p=700/90.jpg

<font size="1" style="color:#DCDCDC">2022-05-18</font>

[Cosplayer] Sameki - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-9/

https://static6.hentai-cosplays.com/upload/20211223/262/268243/p=700/81.jpg

<font size="1" style="color:#DCDCDC">2022-05-18</font>

[Cosplayer] Sameki - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-5/

https://static5.hentai-cosplays.com/upload/20211121/246/251854/p=700/68.jpg

<font size="1" style="color:#DCDCDC">2022-05-18</font>

[Cosplayer] Sameki - エロコスプレ
https://ja.hentai-cosplays.com/image/cosplayer-sameki-15/

https://static8.hentai-cosplays.com/upload/20220324/293/299987/p=700/143.jpg

<font size="1" style="color:#DCDCDC">2022-05-18</font>

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
