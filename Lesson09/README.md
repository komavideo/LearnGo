切片类型
========

## 知识点

* Go语言中的切片语法

## 实战演习

~~~go
package main
import "fmt"
func main() {
    // 创建空切片
    s := make([]string, 3)
    fmt.Println("切片:", s)

    s[0] = "a"
    s[1] = "b"
    s[2] = "c"
    fmt.Println("切片内容:", s)
    fmt.Println("s[2]:", s[2])
    fmt.Println("切片长度:", len(s))

    // 内容追加
    s = append(s, "d")
    s = append(s, "e", "f")
    fmt.Println("数据追加后切片内容:", s)

    // 创建新的切片
    c := make([]string, len(s))
    // 拷贝切片内容
    copy(c, s)
    fmt.Println("新切片内容:", c)

    // 取切片下标：2,3,4
    l := s[2:5]
    fmt.Println("数据234:", l)
    // 取切片下标：0,1,2,3,4
    l = s[:5]
    fmt.Println("数据01234:", l)
    // 取切片下标：2,3,4,5
    l = s[2:]
    fmt.Println("数据2345:", l)

    // 创建数组
    t := []string{"g", "h", "i", "x", "y", "z"}
    fmt.Println("数组t:", t)
    // 数组切片
    fmt.Println("数组t[2:4]:", t[2:4])
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
