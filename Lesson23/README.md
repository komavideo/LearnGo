通道同步
==========

## 知识点

* 通道同步处理方式 - Channel Synchronization

## 实战演习

~~~go
package main
import (
	"fmt"
	"time"
)
func action(done chan bool) {
	fmt.Println("Loading...")
	time.Sleep(2 * time.Second)
	fmt.Println("Finished.")
	// 逻辑执行完后，发送通道消息
	done <- true
}
func main() {
	done := make(chan bool)
	go action(done)
	// 等待通道消息
	<-done
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com