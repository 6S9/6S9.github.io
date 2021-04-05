<script>
   function check(){
      var name=document.getElementById("name").value;
   var pass=document.getElementById("pass").value;
   var y = document.getElementById("myDIV");
   if(name=="" && pass=="y"){
   y.style.display = "block";
   }else{
   y.style.display = "none";
   }
   }
</script>

<form name="f" action="">
<center>用户：<INPUT TYPE="text" NAME="" id="name"><br></center>
<center>密码：<INPUT TYPE="password" NAME="" id="pass"><br></center>
<center><INPUT TYPE="button" value="登入" onclick="check()"><INPUT TYPE="reset" value="重置"></center>
</form>

<div id="myDIV" style="display: none">

  <a href="https://cn.bing.com/th?id=OHR.NorfolkPups_ZH-CN0794024596_UHD.jpg" class="js-smartphoto" data-caption="灰海豹" data-id="bear" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.NorfolkPups_ZH-CN0794024596_480x360.jpg" width="360"/>
  </a>
  <a href="https://cn.bing.com/th?id=OHR.PhotographyEmperor_ZH-CN8188172143_UHD.jpg" class="js-smartphoto" data-caption="帝企鹅（学名：Aptenodytes forsteri" data-id="camel" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.PhotographyEmperor_ZH-CN8188172143_360x270.jpg" width="360"/>
  </a>
  <a href="https://cn.bing.com/th?id=OHR.PRookery_ZH-CN2608300981_1920x1080.jpg" class="js-smartphoto" data-caption="斯诺希尔岛`小企鹅`" data-id="sai" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.PRookery_ZH-CN2608300981_360x270.jpg" width="360"/>
  </a>

  <a href="https://cn.bing.com/th?id=OHR.RedRobin_ZH-CN4148689161_UHD.jpg" class="js-smartphoto" data-caption="欧亚鸲" data-id="camel" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.RedRobin_ZH-CN4148689161_360x270.jpg" width="360"/>
  </a>
  <a href="https://cn.bing.com/th?id=OHR.FalklandRockhoppers_ZH-CN5370686595_1920x1080.jpg" class="js-smartphoto" data-caption="### 跳岩企鹅" data-id="sai" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.FalklandRockhoppers_ZH-CN5370686595_480x360.jpg" width="360"/>
  </a>

  <a href="https://cn.bing.com/th?id=OHR.Mazezilla_ZH-CN8502282112_UHD.jpg" class="js-smartphoto" data-caption="bear" data-id="**克林格尔农场**" data-group="0">
    <img src="https://cn.bing.com/th?id=OHR.Mazezilla_ZH-CN8502282112_360x270.jpg" width="360"/>
  </a>

  <link rel="stylesheet" href="https://unpkg.com/smartphoto@1.1.0/css/smartphoto.min.css">
  <script src="https://unpkg.com/smartphoto@1.1.0/js/smartphoto.min.js"></script>
  <script>
  document.addEventListener('DOMContentLoaded',function(){
    new SmartPhoto(".js-smartphoto");
  });
  </script>

</div>
