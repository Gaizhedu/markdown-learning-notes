# 代码块
代码块是一种用于显示文本内容的工具，你可以代码块里面直观的显示代码
例如：
```python
print("Hello World!")
```
相较于直接显示代码，使用代码块会更加直观
## 代码块的格式
代码块有两种格式，一种是**围栏代码块**，另一种是**缩进代码块**

### 围栏代码块
围栏代码块的实现方法很简单，只需要用三个反引号(\```)包裹代码即可实现；

````
``` 
print("Hello World！") 
```
````
输出：
```
print("Hello World！") 
```
#### 注意
你可能发现了，在一开始演示的代码块中代码是有颜色的，而若想要实现这个效果，只需要在第一个` ``` `后添加指定的语言即可
例如：

````
``` python
print("Hello World！")
```
````

输出：
``` python
print("Hello World！")
```
---
如果你想要在围栏代码块里面说明围栏代码块的格式，需要使用四个反引号\````来包裹三个反引号
例如：
`````
````
```
需要用到四个反引号，并且如果还需要继续显示（如这里的四个反引号）则需要5个反引号
```
````
`````
输出：
````
```
需要用到四个反引号，并且如果还需要继续显示（如这里的四个反引号）则需要5个反引号
```
````

---
### 缩进代码块
缩进代码块也是一种可以直接显示代码的方式

    > 这是缩进代码块
    print("Hello World！")

实现缩进代码块的方式也很简单，只需要先缩进一次后再输入内容即可
```
    > 缩进一次即可实现缩进代码块的功能
```
输出如下：

    > 缩进一次即可实现缩进代码块的功能
#### 注意
如果想要实现缩进代码块的效果，则缩进代码块的前一行需要换行
若没有换行，则会使得**换行失效**，也就无法实现缩进代码块的效果
```
    这里没有换行
    变成了一个普通的段落
```
输出效果：
    这里没有换行
    变成了一个普通的段落
```

    这里换行了
    也就实现了缩进代码块
```
输出效果：

    这里换行了
    也就实现了缩进代码块

---
### 显示代码
如果你只是想在一句话中插入代码，或者Markdown的格式，你可以将你想要显示的内容放入\` \`中，例如`# 这个是标题`或`print("Hello World！") `

--- 
[返回导航页](index.md)
