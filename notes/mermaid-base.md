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

# 各类图表
## Mermaid
Mermaid 是Markdown的一类流程图的类型，允许用户通过简单的文本语法来创建各种类型的图表，如流程图、时序图、甘特图、类图等，使得自己的文档变得更加美观

- [ ] [flowchart-流程图](mermaid-flowchart.md)
