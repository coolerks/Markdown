# Git

目的通过Git进行版本控制并托管项目代码

## Git工作区

### 工作区

添加编辑修改文件

### 暂存区

暂存已经修改的文件，最后提交到Git仓库

###Git repository(Git仓库)

最终确定的文件保存到仓库，成为一个全新版本，并对他人可见

## Git命令

#### 查看文件

```
ls
```

#### 查看目录名称

```
pwd
```

#### 在本地创建文件夹

```
mkdir 文件夹名
```

#### 在本地创建文件

```
touch filename
```

#### 查看文件

```
cat 文件名
```





---

#### 初始化仓库

```
git init
```

此时在该文件夹下生成一个.git的隐藏文件夹，文件夹内保存着仓库文件

#### 查看文件的状态

```git
git status
```

#### 从工作区提交到暂存区

```
git add filename
git add --all
```

#### 从暂存区提交到Git 仓库

```
git commit -m '描述'
```

#### 基本信息设置-用户名和邮箱

```
git config --global user.name '用户名'
git config --global user.mail '邮箱'
```

#### 在git仓库中删除文件

```
git rm 'filename'
```

#### 从远程下载到本地

```
git clone 仓库地址
```

#### 从本地提交到远程仓库

```
git push
git push -f origin master
```



#### 关联GitHub仓库

```
git remote add origin 仓库地址
```

#### 远程代码与本地代码合并

```
git pull --rebase origin master
```



end