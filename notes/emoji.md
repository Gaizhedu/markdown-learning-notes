# emoji
Markdown中支持了多种emoji，除了用直接复制粘贴的方法，还可以用另外的方式实现

例如：:smile:

## emoji的格式
使用的格式相当简单，只需要在两个冒号之间加入特定的emoji名称即可

例如：
```
笑脸：:smile:
100分：:100:
火箭：:rocket:
```
输出效果如下：

笑脸：:smile:

100分：:100:

火箭：:rocket:

一些常见的emoji格式可以在这里面查询到：

[Github的官方API](https://api.github.com/emojis)

使用的方法也很简单，**只需要看引号内部的名称即可**

例如：
```
  "ant": "https://github.githubassets.com/images/icons/emoji/unicode/1f41c.png?v8",
```
以上面这个蚂蚁的emoji为例
你需要看的名称便是里面的 **"ant"**

实际效果如下：

```
这是蚂蚁：:ant:
```
输出效果如下：

这是蚂蚁：:ant:

### 注意
在使用这种短代码插入emoji的时候，需要注意冒号中间的名称必须符合对应的格式，比如说`smile`不能为`Smile`否则不识别

例如：
```
这个是无法识别的笑脸：:Smile:

这个是可以识别的笑脸：:smile:
```
输出效果如下：

这个是无法识别的笑脸：:Smile:

这个是可以识别的笑脸：:smile:

由此，在使用Markdown中的emoji时，需要记得是否符合对应的格式

## 总结
这张笔记主要说明了有关在Markdown中利用短代码插入emoji的方法，同时给出了相应的查询地址 -> [Github的官方API](https://api.github.com/emojis)，以及在使用时的注意事项

---
[返回导航页](index.md)