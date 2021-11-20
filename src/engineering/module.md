### 模块化
- 模块化是一种程序设计，将每个功能的实现规化为一个模块，模块之间建立联系，协作完成程序开发
- 模块化编程主要是解决变量的共享问题

### ES Moudles

- es modules是es6提出的js模块化解决方案

### CommonJs

- commonjs是一种js服务端解决方案，原名serverjs

### CommonJs与ES Moudles的区别

- commonjs是专为服务端使用，从磁盘读取文件，加载时间迅速，属于同步加载
- es modules可以为浏览器服务，浏览器加载资源本质上是请求资源，会有网络耗时，属于异步加载
- commonjs属于运行时加载，会加载整个文件，然后查找可以导出的变量挂在module.exports上
- es moduels属于编译时加载，编译时只会生成一个引用，等到代码运行时才去读取导出的值，所以可能出现两处文件同时导入一个变量a = 1，变量a在先执行的文件中修改为了2，导致在后执行的文件中读取出为2
- commonjs是静态导入，在导入变量时第一次会执行整个文件，然后将变量缓存，后面每次读取都是从缓存中读取
- es modules是动态导入，每次运行时读取引用取值，不会缓存
- node中.mjs代表es modules，.cjs代表commonjs，es modules可以和commonjs共存，如果使用node 13.2以下，使用es modules需要babel