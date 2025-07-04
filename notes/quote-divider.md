# 引用与分割线
在Markdown中你可以通过引用和分割线来优化排版

## 引用
在Markdown中，若需要引用内容，可以使用Markdown的引用功能

具体如下：
> 这是引用的内容

实现的方法也很简单，只需要在引用的文本前加上`>`即可
例如：
```
> 我将引用这个内容
```
输出效果如下：
> 我将引用这个内容

此外，如果你想引用多层内容，可以在`>`后面添加多几个`>`形成嵌套引用

```
> 这是第一层引用
>> 这是第二层引用
>>> 这是第三层引用
```
输出效果如下：

> 这是第一层引用
>> 这是第二层引用
>>> 这是第三层引用

### 注意
在使用引用时，不能在一个句子中间引用

例如：
```
我想引用的内容是这个：> 引用文本

我想引用的内容是这个：

> 引用内容
```
输出效果如下：

我想引用的内容是这个：> 引用文本

我想引用的内容是这个：

> 引用内容

我们可以看到，在第一个例子中，引用的内容处于句子内，导致其无法识别

而第二个例子将`>`放在新的一行，则可以正确识别

---
## 分割线
在Markdown中，你可以添加分割线来隔开文本

例如：

---
如上，这是一条分割线

实现的方法也很简单，只需要在任意一行添加`---或***`

```
---
```
输出效果如下：

---

### 注意
在使用分割线时，要注意分割线的符号要一致，比如说统一使用`*或_`

此外，在使用分割线时，你需要在分割线的前一行换行，否则无法识别

如果没有换行而是直接挨着短横线`-`的话，则会触发Markdown的Setext格式，将你的文本转换成二级标题

就像下面这样：
```
这是个二级标题
---
```
输出如下：

这是个二级标题
---

可以看到，原本的分割线变成了二级标题，因为符合Markdown中Setext的格式

---
[返回导航页](index.md)