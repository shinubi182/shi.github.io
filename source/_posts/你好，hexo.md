---
title: 你好，hexo
date: 2022-05-29 12:38:34
tags:
---

### 一、关于搭建的流程

1. 创建仓库，[http://CrazyMilk.github.io](https://link.zhihu.com/?target=http%3A//CrazyMilk.github.io)；

2. 创建两个分支：master 与 hexo；

3. 设置hexo为默认分支（因为我们只需要手动管理这个分支上的Hexo网站文件）；

4. 使用git clone git@github.com:CrazyMilk/CrazyMilk.github.io.git拷贝仓库；

5. 在本地[http://CrazyMilk.github.io](https://link.zhihu.com/?target=http%3A//CrazyMilk.github.io)文件夹下通过Git bash依次执行npm install hexo、hexo init、npm install 和 npm install hexo-deployer-git（此时当前分支应显示为hexo）;

6. 修改_config.yml中的deploy参数，分支应为master；

7. 依次执行git add .、git commit -m "..."、git push origin hexo提交网站相关的文件；

8. 执行hexo g -d生成网站并部署到GitHub上。

​      这样一来，在GitHub上的[http://CrazyMilk.github.io](https://link.zhihu.com/?target=http%3A//CrazyMilk.github.io)仓库就有两个分支，一个hexo分支用来存放网站的原始文件，一个master分支用来存  放生成的静态网页。
