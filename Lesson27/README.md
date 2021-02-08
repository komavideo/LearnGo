闭包定义与延迟执行
================

## 知识点

* 定义闭包, 并延迟执行它

## 实战演习

~~~go
package main

import "fmt"

// MyLaterFunc 闭包定义与延迟执行
func MyLaterFunc() func(string) string {
	var _oldVal string
	return func(newVal string) string {
		result := _oldVal
		_oldVal = newVal
		return result
	}
}

// 定义一个返回函数的
func main() {
	f1 := MyLaterFunc()
	fmt.Println(f1("helo"))
	fmt.Println(f1("go"))
	fmt.Println(f1("world"))
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com