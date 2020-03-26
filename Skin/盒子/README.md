### 网页布局的本质
- 摆放`Box`的过程

### 盒子模型
- `border`: border-width border-style border-color
- `border-style`(想要出现，必须首先设置为非None):
  - none 忽略宽度啥都没有
  - `solid`: 单实线(最多)
  - `dashed`: 虚线
  - `dotted`: 点线
  - `double`: 双实线

### 圆角边框
- `border-radius`: 左上 右上 右下 左下
- `border-radius`: 左上+右下  右上+左下
- `border-radius`: 左上  右上+左下  右下
- `border-radius`: `宽度/2 = 高度/2` -> Circle

### 盒子水平居中
- `前提条件`：
  - **块级元素**
  - **宽度为正**
- 设定：左右`margin`为`auto`

### 文字水平居中
- `text-align: center`;
- 也可以通过`盒子水平居中`来实现`文字的水平居中`

### 行内元素
- 没有上下margin, **只有左右margin**
- **不要给行内元素制定上下的`内外边距`**

### margin合并
#### 情形：兄弟元素
- 只在**垂直方向**上
- 100px遇到50px最后结果是100px
- 解决方案：**只设置top或者只设置bottom以避免此种情况发生**
#### 情形：父子元素
- 只在**垂直方向**上
- 子元素的margin会被移动到父级元素上，以叠加的方式，而非合并
- 解决方法
  - 1. 为父元素设置1px的border或者1px的padding
  - 2. 为父元素添加`overflow: hidden`(好用一点)

### **box的大小**
- 只有`块级元素`才有`宽度`和`高度`;
- `width`, `height` 单位常用为`px`, `%`代表占父元素的大小;
- `box-sizing`: 默认值为`content-box`;
  - `box-sizing: content-box`: `width`和`height`是属性指向`content`
  - `box-sizing: border-box`: 会让`width`,`height`包含border和padding的大小
  - `box-sizing: padding-box`: 会让`width`,`height`包含padding的大小

### 盒子模型布局稳定性
- 布局使用的优先级
`width > 父元素padding > 子元素margin`
- margin存在`父子边距`**合并**问题；`子border`和`父border`**不合并**
- 父元素`padding` 记得调整父元素`box-sizing`, `content`下`padding`和`border`会撑开盒子, `border`下`padding`和`border`不会撑开盒子
- width: `宽度剩余法`和`高度剩余法`来做即可；

### border-sizing
- content: `size = width + padding + border`
- border:  `padding和border都不撑开盒子` size = width


### 阴影
- 文字阴影
```css
 text-shadow: 10px 3px 3px rgba(0, 0, 0, .5);
```
- 盒子阴影
```css
  box-shadow: 10px 10px 10px rgba(0,0,0,0.5);
  box-shadow: 5px 5px 5px 5px rgba(255,255,255,0.8) inset, 10px 10px 10px 10px rgba(255,255,255,0.9);
```

