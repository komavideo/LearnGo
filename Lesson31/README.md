定义标签
========

## 知识点

* 在程序中定义标签与使用

## 实战演习

~~~go
package main

import (
    "fmt"
)

func main() {
    fmt.Println("Helo Go.")

    // 定义一个标签块
main:
    for {
        for {
            fmt.Println("开始")
            // 跳出标签块
            break main
        }
        fmt.Println("死循环中...")
    }
    fmt.Println("结束")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com