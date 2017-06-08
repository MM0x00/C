# nodejs 在线实验环境

## 软件简介

软件基本信息，License，所属的类别，作用，特点等。

readytalk/nodejs是一个搬运工捆绑的最新版本的基本图像的NodeJS和NPM从安装nodejs.org。它作为readytalk/nodejs-runtime图像的基础。

Node.js是一个Javascript运行环境(runtime)。实际上它是对Google V8引擎进行了封装。V8引 擎执行Javascript的速度非常快，性能非常好。Node.js对一些特殊用例进行了优化，提供了替代的API，使得V8在非浏览器环境下运行得更好。

Node.js是一个基于Chrome JavaScript运行时建立的平台， 用于方便地搭建响应速度快、易于扩展的网络应用。Node.js 使用事件驱动， 非阻塞I/O 模型而得以轻量和高效，非常适合在分布式设备上运行数据密集型的实时应用。

所属类别是编程语言

特点：

1.RESTful API

2.单线程

3.非阻塞IO

4.V8虚拟机

5.事件驱动


## 软件官网

https://nodejs.org/en/

## Dockerfile 使用方法

### 用法
在nodejs应用程序目录中创建一个Docker文件，具有以下内容：

  FROM readytalk/nodejs

  WORKDIR /app
  
  ADD package.json /app/
  
  RUN npm install
  
  ADD . /app

  CMD []
  
  ENTRYPOINT ["/nodejs/bin/npm", "start"]
  
在应用程序目录中运行以下命令：

  docker build -t my/app .

## 资源链接

- https://nodejs.org/en/
