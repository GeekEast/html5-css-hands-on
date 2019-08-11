## 认识浏览器
- **Chrome**
- Firefox
- Safari
- Opera
- Edge
- IE(淘汰)

### 浏览器内核（面试用）
- 分为两部分Rendering Engine and JS Engine
- 这里主要说的是Rendering Engine

| 浏览器         | 内核    |
| -------------- | ------- |
| IE/windows     | Trident |
| Firefox        | Gecko   |
| Safari/ios     | webkit  |
| Chrome/Android | blink   |
| Opera          | blink   |

### Web标准（重点）
- 不同的浏览器，渲染结果不一致.

#### 构成
- 不是一个标准，而是一套标准, 主要包括结构(structure)，表现(Presentation)和行为(Behavior)三个方面。


| 方面 | 描述                 | 内容              |
| ---- | -------------------- | ----------------- |
| 结构 | 网页元素的整理和分类 | XML, `XHTML`      |
| 表现 | 颜色大小等外观样式   | `CSS`             |
| 行为 | 网页模型定义及交互   | DOM, `ECMAScript` |
