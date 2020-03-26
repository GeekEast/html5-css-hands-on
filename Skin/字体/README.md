### font-style
- **平时很少用斜体**
- `html`可以用`i`和`em`
- 标准: normal
- 斜体: italic

### font-weight
- `html`可以用`b`和`strong`
- 400 = normal
- 700 = bold
- **更推荐使用数字方式进行设置**


### font-size
- `em`: 当前对象内文本的的字体尺寸
- `px`: 像素(推荐)
- `in`: 英寸
- `cm`: 厘米
- `mm`: 毫米
- `pt`: 点
  
- 普遍使用**14px+**
- 通常使用**偶数**字号

### line-height
- 行高, 一般情况下比字体大小大7，8px就可以了
- **文字垂直居中**：`line-height: box-height`

### font-family
- 可以设置多个字体
- 如果第一个字体无法使用，会往后，直到找到可用的字体


### 字体综合设定
- 严格顺序
```css
.class{
 font: font-style font-weight font-size/line-height font-family
}
```

### 对齐、缩进、间距
- text-align: left right center
- text-indent: 首行缩进(很常用很常用)，建议em作为单位，汉字1em为一个汉字的宽度
- letter-spacing: 字间距, 一般采取默认值
- word-spacing: 单词间距, 一般采取默认值


### 文字阴影
- text-shadow: 水平位置(正右) 垂直位置(正下) 模糊距离(z方向) 阴影颜色
- 文字凸起 `text-shadow: 1px 1px 1px #000, -1px -1px 1px #fff;`
- 文字凹陷 `text-shadow: 1px 1px 1px #fff, 1px 1px 1px #000;`


### text-decoration
```css
 /* 无效果 */ none
 /* 下划线 */ underline
 /* 上划线 */ overline
 /* 横穿线 */ line-through
```