## Flexbox
- **布局方式一**: `float` + `block`
- **布局方式二**: `grid` 
- **布局方式三**: `flexbox` 

### Concepts
- **主轴(main)**: flex-direction, 主轴**长度**由定义了`display:flex`元素的`width`/`height`来决定
- **副轴(cross)**: `垂直`于flex-direction， 副轴**长度**由定义了`display:flex`元素的`height`/`width`来决定

### Container
- **flex-direction**: `主轴`

```css
/* 水平布局 */
.container {
    display: flex;
    flex-direction: row /* 默认 */
}

/* 垂直布局 */
.container {
    display: flex;
    flex-direction: column;
}
```

- **justify-content**: `主轴`方向对齐方式
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-04-22-18-46-44.png alt="no image found"></p>

- **align-cotent**: `副轴`方向对齐方式
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-04-22-18-49-02.png alt="no image found"></p>

- **align-items**: `副轴`有**额外空间**时的对齐方式，从`container`的角度(**群体**)
<p align="center"><img style="display: block; width: 600px; margin: 0 auto;" src=img/2020-04-22-18-53-26.png alt="no image found"></p>


- **flex-wrap**: 是否`换行`, `wrap`情况下: `flex-shrink`失效
### Item
- **order**: 不改动`markup`的情况下，重新**排序**，`数字越大越靠后`
- **flex-basis**: `主轴`方向上的**元素长度**, 优先级**高**于`width`/`height` (副轴上使用width/height依然有效)
- **flex-grow**: `主轴`有**闲置空间**时，`1`代表**索取**闲置空间，`0`代表**不索取闲置空间**，`1`以上表示索取空间的**相对比例**，`数值越大，索取越多`；
- **flex-shrink**: `主轴`无**闲置空间**时，`1`代表**自动缩小**，`0`代表**不自动缩小**，`1`以上表示缩小的**相对比例**，`数值越大，缩得越小`；**flex-wrap为wrap时，此属性无效**
- **align-self**: `副轴`有**额外空间**时的对齐方式，从单个`item`的角度(**个体**)

### Example

```css
.container {
  display: flex;
  flex-direction: row | row-reverse | column | column-reverse;
  flex-wrap: nowrap | wrap | wrap-reverse;
  flex-flow: row nowrap   /* shorthand for flex-direction + flex-wrap */;
  /* 想象每一列为一条竖线，多条竖线如何对齐， 一般在多列时进行考虑*/
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly /*  主轴对齐方式 */;
  /* 想象每一行为一条横线，多条横线如何对齐, 一般在多行是进行考虑 */
  align-content: flex-start | flex-end | center | stretch | space-between | space-around; /*  副轴 */
  /* 每条横线中在副轴方向上如何对齐，一般在单行时进行考虑 */
  /* 单行最大高度为容器高度，多行最大高度为该行最高元素的高度, 默认值为stretch, 在未设定高度时有效 */
  align-items: flex-start | flex-end | center | stretch | baseline;
}
```
```css
.item {
  /* 单个item的显示序号，序号越大越靠后 */
  order: 0;
  /* 沿着主轴上，当有闲置空间时的空间分配规则 */
  /* 1表示主轴长度大于 items在主轴方向长度的总和 时, item尽可能放大 */
  /* 数字为相对大小，越大表示放得越大, 默认为0: 不放大  */
  flex-grow: 0;
  /* 沿着主轴上，当无闲置空间时的空间分配规则 */
  /* 1表示 主轴长度小于 items在主轴方向长度的总和 时, item尽可能缩小，*/ 
  /* 数字为相对大小，越小表示缩得越小，默认为1, 0为不缩小 */
  flex-shrink: 1;
  /* 元素主轴长度 */
  /* 替代width或者height属性，优先级高于width/height */
  /* 值为auto时，表示是content的大小 */
  flex-basis: <length> | auto; /* auto表示基于content */
  /* 推荐使用：shorthand */
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]; 
  /* 单个item副轴上的对齐方式 */
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```


## Reference
- [Flexbox Playground](https://codepen.io/enxaneta/full/adLPwv/)
- [深入理解css3中的flex-grow、flex-shrink、flex-basis](https://zhoon.github.io/css3/2014/08/23/flex.html)