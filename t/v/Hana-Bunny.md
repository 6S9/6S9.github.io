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

https://static6.hentai-cosplays.com/upload/20211213/254/259619/p=700/3.jpg
https://static5.hentai-cosplays.com/upload/20211211/254/259482/p=700/12.jpg
https://static2.hentai-cosplays.com/upload/20200322/157/160281/p=700/4.jpg
https://static2.hentai-cosplays.com/upload/20200708/168/171410/p=700/10.jpg
https://static2.hentai-cosplays.com/upload/20200508/164/167238/p=700/10.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
Yamato (One Piece) by Hana Bunny 1 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/yamato-one-piece-by-hana-bunny-1/

https://static6.hentai-cosplays.com/upload/20211213/254/259619/p=700/3.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/18 上午10:32:51</b></font><br>

<font size="2"><b>
Yamato (one piece) by Hana Bunny - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/yamato-one-piece-by-hana-bunny/

https://static5.hentai-cosplays.com/upload/20211211/254/259482/p=700/12.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/18 上午10:32:11</b></font><br>

<font size="2"><b>
CosplayHana Bunny - COS Zero Two (Darling in the Franxx) - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/cosplayhana-bunny-cos-zero-two-darling-in-the-franxx/

https://static2.hentai-cosplays.com/upload/20200322/157/160281/p=700/4.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/17 上午10:42:54</b></font><br>

<font size="2"><b>
Hana Bunny - Do-S (One-Punch Man) - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hana-bunny-do-s-one-punch-man/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:10:47</b></font><br>

<font size="2"><b>
DO-S Monster Princess - Hana Bunny - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/do-s-monster-princess-hana-bunny/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午2:12:16</b></font><br>

<font size="2"><b>
Hana Bunny - Ahri Lingerie (League of Legends) 2 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hana-bunny-ahri-lingerie-league-of-legends-2/

https://static6.hentai-cosplays.com/upload/20211230/267/273001/1.jpg
https://static6.hentai-cosplays.com/upload/20211230/267/273001/6.jpg
https://static6.hentai-cosplays.com/upload/20211230/267/273001/10.jpg
https://static6.hentai-cosplays.com/upload/20211230/267/273001/11.jpg
https://static6.hentai-cosplays.com/upload/20211230/267/273001/12.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/31 下午2:06:45</b></font><br>

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
