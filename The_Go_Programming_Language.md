1. 目前已经在Google工作的Ken Thompson和Rob Pike（他们在贝尔实验室时就是同事）、还有Robert Griesemer（设计了V8引擎和HotSpot虚拟机）一起合作，为了解决在21世纪多核和网络化环境下越来越复杂的编程问题而发明了Go语言。

2. Go语言尤其适合编写网络服务相关基础设施，同时也适合开发一些工具软件和系统软件。

3. 顺序通信进程 communicating sequential processes ，缩写为CSP。在CSP中，程序是一组中间没有共享状
态的平行运行的处理过程，它们之间使用管道进行通信和控制同步。

4. Practice Source Code Repo: https://github.com/adonovan/gopl.io/

5. Example

```
$ export GOPATH=$HOME/gobook # 选择工作目录
$ go get gopl.io/ch1/helloworld # 获取/编译/安装
$ $GOPATH/bin/helloworld # 运行程序
Hello, 世界 # 这是中文
```

6. Install
https://golang.org/doc/install

7. Go是一门编译型语言，Go语言的工具链将源代码及其依赖转换成计算机的机器指令

8. Go语言的代码通过包（package）组织，包类似于其它语言里的库（libraries）或者模块（modules）。
一个包由位于单个目录下的一个或多个.go源代码文件组成, 目录定义包的作用。每个源文件都以一条 package 声明语句开始，
这个例子里就是 package main， 表示该文件属于哪个包，紧跟着一系列导入（import）的包，之后是存储在这个文件里的程序语句。

Go的标准库提供了100多个包，以支持常见功能，如输入、输出、排序以及文本处理。比
如 fmt 包，就含有格式化输出、接收输入的函数。 Println 是其中一个基础函数，可以打印
以空格间隔的一个或多个值，并在最后添加一个换行符，从而输出一整行。

9. 注释语句以 // 开头。对于程序员来说，//之后到行末之间所有的内容都是注释，被编译器忽略。

10. for 语句

```
for initialization; condition; post {
// zero or more statements
}

// a traditional "while" loop
for condition {
// ...
}

// a traditional infinite loop
for {
// ...
}
```


11. range 

```
for _, arg := range os.Args[1:] {
	s += sep + arg
	sep = " "
}
```

每次循环迭代， range 产生一对值；索引以及在该索引处的元素值。这个例子不需要索引，
但 range 的语法要求, 要处理元素, 必须处理索引。一种思路是把索引赋值给一个临时变量,
如 temp , 然后忽略它的值，但Go语言不允许使用无用的局部变量（local variables），因为这
会导致编译错误。Go语言中这种情况的解决方法是用 空标识符 （blank identifier），即 _ （也就是下划线）。


12. assignment

s := ""
s, sep := "", ""
var s string

// not recommend below
var s = ""
var s string = ""




