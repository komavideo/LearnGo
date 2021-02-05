匿名函数
========

## 知识点

* Go语言中匿名函数的使用

## 实战演习

~~~go
package main

import "fmt"

func main() {
	/////////////////////////////////////
	// 定义一个匿名函数，然后使用它
	f1 := func(x, y int) int {
		return x + y
	}
	result1 := f1(10, 20)
	fmt.Println(result1)

	/////////////////////////////////////
	// 定义函数的同时，调用它，然后返回结果值
	result2 := func(x, y int) int {
		return x * y
	}(10, 20)
	fmt.Println(result2)

	/////////////////////////////////////
	// 直接定义函数，直接调用，直接输出
	fmt.Println(func(name string) string {
		return "helo " + name
	}("koma"))
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com