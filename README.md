[toc]
# 珠峰Node
## intro

## git
### 检出仓库
```
git clone /path/to/repository  //检出仓库
git clone username@host:/path/to/repository ///检出远端仓库
```
### 工作流
本地仓库由git 维护的三颗树组成
- **工作目录** 持有实际文件
- **缓存区**  保存临时改动
- **HEAD** 指向最后提交

### 创建仓库
```
git init //创建仓库
```
### 添加与提交
```
git add filename //添加到缓存区
git add * // 添加所有文件到缓存区

git commit -m "代码提交信息"
```
### 推送改动
```
git push origin master //提交到远端仓库
//可以把 master 换成你想要推送的任何分支

git remote add origin <server> //如果没有克隆现在仓库
```
### 分支
分支是用来绝缘开发的。创建仓库时master是默认的。在其它分支上进行修改，完成后将它们合并到主分支上。

```
git checkout -b feature_x //创建feature_x分支并切换过去
git checkout master //切回主分支

git branch -d feature_x //删除分支

git push origin <branch> //除非推送到远端仓库，否则不为人所见
```
## node

### 回调


### async
- **异步** 执行的顺序和排列的顺序是一致的

### IO
- **输入** 写入一个文件
- **输出** 读取一个文件

### 单线程
- 同一个时间内只能执行一个任务

###阻塞与非阻塞
- 当前的任务是否阻碍后面的代码的执行

###事件
- node里会触发很多的事件

###事件回调

##http
### 服务端
能接受请求的都叫服务端

###客户端
能发起请求的都叫客户端
- 需要在特定的机器（ip）启动特定的端口

###

## event


### 原型链
- 通过原型和构造函数生成对象
- 构造函数内定义的属性继承方式与原型对象不同，需要子类调用call\apply才能继承
- 构造函数内部的任何属性包括函数在内会被重复创建，不同对象不共享实例
- 构造函数运行的有闭包的开销
- Object/Function 都是构造函数，用于生成对象
- 所有的构造函数，包括Object都是Function 构造函数的实例
- Object.prototyp是所有对象的祖先
- Function.prototype是所有函数的祖先
