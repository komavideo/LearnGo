并发协程再入门
=============

## 知识点

* 再入门异步协程 - go routines

## 实战演习

~~~go
package main
import (
	"os"
	"os/exec"
	"fmt"
	"time"
)

func sayHelo(id string) {
	i := 1
	for {
		fmt.Println("Helo SubGo", id, ":", i)
		i ++
		// 等待一秒
		time.Sleep(time.Second)
	}
}

// 主函数
func main() {
	cmd := exec.Command("clear")
	cmd.Stdout = os.Stdout
	cmd.Run()

	// sayHelo("1")
	go sayHelo("1")
	go sayHelo("2")

	// 主线程循环
	i := 100
	for {
		fmt.Println("Helo MainGo", ":", i)
		i ++
		// 等待一秒
		time.Sleep(time.Second)
	}
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com