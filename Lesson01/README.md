课程介绍
========

## 官方网站

https://golang.org/

### GitHub

https://github.com/golang

## 使用版本

+ 1.14.6

## 面向对象

没有接触过Go语言的初学者朋友。

## 基础知识

简单的编程基础，当然这也不是必须的。

## 开发工具

1. Visual Studio Code(推荐)
2. Brackets/ATOM
3. EmEditor

## 视频计划

* 每个视频只包括一个知识点，并控制在3-5分钟之内（甚至更短，但经常超时）

## 安装

```bash
# 下载go最新版本
$ wget https://golang.org/dl/go1.14.6.linux-amd64.tar.gz
# 解压至系统目录
$ sudo tar -C /usr/local -xzf go1.14.6.linux-amd64.tar.gz
# 设定路径
$ #nano ~/.profile
$ nano ~/.bashrc
...
export PATH="$PATH:/usr/local/go/bin"
...
# 安装版本确认
$ go version
# 编辑一个go代码文件
$ nano main.go
...
package main
import "fmt"
func main() {
    fmt.Println("hello world.")
}
...
# 运行main.go代码
$ go run main.go
# 编译成为二进制执行文件
$ go build main.go
$ ./main
```

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
