递归函数
==========

## 知识点

* 写个累加功能的递归函数

## 实战演习

~~~go
package main
import "fmt"
// 递归函数(自调用)
func sum(num int) int {
    if num == 1 {
        return num
    }
    return sum(num-1) + num 
}
func main() {
    // 求和1-10
    fmt.Println(sum(10))
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
