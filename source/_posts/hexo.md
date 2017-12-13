---
title: 使用HEXO+Github搭建自己的博客
header-img: "Demo.png"
tags:
- Hexo
- Blog
- Android
categories: 地理
---
![icon](https://camo.githubusercontent.com/063c5a8aecdefe228efea177f3bfc55a513997cd/687474703a2f2f6f6c6e7a70646932752e626b742e636c6f7564646e2e636f6d2f556e7469746c65642d313838302e706e67)

## 配置环境

安装Node（必须）

作用：用来生成静态页面的

到Node.js官网下载相应平台的最新版本，一路安装即可。

安装Git（必须）

作用：把本地的hexo内容提交到github上去.

安装Xcode就自带有Git，我就不多说了。

申请GitHub（必须）

作用：是用来做博客的远程创库、域名、服务器之类的，怎么与本地hexo建立连接等下讲。

github账号我也不再啰嗦了,没有的话直接申请就行了，跟一般的注册账号差不多，SSH Keys，看你自己了，可以不配制，不配置的话以后每次对自己的博客有改动提交的时候就要手动输入账号密码，配置了就不需要了，怎么配置我就不多说了，网上有很多教程。
正式安装Hexo

Node和Git都安装好后,首先创建一个文件夹,如blog,用户存放hexo的配置文件,然后进入blog里安装Hexo。

执行如下命令安装Hexo：

sudo npm install -g hexo

初始化然后，执行init命令初始化hexo,命令：

hexo init

好啦，至此，全部安装工作已经完成！blog就是你的博客根目录，所有的操作都在里面进行。

生成静态页面

hexo generate（hexo g也可以）

本地启动

启动本地服务，进行文章预览调试，命令：

hexo s

浏览器输入http://localhost:4000

## 配置Github

建立Repository

建立与你用户名对应的仓库，仓库名必须为【your_user_name.github.io】，固定写法

然后建立关联，我的blog在本地/Users/leopard/blog，blog是我之前建的东西也全在这里面，有：

    _config.yml    node_modules    public      source

    db.json        package.json    scaffolds  themes

现在我们需要_config.yml文件，来建立关联，命令：

vim _config.yml

翻到最下面，改成这样

deploy:
  type: git
  repo: git@github.com:seasonfif/seasonfif.github.io.git
  branch: master

然后执行命令：

npm install hexo-deployer-git --save

然后，执行配置命令：

hexo deploy

## Theme
https://github.com/lewis-geek/hexo-theme-Aath
![icon](https://camo.githubusercontent.com/063c5a8aecdefe228efea177f3bfc55a513997cd/687474703a2f2f6f6c6e7a70646932752e626b742e636c6f7564646e2e636f6d2f556e7469746c65642d313838302e706e67)
https://github.com/CodeDaraW/Hacker
![icon](https://camo.githubusercontent.com/9f682a6ea902cea665d6bbd52fe6e89f31e6d6c0/68747470733a2f2f6f6f6f2e306f302e6f6f6f2f323031362f30382f30342f353761333036663536626565322e706e67)
https://github.com/Kaijun/hexo-theme-huxblog
![icon](https://camo.githubusercontent.com/51586abd6e60f0bd7d85a532d7c0017cbe781421/687474703a2f2f6875616e677875616e2e6d652f696d672f626c6f672d6465736b746f702e6a7067)
https://github.com/YenYuHsuan/hexo-theme-beantech/
![icon](https://camo.githubusercontent.com/905786536d4c9f111d965f29aac8bc8c36fede47/687474703a2f2f6265616e746563682e6f72672f696d672f6265616e746563682d6465736b746f702e706e67)
