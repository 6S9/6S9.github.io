```note
```

{:.font-head}
Detect url / links and replace image with img tag and links with a href
<br>[
https://stackoverflow.com/questions/18920671/detect-url-links-and-replace-image-with-img-tag-and-links-with-a-href
](
https://stackoverflow.com/questions/18920671/detect-url-links-and-replace-image-with-img-tag-and-links-with-a-href
)
```note
var __urlRegex = /(\b(https?|ftp|file):\/\/[-A-Z0-9+&@#\/%?=~_|!:,.;]*[-A-Z0-9+&@#\/%=~_|])/ig;
var __imgRegex = /\.(?:jpe?g|gif|png)$/i;
```

<br>[
http://jsfiddle.net/Victornpb/VSRFX/4/
](
http://jsfiddle.net/Victornpb/VSRFX/4/
)

{:.h4}
Regular Expression
<br>[
https://www.regextester.com/20
](
https://www.regextester.com/20
)

```note
```

{:.font-head}
How to replace plain URLs with links?
<br>[
https://stackoverflow.com/questions/37684/how-to-replace-plain-urls-with-links
](
https://stackoverflow.com/questions/37684/how-to-replace-plain-urls-with-links
)

{:.font-head}
Anchorme
<br>[
http://alexcorvi.github.io/anchorme.js/
](
http://alexcorvi.github.io/anchorme.js/
)

{:.h4}
How to replace plain URLs with links, with example? [duplicate
<br>[
https://stackoverflow.com/questions/19547008/how-to-replace-plain-urls-with-links-with-example/19708150#19708150
](
https://stackoverflow.com/questions/19547008/how-to-replace-plain-urls-with-links-with-example/19708150#19708150
)

{:.h4}
Find urls and make it clickable in reactJs/javascript
<br>[
https://stackoverflow.com/questions/53881835/find-urls-and-make-it-clickable-in-reactjs-javascript
](
https://stackoverflow.com/questions/53881835/find-urls-and-make-it-clickable-in-reactjs-javascript
)

```tip
```

{:.h4}
replaceURLWithHTMLLinks
<br>[
http://jsfiddle.net/EwzcD/1/
](
http://jsfiddle.net/EwzcD/1/
)

{:.h4}
Replace multiple strings at once
<br>[
https://stackoverflow.com/questions/5069464/replace-multiple-strings-at-once
](
https://stackoverflow.com/questions/5069464/replace-multiple-strings-at-once
)
```tip
let text = 'the red apple and the green ball';
const toStrip = ['red', 'green'];
toStrip.forEach(x => {
   text = text.replace(x, '');
});

console.log(text);
// logs -> the apple and the ball
```
