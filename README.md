hello github
---------------

##### 1.撤销最近一次的git push  
  ```
  git reflog  
  git reset --soft HEAD~1  
  git reflog   
  git status   
  git rm --cached ${file}  
  删除/修改该文件后  
  git push origin master --force  
  ```

##### 2.将代码从仓库中拉下来并合并到本地仓库  
  ```
  git pull origin master  
  ```

##### 3.删除指定的文件  
  ```
  git rm -r --cached ${file}  
  git commit -m "delete file"  
  git push -u origin master  
  ```

##### 4.修改commit message  


##### 5.从github中下载指定文件夹  
  ```
  进入以下网址  
  https://minhaskamal.github.io/DownGit/#/home  
  进入github中需要下载的文件夹所在网址
  复制其url粘贴进DownGit下载即可
  ```

##### 6.通过vim命令行实现两个vim文本之间的复制粘贴  
  ```
  假设用vim编辑器分别打开两个不同的文件，一个为/home/test1/1.c，另一个为/home/test2/2.c  
  将2.c的某些语句复制到1.c  
  在1.c所处的vim编辑器中，在命令行输入sp进行窗口分割  
  继续在命令行中输入e /home/test2/2.c  
  通过ctrl + w + 方向键进行窗口切换，yy/p进行复制粘贴  
  ```

##### 7.将Python3.5.2升级至Python3.6.10后，通过快捷键Ctrl+Alt+T无法启动终端    
  ```
  输入命令：  
  $gnome-terminal  
  看到报错信息：ImportError:cannot import name 'gi'  
  解决：  
  $ cd /usr/lib/python3/dist-packages/gi/  
  $ sudo mv _gi_cairo.cpython-35m-x86_64-linux-gnu.so  _gi_cairo.cpython-36m-x86_64-linux-gnu.so  
  $ sudo mv _gi.cpython-35m-x86_64-linux-gnu.so _gi.cpython-36m-x86_64-linux-gnu.so  
  ```
  
##### 8.git push错误failed to push some refs to的解决  
  ```
  这个问题是因为远程库与本地库不一致造成的，那么我们把远程库同步到本地库就可以了。  
  git pull --rebase origin master  
  ```

##### 9.清空history历史命令记录  
```  
  vim ~/.bash_history  
  history -c  
  history -r  
```
  
  
##### 10.局域网ping不通
   ```
   出现如下问题：  
   From 192.168.0.101 icmp_seq=1 Destination Host Unreachable  
   From 192.168.0.101 icmp_seq=2 Destination Host Unreachable  
   From 192.168.0.101 icmp_seq=3 Destination Host Unreachable  

   原因：未知    
   解决方案：rm /var/lib/NetworkManager/NetworkManager.state，重启机器  
   ```

##### 11.histroy命令显示时间
```
编辑/etc/bash.bashrc文件，加入如下几行：
HISTTIMEFORMAT="%F %T "
export HISTTIMEFORMAT
保存后退出，关闭当前shell，并重新登录，再登录时就会有时间显示history记录了。
```
