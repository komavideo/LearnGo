程序崩溃与修复
=============

## 知识点

* 使用 panic/recover 关键字，产生和处理系统崩溃信息

## 实战演习

~~~go
package main

import (
    "fmt"
)

func main() {
    fmt.Println("Helo Go.")

    // 恢复主程序线程
    defer func() {
        if err := recover(); err != nil{
            fmt.Println(err)
        }
        fmt.Println("别怕，我有疫苗。")
    }()

    // 程序崩溃
    panic("不好，有病毒！")

    fmt.Println("走我的Go程序。")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
