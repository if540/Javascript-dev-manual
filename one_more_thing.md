# One More Thing

> 太多東西記不往

```js
// 從網址資料組合新 url
let { origin, pathname } = window.location;
let getUrl = origin + pathname.split("Op")[0] + "logout";
```
