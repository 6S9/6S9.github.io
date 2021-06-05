```note
```

{:.font-head}
Detect URLs in text with JavaScript
<br>[
https://stackoverflow.com/questions/1500260/detect-urls-in-text-with-javascript
](
https://stackoverflow.com/questions/1500260/detect-urls-in-text-with-javascript
)

{:.font-head}
Check if URL Exists
<br>[
https://jsfiddle.net/pu3antasyah/v95Loyvu/
](
https://jsfiddle.net/pu3antasyah/v95Loyvu/
)

{:.font-head}
Check if image exists on server using JavaScript?
<br>[
https://stackoverflow.com/questions/18837735/check-if-image-exists-on-server-using-javascript
](
https://stackoverflow.com/questions/18837735/check-if-image-exists-on-server-using-javascript
)
```tip
function getImageOrFallback(url, fallback) {
  return new Promise((resolve, reject) => {
    const img = new Image()
    img.src = url
    img.onload = () => resolve(url)
    img.onerror = () => {
      reject(`image not found for url ${url}`)
    }
  }).catch(() => {
    return fallback
  })
}

getImageOrFallback("https://google.com", "https://picsum.photos/400/300").then(validUrl => {
  console.log(validUrl)
  document.body.style.backgroundImage = `url(${validUrl})`
})
```
