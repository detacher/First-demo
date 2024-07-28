[markdown语法](https://markdown.com.cn/basic-syntax/paragraphs.html)

# git and github

##什么是git？



[关于git](https://git-scm.com/about/branching-and-merging)

Git 是一个[免费的开源](https://git-scm.com/about/free-and-open-source) 分布式版本控制系统，旨在快速高效地处理从小型到大型的所有项目。

Git[易于学习](https://git-scm.com/doc)，占用 [空间小，性能快如闪电](https://git-scm.com/about/small-and-fast)。它比 Subversion、CVS、Perforce 和 ClearCase 等 SCM 工具更胜一筹，具有[廉价的本地分支](https://git-scm.com/about/branching-and-merging)、方便的[暂存区](https://git-scm.com/about/staging-area)和 [多种工作流程](https://git-scm.com/about/distributed)等功能

操作

$ git -h 帮助

$ git help config 获取详细帮助 打开网页

🖥️ GIT COMMANDS CHEAT SHEET 

- Set configuration values for your username and email 

- - git config --global user.name YOUR NAME 
  - git config --global user.email YOUR EMAIL 

- Set default branch to main 
- - git config --global init.default branch main 

- Get help on a command 

- - git help COMMAND 
  - git COMMAND -h 

- Initialize a new git repository 

- - git init

- Clone a repository 

- - git clone REPOSITORY URL 

- Add a file to the staging area 

- - git add FILE 

- Add all file changes to the staging area 

- - git add --all 
  - git add -A 
  - git add . 
- Check the unstaged changes 
- - git diff Commit the staged changes
  -  git commit -m "MESSAGE" 

- Reset staging area to the last commit

- - git reset

- Check the state of the working directory and the staging area

- - git status



- Remove a file from the index and working directory

- - git rm FILENAME

- Rename a file

- - git mV (OLD NAME)(NEW NAME)

- List the commit history
  - git log

- List all the local branches
- - git branch

- Create a new branch

- - git branch BRANCH NAME

- Rename the current branch

- - git branch -m NEW BRANCH NAME

- Delete a branch

- - git branch -d BRANCH NAME

- Switch to another branch

- - git switch BRANCH NAME

- Merge specified branch into the current branch

- - git merge BRANCH NAME

- Create a connection to a remote repository

- - git remote add (NAME) (REPOSITORY URL)

- Push the committed changes to a remote directory

- - git push (REMOTE)(BRANCH)

- Download the content from a remote repository

- - git pull REMOTE



## 具体操作

- git config --user.name "your name" 设置你的名字
- git config --user.email "your email"设置你的邮箱
- git config init.default branch main 设置默认分支
- 对于想要隐藏的文件 

/ #ignore one.txt files （也许是解释说明）

  my_secret.txt（要隐藏的文件）*.txt（隐藏所有txt文件）

- git statue （状态）
- git init (初始化)
- git add file(添加文件跟踪) 
- git rm --cached file (移除文件的跟踪)
- git diff (对比修改前后区别)
- git mv "oul_file_name" "new_file_name" (修改名称)
- git log --oneline(查看修改情况 git log则是详细 git log -p全面)
- git branch branch_name (增加新分支)
- git switch branch_name(跳转新分支)
- git commit -a -m “（具体描述）”
- git merge -m"" branch_name(合并分支branch_name到现在的分支)
- git branch -d branch_name (删除该分支)

## 相关概念添加文件

- 分支：创建分支后，每当你切换分支时，对应的文件都会切换到其分支。eg：main分支 branch1分支 当分支切换到branch1并在该分支进行修改时，只会修改branch1分支中文件的内容，而当你切换到main分支后，无论branch1中如何修改，都不会影响到main分支，除非使用合并。

