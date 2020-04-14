# 启动 HTTP服务 

>以下内容基于MacOS 系统

这里介绍一些常规用法，具体看个人习惯使用哪种方式，习惯哪种，再去了解高级用法，每个章节基本都有详细用法传送门。

## 阅读导航

<!-- TOC -->

- [启动 HTTP服务](#%e5%90%af%e5%8a%a8-http%e6%9c%8d%e5%8a%a1)
  - [阅读导航](#%e9%98%85%e8%af%bb%e5%af%bc%e8%88%aa)
  - [python](#python)
    - [version 2](#version-2)
    - [version 3](#version-3)
  - [http-server](#http-server)
    - [安装](#%e5%ae%89%e8%a3%85)
    - [使用](#%e4%bd%bf%e7%94%a8)
  - [serve](#serve)
    - [安装](#%e5%ae%89%e8%a3%85-1)
    - [使用](#%e4%bd%bf%e7%94%a8-1)
  - [Surge](#surge)
    - [安装](#%e5%ae%89%e8%a3%85-2)
    - [使用](#%e4%bd%bf%e7%94%a8-2)
  - [Web server for chrome](#web-server-for-chrome)
  - [各种源代码管理平台的Page 服务](#%e5%90%84%e7%a7%8d%e6%ba%90%e4%bb%a3%e7%a0%81%e7%ae%a1%e7%90%86%e5%b9%b3%e5%8f%b0%e7%9a%84page-%e6%9c%8d%e5%8a%a1)

<!-- /TOC -->

## python 

>Python（英国发音：/ˈpaɪθən/ 美国发音：/ˈpaɪθɑːn/）是一种广泛使用的解释型、高级编程、通用型编程语言，由吉多·范罗苏姆创造，第一版发布于1991年。可以视之为一种改良（加入一些其他编程语言的优点，如面向对象）的LISP。[来源请求]Python的设计哲学强调代码的可读性和简洁的语法（尤其是使用空格缩进划分代码块，而非使用大括号或者关键词）。相比于C++或Java，Python让开发者能够用更少的代码表达想法。不管是小型还是大型程序，该语言都试图让程序的结构清晰明了。

以上话术来自网络百科

为什么python会如此热门？江湖有一种传言，由于AI人工智能和深度学习技术的大热，从而带动了python语言的传播，至于AI 和 深度学习为什么选用python，应该还是python自身的特点，或者说是优势，让python成为该领域主流的开发语言。

为什么啰嗦这么多，因为本人也对python很有感触

好，言归正传

phthon 官方文档地址：https://docs.python.org/，好消息是从版本3.7 开始，文档内容已经可以选择简体中文阅读，说明我泱泱大国的pythoner 也是一股不小的力量。

  ### version 2
  当前的mac 系统，都会默认安装python，版本大多是2.7.xx，2.7 版本也会是version 2 里的最后一个版本，所以，使用mac的同学，不用安装，可以直接使用，代码也很简单,如下
  ```
  //8080是端口号，也可不指定，自动分配默认端口
  python -m SimpleHTTPServer 8080
  ```
  这里是SimpleHTTPServer的[详细使用方法](https://docs.python.org/2.7/library/simplehttpserver.html#module-SimpleHTTPServer)
  ### version 3 
  有时，为了使用新版本的特性，我们会在机器上额外安装一个高版本的python，对应启动http服务的指令如下：
  ```
  python -m http.server
  ```
  这是是http.server的[详细使用方法](https://docs.python.org/3.9/library/http.server.html?highlight=http%20server#module-http.server)

## http-server

地址：https://github.com/http-party/http-server

### 安装
```
npm install http-server -g
```
### 使用
```
http-server [path] [options]

//最简单用法：进入对应文件夹执行
//http-server

//-p 指定端口 8081 是端口号
// http-server -p 8081
```

## serve

地址：https://github.com/zeit/serve

### 安装
```
npm install serve -g
```
### 使用
```
server folder_name

//最简单用法：进入对应文件夹执行
//serve
```

## Surge

地址：http://surge.sh/

### 安装
```
npm install surge -g
```
### 使用
```
//最简单用法：进入对应文件夹执行
surge
```
正常部署后，会随机生成一个类似xxxxx.surge.sh的访问地址

## Web server for chrome

这是一款Chrome 浏览器扩展，可在Chrome 网上应用商店[下载](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb/)，这款扩展程序提供可视化界面操作，很多同学应该会喜欢

详细信息[可参见这里](https://github.com/kzahel/web-server-chrome)

## 各种源代码管理平台的Page 服务
比如github page、gitlab page