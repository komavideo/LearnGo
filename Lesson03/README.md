定义变量
========

## 知识点

* 定义Go语言中的变量

## 实战演习

~~~go
package main
import "fmt"
func main() {
    // 字符型
    var a = "你好，Go世界。"
    fmt.Println(a)
    // 数值型
    var b, c int = 10, 20
    fmt.Println(b, c)
    // 布尔型
    var d = true
    fmt.Println(d)
    // 浮点型
    var e float32
    e = 3.1415926
    fmt.Println(e)
    // 定义类型+直接赋值
    f := "摇头库"
    fmt.Println(f)
    // 指针类型
    var pf *string
    // 获取f的地址
    pf = &f
    fmt.Println(pf)
    fmt.Println(*pf)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
