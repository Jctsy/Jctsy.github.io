> 一些常用的 `git` 命令 目前这些基本上是咱常用的吧，后续可能遇到新的可能还会去添加上一些新的常用命令
# 目录
 [配置命令](#配置命令)
[仓库操作](#仓库操作)
[文件操作](#文件操作)
[分支管理](#分支管理)
[远程仓库操作](#远程仓库操作)
[撤销操作](#撤销操作)
[清除代理](#清除代理)
# 配置命令

### 设置全局用户名

```git
git config --global user.name "用户名"
```

### 设置全局用户邮箱

```git
git config --global user.email "邮箱地址"
```

### 查看当前Git配置

返回一大堆东西 后续用到了再细细研究吧

```git
git config --list
```
# 仓库操作

### 初始化一个新的Git仓库

```git
git init
```

### 克隆远程仓库到本地(白嫖项目的话这个命令就是最常用的了)

```git
git clone 远程仓库名
```

### 查看当前工作区的状态，显示文件的变化和暂存情况

```git
git status
```

### 查看提交历史

```git
git log
```

##### 如果看着一大坨别扭的话 可以

```git
git log --oneline
```

还有这个命令
##### 根据commit的唯一提交的哈希值去查看指定提交的详细信息

```git
git show 提交的哈希值
```
# 文件操作

### 将文件添加到暂存区

```git
git add 文件
```

##### 一般更常用这个一股脑全提交暂存区的命令

```git
git add .
```

### 将所有更改的文件添加到暂存区

```git
git commit -m '注释内容'
```

### 重命名文件
感觉有Linux基础就对这命令还是比较熟悉的
mv不熟悉？那`rm -rf *` 呢/手动狗头/

```git
git mv 之前的文件名 现在的文件名
```
### 修改上一次提交，适合在忘记提交某些文件时使用

我做上个markdown的笔记的时候咋就不知道这个命令呢 🙂

``` git
git commit -amend
```

不修改提交信息 

```git
git commit --amend --no-edit
```
# 分支管理

### 查看本地分支

```git 
git branch
```

### 创建新分支

```git
git branch 新分支名
```

### 切换到指定分支

```git
git checkout 分支名
```

### 创建并切换到新分支

```git
git checkout -b 新分支名
```

### 合并指定分支到当前分支

```git
git merge 指定分支
```

### 删除分支（删除前需要切换到其他分支）

```git
git branch -d 要删除的分支名
```
# 远程仓库操作

### 初次连接这个仓库

```git
git remote add origin 仓库名
```

### 第一次往远程仓库扔东西时

```git
git branch -M 分支名  
git push -u origin 分支名
```

### 后续的操作就可以推送

```git
git push
```

### 拉取远程仓库并更新本地仓库

```git
git pull
```

## 查看远程仓库地址

   ```git
   git remote -v
   ```

## 修改远程仓库地址

   ```git
   git remote set-url origin <new-url>
   ```
# 撤销操作

### 撤销对文件的修改，恢复到最近的提交状态

```git
git checkout -- 文件名
```

### 重置工作区和暂存区的所有更改，回到最近一次提交的状态

```git
git reset --hard
```

##### 1. **回退到指定提交，并保留之后的更改**
   ```git
   git reset --soft <commit-hash>
   ```

 回退到指定提交，保留工作区和暂存区的更改。

##### 2. **回退到指定提交，丢弃暂存区更改，保留工作区文件**

   ```git
   git reset --mixed <commit-hash>
   ```

##### 3. **回退到指定提交，并清空所有更改（不可恢复）**

   ```git
   git reset --hard <commit-hash>
   ```

### 创建一个新的提交，撤销指定提交的更改

不是很理解 这个操作 后面用到了再了解吧

```git
git revert 唯一commit哈希值
```
# 清除代理

1. **清除 HTTP 代理**：
   ```git
   git config --global --unset http.proxy
   ```

2. **清除 HTTPS 代理**：
   ```git
   git config --global --unset https.proxy
   ```

3. **检查代理设置是否存在**：
   ```git
   git config --global --get http.proxy
   git config --global --get https.proxy
   ```