### Git
#### 快捷方法
+ 当要切换分支时由于有一些如*.xml~的文件很多，`rm` 命令删除很不方便，可以使用 `vim .gitignore` 然后编译`.gitignore` (使用i),在.gitignore中添加`*.xml~`等，然后`git commit .gitignore`即可;在当前目录所在的主目录下的所有目录都执行`git status:repo forall -c "pwd;git status"`;
#### 本地代码不干净情况办法
+ 不需要切换到其他分之上：如果目前已经次改了代码，但是临时有个在该代码进行修改，需要将本地目前修改的备份：一、直接将修改的代码copy一份；二、打patch:需要切换到其他分支上操作：本地代码不干净，但是需要切换到其他的分支去做事情，可以使用` git commit -m "do not git push "`将此分支上的修改提交带本地，但是不要push到服务器，如果在另一个分支上做完了事情需要再次切换过来，然后使用`git reset HEAD^`(表示恢复最后一次提交)；
#### 提交到服务器全步骤

+ 查看当前的修改情况：`git diff ./`；查看git 状态：`git status ./`；将修改的东西添加起来：`git add ./`；提交到本地：`git commit -m "[package][apps]说明" `(如果使用过git add 则就此结束，如果没有使用则需要在后天添加 ./路径)；将commit 的推送到服务器：`git push origin local:MT6737`；

#### patch相关
##### 未增加文件，只是本地修改

+ 生成patch：`git diff . > patchname.patch`；合入patch：`patch -p0 < patch名 （跳过0级目录合patch）`；`patch -p1 < patch名 （跳过1级目录合patch）`；
##### 如果在本地又增加的文件需要提交到本地打patch
+ 生成patch；`git add ./ ；git commit -m "what you should say"`将代码提交到本地；`git format-patch 6ef8fe2d8687cdfa79efa27fd14e53410c68a9fd`(6ef8fe2d8687cdfa79efa27fd14e53410c68a9fd以上的提交是需要打patch的部分)；`git reset `(6ef8fe2d8687cdfa79efa27fd14e53410c68a9fd恢复提交与(HEAD^相同)；合入patch；`git apply --check patch文件名`（检测该patch包）；`git am 0001-do-not-git-push.patch`（将patch中的内容提交到本地）；`git reset 2639da31093ff5e56fe82c294f9dbae0880a492c`（将提交到本地的代码撤销）；
#### git命令

+ 在本地目录下查看提交的记录：`gitk` ；从服务器的仓库中下载代码，不会自动合并。比git pull更安全一些：`git fetch`；提交更新到本地：`git commit -m “modify java.c”`提交并编写说明（注：运行了git add 之后又做修改的文件需要重新运行git add把最新版本重新暂存起来）；恢复上一次提交到本地的代码：`git reset HEAD^`；查看该项目版本的更新细节：`git show 项目版本号`；回滚到指定的提交ID阶段：`git revert c011eb3c20ba6fb38cc94fe5a8dda366a3990c61`；将本地commit的代码更新到远端版本库中：`git push`；从服务器的仓库中获取代码和本地代码合并：`git pull`；

##### git rm

+ 进入某个目录中，执行此语句，会删除该目录中的所有目录和文件 ：`git rm -r*`；删除文件f1，不会删除本地目录文件，只删除index中的文件记录，将已经git add的文件remove到cache中，这样commit的时候不会提交这个文件，适用于一下子添加了很多文件，却不想排除其中个别几个文件的情况：`git rm --ached f1`；
##### git log
+ 表示只显示一个commit：`git log -l`；查看两个commit：`git log --max-count=2`；
##### git branch
+ 删除分支：`git branch -d 分支名`；查看服务器上所有的分支：`git branch -a`； 查看当前代码的所在分支：`git branch`；
##### git checkout
+ 恢复本地代码：`git checkout ./`；切换到这个分支：`git checkout 分支名`；创建一个分支并且切换到这个分支上：`git checkout -b 分支名`（remotes/origin/K558_INNJOO_V2，如果加入本服务器分支，则新创建的分支将会追踪本服务器分支）；切换到某个已经建立的本地分支，并且在该分支的基础上初始化一个新的分支：`git checkout -b newbranch localbranch`；
### repo
+ 是Google为了简化git的使用，创建的对git简化的包装工具；
#### 初始化软件仓库
+ `repo init -u 代码库地址 -b 分支名`（-u参数用来初始化代码仓库 -b参数指定某个分支 如果不指定默认为master分支）；
#### 同步代码
+ `repo sync -j4 `（使用-j参数来指定启动多线程同时下载 -j4 将会使用8个线程同时下载）；


### git面试
#### 工作区
+ 拉下来的项目就是一个`工作区`，在其目录下有一个`.git`隐藏目录；
#### .gitignore
+ 该文件指的是：`过滤掉哪些文件`不上传至服务器；
#### 主流的git工作流
##### fork/clone
+ 如果以该工作流的形式：第一步：fork将其他人的远程仓库的文件，拉取到自己的远程仓库中；第二步：自己远程仓库发送一个复制文件发送到本地电脑上；第三步：可以在本地更新某些文件，提交修改；第四步：push将本地仓库的更新发送到自己远程仓库上；第五步：将自己的远程代码提交到其他人的远程仓库中需要发送`pull request`命令；
##### clone
+ 是直接将别人远程的仓库clone到本地；然后本地直接push到远程仓库；
