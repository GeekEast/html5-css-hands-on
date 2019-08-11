### 选择器命名
- 语义清晰,直接表明属性
- 不要用纯数字和中文

### 链接伪类选择器
- :hover
- :link

### 结构伪类选择器
- :first-child
- :last-child
- :nth-child(4)： 第四个
- :nth-child(even)：偶数元素
- :nth-child(odd)： 奇数元素
- :nth-child(n): 全部元素
- :nth-child(2n): 偶数元素
- :nth-last-child(n)

### 目标伪类选择器
- 页内当前所处对象，即url最后的#id
```css
    div:target{

    }
```