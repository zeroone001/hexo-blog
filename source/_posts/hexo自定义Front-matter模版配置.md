---
title: hexo自定义Front-matter模版配置
tags:
  - hexo
date: 2019-04-13 15:00:23
categories: hexo
---
hexo自定义Front-matter模版配置
<!-- more -->
>生而知之者上也；学而知之者次也；困而学之又其次也；困而不学，民斯为下矣。——论语

#### 背景
hexo 自带的Front-matter配置不够全，每次都要手动去写

#### 办法
1. 找到`\scaffolds\post.md`文件
2. 在下面添加你需要的配置就OK了
3. 我的，如下
```shell
---
title: {{ title }}
date: {{ date }}
tags:
-
categories:
---

<!-- more -->
```
####  参考链接
[Front-matter官网](https://zhangjiejun.com/posts/config_Front-matter_in_hexo/)
