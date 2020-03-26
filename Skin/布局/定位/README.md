

### 定位
### 边偏移
- top, bottom, left, right
### 定位模式
- static: 默认, 无法使用边偏移，**相当于不定位**
- relative: 相对于文档流`原本位置`进行`偏移`, 还`在文档流`当中, `safe to use as base of absolute` positioning
- absolute: 相对于`父元素`进行定位，默认是`viewport`，`脱离文档流`
- fixed: 相对于`viewport`进行定位, `脱离文档流`

#### absolute定位居中对齐
- 子元素 `left: calc(50% - 子元素宽度/高度的一半);`
- 应用: `轮播条`


### 定位模式转换
- 定位为`absolute`或者`fixed`的元素自动转换为`行内块`模式
  - 所以`定位后的元素`无需指定`display`为`block`或者`inline-block`
- 定位为`absolute`或者`fixed`时，注意给`高度`和`宽度`
