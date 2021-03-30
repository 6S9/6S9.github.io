```note
```
**HTML网页中怎么控制图层的显隐**{:.h3}<br>
<https://zhidao.baidu.com/question/39504771.html>

**div 隐藏和显示**{:.h3}<br>
<https://blog.csdn.net/qq_44884203/article/details/89292756>

```note
```
**Details**{:.h3}<br>
<https://primer.style/css/utilities/details>

**Box overlay**{:.h3}<br>
<https://primer.style/css/components/box-overlay>

**Tooltips**{:.h2}<br>
<https://primer.style/css/components/tooltips>

**Truncate**{:.h3}<br>
<https://primer.style/css/components/truncate>

```note
```
**Jekyll Text Expand or Collapsible Markdown**{:.h4}<br>
<https://www.tomordonez.com/jekyll-text-expand-collapsible-markdown/>

**Collapse**{:.h5}<br>
<https://getbootstrap.com/docs/4.0/components/collapse/>

**How TO - Collapse**{:.h6}<br>
<https://www.w3schools.com/howto/howto_js_collapsible.asp>
[Try it Yourself](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_js_collapsible)

[expand]
Long content here
and here
...
[/expand]

<details>
	<summary>Click to expand</summary>
	Long content here
	and here
</details>

<p>Click the "Try it" button to toggle between hiding and showing the DIV element:</p>

<button onclick="myFunction()">Try it</button>

<div id="myDIV" style="display: none">
This is my DIV element.
</div>

<p><b>Note:</b> The element will not take up any space when the display property set to "none".</p>

<script>
function myFunction() {
  var x = document.getElementById("myDIV");
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
</script>
