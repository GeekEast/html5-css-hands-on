### font-size
- em: 当前对象内文本的的字体尺寸
- px: 像素(推荐)
- in: 英寸
- cm: 厘米
- mm： 毫米
- pt: 点
  

- 普遍使用**14px+**
- 通常使用**偶数**字号

### font-family
- 可以设置多个字体
- 如果第一个字体无法使用，会往后，直到找到可用的字体


### font-weight
- `html`可以用`b`和`strong`
- 400 = normal
- 700 = bold
- 更推荐使用数字方式进行设置


### font-style
- **平时很少用斜体**
- `html`可以用`i`和`em`
- 标准: normal
- 斜体: italic


### 字体综合设定
- 严格顺序
```css
.class{
 font: font-style font-weigth font-size/line-height font-family
}
```