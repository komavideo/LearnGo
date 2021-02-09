延迟的使用例 - defer sample
==========================

## 知识点

* 延迟的使用例 - 文件的打开与关闭

## 实战演习

~~~go
package main

import (
    "fmt"
    "os"
)

func main() {
    fmt.Println("Helo Go.")

    file, err := os.Create("mytest.txt")
    if err != nil {
        fmt.Println("我去，出错啦！", err)
    }
    defer file.Close()

    file.WriteString("我爱Go浪！")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com

## 小马部落(Discord)

https://discord.gg/VSKw72P
