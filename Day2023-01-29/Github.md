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





