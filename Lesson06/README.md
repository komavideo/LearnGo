If/Else逻辑判断
==============

## 知识点

* If/Else逻辑判断的写法

## 实战演习

~~~go
package main
import "fmt"
func main() {

    score := 30

    if score >= 30 {
        fmt.Println("MVP级别")
    } else if score >= 20 {
        fmt.Println("球星级别")
    } else if score >= 10 {
        fmt.Println("首发球员")
    } else {
        fmt.Println("酱油球员")
    }
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
