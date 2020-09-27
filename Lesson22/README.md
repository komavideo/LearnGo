通道缓冲区
==========

## 知识点

* 带缓冲区的通道 - Channel Buffering

## 实战演习

~~~go
package main
import "fmt"
func main() {
	// 建立有3个缓冲区的通道，即缓冲区消息达到3个时会阻塞当前线程
	message := make(chan string, 2) // 如果是2的话，系统会报错，因为线程阻塞死锁

	// 发送消息
	message <- "消息1"
    message <- "消息2"
	message <- "消息3"

	// 接收消息
	fmt.Println(<-message)
	fmt.Println(<-message)
	fmt.Println(<-message)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com