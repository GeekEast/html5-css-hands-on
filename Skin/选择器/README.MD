### 选择器命名
- 语义清晰,直接表明属性
- 不要用纯数字和中文

### `链接`伪类选择器(`:`)
- :hover
- :link
- :visited
- :active

### `结构`伪类选择器
- :first-child
- :last-child
- :nth-child(4)： 第四个
- :nth-child(even)：偶数元素
- :nth-child(odd)： 奇数元素
- :nth-child(n): 全部元素
- :nth-child(2n): 偶数元素
- :nth-last-child(n)

### `目标`伪类选择器
- 页内当前所处对象，即url最后的#id
```css
    div:target{
        ...
    }
```

### `伪元素`选择器(`::`)
- 第一个字母 `p::first-letter`
- 第一行 `p::firstline`
- 选中文本 `p::selection`
- 元素之前 `div::before { content: "开始"}`
- 元素之后 `div::after { content: "结束"}`

### `复合`选择器
- 多个元素 `div,p`
- 单个元素 `div.btn`
- 儿孙 `div p`
- 儿子 `div > p`
- 兄弟 `div ~ p`
- 亲兄弟 `div + p`


### `属性`选择器
- 属性存在 `a[title]`
- 属性值等于 `a[title=text]`
- 属性值包含 `a[title*=text]`
- 属性值以...开始 `a[title^=text]`
- 属性值以...结束 `a[title$=text]`


### 权重叠加
- 如何增加权重：在`css`中增加选择器的数目即可，越详细权重越高
- `行内，id，类，元素` (前四为0 ？继承：继承为0)