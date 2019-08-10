### 标签分类
- 双标签
```html
<body></body>
```
- 单标签
```html
<br/>
```
### 标签关系
- 嵌套关系
- 并列关系

### 字符集
- utf-8: 所有国家全部字符
- gb2312：包括6723个汉字
- BIG5：繁体中文，港澳台专用
- GBK：包含全部中文字符，兼容gb2312

### 标签语义化
- 使得标签名像人类语言，容易读懂

### 常用标签
#### 标题标签
```html
<!-- h1尽量少用，一般留给logo使用 -->
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
```
#### 段落标签
- 用来分段落的
```html
<p>段落</p>
```

#### 水平线标签
- 水平横线用来分搁区域
```html
<hr> 
```

#### 换行标签
```html
<br>
```

#### div span
- div 换行分区
- span 不换行分区

#### 文本格式化标签
- stong em del ins的语义更强烈 会涉及到搜索引擎优化
| 标签                     | 显示效果                |
| ------------------------ | ----------------------- |
| <b></b><strong></strong> | 粗体，XHTML推荐用strong |
| <i></i><em></em>         | 斜体，XHTML推荐用em     |
| <s></s><del></del>       | 删除线,XHTML推荐使用del |
| <u></u><ins></ins>       | 下划线,XHTML推荐使用u   |

#### 图片标签
```html
    <img>
```
- border: 图片边框
- title: 鼠标悬停时显示的问题

#### 链接标签
- target: _self在本窗口中打开，_blank在新页面中打开
- href: #代表空链接，可以暂时设定为#
```html
 <a href="" target=""></a>
```

#### 页内跳转
```html
<a href="#id"></a>
<img id="id">
```


#### base标签
- 统一设置页面内所有`<a>`的target
```html
<head>
    <base target="_blank">
</head>
```

#### 特殊字符

| 特殊字符 | 描述 | 字符代码 |
| -------- | ---- | -------- |
|          | 空格 | `&nbsp;` |

#### 无序列表
- 所有内容都只能放在`<li></li>`里面
```html
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

#### 有序列表
```html
<ol>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ol>
```

#### 自定义列表
- 页面底部经常用
```html
<dl>
    <dt></dt>
    <dd></dd>
    <dd></dd>
    <dd></dd>
</dl>
```

