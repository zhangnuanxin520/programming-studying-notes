# Git学习笔记

[TOC]



Git clone 时，可以所用不同的协议，包括 ssh, git, https 等，其中最常用的是 ssh，因为速度较快，还可以配置公钥免输入密码。各种写法如下：

```
git clone git@github.com:fsliurujie/test.git         --SSH协议
git clone git://github.com/fsliurujie/test.git          --GIT协议
git clone https://github.com/fsliurujie/test.git      --HTTPS协议
```



## 第四章	多次提交

### 4.0	Git结构

- **工作区：**就是你在电脑里能看到的目录。
- **暂存区：**英文叫 stage 或 index。一般存放在 **.git** 目录下的 index 文件（.git/index）中，所以我们把暂存区有时也叫作索引（index）。
- **版本库：**工作区有一个隐藏目录 **.git**，这个不算工作区，而是 Git 的版本库。

  下面这个图展示了工作区、版本库中的暂存区和版本库之间的关系：

![img](https://www.runoob.com/wp-content/uploads/2015/02/1352126739_7909.jpg)

### 4.1	status命令

#### **作用**：

​	查看当前工作区中所发生的修改

**输出结果：**

- **被提交的修改（changes to be committed）:**这部分将列出那些将在下次提交中被纳入到版本库中的、被修改的文件。
- **不会更新的修改(changes but not updated)：**这部分将列出那些已经被修改但是尚未被注册到下次提交的文件。
- **未被跟踪的文件(untracked files)：**这部分将列出所有的新增文件。

#### 选择性提交：

​	由于创建新的提交未必就一定会包含当前所有的更新，所以我们可以选择纳入所有文件或者只选取其中的一些文件

##### 1.查看所发生的修改

> git status

##### 2.收集相关修改

​	用`add`命令将相关修改添加到暂存区中，既可以单独指定文件的路径也可以从其所有子目录中指定某一包含了新增文件与被修改文件的目录

> git add foo.txt bar.txt		   # selected files
>
> git add dir/ 							# a directory and everything underneath
>
> git add.								  #current directory and everything underneath

##### 3.创建提交

> git commit

​	完成该操作后，暂存区就会被清空。

### 4.2	怎样的修改不该被提交

- **为调试而做的实验性修改 **
- **意外添加的修改 **
- **尚未准备好的修改 **
- **自动生成文件中所发生的修改 **

#### 方法：从暂存区中撤回修改

##### 	**rest**命令可以用来重置暂存区。

​	其中第一个参数为`HEAD`，表示的是我们要将其重置为当前的HEAD版本。

​	第二个参数则用于制定要被重置的文件或目录。

例如：

> git reset HEAD .

或者：

> git reset HEAD foo.txt src/test/

​	在重置过程中，暂存区将会被重写。

##### 	对于上述问题Git为我们提供了以下几种应对方法：

- 使用**reset**命令重置那些实验性的或者被意外修改的内容。
- 将我们不希望提交的忽略文件列表写入**.gitignore**
- 使用**stash**命令将我们希望日后在做提交的修改内容暂时保存起来。

## 第五章	版本库

5.1	一种简单而高效的存储系统

Git的核心是一个对象数据库。该数据库可以用来存储文本或二进制数据。