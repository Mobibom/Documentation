
**本项目可以使用Github或者Gitee进行访问**

- [Github地址](https://github.com/mobibom)
- [Gitee地址](https://gitee.com/mobibom)

# Git的使用教程

## 1. Git的安装

下载地址: [Git官网](https://git-scm.com/)
下载完成后, 双击安装包, 一路下一步即可。

## 2. Git的配置

安装完成后, 打开Git Bash, 输入以下命令:

```bash
git config --global user.name "Your Name"
git config --global user.email "
```

这里的`Your Name`和`Your Email`分别是你的Github用户名和邮箱。

## 3. Git的基本操作

克隆远程仓库, 这里的`url`是远程仓库的地址:

```bash
git clone url
```

初始化一个git仓库, 一般是在自己新建的文件夹, 而非克隆的远程仓库(因为克隆的远程仓库已经是一个git仓库了):

```bash
git init
```

添加所有文件到暂存区:

```bash
git add .
```

提交到本地仓库, 记得把`commit message`替换成你的提交信息:

```bash
git commit -m "commit message"
```

推送到远程仓库(第一次推送要选择推送到的分支, 例如`master`或者`main`, 之后只需要`git push`):

```bash
git push -u origin master
```

从远程仓库拉取(也可以直接用`git pull`, 区别是`git pull`会拉取所有分支, 这里的`master`是远程仓库的分支):

```bash
git pull origin master
```

## 4. Git的分支操作

创建一个新分支:

```bash
git branch branch_name
```

切换到新分支:

```bash
git checkout branch_name
```

合并分支:

```bash
git merge branch_name
```

删除分支:

```bash
git branch -d branch_name
```

## 5. Git 合并冲突

当两个分支的内容有冲突时, Git会提示合并冲突, 这时需要手动解决冲突, 然后再提交。

解决冲突的步骤:

1. 打开冲突文件, 手动解决冲突。
2. `git add .` 添加解决后的文件。
3. `git commit -m "commit message"` 提交解决后的文件。
4. `git push` 推送到远程仓库。
5. 删除不需要的分支。
6. 合并分支。

# Unity项目的Git管理

创建一个新的Unity项目, 并且把它备份到Github:
参考链接: [Unity项目的Git管理](https://adamwreed93.medium.com/how-to-set-up-git-lfs-into-your-unity-project-9fd276305fe7)

.gitignore文件是用来忽略不需要上传的文件的, 例如Library, Temp等。

下面是一个标准的Unity 项目 `.gitignore` 文件: 

```plaintext
# This .gitignore file should be placed at the root of your Unity project directory
# Get latest from https://github.com/github/gitignore/blob/main/Unity.gitignore
/[Ll]ibrary/
/[Tt]emp/
/[Oo]bj/
/[Bb]uild/
/[Bb]uilds/
/[Ll]ogs/
/[Uu]ser[Ss]ettings/
# Asset Store tools
/[Aa]ssets/AssetStoreTools*
# Uncomment if you have Vuforia files in your project
# /[Aa]ssets/Vuforia/
# Visual Studio cache directory
.vs/
# Rider
.idea/
*.sln
*.csproj
```

# Git的LFS管理大文件

Git LFS是一个Git的扩展, 用来管理大文件。

安装Git LFS:

```bash
git lfs install
```

其余步骤参考: [Git LFS](https://adamwreed93.medium.com/how-to-set-up-git-lfs-into-your-unity-project-9fd276305fe7)

# Git的GUI工具

1. [Github Desktop](https://desktop.github.com/download/) (官方, 功能少)
2. [SourceTree](https://www.sourcetreeapp.com/) (第三方, 推荐)