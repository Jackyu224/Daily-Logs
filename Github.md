## Git中的三个区域

``` mermaid
graph LR
A[工作区] --> B(处理工作的区域) 
C{暂存区} --> D(等待被提交) 
E(Git仓库) --> F[最终的存放区域]

```



## Git中的三种状态

``` mermaid
graph TD;
	A[已修改 modified] --> D[修改了文件还没有放到暂存区]
	B[已暂存 staged] --> E[对已修改的文件进行了标记]
	C[已提交 committed] --> F[文件安全的保存到本地的Git仓库中]
```



## Git基本工作流程

``` sequence

工作区->暂存区: Stage Fixes暂存修改 
暂存区-->Git仓库: Commit 提交更新
Note over 暂存区: 将你想提交的更改进行暂存;

```



## 配置Git

设置自己的**用户名**和**邮箱地址**，来记录是谁对项目进行操作

``` java
git config --global user.name "Jackyu224"
git config --global user.email "y226039081@gmail.com"
```

使用命令快速查看**Git**全局配置

```python
# 查看所有的全局配置
git config --list --global

# 查看指定的全局配置项
git config user.name
git config user.email
```



## 获取帮助信息

使用`git help <verb>`命令，无需联网在浏览器中打开帮助手册

```python
git help config

# 不想查看完整的手册
git config -h

git@github.com:Jackyu224/Daily-Logs.git
```



## 分支操作

#### main 主分支

在初始化本地Git仓库的时候，默认创建了一个名字叫做 `main`的分支，通常就叫做主分支

在实际工作中，`main`的作用是：`用来保存和记录整个项目已完成的功能代码`。

**不允许**直接在`main`分支上修改代码，因为这样做风险太高，容易导致整个项目崩溃



#### 功能分支

专门用来开发新功能的分支，临时从 `main` 上分叉出来的，当新功能开发且测试完毕后，最终需要合并到主分支上



##### 查看当前Git仓库分支列表

``` bash
# 查看当前Git仓库分支列表
git branch
* main
 * 表示当前所处分支
 
```

##### 创建新分支

可以基于查看当前分支，创建一个新的分支，执行完之后所处的还是 `main` 分支

``` bash
git branch 分支名称


```

##### 切换分支

``` bash
git checkout 分支名称

# 快速创建并切换
# 快速创建一个新分支 -b
git checkout -b 分支名称 

```

##### 合并分支

功能分支的代码测试完毕后，将完成的代码合并到 `main`分支上

```bash
# 首先切换到 main 分支
git checkout main

# 在 main 分支上运行 git merge 命令，将分支的代码合并到main
git merge 分支名称

```







