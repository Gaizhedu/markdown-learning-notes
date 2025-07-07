# 自定义表格
在Markdown中，可以实现简单的表格效果，例如：
```
|表头1|表头2|表头3|
|---|---|---|
|内容1|内容2|内容3|
```

输出效果如下：

|表头1|表头2|表头3|
|---|---|---|
|内容1|内容2|内容3|

如果是简单的表格，可以使用Markdown来实现

但如果是较复杂的表格，则必须要使用HTML中的表格来实现：

<table>
    <thead>
        <tr>
            <th>日期</th>
            <th colspan = "2">学习内容</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Day1</td>
            <td rowspan = "2">数学</td>
            <td>英语单词</td>
        </tr>
        <tr>
            <td>Day2</td>
            <td>英语语法</td>
        </tr>
    </tbody>
</table>

这里是一个较为复杂的表格

## 自定义表格的格式
HTML的自定义表格主要由`<table>`标签来构成
一个完整的表格有以下几部分组成
|标签|功能|
|---|---|
|`<table>`|HTML中表格的最基本形式，是组成表格必不可少的标签|
|`<thead>`|表格的表头部分|
|`<tbody>`|表格的单元格部分|
|`<tr>`|表格的一行内容，每多一个`<tr>`表格便多一行|
|`<th>`|表头的标签，可以用来声明表头|
|`<td>`|单元格的标签，可以用来声明单元格|

完整的结构如下：
``` HTML
<table>
    <!-- 表头 -->
    <thead>
        <tr>
            <th>表头1</th>
            <th>表头2</th>
        </tr>
    </thead>
    <!-- 单元格 -->
    <tbody>
        <tr>
            <td>单元格1</td>
            <td>单元格2</td>
        </tr>
        <tr>
            <td>单元格3</td>
            <td>单元格4</td>
        </tr>
    </tbody>
</table>
```
输出效果如下：

<table>
    <!-- 表头 -->
    <thead>
        <tr>
            <th>表头1</th>
            <th>表头2</th>
        </tr>
    </thead>
    <!-- 单元格 -->
    <tbody>
        <tr>
            <td>单元格1</td>
            <td>单元格2</td>
        </tr>
        <tr>
            <td>单元格3</td>
            <td>单元格4</td>
        </tr>
    </tbody>
</table>

## 表格的属性
在HTML中，若想设置表格的一些属性（例如：颜色，对齐方式），可以对相应内容的属性进行设置

以下是一些常见的属性：
```
style:
    font-size：字体大小
    font-weight：设置文字粗细
    font-style：设置文字风格
    color：设置文字颜色
    text-align：设置水平对齐方式
    text-decoration：设置文字装饰线
    letter-spacing：设置字符间距
    word-spacing：设置单词间距
    text-shadow；设置文字阴影
colspan：跨列合并
rowspan：跨行合并
```

在这里顺便给一个例子，可以参考一下：
``` HTML
<table>
    <thead>
        <tr>
           <th>属性</th>
           <th>效果</th>
           <th>事例</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>font-size</td>
            <td>设置文字大小</td>
            <td style="font-size:10px">这个字体大小是10px</td>
        </tr>
        <tr>
            <td>font-weight</td>
            <td>设置文字粗细</td>
            <td style="font-weight:Bold">这句话的粗细为粗（Bold）</td>
        </tr>
        <tr>
            <td>font-style</td>
            <td>设置文字风格</td>
            <td style="font-style:italic">这句话的文字风格斜体（italic）</td>
        </tr>
        <tr>
            <td>color</td>
            <td>设置文字颜色</td>
            <td style="color:#10CAFE">这句话的文字颜色为 #10CAFE</td>
        </tr>
        <tr>
            <td>text-align</td>
            <td>设置水平对齐方式</td>
            <td style="text-align:right">这句话的水平对齐方式为向右</td>
        </tr>
        <tr>
            <td>text-decoration</td>
            <td>设置文字装饰线</td>
            <td style="text-decoration:underline">这句话的文字装饰线为下划线（underline）</td>
        </tr>
        <tr>
            <td>letter-spacing</td>
            <td>设置字符间距</td>
            <td style="letter-spacing:2px">这句话的字符间隔为2px
            The letter-spacing of this sentence is 2px.
            </td>
        </tr>
        <tr>
            <td>word-spacing</td>
            <td>设置单词间距</td>
            <td style="word-spacing:5px">这句话的单词间隔为5px（注意例句各个单词之间的间距）
            The letter-spacing of this sentence is 5px.
            </td>
        </tr>
        <tr>
            <td>text-shadow</td>
            <td>设置文字阴影</td>
            <td style="text-shadow:1px 2px 3px rgba(0,0,0,255)">这句话现在带有文字阴影
            （各个参数代表的含义分别为：水平偏移，垂直偏移，模糊半径，阴影颜色）
            </td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <td>colspan</td>
            <td colspan="2">跨列合并</td>
        </tr>
        <tr>
            <td rowspan="2">rowspan</td>
            <td>第一列</td>
            <td rowspan="2">跨行合并</td>
        </tr>
        <tr>
            <td>第二列</td>
        </tr>
    </tbody>
</table>
```

