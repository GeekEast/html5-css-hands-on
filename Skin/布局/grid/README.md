## Grid
- flex是1-dimension, grid是2-dimension
- 主要用来做layout

### Concepts
- grid **container**: `display: grid`, direct of all grid items.
- grid **item**: the **direct** descendants of the grid container.
- grid **line**: dividing **lines** make up the structure of the grid.
- grid **cell**: space between 2 `adjacent` row **and** 2 `adjacent` column grid lines.
- grid **track**: space between 2 `adjacent` rows **or** 2 `adjacent` column grid lines.
- grid **area**: space between 2 rows and 2 column grid lines.

### Container
- `display: grid`: 将当前元素设定为grid container
- `grid-template-columns: 40px 50px 50px 40px`: 从左到右4列, 加名字`[first] 40px [second] 40px`
- `grid-template-rows: 25% 100px auto`: 从上到下3行
- `grid-template-areas`: 引用方式集中定义布局
```css
.item-a {
  grid-area: header;
}
.item-b {
  grid-area: main;
}
.item-c {
  grid-area: sidebar;
}
.item-d {
  grid-area: footer;
}

.container {
  display: grid;
  grid-template-columns: 50px 50px 50px 50px;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
}
```
- `grid-template`: 更简化 **一般不用**
```css
.container {
  grid-template:
    /* line name name name name size */
    [row1-start] "header header header" 25px [row1-end]
    [row2-start] "footer footer footer" 25px [row2-end]
    / auto 50px auto; /* grid-template-rows */
}
```
- `gap`: 设置items间距
```css
.container{
    column-gap: 15px;
    row-gap: 10px;
    gap: 4px;
}
```
- `justify-items`: container群体角度 行对齐方式
- `align-items`: container群体角度 列对齐方式
- `place-items`: container群体角度 行列对齐方式
- `justify-content`: 多行整体对齐方式
- `align-content`: 多列整体对齐方式
- `place-content`: 团儿整齐对齐方式
<!-- TODO: 对dense的研究 -->
- `grid-auto-flow`: 在item处未添加grid配置时默认排列方式
- `grid`: 极简版本 我不喜欢谢谢

### Item
- `grid-column-start`: 后面加Line, 列起位置
- `grid-column-end`: 后面加Line, 列终位置
- `grid-column: start-line end-line | start-line span x`: 
- `grid-row-start`: 后面加Line, 行起位置
- `grid-row-end`: 后面加Line, 行终位置
- `grid-row`: `start-line end-line | start-line span x`
- `grid-area: name`: 配合container的`grid-template-areas`使用
- `justify-self`: 行对齐方式
- `align-self`: 列对齐方式
- `place-self`: 行列对齐方式
  

### Function & Keywords
- `px`, `rem`, `%`, `min-content`, `max-content`, `auto`, `fr`
- `minmax()`, `repeat()`
  

## Reference
- [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/#prop-display)