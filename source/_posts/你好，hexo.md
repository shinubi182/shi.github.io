---
title: 你好，hexo 更换电脑操作
date: 2022-05-29 12:38:34
tags:
---

### 关于换电脑后hexo操作

##### 创建仓库，[http://shinubi182.github.io](https://link.zhihu.com/?target=http%3A//CrazyMilk.github.io)；

  创建两个分支：**main** 与 **hexo**
设置hexo为默认分支（因为我们只需要手动管理这个分支上的Hexo网站文件）
使用git  git@github.com:shinubi182/shinubi182.github.io.git拷贝仓库
在本地shinubi182.io文件夹下通过Git bash依次执行`npm install hexo`、`hexo init`、`npm install` 和 `npm install hexo-deployer-git`（此时当前分支应显示为hexo）
修改_config.yml中的deploy参数，分支应为main
依次执行`git add` .、`git commit -m "..."`、`git push origin hexo`提交网站相关的文件
执行hexo g -d生成网站并部署到GitHub上。

这样一来，在GitHub上的[http://shinubi182.github.io](https://link.zhihu.com/?target=http%3A//CrazyMilk.github.io)仓库就有两个分支，一个hexo分支用来存放网站的原始文件，一个main分支用来存  放生成的静态网页。

​       今后无论什么时候想要在其他电脑上面用hexo写博客，就直接把创建的分支克隆下来，npm install安装依赖之后就可以用了。
克隆分支的操作
​         `git clone -b hexo https://github.com/yourname/xxx.github.io.git`

​     因为上面创建的是一个名字叫hexo的分支，所以这里-b后面的是hexo，再把后面的gitHub的地址换成你自己的hexo博客的地址就可以了。
这样做完了以后，每次写完博客发布之后不要忘了还要`git push`把源文件推到分支上
