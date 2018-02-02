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
## npm script
### npm script是什么
讲这个问题之前，我们来看下一个很重要的文件，包描述文件-package.json文件，它必须是一个真真正正的JSON，不能是js的对象字面量。
package.json 其本质上一个commonjs规范中的一个很重要的文件。不过由于npm实现太普及了，以至于人们认为package.json是npm独有的。
commonjs详细介绍可以参考[这篇文章](http://wiki.commonjs.org/wiki/Packages/1.1)

其实我们更加关注的package.json里面的字段。 package.json里面有的是内置字段比如name，maintainers。你可以在里面定制任何的字段比如proxy。

下面我们介绍一下`日常开发`中比较常用的字段。

#### dependencies & devDependencies
这两个是依赖相关。定义了项目的依赖。后者是开发依赖，只有在开发阶段（NODE_ENV=development）才会被安装。
我们通常将一些测试相关，构建相关的依赖加入到devDependencies中。

值得一提的是npm的版本管理。node通过语义化的版本号管理包。你可以定义包的版本范围，
版本范围是一个包含一个或多个空格分割的描述符，也可以直接引用一个tarball或者git url。

版本范围有如下几种类型：

```
version Must match version exactly
>version Must be greater than version
>=version etc
<version
<=version
~version "Approximately equivalent to version" See semver
^version "Compatible with version" See semver
1.2.x 1.2.0, 1.2.1, etc., but not 1.3.0
http://... See 'URLs as Dependencies' below
* Matches any version
"" (just an empty string) Same as *
version1 - version2 Same as >=version1 <=version2.
range1 || range2 Passes if either range1 or range2 are satisfied.
git... See 'Git URLs as Dependencies' below
user/repo See 'GitHub URLs' below
tag A specific version tagged and published as tag See npm-dist-tag
path/path/path See Local Paths below
```
#### script
这个是脚本相关。通过它可以简单一些简单的”自动化“。
#### engines && browserslist
这个是项目的兼容性相关。描述的是支持的引擎版本和支持的浏览器版本。

更多关于[package.json字段的解释](https://docs.npmjs.com/files/package.json)
### 结合hooks实现代码检测以及CI，CD
## workflow
### 前端有哪些优秀的工作流

### 如何用node + npm实现
