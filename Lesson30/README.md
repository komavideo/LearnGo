空接口的类型转换
==============

## 知识点

* 使用空接口类型完成类型转换与判断

## 实战演习

~~~go
package main

import (
    "fmt"
)

func myfunc(val interface{}) {
    fmt.Println(val)
    // 类型判断
    switch val.(type) {
    case bool:
        fmt.Println("布尔类型", val)
    case int:
        fmt.Println("整型数值", val)
    case string:
        fmt.Println("字符型", val)
    default:
        fmt.Println("未知类型", val)
    }
}
func main() {
    myfunc(123)
    myfunc("abc")

    // x 可动态类型变换
    var x interface{} = 100
    i1 := x.(int)
    fmt.Println(i1)
    fmt.Println(i1 + 100)

    // 浮点数
    x = 3.14
    i2 := x.(float64)
    fmt.Println(i2)
    fmt.Println(i2 + 10)

    // 加入转换结果 - isFloat64
    i3, isFloat64 := x.(float64)
    fmt.Println(i3)
    fmt.Println(isFloat64)

    // 赋值字符串
    x = "i love go."
    fmt.Println(x)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com