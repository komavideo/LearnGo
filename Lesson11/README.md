range的使用
==========

## 知识点

* Go语言中迭代数组，切片，字典，字符串，通道的函数 - range

## 实战演习

~~~go
package main
import "fmt"
func main() {
	// 定义一个数组
    nums := []int{2, 3, 4}
	sum := 0
	// range 循环数组
    for _, num := range nums {
        sum += num
    }
    fmt.Println("sum:", sum)
	// 连带索引一起迭代
    for i, num := range nums {
		fmt.Println("index:", i, ", num:", num)
    }
	// 迭代一个字典
    kvs := map[string]string{"a": "apple", "b": "banana", "c": "orange"}
    for k, v := range kvs {
        fmt.Printf("%s -> %s\n", k, v)
    }
	// 仅仅迭代字典的key
    for k := range kvs {
        fmt.Println("key:", k)
    }
	// 迭代循环一个字符串
    for i, c := range "iloveu" {
        fmt.Println(i, string(c))
    }
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
