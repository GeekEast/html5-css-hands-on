## 表单
- 为了`收集`用户`信息`而生
- 控件：文本输入框，密码输入框，复选框，提交按钮，重置按钮
- 提示信息：说明性的问题
- 表单域：定义url地址，数据传输方法

### input控件
| 属性      | 属性值     | 描述                                       |
| --------- | ---------- | ------------------------------------------ |
| type      | B1         | 控件类型                                   |
| **name**  | 用户自定义 | 控件分组名称, `给多个单选框设置同一个name` |
| value     | 用户自定义 | 控件内部默认文本值                         |
| size      | 正整数     | 宽度                                       |
| checked   | checked    | 默认被选中的项                             |
| maxlength | 正整数     | 最大字符数                                 |
- type值不同，会有直观的影响

| 属性值   | 描述                              |
| -------- | --------------------------------- |
| text     | 单行文本输入框                    |
| password | 密码输入框                        |
| radio    | 单选按钮                          |
| checkbox | 复选框                            |
| button   | 普通按钮                          |
| submit   | 提交按钮,跟`表单域`相关           |
| reset    | 重置按钮，跟`表单域`相关          |
| image    | 图像形式的提交按钮,跟`表单域`相关 |
| file     | 文件域,跟`表单域`相关             |
- 空格可以用搜狗的全角打出来，神奇！
### label标签
- label标签为input元素定义标注
- 作用：用于绑定一个表达元素，当点击label标签的时候，被绑定的表单元素就会获得输入焦点
- 如何绑定元素呢？
  - for属性规定label与哪个表单元素绑定
```html
<!-- 单个 直接包裹 -->
<label> 密码：<input type="password"></label>
<!-- 多个 for id -->
<label for="female" >单选框： <input type="radio" name="sex" checked="checked"> 男 <input type="radio" name="sex" id='female'> 女</label>
```
### textarea空间(文本域)
- 多行文本
- 很少用cols和rows，用css来控制文本域的高和宽
```html
<textarea cols="每行字符数" rows="每列字符数"></textarea>
```
### 下拉菜单
```html
<select >
        <option selected="selected">请选择</option>
        <option>选项1</option>
        <option>选项2</option>
        <option>选项3</option>
</select>
```
### 表单域
```html
<form action="url地址" method="提交方式" name="表单名称">
    各种表单控件、label
</form>
```