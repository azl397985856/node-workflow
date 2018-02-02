# 简介
本文主要介绍node相关的基础知识，以及node的一个很常用的包管理工具npm。最后会讲解如何根据node + npm打造前端工作流程。
## node
### node是什么
Node.js® 是一个基于 Chrome V8 引擎的 JavaScript 运行时。 Node.js 使用高效、轻量级的事件驱动、非阻塞 I/O 模型。
它的包生态系统，npm，是目前世界上最大的开源库生态系统。
### 为什么是node
1. 语法一致
一个重要的原因在于node的语法和前端用的开发语言javascipt是一致的。原因就在于node是一个基于V8的js runtime。
2. 社区一致
node上的绝大多数包既可以运行在浏览器也可以运行在node。做出node和浏览器通用的包是非常简单的。
也就是说你在浏览器写的一个包可以毫不费力的运行在node上。
### 它可以帮前端做什么
node扩展了前端的领域。 值得一提的是，node并不是第一个将js魔爪伸向后的。
node借助了V8的强大性能以及js天生的异步的支持能力，node底层也是基于libuv，用于实现底层功能。
其本身并没有什么特别出色的地方，但是他的这个将出色的东西组合起来想法非常棒。

简而言之，node可以帮我们做一些浏览器中不容易实现或者无法实现的功能。比如获取操作系统的信息，新建进程，执行shell脚本。
甚至是搭建一个node sever（node 搭建一个server真是再简单不过了）。
但是这样东西，对我们做一些前端自动化是非常有必要。
## npm
### npm是什么
npm是一个常用的node包管理工具。在我写这篇的文章yarn的气势已经逐渐超过了npm。笔者也在使用yarn。
但我还是决定介绍npm，因为他们的使用和原理基本大同小异。

那么什么是npm？

npm全称是node packge management是一个发布共享代码，管理项目依赖的工具。 它维护了600,000多个（January 31, 2018）仓库

npm由三部分组成：

1. the website
2. the registry
3. the Command Line Interface (CLI)

### 如何管理包依赖
### 发布一个npm包
## script
### npm script是什么
### 结合hooks实现代码检测以及CI，CD
## workflow
### 前端有哪些优秀的工作流

### 如何用node + npm实现
