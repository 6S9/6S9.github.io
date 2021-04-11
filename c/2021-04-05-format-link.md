`　`　
```note
```

**Format Link**{:.h3}<br>
<https://chrome.google.com/webstore/detail/format-link/pocemhmkmchpgamlnocemnbhlcjcbjgg>

**FormatLink-Chrome**{:.h3}<br>
<https://github.com/hnakamur/FormatLink-Chrome>

```tip
```
**FormatLink settings**{:.h3}<br>
\ndocument.write(ah1+pp2+'{{url}}'+sc4+''+si6+'{{text}}'+sg8+sg9+i10+pp2+'{{url}}'+w12);\n

\n<a href="https://slack-imgs.com/?url={{url}}" class="js-smartphoto" data-caption="{{text}}" data-id="" data-group=""><img src="https://slack-imgs.com/?url={{url}}" width="128"/></a>\n

\n{{text}}<br>\n<img src="https://slack-imgs.com/?url={{url}}"><br>\n<a href="{{url}}">\n<br>{{url}}</a><hr/>\n

\n{{text}}\n<img src="{{url}}">\n<a href="{{url.s("\"","&quot;")}}">{{text.s("<","&lt;")}}</a>\n

\n[{{text.s("\\[","\\[").s("\\]","\\]")}}]({{url.s("\\(","%28").s("\\)","%29")}})\n![]({{url.s("\\(","%28").s("\\)","%29")}})\n

<a href="{{url.s("\"","&quot;")}}">{{text.s("<","&lt;")}}</a>

\n{{text}}\n<img src="{{url}}">\n
