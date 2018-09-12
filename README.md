# github-notes
记录一些git和github的使用方法，忘记时可以拿来参考
## git
- git三棵树结构
![git三棵树结构](https://github.com/Sienbo/github-notes/blob/master/git.pdf)
- 一些常用的命令
  - reset
    - git reset HEAD  使用仓库中存有的文件覆盖暂存区的文件
    - git reset --mixed HEAD` 其中--mixed是默认的参数，使用此参数时，首先是将仓库中的文件指回到上一个版本，再用此时指向的文件覆盖暂存区域；（影响仓库以及暂存区两棵树）
