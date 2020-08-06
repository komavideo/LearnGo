For循环
==========

## 知识点

* Go语言不一样的For循环

## 实战演习

~~~go
package main
import "fmt"
func main() {
    fmt.Println("---------------------------")
    i := 1
    for i <= 3 {
        fmt.Println(i)
        i = i + 1
    }
    fmt.Println("---------------------------")
    for j := 1; j <= 5; j++ {
        fmt.Println(j)
    }
    fmt.Println("---------------------------")
    for {
        fmt.Println("怒吃一鸡")
        break
    }
    fmt.Println("---------------------------")
    for n := 0; n <= 10; n++ {
        if n%2 == 0 {
            // 偶数继续
            continue
        }
        fmt.Println(n)
    }
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
