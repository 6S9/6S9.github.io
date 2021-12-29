```note
```

{:.h4}
JavaScript Array forEach() 方法
<br>[
https://www.jc2182.com/javascript/javascript-array-foreach-method.html
](
https://www.jc2182.com/javascript/javascript-array-foreach-method.html
)
<br>[
https://www.jc2182.com/runcode.html?filename=js_array_foreach_ref&type=1&module=jsarrayref
](
https://www.jc2182.com/runcode.html?filename=js_array_foreach_ref&type=1&module=jsarrayref
)
```
<p>单击按钮以列出阵列中的所有项目。</p>
<button onclick="numbers.forEach(myFunction)">尝试</button>
<p id="demo"></p>

<script>
    demoP = document.getElementById("demo");
    var numbers = [4, 9, 16, 25];

    function myFunction(item, index) {
        demoP.innerHTML = demoP.innerHTML + "索引[" + index + "]: " + item + "<br>";
    }
</script>
```

```note
```

{:.h4}
Javascript - can modify array passed to function only sometimes
<br>[
https://stackoverflow.com/questions/29980563/javascript-can-modify-array-passed-to-function-only-sometimes
](
https://stackoverflow.com/questions/29980563/javascript-can-modify-array-passed-to-function-only-sometimes
)
```
var a= [3, 4, 5];
function doesNothing(a) {
    a=[1,1,1];
}

function doesSomething(a) {
    a.push(6);
}

doesNothing(a);
console.log(a);     // [3,4,5] not [1,1,1]
doesSomething(a);
console.log(a);     //[3,4,5,6]
```

```note
```

{:.h4}
JavaScript中的回调函数（callback
<br>[
https://www.jianshu.com/p/84cc8732689c
](
https://www.jianshu.com/p/84cc8732689c
)

{:.h4}
一句话攻略】彻底理解JS中的回调(Callback)函数
<br>[
https://blog.csdn.net/rockage/article/details/79513450
](
https://blog.csdn.net/rockage/article/details/79513450
)
```tip
```

{:.h4}
javascript怎么让函数执行完毕再执行
<br>[
https://bbs.csdn.net/topics/390582064
](
https://bbs.csdn.net/topics/390582064
)
