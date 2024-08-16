---
title: hexo 使用教程
date: 2019-04-13 09:07:19
tags: hexo
categories: hexo
---
hexo技术搭建博客
<!-- more -->
>学者的一天比不学无术的人一生还有价值。——阿拉伯

### 背景
>依托github.io 建自己的博客网站

### 准备工作
1. sudo npm install hexo-cli -g
2. hexo init generate-blog
3. hexo new "文章名"
4. hexo g #生成静态文件

### 配置SSH
>目的：上传代码到GitHub上，使用 `hexo d`

```shell
cd ~/.ssh # ssh密钥存放的路径
```
1. 生成密钥
```shell
ssh-keygen -t rsa -C "ilylys@163.com"
```
2. 然后去找文件`.ssh/id_rsa.pub`,复制里面的内容
3. 去GitHub个人设置， SSH and GPG keys -> New SSH key
4. 粘贴，保存
5. 测试，`ssh -T git@github.com` # 注意邮箱地址不用改

### 配置
配置_config.yml中有关deploy的部分：
```javascript
deploy:
  type: git
  repo: git@github.com:zeroone001/zeroone001.github.io.git
  branch: master
```
安装插件：
```shell
npm install hexo-deployer-git --save
```

### HEXO 相关命令
```shell
hexo new "article name" #新建文章
hexo clean #清理public
hexo g #生成静态页面到public目录
hexo s #启动本地服务，查看编写的页面
hexo d #上传静态文件到GitHub
hexo help #查看帮助
```
### theme
[theme-ad](https://github.com/dongyuanxin/theme-ad)
[主题文档](https://godbmw.com/passages/2019-03-03-theme-ad-docs-zh/)

#### 参考资料
[参考资料](https://www.cnblogs.com/liuxianan/p/build-blog-website-by-hexo-github.html)
[hexoGithub](https://github.com/hexojs/hexo/)
[hexo官网](https://hexo.io/zh-cn/)
