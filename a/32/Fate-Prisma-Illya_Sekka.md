```tip
```

<table id="tbc" style="white-space:pre-wrap">
</table>
<button onclick="toggleb()">toggle</button>
<button onclick="loadparse()">loadparse</button>
<br>
<!-- 🌸<br>🍅-　-🍑<hr>🍀 --> <textarea rows="30" cols="100" style="display: none" id="tar">

有个男人梦想 拯救全世界

历史悠久的名门
虽然除了历史长就没什么了

在那个家里出生的孩子
是没人看到过七岁以下的女童

七岁以前的幼子不是人类

如果只是一个城市还好
那个黑暗会扩张到什么程度 无法预测

结界消失
人们的哀怨和潮水般的思绪
传达给了美游

切嗣是个怪人
想要从这个世界上消除痛苦和悲伤
实现真正的和平
他是真心这样想

五年前的灾害以来
这个市里几乎都没有人了
虽然对外说是特殊的瓦斯爆炸
但冬木的人都知道并非如此

我一直企图做正确的事情 而一直在犯错
想要纠正错误
而无限的错上加错
然后 在走投无路的时候
开始自私的追求奇迹

要拯救的是全体人类
不是眼前的小生命

有个偶尔坏心眼 但温柔的前辈
虽然人少 但能普通的上学
学习 社团活动
这种不起眼的岁月循环往复
让我感觉好幸福

我对于谎言很宽容
可是 我厌恶只是模仿外表 无法成为任何人的假货
你先前的笑容就是如此
今天的嬉笑虽然打从心底让人恶心
但不是空无一物的 所以要好上一万倍

真是可悲
假货没有作为假货的自觉

作为守望这一世界的终焉之人
欢迎迷惘羔羊的来访

不是个体 而是种族
为了完成大事而不拘小节

我有还没能说出的话 没能传达的事情

我其实也想更多的和前辈在一起
去学校 参加社团活动
一起回家 道一声明天见
这一点事情 就是我的宝石

由我 来打倒哥哥

没关系 哥哥早就已经死了

比射精爽一百倍！

没有奇迹
也没有希望
理想 消失于黑暗中
即使如此 我还留在这里

重要的人 已经不在了
继承下来的骄傲 由我自己舍弃了
暴露出来的真我
是如此的空洞
然后失去了一切
终于注定了我要做的事情

就算这是对全人类的背叛吗
从充满这个星球的悲剧

抱歉了 切嗣
就算是错误的 我果然还是要走这边的路

那个家里的日记
从初代到美游这一代为止
连绵记录了一切
将其力量独占的朔月家
许下了什么愿望
你知道吗
他们
只是许愿孩子健康成长
财富 繁荣
明明都唾手可得
却只实现了父母对孩子的
极为理所当然的愿望
整整四百年间 无一例外
你要说… 这是恶的话
我甘心为恶

虽然已经是将死之人
只有战斗力还在继续提升
虽然不知道你用了什么荒唐手段
没用的
你的前方 只有明确的灭亡

唯一之物 有时也会凌驾于全部之上

</textarea> <!-- 🍀<br>🍑-　-🍅<hr>🌸 -->

<script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js"></script>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.css" />
<script src="https://cdn.jsdelivr.net/gh/fancyapps/fancybox@3.5.7/dist/jquery.fancybox.min.js"></script>

<script type="text/javascript">

var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png)$/i;

loadparse();

function parseURL($string){

    var exp = __urlRegex;
    return $string.replace(exp,function(match){
            __imgRegex.lastIndex=0;
            if(__imgRegex.test(match)){
                return '<a data-fancybox="gallery" href="' + match.replace("/p=700", "")
                 + '"><img src="' + match.replace("/p=700", "/p=160x200")+'" width="64"></a>';
            }
            else{
                return '<a href="' + match + '" target="_blank">' + match + '</a>';
            }
        }
    );
}

function loadparse() {
  tbc.innerHTML = parseURL(tar.value);
}

function toggleb() {
  var x = document.getElementById("tar");
  if (x.style.display === "none") {
    x.style.display = "";
  } else {
    x.style.display = "none";
  }
}

</script>
