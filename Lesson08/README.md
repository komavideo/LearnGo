数组定义
========

## 知识点

* 数组的定义与使用

## 实战演习

~~~go
package main

import "fmt"

func main() {
    // 数组定义
    var a [5]int
    fmt.Println("a数组:", a)
    // 元素赋值
    a[4] = 100
    fmt.Println("a数组:", a)
    fmt.Println("a[4]:", a[4])
    // 数组长度
    fmt.Println("len:", len(a))
    // 数组定义且赋值
    b := [5]int{1, 2, 3, 4, 5}
    fmt.Println("b数组:", b)
    for i := 0; i < len(b); i++ {
        fmt.Println(b[i])
    }
    // 二维数组
    var c [2][3]int
    for i := 0; i < 2; i++ {
        for j := 0; j < 3; j++ {
            c[i][j] = i + j
        }
    }
    fmt.Println("二维数组: ", c)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
