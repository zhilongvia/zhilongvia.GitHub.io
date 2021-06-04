---
title: hexo搭建博客踩坑记
date: 2021-06-04 21:00:33
tags: ["hexo"]
---

1. #### 安装node

``` bash
$ 官网下载安装
```

2. #### 安装git

``` bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

可能需要安装xcode
```

3. #### 安装hexo
``` bash
$ sudo npm install -g hexo-cli
```
4. #### 本地建一个blog目录

``` bash
$ mkdir myblogContents
```

5. #### 进入blog目录，使用hexo生产博客工程

``` bash
$ cd myblogContents
$ hexo init myfirtblog
```

   **工程名称无需跟github项目保持一致**

6. #### 进入myfirtblog下面的theme目录。下载需要使用的模板

``` bash
$ cd theme
sudo git clone https://github.com/XPoet/hexo-theme-keep themes/keep
```
    
7. #### 使用sudo hexo generate 生成工程文件

``` bash
$ sudo hexo generate
```

8. #### 使用sudo hexo server 启动工程；访问http://localhost:4000/查看效果

``` bash
$ sudo hexo server
```

9. #### github建立博客工程
参考
``` bash
$ https://github.com/HarleyWang93/blog/issues/1
```

10. #### github建立工程后，使用git的https地址。 在博客工程中_config.yml中增加配置

``` bash
$ deploy:
  type: git
  repo: https://github.com/user/user.GitHub.io.git
  branch: master
```

11. #### 使用sudo hexo deploy之前。需要clean和generate。否则会出现`**在线和本地不一致**`的情况

``` bash
$ sudo hexo clean
$ sudo hexo generate
```

12. #### `ERROR Deployer not found: git`错误需要执行下列命令
``` bash
$ sudo npm install--save hexo-deployer-git
```

# 至此可以看到在线博客和本地一致














