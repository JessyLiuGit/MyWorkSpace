# Git安装
- 在ubuntu安装Git

		jessy@jessy-linux:~$ sudo apt-get install git

# Git配置

		jessy@jessy-linux:~$ git config --system （/etc/gitconfig 对系统生效）
		jessy@jessy-linux:~$ git config --global （~/.gitconfig 对当前用户生效）
		jessy@jessy-linux:~$ git config          （工作目录中的.git/config 对当前项目生效）

- Git配置用户名和密码

		jessy@jessy-linux:~$ git config --global user.name "Jessyliu"
		jessy@jessy-linux:~$ git config --global user.email "jessyliu@foxmail.com"

- 设置默认文本编辑器

		jessy@jessy-linux:~$ git config --global core.editor vi
		jessy@jessy-linux:~$ git config --global merge.tool vimdiff

- 查看配置信息

		jessy@jessy-linux:~$ git config --list （查看所有的配置信息）
		jessy@jessy-linux:~$ git config user.name （查看某一条配置信息）
		jessy@jessy-linux:~$ cat .gitconfig (直接查看配置文件)

# 获取帮助

		jessy@jessy-linux:~$ git help <verb>
		jessy@jessy-linux:~$ git <verb> --help
		jessy@jessy-linux:~$ man git-<verb>
		举例：jessy@jessy-linux:~$ git help config

# 获取Git仓库

- 初始化全新的Git仓库

		jessy@jessy-linux:~/my_git_workspace/my_git_test$ git init 
		Initialized empty Git repository in /home/jessy/my_git_workspace/my_git_test/.git/

		jessy@jessy-linux:~/my_git_workspace$ git init my_git_test/
		Initialized empty Git repository in /home/jessy/my_git_workspace/my_git_test/.git/

- clone一个已经存在的远端仓库

		jessy@jessy-linux:~$ git clone git@github.com:JessyLiuGit/MyWorkSpace.git
		Cloning into 'MyWorkSpace'...
		remote: Counting objects: 24, done.
		remote: Compressing objects: 100% (5/5), done.
		remote: Total 24 (delta 0), reused 0 (delta 0), pack-reused 19
		Receiving objects: 100% (24/24), done.
		Checking connectivity... done.

# 查看Git版本号

		linux-omlu:/home/g00221245/br_V8R9C00_CarryingService # git --version
		git version 2.1.3

# 检查当前文件状态

- git status(目录无任何新增内容)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is up-to-date with 'origin/master'.
		nothing to commit, working directory clean

- git status(目录中存在新增未跟踪的文件)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is up-to-date with 'origin/master'.
		Untracked files:
		  (use "git add <file>..." to include in what will be committed)

			markdown/md_syntax/

		nothing added to commit but untracked files present (use "git add" to track)

- git status(目录中存在新增但是已经跟踪的文件)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is up-to-date with 'origin/master'.
		Changes to be committed:
		  (use "git reset HEAD <file>..." to unstage)

			new file:   markdown/md_syntax/md_syntax.md

- git status(目录中存在修改但是未跟踪的文件)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is up-to-date with 'origin/master'.
		Changes not staged for commit:
		  (use "git add <file>..." to update what will be committed)
		  (use "git checkout -- <file>..." to discard changes in working directory)

			modified:   git_learning/git_cmd/git_cmd.md

		no changes added to commit (use "git add" and/or "git commit -a")

- git status(目录中存在修改但是已经跟踪的文件)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is up-to-date with 'origin/master'.
		Changes to be committed:
		  (use "git reset HEAD <file>..." to unstage)

			modified:   git_learning/git_cmd/git_cmd.md

- git status(目录中存在已经提交但是没有push到远端的文件)

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git status
		On branch master
		Your branch is ahead of 'origin/master' by 1 commit.
		  (use "git push" to publish your local commits)
		nothing to commit, working directory clean

# 暂存已修改的文件

- 将某个文件单独加入暂存区

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git add git_learning/git_cmd/git_cmd.md

- 将所有文件同时加入暂存区

		jessy@jessy-linux:~/my_git_workspace/MyWorkSpace$ git add -A




