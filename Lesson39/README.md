包的定义与引用
============

## 知识点

* 定义自己的包，然后在程序中使用它

## 实战演习

### /db/db.go

~~~go
package db

import "fmt"

const (
	ConnectString string = "127.0.0.1:..."
)

func ConnectDB() {
	fmt.Println("数据库连接...")
}

func CloseDB() {
	fmt.Println("数据库关闭。")
}
~~~

### /main.go

~~~go
package main

import (
	"./db"
	. "./db"
	d "./db"
	"fmt"
)

func main() {
	fmt.Println("Helo Go.")

	// 默认包引用写法
	fmt.Println(db.ConnectString)
	db.ConnectDB()
	db.CloseDB()

	// 自定义前缀写法
	d.ConnectDB()
	d.CloseDB()

	// 省略前缀写法
	ConnectDB()
	CloseDB()
}

~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com