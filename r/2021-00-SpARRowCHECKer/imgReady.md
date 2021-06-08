```note
console.log(LoadingImage.prototype.check);

function getImageItem(src) {
  console.log($container.prepend());

function onProgress( imgLoad, image ) {
  console.log(image.isLoaded);
```
```note
```

{:.font-head}
gitgrimbo/ImageLoaded-mod.js
<br>[
https://gist.github.com/gitgrimbo/6451492#file-imageloaded-mod-js-L726
](
https://gist.github.com/gitgrimbo/6451492#file-imageloaded-mod-js-L726
)
```tip
var cached = cache[ this.img.src ];
    if ( cached ) {
      this.useCached( cached );
      return;
    }
    // add this to cache
    cache[ this.img.src ] = this;
```

{:.font-head}
js动态获取图片尺寸（兼容所有浏览器，速度极快
<br>[
http://blog.phpdr.net/js-get-image-size.html
](
http://blog.phpdr.net/js-get-image-size.html
)

{:.font-head}
`imgReady`Demo
<br>[
http://blog.phpdr.net/wp-content/uploads/2012/06/imgReadyDemo.html
](
http://blog.phpdr.net/wp-content/uploads/2012/06/imgReadyDemo.html
)

{:.h4}
转]js动态获取图片长宽尺寸
<br>[
https://www.cnblogs.com/newsea/p/4286423.html
](
https://www.cnblogs.com/newsea/p/4286423.html
)

{:.font-head}
How can I determine if an image has loaded, using Javascript/jQuery
<br>[
https://stackoverflow.com/questions/263359/how-can-i-determine-if-an-image-has-loaded-using-javascript-jquery
](
https://stackoverflow.com/questions/263359/how-can-i-determine-if-an-image-has-loaded-using-javascript-jquery
)

```tip
$('container').imagesLoaded(function(){
 console.log("I loaded!");
})
```

```tip
imageLoaded = function(node) {
    var w = 'undefined' != typeof node.clientWidth ? node.clientWidth : node.offsetWidth;
    var h = 'undefined' != typeof node.clientHeight ? node.clientHeight : node.offsetHeight;
    return w+h > 0 ? true : false;
};
```

{:.font-head}
JavaScript image preloading complete example
<br>[
https://www.tutorialfor.com/blog-216648.htm
](
https://www.tutorialfor.com/blog-216648.htm
)
