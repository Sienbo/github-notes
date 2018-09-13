# github-notes
记录一些git和github的使用方法，忘记时可以拿来参考
## git
- git三棵树结构
![git三棵树结构](https://github.com/Sienbo/github-notes/blob/master/git.pdf)
- 一些常用的命令
  - reset
    - git reset HEAD：使用仓库中存有的文件覆盖暂存区的文件；
    - git reset --mixed HEAD~：其中--mixed是默认的参数，使用此参数时，首先是将仓库中的HEAD指回到上一个版本，再用此时指向的文件覆盖暂存区域；（影响仓库以及暂存区两棵树）；
    - git reset --soft HEAD~：只影响仓库这棵树，将仓库中的HEAD指向上一个版本，并不修改暂存区域里面的内容；
    - git reset --hard HEAD~：影响三棵树，首先将仓库中的HEAD指向上一个版本，再用此时指向的文件覆盖暂存区域；最后将暂存区的内容还原到工作区域；
    - git reset 版本ID：也可使用soft,mixed.hard三个参数，这个命令不是指向上一个版本，而是指向版本ID号对应的版本；
    - git reset 版本ID 文件名：将暂存区内该文件回滚指定版本ID对应的那个版本的文件。
  - git diff
    - ![git diff](https://github.com/Sienbo/github-notes/blob/master/git.pdf)

