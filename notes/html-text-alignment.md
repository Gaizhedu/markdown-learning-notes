# 文本对齐
在[图片居中](html-image-center.md)这一张笔记中，已经介绍了HTML的一个CSS属性：`text-align`

这个属性可以调整文字，图片的对齐方式

比如说：

<div style="text-align:center">这个句子是居中对齐的</div>

## 文本对齐的格式
文本对齐的格式与图片对其相一致，只需要在`<div>`中，将`text-align`的属性设置成你想要的对齐方式
即可

以下是对齐的方式

```
left：向左对齐
right：向右对齐
center：居中对齐
justify：两端对齐
start：起始对齐
end：结束对齐
match-parent：继承父元素的对齐
```

与图片对齐相同，在用`<div>`时还需要用`</div>`收尾

例如：
```
<div style="text-align:right">这个是向右对齐</div>
```
输出效果如下：

<div style="text-align:right">这个是向右对齐</div>

## 总结
这张笔记是对图片居中对齐的补充，主要介绍了对其功能在文字上的展示

---
[返回导航页](index.md)