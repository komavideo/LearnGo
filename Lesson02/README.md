各种各样的约定
===========

## 知识点

* 讲述一下Go语言中各种各样的约定

## 实战演习

~~~go
// 包名，必须指定
package main
// 引入fmt包，如果没有使用则报错，变量同理
import "fmt"
// 主入口函数
func main() {
    // 字符串
    fmt.Println("go" + "lang")
    // 数值
    fmt.Println("1+1 =", 1+1)
    // 小数
    fmt.Println("10.0/2.0 =", 10.0/2.0)
    // 布尔值+逻辑运算
    fmt.Println(true && false)
    fmt.Println(true || false)
    fmt.Println(!true)
    // 指针
    a := 5
    fmt.Println(a)
    // 注意区分大小写
    // fmt.Println(A)
    // 指向int类型的指针
    var pa *int
    // 获取a的地址
    pa = &a
    fmt.Println(pa)
    fmt.Println(*pa)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
