# Learn Git
## 什么是Git
Git是一种**分布式版本管理系统**。  
版本管理系统可以对文本文件的修改进行记录，使文件可以轻易的回到之前的某一次修改状态，从而进行版本管理。  
版本系统分为集中式和分布式。集中式版本管理系统将版本库放在中央服务器中，每个人需要从先从服务器拿到最新版本，再开始干活，最后将工作成果上传至中央服务器，缺点是必须要联网才能工作。分布式的版本管理系统没有中央服务器的概念，每个人的电脑上都是一个完整的版本，安全性也更高，同时不需要联网也能进行工作。
## 安装Git
前往Git官网下载windows安装包，默认选项进行安装。  
在任意目录下右键，Git Bash Here，弹出Git命令行窗口。  
最后一步，使用如下命令创建用户名及邮箱  
`git config --global user.name "name"`  
`git config --global user.email "email address"`  
## 创建版本库
1. 在合适的位置创建目录
2. 创建版本库  
命令：`git init`  
目录中会自动生成.git文件夹，用于存放git相关信息，不可随意修改  
3. 创建新文件  
创建文本文件firstText.txt，写入文本：Git is a version control system  
命令：`git status`  
输出:  
`Untracked files: `  
`(use "git add <file>..." to include in what will be committed)`   
`new.txt`   
表明当前目录下存在未跟踪的文件，建议使用`git add`命令将文件添加至待上传范围内  
4. 添加文件
命令：`git add new.txt`  `git status`   
输出：  
`Changes to be committed:`  
`(use "git restore --staged <file>..." to unstage)`  
`new file:   new.txt`   
表明当前目录下有待上传的修改，是一个新的文件，建议使用`git restore --staged`命令将文件撤销至未跟踪状态  
5. 撤销文件  
命令：`git restore --staged new.txt` `git status`
输出：  
`Untracked files: `  
`(use "git add <file>..." to include in what will be committed)`   
`new.txt`   
回到创建文件时的状态
6. 上传文件  
命令：`git commit -m "create a new txt"` `git status`   
输出：  
`nothing to commit, working tree clean`   
表明当前工作树干净，无任何文件需要上传  


