并发编程 - 协程
=============

## 知识点

* 协程Goroutines的使用方法

## 实战演习

~~~go
package main
import (
	"os"
	"os/exec"
	"fmt"
	"time"
)
func sayHelo(name string) {
	for i := 1; i <= 5; i++ {
		fmt.Println("Helo", name, ":", i)
	}
}

// 主函数
func main() {
	cmd := exec.Command("clear")
	cmd.Stdout = os.Stdout
	cmd.Run()
	// 同步执行函数
	sayHelo("koma")
	// 异步执行函数
	go sayHelo("xiaoma")
	go sayHelo("iphone")
	go sayHelo("ipad")
	go sayHelo("swiftui")
	// 匿名函数，异步执行
	go func(msg string) {
		fmt.Println("this is a", msg)
	}("lesson")
	// 等待一秒
	time.Sleep(time.Second)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com