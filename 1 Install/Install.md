# Install

## 安装方法

简单的安装方式是直接官网下载，然后本地安装即可。官网地址：[nodejs.org](https://nodejs.org/en/download/)

> Windows系统下，选择和系统版本匹配的.msi后缀的安装文件。Mac OS X系统下，选择.pkg后缀的安装文件。

打开终端，键入命令`node`，如果进入命令行式js交互环境，即安装成功。如图：

![](C:\Users\65151\Desktop\Nodejs\1 Install\img\1.png)

我们可以直接在终端node环境下输入简短的js代码，比如正则表达式。

如果要运行一大段代码的话，可以先写一个JS文件再运行。例如有以下hello.js。

```js
function hello() {
    console.log('Hello World!');
}
hello();
```

写好后在终端下键入`node hello.js`运行，结果如下：

```terminal
$ node hello.js
Hello World!
```

如果需要退出node环境，可以在终端连续输入**两次**：`Ctrl+C`即可。如图：

![](C:\Users\65151\Desktop\Nodejs\1 Install\img\2.png)

Node.js使得JavaScript可以脱离浏览器的窗口，独立运行在Node.js提供的环境中，所以Node.js中没有**BOM，DOM**这些概念。Node.js中根本没有页面，主要是进行一些服务器上的操作（比如：读写文件，网络通信...）。我们只需要基本的JavaScript语法基础（ES6）即可学习。

## 使用Nodemon自动重启项目

我们在开发的过程中，每次改完代码之后都必须重启服务器，显然这样的操作效率是比较低，这里给大家推荐个工具，`nodemon`,`nodemon`可以帮我们实时监听项目中代码的变化，并且自动重启服务，而且配置简单。

1. 安装：`npm install -g nodemon`
2. 使用`nodemon`运行项目，取代之前的`node app.js`。

```terminal
nodemon  [your app.js]
```

项目运行之后，`nodemon`会自动监听代码的改动，并且重新启动服务，大大增加我们开发效率。

#### `nodemon`常见配置

- 在命令行指定应用的端口号：`nodemon ./server.js localhost 8080`
- 查看帮助，帮助里面有很多选项都是一目了然：`nodemon -h 或者 nodemon --help`
- 运行 debug 模式：`nodemon --debug ./server.js 80`
- 手动重启项目： `Nodemon` 命令运行的终端 窗口中输入 `rs` 两个字符，然后再按下回车键，就能手动重启 `Nodemon`了。