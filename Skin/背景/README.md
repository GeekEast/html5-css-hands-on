### 背景
- background-color: 背景颜色
- background-image: url() 背景图片
- background-repeat: 是否复制
- background-attachment: 背景会随滚轮滑动滚动还是固定, scroll fixed
- background-position: 水平 垂直
- background: 背景颜色 背景图片地址 背景平铺 背景滚动 背景位置
- background: rgba(0,0,0,0.5) 半透明 **很常用**
- background-size: 背景图片的缩放 **只改宽度就可以，等比例缩放** 
  - 百分比 按比例缩放
  - cover: 铺满且不失真，溢出部分隐藏(**用的多**)
  - contain: 等比例缩放，保证没有溢出部分(**用的少**)
- background: url() no-repeat scroll 10px 20px/50px 60px,
  url()...,
  url()..., 多背景图片, **背景色通常定义在最后背景图上面**

### 文字凸起
```css
text-shadow: 1px 1px 1px #000, -1px -1px 1px #fff;
```

### 文字凹陷
```css
text-shadow: 1px 1px 1px #fff, 1px 1px 1px #000;
```

### 文字垂直居中
```css
line-height: box-height
```

### text-decoration
```css
 /* 无效果 */ none
 /* 下划线 */ underline
 /* 上划线 */ overline
 /* 横穿线 */ line-through
```


> 有些效果是通过图片来实现的