返回函数类型的函数
=================

## 知识点

* 定义一个可以返回函数类型的函数

## 实战演习

~~~go
package main

import "fmt"

// 定义一个返回函数的函数
func returnDatabaseType() func() {
	return func() {
		fmt.Println("RDB(PostgreSQL)")
	}
}

// 返回函数带有参数的函数
func fetchDatabaseType() func(string) string {
	return func(name string) string {
		return "Database is " + name
	}
}

func main() {
	/////////////////////////////////////
	// 定义一个返回函数的函数，然后使用它
	resultFunc := returnDatabaseType()
	resultFunc()

	resultFunc2 := fetchDatabaseType()
	result := resultFunc2("MySQL")
	fmt.Println(result)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com