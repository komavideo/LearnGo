通道协作，主从配合 - chan
=======================

## 知识点

* 使用通道方式协作主从线程的合作

## 实战演习

~~~go
package main

import (
	"fmt"
	"time"
)

func worker(p_name string, p_chan chan int) {
	for {
		val, ok := <-p_chan
		if ok {
			fmt.Println(p_name, val, ok)
		} else {
			break
		}
	}
}

// 主函数
func main() {
	fmt.Println("Helo Go.")

	// 定义通道
	chan1 := make(chan int)
	chan2 := make(chan int)
	defer close(chan1)
	defer close(chan2)

	// 定义通道处理协程
	go worker("工人", chan1)
	go worker("秘书", chan2)

	// 主线程处理业务逻辑，并向通道发送消息协作处理
	i := 1
	for i <= 5 {
		// 分别向通道发送消息
		chan1 <- i
		chan2 <- i + 100
		i++
		time.Sleep(time.Second)
	}
	fmt.Println("End...")
	time.Sleep(time.Second)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com