# github-using-method
一、首次上传一个文件夹
1. 初始化git：                                       git init
2. 添加要上传的文件（上传目录）：                        git add *   
3. 将文件提交到本地仓库，并表明属性：                    git commit -m "First commit"
4. 本地分支默认为master，修改为main：                  git branch -a
                                      				     git branch -m master main
                                      				     git branch -r 
                                      				     git branch
5. 关联远程仓库：		           git remote add EthernetSSD git@github.com:xkjiang-srfv/EthernetSSD.git
(1)关联一次即可
6. 将远程仓库中内容roll到本地：              git pull EthernetSSD main --allow-unrelated-histories
(1)这个main是远端branch
(2)加这个参数的原因是本地仓库和远程仓库是不同的仓库，它们没有共同的历史记录，或者远程仓库是一个新的空仓库，并且它的历史记录与你的本地仓库不相关，加上该参数可以让 Git 强制合并不相关的历史记录。
7. 将本地仓库push到远端仓库中：              git push EthernetSSD main
(1)这个branch是本地branch名

二、本地端更新一个文件后再提交到远端
1. 首先拉取一下远端仓库代码，防止多人共同修改代码，你没有拉取别人修改的代码直接上传自己的，把别人修改的代码删了。                     
git pull EthernetSSD main
2. 执行git add *，会自动找到被修改的那些文件：
git add *
git commit -m "Second commit"
3. 上传
git push EthernetSSD main
