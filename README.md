hello github


1.撤销最近一次的git push
  git reflog
  git reset --soft HEAD~1
  git reflog 
  git status 
  git rm --cached ${file}
  删除/修改该文件后
  git push origin master --force


2.将代码从仓库中拉下来并合并到本地仓库
  git pull origin master


3.删除指定的文件
  git rm -r --cached ${file}
  git commit -m "delete file"
  git push -u origin master


4.修改commit message

