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

</textarea><br><!-- 🍀<br>🍑　🍅<hr>🌸 -->

<textarea rows="30" cols="100" id="tar" oninput="loadparse()">

九泉之岛,九泉之島 - 东田裕介 - 快岸漫画(www.kanbook.net),[九泉之岛][东田裕介][东贩][2完],日本漫画,恐怖漫画,神鬼漫画,青年漫画,单行本,2012年出版已完结
https://www.kanbook.net/939?v=0.8700749206784733

https://s1smedia.kanbook.net:2087/939/1/2/25_314988.jpg
https://s1smedia.kanbook.net:2087/939/1/2/24_788603.jpg

<font size="1" style="color:#DCDCDC">2022-06-07</font>

View rycaon's Profile, Contact Details & Sexy Pics on ImageFap
https://www.imagefap.com/profile/rycaon

<font size="1" style="color:#DCDCDC">2022-06-06</font>

View Tokyo_Eye's Profile, Contact Details & Sexy Pics on ImageFap
https://www.imagefap.com/profile/Tokyo_Eye

<font size="1" style="color:#DCDCDC">2022-06-06</font>

https://m.afast.ws/L5ZJDdxlBYn/images/cover.jpg
https://m.afast.ws/Kq8w0Y7NZ1x/images/cover.jpg
https://m.afast.ws/J4XGVrKbZnA/images/cover.jpg
https://m.afast.ws/WoXddkj6XeV/images/cover.jpg

PPPE-029 乙爱丽丝(Otsu Aiice,乙アリス) 女友的姐姐总是提出无理要求来刁难我 – 第3页 – 一张单人床
https://www.woobuzz.com/3779.html/3

https://www.woobuzz.com/wp-content/uploads/2022/05/1-21.gif
https://www.woobuzz.com/wp-content/uploads/2022/05/2-21.gif
https://www.woobuzz.com/wp-content/uploads/2022/05/3-21.gif

<font size="1" style="color:#DCDCDC">2022-06-07</font>

弟控肉慾姐姐們的夾擊．乙愛麗絲／百永紗里奈 : AVΗD101 高清在线谜片
https://cn2.af101.live/watch?v=VvBEoGEWZK9

https://m.afast.ws/VvBEoGEWZK9/images/cover.jpg

<font size="1" style="color:#DCDCDC">2022-06-07</font>

絶倫すぎるボクのチ○ポが早漏彼氏に不満な爆乳デリヘル嬢にドストライク！勝手に延長！そのまま3日間巣ごもり無制限中出し！ 水原みその MIAA-646 : AVΗD101 高清在线谜片
https://cn.af101.net/watch?v=okBYRmp58bz

https://m.afast.ws/okBYRmp58bz/images/cover.jpg

<font size="1" style="color:#DCDCDC">2022-06-06</font>

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
