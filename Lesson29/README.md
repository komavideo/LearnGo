接收函数的错误
============

## 知识点

* 调用函数时，同时接收返回的错误(如果有)

## 实战演习

~~~go
package main

import (
	"fmt"
	"strconv"
)

// 定义一个返回函数的
func main() {
	fmt.Println("Helo Go.")

	var strAge string = "25" // "25" or "abc"
	var intAge, err = strconv.Atoi(strAge)
	if err != nil {
		fmt.Println("出错啦！", err)
	} else {
		fmt.Println("My age is", intAge)
	}
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com