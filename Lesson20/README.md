通道的使用
==========

## 知识点

* 通道的使用 - channel

## 实战演习

~~~go
package main
import (
	"fmt"
	"strconv"
)
func main() {
	// 定义一个字符型的通道
	message := make(chan string)
	go func() {
		for i := 1; i <= 3; i++ {
            message <- (strconv.Itoa(i) + ".helo channel.")
		}
	}()
	// 接收通道发送的消息
	result := ""
	result = <-message
	fmt.Println(result)
	result = <-message
	fmt.Println(result)
	result = <-message
	fmt.Println(result)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com