# Linux Archive 
[![Deploy Hugo](https://github.com/Linux-CN/archive/actions/workflows/hugo.yml/badge.svg)](https://github.com/Linux-CN/archive/actions/workflows/hugo.yml)


https://github.com/Linux-CN/archive/wiki



在本地构建站点
如果你需要在本地构建 Linux 中国的 Archive 站点，需要自行安装 Hugo & Git，然后执行如下命令，即可在本地预览站点

git clone git@github.com:Linux-CN/archive.git
cd archive
goproxy
https://goproxy.io/zh/
1
七牛云
https://goproxy.cn
1
阿里云
https://mirrors.aliyun.com/goproxy/
1
设置代理
其实，上面三个网站中都有详细的设置代理的方式

Go 版本是 1.13 及以上
go env -w GO111MODULE=on
go env -w GOPROXY=https://goproxy.cn,direct
安装hugo
go install github.com/gohugoio/hugo@latest
安装主题
git clone https://github.com/vimux/mainroad.git themes/mainroad
hugo server
执行如下命令，可以直接构建站点

hugo --gc --minify
使用其他程序加载
在 Release 当中，可以获取到 markdown 文件和图片素材包。

content.zip: Linux 中国所有原创文章的 Markdown 内容备份。
attachment.zip： 上述文章中引用的图片地址，需要放在 /data/attachment/ 目录下。如图片所示文件应当放置在服务器的 /data/attachment/album/201104/26/2133403xgbzgb3zfggxfzj.png 下，这样才可以在渲染的时候被替换。（也可放在 CDN 上，并在内容中全局替换）
文件头说明
在 markdown 文件中，可以使用 Frontmatter 来加载和解析标签。

image
标签含义如下

id：文章ID
title: 文章标题
author: 文章作者
fromurl: 文章源地址（仅翻译类文章有）
summary: 总结
excerpt： 摘要
pic: 头图（缩略图版）
largepic：头图（大图版）
titlepic：是否有头图，可以渲染用。
islctt：是否是 LCTT 文章（翻译文章）
selector：选题人员，值为 Github ID
translator：翻译人员，值为 Github ID
reviewer：校对人员，值为 Github ID
tags：文档标签
category：文档所属目录
count：计数
viewnum: 访问量
commentnum： 评论量
favtimes： 收藏量
sharetimes： 分享量
likes： 喜欢量
comments_data： 评论数据
postip：评论 IP
dateline：评论时间
message：评论内容
username：评论名
repcids：回复的评论的 ID
related： 相关文章的 ID
date：发布日期
updated：最后更新日期
permalink：永久链接（Linux.cn 上的链接）
content：文章内容
素材国内下载地址
百度网盘
如果你使用 Github 下载较慢，可以选择下方的百度网盘渠道来下载。

链接: https://pan.baidu.com/s/1i7DTuf_umPkkleHFtdmZJA?pwd=lccn 提取码: lccn
