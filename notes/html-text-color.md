# 改变文字颜色
在Markdown中，文字的颜色是固定的

但如果想要实现其他颜色的效果，可以使用HTML中的`color`标签：

<span style="color:blue">这是蓝色</span>

<span style="color:#AF6200;">这行字的颜色是#AF6200</span>

## 格式
要想实现这样的效果很简单，首先，需要认识一个HTML的标签：`<span>`

`<span>`是HTML中的一个内联容器标签，你可以用这个标签来设置文字的样式

例如，`<span style="color:#ABCDEF">`便是设置文字的颜色

为了让程序明白我们要设定的文字，我们需要用`</span>`放在文字的后面

整体的格式如下：
```
这是一句话，这句话的部分文字是<span style="color:#10CAFE;">蓝色</span>的
```
输出效果如下：

这是一句话，这句话的部分文字是<span style="color:#10CAFE;">蓝色</span>的

这里的CSS属性：`color`可以为**颜色名称**或是**十六位进制代码**

颜色名称可以在这里查到：[W3C CSS Color Module](https://www.w3.org/TR/css-color-3/)

利用HTML的style属性，还可以使文字变得更有特色，这里不多赘述

## 总结
这张笔记简单介绍了用HTML中的CSS属性`color`修改文字颜色

---
[返回导航页](index.md)