输出效果如下：
<table>
    <thead>
        <tr>
           <th>属性</th>
           <th>效果</th>
           <th>事例</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>font-size</td>
            <td>设置文字大小</td>
            <td style="font-size:10px">这个字体大小是10px</td>
        </tr>
        <tr>
            <td>font-weight</td>
            <td>设置文字粗细</td>
            <td style="font-weight:Bold">这句话的粗细为粗（Bold）</td>
        </tr>
        <tr>
            <td>font-style</td>
            <td>设置文字风格</td>
            <td style="font-style:italic">这句话的文字风格斜体（italic）</td>
        </tr>
        <tr>
            <td>color</td>
            <td>设置文字颜色</td>
            <td style="color:#10CAFE">这句话的文字颜色为 #10CAFE</td>
        </tr>
        <tr>
            <td>text-align</td>
            <td>设置水平对齐方式</td>
            <td style="text-align:right">这句话的水平对齐方式为向右</td>
        </tr>
        <tr>
            <td>text-decoration</td>
            <td>设置文字装饰线</td>
            <td style="text-decoration:underline">这句话的文字装饰线为下划线（underline）</td>
        </tr>
        <tr>
            <td>letter-spacing</td>
            <td>设置字符间距</td>
            <td style="letter-spacing:2px">这句话的字符间隔为2px
            The letter-spacing of this sentence is 2px.
            </td>
        </tr>
        <tr>
            <td>word-spacing</td>
            <td>设置单词间距</td>
            <td style="word-spacing:5px">这句话的单词间隔为5px（注意例句各个单词之间的间距）
            The letter-spacing of this sentence is 5px.
            </td>
        </tr>
        <tr>
            <td>text-shadow</td>
            <td>设置文字阴影</td>
            <td style="text-shadow:1px 2px 3px rgba(0,0,0,255)">这句话现在带有文字阴影
            （各个参数代表的含义分别为：水平偏移，垂直偏移，模糊半径，阴影颜色）
            </td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <td>colspan</td>
            <td colspan="2">跨列合并</td>
        </tr>
        <tr>
            <td rowspan="2">rowspan</td>
            <td>第一列</td>
            <td rowspan="2">跨行合并</td>
        </tr>
        <tr>
            <td>第二列</td>
        </tr>
    </tbody>
</table>

### 注意
在HTML中，表格的跨行合并与跨列合并和文本的属性是并列关系，也就是说这三者是不同的属性

而类似文本颜色，对齐方式这种，都归属于`style`

此外，若想在`style`属性里面同时使用多个属性，每个属性之间要用`;`隔开

而像跨行合并这一类则需要用空格隔开

实际例子如下：

``` HTML
<table>
    <thead>
        <tr>
            <th>示例表头1</th>
            <!-- 可以看到，这里colspan与style中间用了空格隔开 -->
            <th colspan="2" style="color:skyblue">示例表头2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>示例单元格1</td>
            <!-- 可以看到，这里rowspan与style中间用了空格隔开 -->
             <!-- 而style中的text-decoration与color之间用了;隔开 -->
            <td rowspan="2" style="text-decoration:underline;color:#12CAFE">示例单元格2</td>
            <td>示例单元格3</td>
        </tr>
        <tr>
            <td>示例单元格4</td>
            <td>示例单元格5</td>
        </tr>
    </tbody>
</table>
```
输出效果如下：


<table>
    <thead>
        <tr>
            <th>示例表头1</th>
            <!-- 可以看到，这里colspan与style中间用了空格隔开 -->
            <th colspan="2" style="color:skyblue">示例表头2</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>示例单元格1</td>
            <!-- 可以看到，这里rowspan与style中间用了空格隔开 -->
             <!-- 而style中的text-decoration与color之间用了;隔开 -->
            <td rowspan="2" style="text-decoration:underline;color:#12CAFE">示例单元格2</td>
            <td>示例单元格3</td>
        </tr>
        <tr>
            <td>示例单元格4</td>
            <td>示例单元格5</td>
        </tr>
    </tbody>
</table>

## 总结
这张笔记主要介绍了HTML中自定义表格的格式，以及一些文本属性的设置方法，弥补了Markdown中表格功能过于简单的问题

---
[返回导航页](index.md)