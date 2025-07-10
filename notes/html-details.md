# 可折叠内容
在Markdown中，当需要添加一个可以折叠的内容时，会发现到Markdown中并没有对应的功能

这时候若想要实现对应的功能可以使用HTML中的标签来实现这一功能

例如：
<details>
    <summary>点击展开折叠内容</summary>
    <div>
    这是折叠内容
    </div>
</details>

## 折叠内容的格式
想要在Markdown中实现这种效果，我们可以使用HTML中的`<details>`标签

这个标签的使用格式如下：

```
<details>
    <summary>
        这里是标题，点击展开折叠内容
    </summary>
    <div>
        这里是折叠掉的内容
    </div>
<details>
```

输出效果如下：

<details>
    <summary>
        这里是标题，点击展开折叠内容
    </summary>
    <div>
        这里是折叠掉的内容
    </div>
</details>

简单说明一下各个部分的作用，首先是最重要的`<details>`标签，使用这个标签相当于跟浏览器说：我下面的内容是可以折叠的

而接下来的`<summary>`则是折叠区域的**标题**，相当于告诉浏览器说：我这个折叠区域的标题是什么

最后的`<div>`则是折叠部分的详细内容，效果相当于告诉浏览器折叠区域的内容是什么，**注意**：这里如果不填`<div>`直接写内容其实也可以，但用`<div>`会更加美观

若要将折叠内容嵌套，其实也可以。以下是实例：

``` HTML
<details>
    <summary>
        这是第一层的标题
    </summary>
    这是第一层的内容，注意这里没有加&lt;div&gt;，但依旧可以识别
    <details>
        <summary>
            这是第二层标题
        </summary>
        <div>
            这是第二层的内容
        </div>
    </details>
</details>
```

输出效果如下：

<details>
    <summary>
        这是第一层的标题
    </summary>
    这是第一层的内容，注意这里没有加&lt;div&gt;，但依旧可以识别
    <details>
        <summary>
            这是第二层标题
        </summary>
        <div>
            这是第二层的内容
        </div>
    </details>
</details>

> 注：这里的`&lt;`和`&gt;`是HTML中的转义符号，对应`<`和`>`

## 总结
这张笔记主要介绍了HTML中的可折叠内容，弥补了Markdown中无法实现这一功能的缺陷

主要介绍了两个标签：`<details>`和`<summary>`

---
[返回导航页](index.md)