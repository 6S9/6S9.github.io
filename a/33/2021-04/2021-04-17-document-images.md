```tip
{:.font-head}
video.js--很赞的H5视频播放库
[
https://www.cnblogs.com/webenh/p/5815741.html
](
https://www.cnblogs.com/webenh/p/5815741.html
)
```

```note
document.write() 中如何使用变量
[
https://bbs.csdn.net/topics/392024474
](
https://bbs.csdn.net/topics/392024474
)
{:.font-head}
```
var url ='http://www.baidul.com/';

document.write('<script src="'+url +'"></script>');

```note
js document.write()使用介绍
[
https://www.jb51.net/article/47147.htm
](
https://www.jb51.net/article/47147.htm
)
{:.font-head}
```

```tip
{:.font-head}
JS中的document.images属性
[
http://www.uw3c.com/jsviews/js68.html
](
http://www.uw3c.com/jsviews/js68.html
)
```

document.images.length //对应页面上img标签的个数

document.images.oImage.src=”1.jpg”

<div><div class="syntaxhighlighter  js" id="highlighter_97695"><div class="toolbar"><span><a class="toolbar_item command_help help" href="#">?</a></span></div><table border="0" cellspacing="0" cellpadding="0"><tbody><tr><td class="gutter"><div class="line number1 index0 alt2">1</div><div class="line number2 index1 alt1">2</div><div class="line number3 index2 alt2">3</div><div class="line number4 index3 alt1">4</div><div class="line number5 index4 alt2">5</div><div class="line number6 index5 alt1">6</div><div class="line number7 index6 alt2">7</div><div class="line number8 index7 alt1">8</div><div class="line number9 index8 alt2">9</div><div class="line number10 index9 alt1">10</div><div class="line number11 index10 alt2">11</div><div class="line number12 index11 alt1">12</div><div class="line number13 index12 alt2">13</div><div class="line number14 index13 alt1">14</div><div class="line number15 index14 alt2">15</div><div class="line number16 index15 alt1">16</div><div class="line number17 index16 alt2">17</div><div class="line number18 index17 alt1">18</div></td><td class="code"><div class="container"><div class="line number1 index0 alt2"><code class="js plain">a)通过集合引用</code></div><div class="line number2 index1 alt1"><code class="js plain">document.images </code><code class="js comments">//对应页面上的img标签</code></div><div class="line number3 index2 alt2"><code class="js plain">document.images.length </code><code class="js comments">//对应页面上img标签的个数</code></div><div class="line number4 index3 alt1"><code class="js plain">document.images[0] </code><code class="js comments">//第1个img标签</code></div><div class="line number5 index4 alt2"><code class="js plain">document.images[i] </code><code class="js comments">//第i-1个img标签</code></div><div class="line number6 index5 alt1">&nbsp;</div><div class="line number7 index6 alt2"><code class="js plain">b)通过name属性直接引用</code></div><div class="line number8 index7 alt1"><code class="js plain">img name=”oImage”</code></div><div class="line number9 index8 alt2"><code class="js plain">document.images.oImage </code><code class="js comments">//document.images.name属性</code></div><div class="line number10 index9 alt1">&nbsp;</div><div class="line number11 index10 alt2"><code class="js plain">c)引用图片的src属性</code></div><div class="line number12 index11 alt1"><code class="js plain">document.images.oImage.src </code><code class="js comments">//document.images.name属性.src</code></div><div class="line number13 index12 alt2">&nbsp;</div><div class="line number14 index13 alt1"><code class="js plain">d)创建一个图象</code></div><div class="line number15 index14 alt2"><code class="js keyword">var</code> <code class="js plain">oImage</code></div><div class="line number16 index15 alt1"><code class="js plain">oImage = </code><code class="js keyword">new</code> <code class="js plain">Image()</code></div><div class="line number17 index16 alt2"><code class="js plain">document.images.oImage.src=”1.jpg”</code></div><div class="line number18 index17 alt1"><code class="js plain">同时在页面上建立一个img /标签与之对应就可以显示</code></div></div></td></tr></tbody></table></div></div>
