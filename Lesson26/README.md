传入回调函数
==========

## 知识点

* 调用函数时传入回调函数的语法

## 实战演习

~~~go
package main

import "fmt"

func updatedb(cb func()) {
	////////////////////////////////////////////////
	fmt.Println("数据处理中...1,2,3...")
	////////////////////////////////////////////////
	fmt.Println("数据库更新完成，调用回调函数报告主线程.")
	cb()
}

func main() {
	fmt.Println("主线程运行...")
	updatedb(func() {
		fmt.Println("收到回调信息，数据库关闭.")
	})
    fmt.Println("主线程结束.")
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com