# Git安装
- 在ubuntu安装Git
		jessy@jessy-linux:~$ sudo apt-get install git

- Git初始化
		jessy@jessy-linux:~/my_git_workspace$ git init test
		Initialized empty Git repository in /home/jessy/my_git_workspace/test/.git/

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

# 获取帮助

		jessy@jessy-linux:~$ git help <verb>
		jessy@jessy-linux:~$ git <verb> --help
		jessy@jessy-linux:~$ man git-<verb>
                举例：jessy@jessy-linux:~$ git help config

# 获取Git仓库

- 初始化全新的Git仓库
		



