---
title: first
date: 2023-03-14 20:38:26
tags:
---
山东大学   计算机科学与技术   学院
   云计算技术   课程实验报告
 
学号：202018130182	姓名：张凯军 	班级：1班 
实验题目：利用云平台搭建个人博客
实验学时：2	实验日期：2023.3.14    
实验目的：熟悉个人博客系统的搭建。
具体包括：
参考方案：注册Github账号，搭建Hexo环境并实现个人博客搭建，撰写实验报告。


硬件环境： 
联网的计算机一台


软件环境：
Windows or Linux

 
实验步骤与内容：
1.首先安装两个需要使用的软件node.js和Git。


安装完成之后，发现两者已自动修改了环境变量，通过cmd命令查看两者版本并确认是否安装成功及可以使用，通过node -v来查看Node.js版本，通过git --version来查看Git版本。

2.登陆Github建立仓库。


3. 进入本地配置安装Hexo
（1）在磁盘中创建一个用来存放Github本地仓库文件的目录

（2）选中创建的目录，右键选择使用Gti Bash Here打开Git命令窗口，输入命令：npm install -g cnpm --registry=https://registry.npm.taobao.org

（2）正式开始安装hexo，输入命令：cnpm install -g hexo-cli

（3）初始化Hexo,输入命令：hexo init

这时创建的目录下已经多出许多文件

(4)输入命令：hexo s启动hexo之后在浏览器输入localhost:4000可以在本地浏览博客


4. 设置ssh，生成sshkey
（1）首先创建一个.ssh文件：mkdir ~/.ssh，之后输入命令：cd ~/.ssh进入.ssh文件，再输入命令：ssh-keygen -t rsa -C ‘2763471233@qq.com’

(2)查看C盘目录

(3)使用记事本打开id_rsa.pub文件并复制生成的key

(4)在已登陆的Github主页点击右侧头像进入Settings设置

（5）再点击SSH and GPG keys->New SSH key

（6）将刚刚在.ssh目录下所复制id_rsa.put文件中的信息复制进key，并取名为sszkj

（7）进行本地验证，输入命令：ssh -T git@github.com，然后输入yes

(8)绑定成功并且邮箱收到邮件

(9)在本地绑定与Github的用户名和邮箱
输入命令：git config --global user.name “sszkj”
输入命令：git config --global user.email “2763471233@qq.com”

5.上传测试博客
(1)用记事本打开并修改本地仓库目录下_config.yml文件

(2)复制Github仓库Http地址

（3）在文件的末尾修改
deploy:
type: git
repository: https://github.com/sszkj/sszkj.github.io.git
branch: master

(4)安装上传工具
输入命令：cnpm install hexo-deployer-git

(5)新建一篇测试文章
输入命令：hexo new “zzz”

(6)生成文件
输入命令：hexo g

(7)本地预览
输入命令：hexo s浏览器输入：localhost:4000


(8)部署到Github
输入命令：hexo d

(9)在Github仓库查看发现多了很多文件


结论分析与体会：
经过以上步骤，我成功地注册了Github账号，搭建了Hexo环境并实现了个人博客搭建，我的博客网站可以通过访问“https://sszkj.github.io”来查看，通过本次实验，我掌握了Github账号注册、Hexo环境搭建、博客网站生成等技能，了解到了一些Hexo的基本命令。同时，我也在实验过程中遇到了一些Hexo环境的配置问题，但通过查询文档和询问其他人的帮助，最终都得到了解决。总体来说，本次实验让我更加熟练地掌握了Hexo和Github的使用，技术得到了提升。






