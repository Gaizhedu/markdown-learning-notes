# 流程图（flowchart）
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

首先，流程图的代码部分是被包裹在**代码块**里面的，并且还要声明语言为`Mermaid`
比如说：
````
``` Mermaid
```
````
在上面这个流程图框架中，声明了使用的图表为Mermaid，这时Markdown会将代码块内的内容按照Mermaid的格式输出（若格式正确）

## 流程图方向
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

在使用时，只需要在`flowchart`后面加上对应的方向名称即可即可，这里若不添加，则为默认的**TD（从上到下）**，可以选择不填，但是一定要有`flowchart`

例如：

````
``` Mermaid
flowchart LR
```
````

## 流程图主体部分
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

### 节点格式
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

此外，还有一些格式，由于篇幅问题放在了文章最后面

可以点击这个链接直达->[其他节点格式](#other-nodes)

### 节点连接
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
            <td>--o</td>
            <td>圆形箭头</td>
        </tr>
        <tr>
            <td>--文本--o</td>
            <td>带文本的圆形箭头</td>
        </tr>
        <tr>
            <td>--x</td>
            <td>交叉箭头</td>
        </tr>
        <tr>
            <td>--文本--x</td>
            <td>带文本的交叉箭头</td>
        </tr>
        <tr>
            <td>~~~</td>
            <td>看不见的连接</td>
        </tr>
    </tbody>
</table>

此外，你还可以使用双向连接来连接两部分内容
<table>
    <thead>
        <tr>
            <th>符号</th>
            <th>作用</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><--></td>
            <td>双向实线箭头</td>
        </tr>
        <tr>
            <td><--文字--></td>
            <td>有文本的双向实线箭头</td>
        </tr>
        <tr>
            <td><==></td>
            <td>双向粗实线箭头</td>
        </tr>
        <tr>
            <td><==文本==></td>
            <td>有文本的双向粗实线箭头</td>
        </tr>
        <tr>
            <td><-.-></td>
            <td>双向虚线箭头</td>
        </tr>
        <tr>
            <td><-.文本.-></td>
            <td>有文本的双向虚线箭头</td>
        </tr>
        <tr>
            <td>o--o</td>
            <td>双向圆形箭头</td>
        </tr>
        <tr>
            <td>o--文本--o</td>
            <td>有文本的双向圆形箭头</td>
        </tr>
        <tr>
            <td>x--x</td>
            <td>双向交叉箭头</td>
        </tr>
        <tr>
            <td>x--文本--x</td>
            <td>有文本的双向交叉箭头</td>
        </tr>
    </tbody>
</table>

#### 增加你链接的长度
若想要在两个节点之间的连接长度变得更长，可以增加中间的连接号数量，例如

````
``` Mermaid
flowchart LR
A[开始] --长度（默认）--> B[结束]
```


``` Mermaid
flowchart LR
A[开始] --长度（增加两个连接号）----> B[结束]
```
````

输出效果如下：

``` Mermaid
flowchart LR
A[开始] --长度（默认）--> B[结束]
```


``` Mermaid
flowchart LR
A[开始] --长度（增加两个连接号）----> B[结束]
```

**这里需要注意的一点是**，当你的连接是带文本的连接时，连接号需要加在文本的右边，也就是靠近箭头的一侧

### 添加ID
要想给流程图里面的边（也就是每个节点）添加ID，可以在每个流程的连接前添加`[ID]@`

例如：
````
``` Mermaid
flowchart LR
    A n1@--> B
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A n1@--> B
```

有了ID之后，便可以给边（节点）添加一些样式了

### 添加动画
在给节点分配ID之后，便可以为节点之间的连接添加一些动画

具体的实现方法是，在分配完ID后，再另起一行输入：`id名称@{animate: true}`

这里注意，冒号与`true`之间必须要有一个空格隔开

下面给出示例：
````
``` Mermaid
flowchart LR
    A n1@--> B
    n1@{animate: true}   
```
````

#### 对动画的各个细节进行调整
添加完动画后，还可以对动画的一些细节进行调整，比如说速度，线条粗细之类的

##### 动画速度
若想要调节动画的速度，可以使用`animation`属性来调节速度大小，以下给出两种不同速度的大小
``` Mermaid
flowchart TD
    subgraph slow
        A1[start] s1@--> B1[end]
        s1@{animate: true, animation: slow}
    end
    subgraph fast
        A2[start] s2@--> B2[end]
        s2@{animate: true, animation: fast}
    end 
```
`animation`支持的值有`fast`和`slow`，具体对比效果可以参照上面

具体的代码在这里：
````
``` Mermaid
flowchart TD
    subgraph slow
        A1[start] s1@--> B1[end]
        s1@{animate: true, animation: slow}
    end
    subgraph fast
        A2[start] s2@--> B2[end]
        s2@{animate: true, animation: fast}
    end 
```
````
若你想自由的调节速度，可以使用这个，`animation: dash + 时间 + 是否匀速 + 是否循环`

具体的细则可以看下面这个表格
<table>
    <thead>
        <tr>
            <th>属性名称</th>
            <th>值</th>
            <th>作用</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>时间</td>
            <td>数字 + s</td>
            <td>每个循环所使用的时间，如1s则单个循环为1s</td>
        </tr>
        <tr>
            <td rowspan = "5">是否匀速</td>
            <td>linear</td>
            <td>动画运动速度为<strong>匀速</strong></td>
        </tr>
        <tr>
            <td>ease</td>
            <td>变速运动，变速规律为<strong>慢 -> 快 -> 慢</strong></td>
        </tr>
        <tr>
            <td>ease-in</td>
            <td>变速运动，变速规律为<strong>慢 -> 快</strong></td>
        </tr>
        <tr>
            <td>ease-out</td>
            <td>变速运动，变速规律为<strong>快 -> 慢</strong></td>
        </tr>
        <tr>
            <td>ease-in-out</td>
            <td>变速运动，变速规律为<strong>开始和结束慢，中间快</strong></td>
        </tr>
        <tr>
            <td rowspan = "2">是否循环</td>
            <td>infinite</td>
            <td>无限循环播放</td>
        </tr>
        <tr>
            <td>数字</td>
            <td>循环n次，n为数字大小</td>
        </tr>
    </tbody>
</table>

##### 动画样式
除了调整动画的速度，还可以调整动画的各种样式，如线条颜色，长短等

以下是一个具体例子，在这个例子中，线条的颜色和粗细都发生了改变

``` Mermaid
flowchart LR
    A[Start] n1@--> B[End]
    classDef color1 stroke: #10CAFE, stroke-width: 5px;
    class n1 color1
```
常见的属性如下：
<table>
    <thead>
        <tr>
            <th>类别</th>
            <th>属性</th>
            <th>作用</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan = "6">节点属性</td>
            <td>fill</td>
            <td>为节点填充颜色</td>
        </tr>
        <tr>
            <td>stroke</td>
            <td>改变节点的边框颜色</td>
        </tr>
        <tr>
            <td>stroke-width</td>
            <td>节点边框的像素厚度</td>
        </tr>
        <tr>
            <td>class</td>
            <td>使用类</td>
        </tr>
        <tr>
            <td>shape</td>
            <td>节点的形状</td>
        </tr>
        <tr>
            <td>style</td>
            <td>自定义CSS类型</td>
        </tr>
        <tr>
            <td rowspan = "6">连接属性</td>
            <td>stroke</td>
            <td>连接线颜色</td>
        </tr>
        <tr>
            <td>stroke-width</td>
            <td>连接线宽度</td>
        </tr>
        <tr>
            <td>stroke-dasharray</td>
            <td>连接线为虚线（可以调整参数）</td>
        </tr>
        <tr>
            <td>arrowhead-end</td>
            <td>箭头样式</td>
        </tr>
        <tr>
            <td>label</td>
            <td>连接线上的文本</td>
        </tr>
        <tr>
            <td>linkStyle</td>
            <td>批量设置连接线的样式</td>
        </tr>
        <tr>
            <td rowspan = "3">动画属性</td>
            <td>animate</td>
            <td>启用连接线动画</td>
        </tr>
        <tr>
            <td>animation</td>
            <td>控制动画速度</td>
        </tr>
        <tr>
            <td>click</td>
            <td>点击事件（要绑定JavaScript函数）</td>
        </tr>
    </tbody>
</table>

接下来来详细介绍每个属性

###### fill
例子：
````
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A fill: #10CAFE
```
````
输出效果如下：

``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A fill: #10CAFE
```
这里的`style A fill: #10CAFE`是后面的`style`的内容，可以先跳到这个部分

###### stroke
`stroke`可以用在节点，或者用在连接上，这里两者全部展示，后面便不再重复说明
````
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A stroke: #10CAFE
    C[start] e1@--> D[end]
    classDef e1_c stroke: #10CAFE
    class e1 e1_c
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A stroke: #10CAFE
    C[start] e1@--> D[end]
    classDef e1_c stroke: #10CAFE
    class e1 e1_c
```

###### stroke-width
与上文的`stroke`一致，这里同样演示该属性在节点和连接上的应用，下文节点属性处便不再演示
````
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A stroke-width: 5px
    C[start] e1@--> D[end]
    classDef e1_c stroke-width: 5px
    class e1 e1_c
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A stroke-width: 5px
    C[start] e1@--> D[end]
    classDef e1_c stroke-width: 5px
    class e1 e1_c
```

可以明显的观察到边框和连接变粗了

###### class
使用类（class）可以为节点批量分配属性：
````
``` Mermaid
flowchart LR
    A[start] --> B[end]
    classDef n1 fill:#12CAFE, stroke-width:5px;
    class A e1_c
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start] --> B[end]
    classDef n1 fill:#12CAFE, stroke-width:5px;
    class A n1
```
这里简单介绍一下：`classDef`是创建一个类，接下来跟着的`n1`是这个类的名字，后面跟着的是这个类的属性

接下来要将这个类分配给对应的地方，需要用到`class`，比如说这里要分配给 节点A ，则写作`class A n1`
这里A就是对应的节点名称，后面的`n1`就是对应的类的名称

此外，除了用`class`分配外，还可以用另一种方法，也就是`:::`
````
``` Mermaid
flowchart LR
    A[start]:::n1 --> B[end]
    classDef n1 fill:#12CAFE,stroke-width:5px
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start]:::n1 --> B[end]
    classDef n1 fill:#12CAFE,stroke-width:5px
```
节点后面的`:::`后面跟着的是类的名称，其他创建类的方法跟上面是一致的

###### shape
利用`shape`可以改变你的节点形状，这里简单举几个例子，其他例子可在文章末尾看到

这里需要另外注意的一点是，使用`shape`需要用到一种新的语法
````
``` Mermaid
flowchart LR
    A[start]@{shape: cyl} --> B[end]
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start]@{shape: cyl} --> B[end]
```
格式如下：
在原本的节点后面加上`@{shape: 形状}`，**这里需要注意的是，冒号与后面的形状的ID之间需要用空格隔开**

此外，如果想要更加简洁的话，可以将原本节点中的文本样式删去，改为在花括号中添加`label`标签

例如：
````
``` Mermaid
flowchart LR
    A@{shape: cyl, label: "start"} --> B[end]
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A@{shape: cyl, label: "start"} --> B[end]
```
这里`label`的内容对应的就是原先方括号中的文本

###### style
在Mermaid中，你还可用用`style`为节点添加CSS属性
例如：
````
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A fill:#10CAFE
```
````
输出效果如下：
``` Mermaid
flowchart LR
    A[start] --> B[end]
    style A fill:#10CAFE
```
这里`style`后面跟着的就是节点的ID，取决于你想修改哪个节点的属性，ID后面跟着的是CSS属性

### 子图
``` Mermaid
flowchart TD
    subgraph project_1
    A[start] --> B[end]
    end
    subgraph project_2
    C[start] --> D[end]
    end
    B --> C
    A --> D
```
上面是一个子图的实例，可以看到整个流程图被分为两个部分，一个是`project 1`另一个是`project 2`，接下来来讲讲具体格式

首先，为了实现子图的效果，需要认识一个新的容器组件：`subgraph`


具体的格式如下：
````
``` Mermaid
flowchart TD
    subgraph graph_name1
    A --> B
    end
```
````
输出效果如下：
``` Mermaid
flowchart TD
    subgraph graph_name1
    A --> B
    end
```
可以看到，在`subgraph`后面跟着的是组的名称，而后在下一行输入这个组内的流程，最后用`end`结束这个组的分配

TODO ID分配

### 修改文字大小，背景填充等样式
TODO

### 其他节点 {#other-nodes}
TODO