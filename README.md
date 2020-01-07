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


5.从github中下载指定文件夹  
  进入以下网址  
  https://minhaskamal.github.io/DownGit/#/home  
  进入github中需要下载的文件夹所在网址
  复制其url粘贴进DownGit下载即可

6.通过vim命令行实现两个vim文本之间的复制粘贴  
  假设用vim编辑器分别打开两个不同的文件，一个为/home/test1/1.c，另一个为/home/test2/2.c
  将2.c的某些语句复制到1.c
  在1.c所处的vim编辑器中，在命令行输入sp进行窗口分割
  继续在命令行中输入e /home/test2/2.c
  通过ctrl + w + 方向键进行窗口切换，yy/p进行复制粘贴
