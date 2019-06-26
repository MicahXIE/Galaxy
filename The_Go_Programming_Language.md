1. 目前已经在Google工作的Ken Thompson和Rob Pike（他们在贝尔实验室时就是同事）、还有Robert Griesemer（设计了V8引擎和HotSpot虚拟机）一起合作，为了解决在21世纪多核和网络化环境下越来越复杂的编程问题而发明了Go语言。

2. Go语言尤其适合编写网络服务相关基础设施，同时也适合开发一些工具软件和系统软件。

3. 顺序通信进程 communicating sequential processes ，缩写为CSP。在CSP中，程序是一组中间没有共享状
态的平行运行的处理过程，它们之间使用管道进行通信和控制同步。

4. Practice Source Code Repo: https://github.com/adonovan/gopl.io/

5. Example
$ export GOPATH=$HOME/gobook # 选择工作目录
$ go get gopl.io/ch1/helloworld # 获取/编译/安装
$ $GOPATH/bin/helloworld # 运行程序
Hello, 世界 # 这是中文

6. Install
https://golang.org/doc/install

