延迟调用 - defer
================

## 知识点

* 延迟调用 - defer 的使用方法

## 实战演习

~~~go
package main

import (
    "fmt"
)

// 内有 defer 的执行函数
func MyDeferFunc1() {
    defer fmt.Println("结束") // defer:函数执行结束时调用
    fmt.Println("开始")
}
func main() {
    fmt.Println("Helo Go.")

    /////////////////////////////////////////////
    // 执行我的延迟函数1
    MyDeferFunc1()

    /////////////////////////////////////////////
    // 在线定义一个延迟函数
    defer func() {
        fmt.Println("Helo My Defer.1")
        fmt.Println("Helo My Defer.2")
        fmt.Println("Helo My Defer.3")
    }()

    /////////////////////////////////////////////
    // 执行我的延迟函数2
    MyDeferFunc2()
}

func MyDeferFunc2() {
    defer fmt.Println("Helo My Defer.1")
    defer fmt.Println("Helo My Defer.2")
    defer fmt.Println("Helo My Defer.3")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com