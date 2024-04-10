1、进入要管理的目录
如果用编辑器vim编辑文件，退出时按：
Esc+shift+z+z。
如果用Git命令（如git commit amend）修改.git里面的文件，Git自动启用Gun nano 6.2编辑器，
其退出方式则不同：
要先按 ctrl+X，再选Y，即可存盘退出。
如果执行浏览提交日志命令（如git log等）进入浏览模式，退出时：
先按回车到最后（见到END标记），然后按字母q即可退出。


2、git init  ,               初始化，即让git帮助我们管理当前文件夹

3、git status          检测当前目录下文件的状态

4、个人信息配置：用户名、邮箱
	git config --global user.email "xxx@qq.com"
	git config --global user.name 'your name'

5、三种状态的变化
	* 红色        新增的文件/修改了原来的文件                git add 文件名                   工作区
	* 绿色         git已经管理起来                       git commit -m  '描述信息'	              暂存区
	*生成版本                                                                                                              版本库

6、回到上面的版本        回滚操作
    git log  
    git reflog 
    git reset --hard  (版本号)

7、分支
git branch
git branch dev
切换到dev分支          git checkout dev
切换到主线             git checkout master
把bug分支合并到主分支           git merge bug
删除bug分支            git branch -d bug

8、上传和复制代码
给远程仓库起别名       git    remote add origin 远程仓库地址
向远程推送代码           git push -u origin 分支
克隆远程仓库代码       git clone 远程仓库地址(内部已实现 git remote add origin 远程仓库地址）
切换分支                git checkout 分支
推送代码               git push origin dev
更新代码               git pull origin dev

在公司进行开发：
1、切换到dev分支进行开发             git checkout dev
2、把master分支合并到dev[仅一次]         git merge master
3、修改代码
4、提交代码            
git add .
git commit -m 'xx'
git push origin dev
回到家继续写代码
1、切换到dev分支进行开发             git checkout dev
2、拉代码                           git pull origin dev
3、继续开发
4、提交代码            
git add .
git commit -m 'xx'
git push origin dev
开发完毕，要上线
1、把dev分支合并到master，进行上线
git checkout master
git merge dev
git push origin master
2、把dev分支也推送到远程
git checkout dev
git merge master
git push origin dev



