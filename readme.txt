1、进入要管理的目录
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
 查看分支                   git branch
创建分支                    git branch dev
切换到dev分支          git checkout dev
切换到主线             git checkout master
把bug分支合并到主分支           git merge bug          切换分支再合并（可能产生冲突）
删除bug分支            git branch -d bug
分支合并可能会产生冲突，需要手动去解决冲突    ----------- 一切都建立在master主支上
8、工作流
9、进军三里屯
给远程仓库起别名          git remote add origin <远程仓库地址>https://github.com/Su1688/dbhot2.git
给远程推送代码          git push -u origin 分支
克隆远程仓库的代码                     git clone  <远程仓库地址>https://github.com/Su1688/dbhot2.git