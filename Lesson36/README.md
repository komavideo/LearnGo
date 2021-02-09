初始化函数 - init
================

## 知识点

* 使用初始化函数 - init

## 实战演习

~~~go
package main

import (
	"fmt"
)

func init() {
	fmt.Println("初始化函数 init()")
}

// 可以定义多个 init 初始化函数
func init() {
	fmt.Println("初始化函数2 init()")
}

// 主函数
func main() {
	fmt.Println("主函数")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com