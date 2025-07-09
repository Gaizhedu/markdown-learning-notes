# 流程图与图表
在Markdown中，你可以插入一张图表来优化自己的表达，使得排版更加美观

例如：
```Mermaid
flowchart TD
    A[开始] --> B((条件判断))
    B --> |是| C[处理流程1]
    B --> |否| D[处理流程2]
    C --> E[结束]
    D --> E
```

# 流程图的格式
## Mermaid
Mermaid 是Markdown的一类流程图的类型，允许用户通过简单的文本语法来创建各种类型的图表，如流程图、时序图、甘特图、类图等，使得自己的文档变得更加美观

### 流程图（flowchart）
以下是一个最基本的Mermaid流程图
````
``` MerMaid
flowchart LR
A[开始] --> B[结束]
```
````

输出效果如下：

``` Mermaid
flowchart LR
A[开始] --> B[结束]
```

接下来开始介绍一下各个部分

首先，流程图的代码部分是被包裹在**代码块**里面的，并且还要声明语言
比如说：
````
``` Mermaid
```
````
在上面这个流程图框架中，声明了使用的流程图为Mermaid，这时Markdown会将代码块内的内容按照Mermaid的格式输出（若格式正确）

#### 流程图方向
接下来，一个流程图还需要告诉读者阅读方向，可以在第一个` ``` `的下一行加入`flowchart`来说明流程图的方向

常见的顺序如下：

<table>
    <thead>
        <tr>
            <th>名称</th>
            <th>作用</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align:center">TD</td>
            <td>TD（Top-Down），也就是<strong>从上到下</strong>的方向，这是默认的方向，若不设置则自动为该方向</td>  
        </tr>
        <tr>
            <td style="text-align:center">BT</td>
            <td>BT（Bottom-Top），也就是<strong>从下到上</strong>的方向</td>  
        </tr>
        <tr>
            <td style="text-align:center">LR</td>
            <td>LR（Left-Right），也就是<strong>从左到右</strong>的方向</td>  
        </tr>
        <tr>
            <td style="text-align:center">RL</td>
            <td>RL（Right-Left），也就是<strong>从右到左</strong>的方向</td>  
        </tr>
    </tbody>
</table>

在使用时，只需要在`flowchart`后面加上对应的方向名称即可即可

例如：

````
``` Mermaid
flowchart LR
```
````

#### 流程图主体部分
在介绍完基本的框架之后，接下来是流程图的主体部分

流程图可以简单介绍为这样
从 A 到 B
也就是`A --> B`
若想给A和B添加名称，则只需要在后面用一定的格式括起来即可，这里以默认的格式来说明

还是以上面的例子为例，若想要实现从开始到结束的效果，只需要在A和B后面用方括号将名称括起来即可

````
``` Mermaid
flowchart LR
A[开始] --> B[结束]
```
````

输出效果如下：
``` Mermaid
flowchart LR
A[开始] --> B[结束]
```

这里方括号里面的内容就是表格中矩形显示的文字

##### 节点格式
除了方括号，还有以下格式

<table>
    <thead>
        <tr>
            <th>符号</th>
            <th>节点名称</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>[]</td>
            <td>矩形（默认格式）</td>
        </tr>
        <tr>
            <td>()</td>
            <td>圆角矩形</td>
        </tr>
        <tr>
            <td>{}</td>
            <td>菱形（判断）</td>
        </tr>
        <tr>
            <td>(())</td>
            <td>圆形</td>
        </tr>
    </tbody>
</table>

具体效果如下
``` Mermaid
flowchart TD
    A[节点形状] --> B[矩形]
    A --> C(圆角矩形)
    A --> D{菱形}
    A --> E((圆形))
    A --> F>形状不对称节点]
```

##### 节点连接
若你想连接各个节点，常用的方式是使用`-->`，但如果不想用箭头，你还可以使用以下格式
<table>
    <thead>
        <tr>
            <th>符号</th>
            <th>作用</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>---</td>
            <td>无箭头实线</td>
        </tr>
        <tr>
            <td>--文本--</td>
            <td>无箭头带文本实线</td>
        </tr>
        <tr>
            <td>--></td>
            <td>有箭头实线</td>
        </tr>
        <tr>
            <td>--文字--></td>
            <td>有箭头带文本的实线</td>
        </tr>
        <tr>
            <td>===</td>
            <td>无箭头的粗实线</td>
        </tr>
        <tr>
            <td>==文本==</td>
            <td>无箭头带文本的粗实线</td>
        </tr>
        <tr>
            <td>==></td>
            <td>有箭头的粗实线</td>
        </tr>
        <tr>
            <td>==文本==></td>
            <td>有箭头带文本的粗实线</td>
        </tr>
        <tr>
            <td>-.-</td>
            <td>无箭头虚线</td>
        </tr>
        <tr>
            <td>-.文本.-</td>
            <td>无箭头带文本虚线</td>
        </tr>
        <tr>
            <td>-.-></td>
            <td>有箭头虚线</td>
        </tr>
        <tr>
            <td>-.文本.-></td>
            <td>有箭头带文本虚线</td>
        </tr>
        <tr>
            <td>~~~</td>
            <td>看不见的连接</td>
        </tr>
    </tbody>
</table>

##### 修改文字大小，背景填充等样式