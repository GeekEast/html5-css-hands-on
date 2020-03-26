### cursor
- default: arrow
- pointer: 小hand
- move: 十字箭头

### outline
- 在border线外围
- 用来突出
- 一般来说都是直接设置为 `outline: 0`


### textarea: resize
- 防止textarea调整大小
- `resize: none`
- 文本域通常设定 `outline: 0; resize: none`


### vertical-align
- 对于**块级元素**无效
- 只针对**行内**或者**行内块**元素有效
- 通常用来控制
  - `图片`**与**`文字`
  - `表单`**与**`文字`的对齐
- **图片和文字默认基线对齐**


### 溢出文字隐藏
- `word-break`: **主要处理英文单词**
  - `normal`: 使用浏览器默认的换行规则
  - `break-all`: 允许在单词内换行
  - `keep-all`: 在单词外换行
- `white-space`: **通常用来在一行内强制显示内容**
  - `normal`: 默认处理方式
  - `nowrap`: 强制在**同一行内**显示所有文本，直到文本结束或者遭遇`br`对象才换行
- `text-overflow`: 溢出文本是否用`...`表示, **前提**: 使用`white-space`为`nowrap`和`overflow`为`hidden`
  - `clip`: 不使用`...`, 简单裁切
  - `ellipsis`: 使用`...`代替溢出文本


### sprite图： 雪碧图
- `描述`: 将很多**小图片**放置到一张**大图**上面,`batch`
- `目的`: **减少请求服务器的次数**
- `对象`: 主要拼接`小`的`背景图片`
- `场景`: **小公司**使用比较少 没必要
- `使用`: 通过`background`来控制
  - `div的width和height`: 控制图片的大小
  - `position: left top`: 来控制起始位置 


### Icon Font字体图标
- `优点`: 体积`小`，`支持各种浏览器`，适配`移动端`
- `使用`: 就像设置`字体`一样设置`图标`，极其酸爽
- `配置`: 需要将`icon`导入到`font-family`中
- Icon Font字体库: [Icofont](https://icofont.com/icons)