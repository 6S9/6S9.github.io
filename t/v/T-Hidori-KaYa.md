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

https://static6.hentai-cosplays.com/upload/20220116/279/285303/p=700/29.jpg
https://static4.hentai-cosplays.com/upload/20210629/228/232832/p=700/12.jpg
https://static3.hentai-cosplays.com/upload/20201229/191/195412/p=700/350.jpg
https://static4.hentai-cosplays.com/upload/20210305/209/213940/p=700/754.jpg
https://static2.hentai-cosplays.com/upload/20180605/81/82694/p=700/56.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

<font size="2"><b>
Hidori Rose - Ram Bride Lingerie - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/hidori-rose-ram-bride-lingerie-1/

https://static6.hentai-cosplays.com/upload/20220116/279/285303/p=700/29.jpg

<font size="1" style="color:#DCDCDC"><b>2022/1/17 下午8:03:05</b></font><br>

<font size="2"><b>
KaYa 萱 - Jeanne Alter Reverse Bunny - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/kaya--jeanne-alter-reverse-bunny/

https://static4.hentai-cosplays.com/upload/20210629/228/232832/p=700/12.jpg

<font size="1" style="color:#DCDCDC"><b>2021/12/30 下午2:27:03</b></font><br>

<font size="2"><b>
[Twitter] KaYa Huang ❤️萱❤️ (@kaya1028) [Twitter] KaYa Huang ❤️萱❤️ (@kaya1028) - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/twitter-kaya-huang--kaya1028-twitter-kaya-huang--kaya1028-1/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:17:46</b></font><br>

<font size="2"><b>
kaya萱 cosplay collection - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/kaya-cosplay-collection/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 上午11:18:52</b></font><br>

<font size="2"><b>
七つの大罪 - 強欲の像 - エロコスプレ</b></font><br>
https://ja.hentai-cosplays.com/image/the-seven-deadly-sins-the-statue-of-greed/

<font size="1" style="color:#DCDCDC"><b>2021/12/15 下午3:13:18</b></font><br>

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
