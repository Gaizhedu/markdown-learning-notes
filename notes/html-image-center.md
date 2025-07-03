# 图片居中
在Markdown中，你可以使用[图片链接](links-images.md)来嵌入一张图片

格式为：
```
![文本](链接+鼠标放上时显示的文字)
```

![示例图片](assets/004.jpg)

此时我们可以发现，这张图片是居中设置的

<div style="text-align:left">
  <img src=assets/004.jpg alt="麦田">
</div>

但此时可以看到，第二张图片是向左对齐的

这便实现了Markdown无法实现的功能

## 设置图片对齐的格式
为了实现这个效果，可以使用HTML中的`text-align`标签

格式如下：
``` HTML
<div style="text-align:left">
  <img src=图片链接 alt="图片描述">
</div>
```

输出效果如上：

接下来来解释这个格式：

这个格式大致可以分为两部分：
第一部分是
``` HTML
<div>

</div>
```

第二部分是中间的
``` HTML
  <img src=图片链接 alt="图片描述">
```

先从第一部分讲起：

第一部分的`<div>`可以理解为一个块的**开始和结束**，相当于代码块中的` ``` `

其中不带斜杠的是开头（`<div>`），前面带斜杠的是结尾（`</div>`）

为了实现对其的效果，需要在开始的那个`<div>`里面加入对齐的标签：`text-align`，同时还要告诉它这是什么：
```
<div style="text-align:left">
```

但只有标签可不行，还要告诉它说对齐的方向：

对齐的方向有这几种：
```
left：向左对齐
right：向右对齐
center：居中对齐
justify：两端对齐
start：起始对齐
end：结束对齐
match-parent：继承父元素的对齐
```

例子：

``` HTML
<div style="text-align:left">
 <img src=assets/005.jpg alt="粉红色的天">
</div>
```

输出效果如下：

<div style="text-align:left">
 <img src=assets/005.jpg alt="粉红色的天">
</div>

其他格式同理

## 总结
这张笔记主要介绍了HTML中将图片对其的方式，并简单介绍了一下有关`<div>`的内容，以及嵌入图片的格式`<img scr="链接" alt="名称">`

---
[返回导航页](index.md)