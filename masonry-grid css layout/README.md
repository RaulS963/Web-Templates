# Responsive CSS Masonary-grid layout

## HTML
```html
<div class="main-grid">
  <!-- item1 #1 -->
  <div class="item">
    <div class="content">
      <!-- content here -->
    </div>
  </div>  
      <!-- item #2 
           item #3
            ....
      -->  
</div>
```

## CSS
```css
.main-grid{
  display: grid;
  grid-gap: 10px;
  grid-template-columns: repeat(auto-fill, minmax(250px,1fr));
  grid-auto-rows: 10px;
}
```

## JS
```javascript
function resizeGridItem(item){
  grid = document.getElementsByClassName("main-grid")[0];
  rowHeight = parseInt(window.getComputedStyle(grid).getPropertyValue('grid-auto-rows'));
  rowGap = parseInt(window.getComputedStyle(grid).getPropertyValue('grid-row-gap'));
  rowSpan = Math.ceil((item.querySelector('.content').getBoundingClientRect().height+rowGap)/(rowHeight+rowGap));
  item.style.gridRowEnd = "span "+ rowSpan;
}
		  
function resizeAllGridItems(){
  allItems = document.getElementsByClassName("item");
  for(x=0;x<allItems.length;x++){
  resizeGridItem(allItems[x]);
  }
}	  

window.addEventListener("load",resizeAllGridItems);
window.addEventListener("resize", resizeAllGridItems);
```
