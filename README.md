# github-notes
记录一些git和github的使用方法，忘记时可以拿来参考
## git
- git三棵树结构
  - ![git三棵树结构](https://github.com/Sienbo/github-notes/blob/master/git%20%E4%B8%89%E6%A3%B5%E6%A0%91%E7%BB%93%E6%9E%84.jpg)
- 一些常用的命令
  - reset（撤回操作）
    - git reset HEAD：使用仓库中存有的文件覆盖暂存区的文件；
    - git reset --mixed HEAD~：其中--mixed是默认的参数，使用此参数时，首先是将仓库中的HEAD指回到上一个版本，再用此时指向的文件覆盖暂存区域；（影响仓库以及暂存区两棵树）；
    - git reset --soft HEAD~：只影响仓库这棵树，将仓库中的HEAD指向上一个版本，并不修改暂存区域里面的内容；
    - git reset --hard HEAD~：影响三棵树，首先将仓库中的HEAD指向上一个版本，再用此时指向的文件覆盖暂存区域；最后将暂存区的内容还原到工作区域；
    - git reset 版本ID：也可使用soft,mixed.hard三个参数，这个命令不是指向上一个版本，而是指向版本ID号对应的版本；
    - git reset 版本ID 文件名：将暂存区内该文件回滚指定版本ID对应的那个版本的文件。
  - git diff（比较操作）
    - ![git diff](https://github.com/Sienbo/github-notes/blob/master/git%20diff.jpg)
  - git commit（提交操作）
    - 使用 -- amend选项，git会更正最近一次提交，但是不会产生一个新的版本，例如 git commit --amend -m "重新提交一次"，会将最近提交的说明进行更改，但是不会新增加一个版本快照。
  - git rm（删除操作）
    - git rm 文件名，只是删除工作区和暂存区的文件，条件是工作区与暂存区文件内容相同，否则报错；
    - git rm -f 文件名，可以强制将两处的文件都删除，不管工作区与暂存区文件的内容是否相同；
    - git rm --cached 文件名，只删除暂存区的文件。
  - git mv
    - to be continue；
  - git branch（分支操作）
    - git branch:查看目前分支列表；
    - git branch develop：创建一个名字为develop的分支；（相当于从现在所处的分支上完全拷贝一份快照，包括其中的添加和提交状态）
    - git checkout develop:切换到develop分支，在develop分支中修改，并add,commit后新的develop分支才算完全建立
    - git checkout -b develop:创建develop分支并且直接切换到分支上；
    - git branch -d develop:删除develop分支;（需要在其他的分支上进行）
    - git checkout develop origin/develop:如果远程有个分支，将远程develop分支迁到本地；
    - git checkout -b develop origin/develop:将远程分支迁到本地后顺便切换到该分支。
  - git merge（合并操作）
    - git merge develop:将develop分支合并到当前所处的分支上。
  - git checkout（切换操作）
    - git checkout --文件名：从暂存区回复文件到工作区；
    - git checkout 分支名：切换分支；
    - git checkout 版本ID:HEAD指针跳转到对应版本ID的快照，并将此版本内容还原到暂存区和工作区；
    - git checkout 版本ID 文件名：使用版本ID快照对应的文件还原工作去和暂存区的文件。
  - git push（远程推送）
    - git push origin master:将master分支的内容推送到远程仓库；
    - git push origin:develop:删除远程分支。
    
    
    
