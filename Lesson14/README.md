指针调用
========

## 知识点

* 指针调用方式和函数

## 实战演习

~~~go
package main
import "fmt"
// 接收一个数值
func byValue(ival int) {
    ival = 0
}
// 接收一个指向 int 类型的指针
func byPointer(iptr *int) {
    *iptr = 0
}
func main() {
    // 定义一个数值
    i := 10
    fmt.Println("initial:", i)
    // 值传递给函数byValue
    byValue(i)
    fmt.Println("byval:", i)
    // 地址传递给函数byValue
    byPointer(&i)
    fmt.Println("byptr:", i)
    // 打印出 i 的地址
    fmt.Println("pointer:", &i)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
