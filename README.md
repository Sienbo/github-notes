# github-notes
记录一些git和github的使用方法，忘记时可以拿来参考
## git
- git三棵树结构
  - ![git三棵树结构](https://github.com/Sienbo/github-notes/blob/master/git%20%E4%B8%89%E6%A3%B5%E6%A0%91%E7%BB%93%E6%9E%84.jpg)
- 一些常用的命令
  - reset
    - git reset HEAD：使用仓库中存有的文件覆盖暂存区的文件；
    - git reset --mixed HEAD~：其中--mixed是默认的参数，使用此参数时，首先是将仓库中的HEAD指回到上一个版本，再用此时指向的文件覆盖暂存区域；（影响仓库以及暂存区两棵树）；
    - git reset --soft HEAD~：只影响仓库这棵树，将仓库中的HEAD指向上一个版本，并不修改暂存区域里面的内容；
    - git reset --hard HEAD~：影响三棵树，首先将仓库中的HEAD指向上一个版本，再用此时指向的文件覆盖暂存区域；最后将暂存区的内容还原到工作区域；
    - git reset 版本ID：也可使用soft,mixed.hard三个参数，这个命令不是指向上一个版本，而是指向版本ID号对应的版本；
    - git reset 版本ID 文件名：将暂存区内该文件回滚指定版本ID对应的那个版本的文件。
  - git diff
    - ![git diff](https://github.com/Sienbo/github-notes/blob/master/git%20diff.jpg)
  - git commit
    - 使用 -- amend选项，git会更正最近一次提交，但是不会产生一个新的版本，例如 git commit --amend -m "重新提交一次"，会将最近提交的说明进行更改，但是不会新增加一个版本快照；
  - git rm
    - git rm 文件名，只是删除工作区和暂存区的文件，条件是工作区与暂存区文件内容相同，否则报错；
    - git rm -f 文件名，可以强制将两处的文件都删除，不管工作区与暂存区文件的内容是否相同；
    - git rm --cached 文件名，只删除暂存区的文件。
  - git mv
    - 
