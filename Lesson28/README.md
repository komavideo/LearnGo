数值生成器
==========

## 知识点

* 使用闭包的方式制作数值生成器

## 实战演习

~~~go
package main

import "fmt"

// integers 数值生成器
func integers() func() int {
	i := 0
	return func() int {
		// 定义数值生成规则
		i++
		// i += 2
		return i
	}
}

// 定义一个返回函数的
func main() {
	fmt.Println("Helo Go.")
	myInt := integers()
	fmt.Println(myInt())
	fmt.Println(myInt())
	fmt.Println(myInt())
	fmt.Println(myInt())
	fmt.Println(myInt())
	fmt.Println(myInt())
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com