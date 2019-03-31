[TOC]

# JS 点击事件在 iOS 中失效的解决方案

iOS 中不允许将点击事件绑定在 document 或者 body 上，如果绑定上的话将会失效。
例如：
```
$(document).on('click', '#el', function() {}) //无效
```

**解决方案：**

1. 使用元素的父标签代替 document 或 body
```
$('任意的 #el 的父元素').on('click', '#el', function() {})
```

2. 点击元素用 button 代替

3. 在点击元素上增加 CSS 样式`cursor: pointer;`