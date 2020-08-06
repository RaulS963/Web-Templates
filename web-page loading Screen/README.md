# Web Page loading Screen

## HTML:
```html
<div class="loader">
  <img src="loading.gif" />
</div>
```

## CSS:
```css
.loader{
    position: fixed;
    z-index: 99;
    top:0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: white;
    display: flex;
    justify-content: center;
    align-items: center;
}

@keyframes fadeOut{
 100%{
    opacity: 0;
    visibility: hidden;
 }
}

.loader.hidden{
    animation: fadeOut 0.5s;
    animation-fill-mode: forwards;
}
```
## JS:
```javascript
window.addEventListener("load",function(){  // or "DOMContentLoaded" => if images can load after the page is visible
    const loader = document.querySelector(".loader");
    loader.className += " hidden";  // space is important => class="loader hidden"
})

```
