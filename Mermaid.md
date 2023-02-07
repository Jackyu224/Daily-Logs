## 图标类型

### 流程图

所有流程图均由**节点**、**几何形状**和**边**、**箭头**或**线**组成。

> **重要说明**：不要键入“结束”一词作为流程图节点。将所有或任何一个字母大写以防止流程图中断，即“End”或“END”。

``` java
graph TD
	A-->B;
	A-->C;
	B-->D;
	C-->D;
```

``` mermaid
graph TD
	A-->B;
	A-->C;
	B-->D;
	C-->D;
```





#### 带有文本的节点

``` java
---
title: Node with text
---
flowchart LR
    id1[This is the text in the box]

```

``` mermaid
---
title: Node with text
---
flowchart LR
    id1[This is the text in the box]

```





#### 图形

声明了流程图的方向,从上到下（`TD`或`TB`）。从左到右 ( `LR`)。

``` 
flowchart LR
    Start --> Stop
```

``` mermaid
flowchart LR
    Start --> Stop
```

#### 流程图方向

可能的流程图方向是：

**- TB——从上到下**
**- TD - 自上而下/与自上而下相同**
**- BT-- 从下到上**
**- RL——从右到左**
**- LR——从左到右**



#### 方框形状

##### 圆边

``` java
flowchart LR
    id1(This is the text in the box)
```

``` mermaid
flowchart LR
    id1(This is the text in the box)

```

##### 操场形状

``` java
flowchart LR
    id1([This is the text in the box])
```

``` mermaid
flowchart LR
    id1([This is the text in the box])

```

#####  子程序形状

```java 
flowchart LR
    id1[[This is the text in the box]]

```

``` mermaid
flowchart LR
    id1[[This is the text in the box]]

```

##### 圆柱

``` java 
flowchart LR
    id1[(Database)]

```

``` mermaid
flowchart LR
    id1[(Database)]

```

##### 圆圈

```java
flowchart LR
    id1((This is the text in the circle))

```

``` mermaid
flowchart LR
    id1((This is the text in the circle))

```

##### 不对称

``` java
flowchart LR
    id1>This is the text in the box]

```

``` mermaid
flowchart LR
    id1>This is the text in the box]

```

##### 菱形

``` java
flowchart LR
    id1{This is the text in the box}

```

``` mermaid
flowchart LR
    id1{This is the text in the box}

```

##### 六边形

``` java
flowchart LR
    id1{{This is the text in the box}}

```

``` mermaid
flowchart LR
    id1{{This is the text in the box}}

```

##### 平行四边形

``` java
flowchart TD
    id1[/This is the text in the box/]
```

``` mermaid
flowchart TD
    id1[/This is the text in the box/]
    
```

##### Alt 平行四边形

``` java
flowchart TD
    id1[\This is the text in the box\]

```

``` mermaid
flowchart TD
    id1[\This is the text in the box\]

```

##### 梯形

``` java
flowchart TD
    A[/Christmas\]

```

``` mermaid
flowchart TD
    A[/Christmas\]

```

##### Alt 梯形

``` java
flowchart TD
    B[\Go shopping/]

```

``` mermaid
flowchart TD
    B[\Go shopping/]

```

##### 双圈

``` java
flowchart TD
    id1(((This is the text in the circle)))

```

``` mermaid
flowchart TD
    id1(((This is the text in the circle)))

```

#### 边框之间的连接

##### 带箭头的链接

``` java
flowchart LR
    A-->B

```

``` mermaid
flowchart LR
    A-->B

```

##### 没有箭头的连接

``` java
flowchart LR
    A --- B

```

``` mermaid
flowchart LR
    A --- B

```

##### 带文本的连接

``` java
flowchart LR
    A-- This is the text! ---B
    C---|This is the text|D
    E-->|text|F
    G-- text -->H
    
```

``` mermaid
flowchart LR
    A-- This is the text! ---B
    C---|This is the text|D
    E-->|text|F
    G-- text -->H
    
```

##### 虚线连接

``` java
flowchart LR
   A-.->B;

```

``` mermaid
flowchart LR
   A-.->B;

```

##### 带文本的虚线链接

```java
flowchart LR
    A-. text .-> B
    A ==> B
    A == text ==> B
    
```

``` mermaid
flowchart LR
    A-. text .-> B
    C ==> D
    E == text ==> F
    
```

##### 多个连接

可以在**同一行**中声明多个链接

``` java
flowchart LR
   A -- text --> B -- text2 --> C

```

``` mermaid
flowchart LR
   A -- text --> B -- text2 --> C

```

可以在同一行中声明多个节点链接

``` java
flowchart LR
   a --> b & c--> d
```

``` mermaid
flowchart LR
   a --> b & c--> d
```

可以用一种非常有表现力的方式描述依赖关系

如果您使用基本语法描述同一个图表，则需要四行。

``` java
flowchart TB
    A & B--> C & D

or

flowchart TB
    A --> C
    A --> D
    B --> C
    B --> D

```

``` mermaid
flowchart TB
    A & B--> C & D

```

##### 新箭头类型

``` java
flowchart LR
    A --o B
    B --x C

```

``` mermaid
flowchart LR
    A --o B
    B --x C

```

###### 多向箭头

``` java
flowchart LR
    A o--o B
    B <--> C
    C x--x D
```

``` mermaid
flowchart LR
    A o--o B
    B <--> C
    C x--x D

```

##### 最小长度

​	流程图中的每个节点最终都被分配给渲染图中的一个等级，即垂直或水平级别（取决于流程图方向），基于它所链接的节点。默认情况下，链接可以跨越任意数量的等级，但您可以通过在链接定义中添加额外的破折号来要求任何链接比其他链接更长。

``` java
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

```

``` mermaid
flowchart TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    C --> D[Rethink]
    D --> B
    B ---->|No| E[End]

```







































