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

https://static8.hentai-cosplays.com/upload/20220328/294/300325/p=305/237.jpg
https://static8.hentai-cosplays.com/upload/20220327/294/300224/p=700/157.jpg
https://static2.hentai-cosplays.com/upload/20200316/150/153359/p=700/141.jpg
https://static5.hentai-cosplays.com/upload/20211111/246/251262/p=700/151.jpg
https://static4.hentai-cosplays.com/upload/20210328/212/216532/p=700/107.jpg

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

[Fantia] Coser@Kano Nozomi (鹿野希) Nov 2021 (237 ảnh + 3 videos) - エロコスプレ
https://ja.hentai-cosplays.com/image/fantia-coserkano-nozomi-nov-2021-237-nh--3-videos/

https://static8.hentai-cosplays.com/upload/20220328/294/300325/p=305/237.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

[Fantia] Coser@Kano Nozomi (鹿野希) Oct 2021 (157 ảnh + 6 videos) - エロコスプレ
https://ja.hentai-cosplays.com/image/fantia-coserkano-nozomi-oct-2021-157-nh--6-videos/

https://static8.hentai-cosplays.com/upload/20220327/294/300224/p=700/157.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

鹿野希 Vol.07 白色高叉泳装 [140P3V-445MB] - エロコスプレ
https://ja.hentai-cosplays.com/image/kano-nozomi-vol07-white-takato-swimming-140p3v-445mb/

https://static2.hentai-cosplays.com/upload/20200316/150/153359/p=700/141.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

鹿野希 - Kano Nozomi Vol.3 - エロコスプレ
https://ja.hentai-cosplays.com/image/nozomi-shikano-kano-nozomi-vol3/

https://static5.hentai-cosplays.com/upload/20211111/246/251262/p=700/151.jpg

<font size="1" style="color:#DCDCDC">2022-03-29</font>

鹿野希 酒酔い先輩 [107P] - エロコスプレ
https://ja.hentai-cosplays.com/image/nozomi-shikano-drunken-senior-107p/

https://static4.hentai-cosplays.com/upload/20210328/212/216532/46.jpg
https://static4.hentai-cosplays.com/upload/20210328/212/216532/p=700/107.jpg

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
