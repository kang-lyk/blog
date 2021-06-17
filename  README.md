# Hugo
## 安装
```
$ export GOPATH=$HOME/go
$ go get -v github.com/spf13/hugo
```

## 生成站点

使用Hugo快速生成站点，比如希望生成到 /path/to/site 路径：

```$ hugo new site /path/to/site```

这样就在 /path/to/site 目录里生成了初始站点，进去目录：

```$ cd /path/to/site```

## 创建文章

创建一个 about 页面：

```$ hugo new about.md```

about.md 自动生成到了 content/about.md ，打开 about.md 看下：

```
+++
date = "2015-10-25T08:36:54-07:00"
draft = true
title = "about"

+++

正文内容
内容是 Markdown 格式的，+++ 之间的内容是 TOML 格式的，根据你的喜好，你可以换成 YAML 格式（使用 --- 标记）或者 JSON 格式。
```

创建第一篇文章，放到 post 目录，方便之后生成聚合页面。

```
$ hugo new post/first.md
```

## 部署

```
$ hugo --theme=hyde --baseUrl="http://coderzh.github.io/"
```

或者直接修改 `config.toml`配置文件，只运行

```
$ hugo
```

