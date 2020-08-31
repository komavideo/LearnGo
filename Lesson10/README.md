map哈希字典
==========

## 知识点

* Go语言中map哈希字典的使用(key:value)

## 实战演习

~~~go
package main
import "fmt"
func main() {
    // 定义一个key:value的哈希表
    m := make(map[string]int)
    // 赋值
    m["k1"] = 7
    m["k2"] = 13

    fmt.Println("m:", m)
    // 给变量赋值
    v1 := m["k1"]
    fmt.Println("v1: ", v1)
    // 哈希长度
    fmt.Println("len(m):", len(m))

    // 删除一个哈希值
    delete(m, "k2")
    fmt.Println("m:", m)

    // 定义+初始化
    n := map[string]int{"foo": 1, "bar": 2}
    fmt.Println("n:", n)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
