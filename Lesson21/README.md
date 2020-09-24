循环接收通道内容
==============

## 知识点

* 循环接收通道内容，直到退出

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
		for i := 1; i <= 5; i++ {
			if i == 5 {
				message <- ""
			} else {
				message <- (strconv.Itoa(i) + ".helo channel.")
			}
		}
	}()
	// 接收通道发送的消息
	for result := range message {
		if result == "" {
			break
		} else {
			fmt.Println(result)
		}
	}
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
