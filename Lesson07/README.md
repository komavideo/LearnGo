Switch分支
==========

## 知识点

* Go语言Switch分支语法

## 实战演习

~~~go
package main

import (
    "fmt"
    "time"
)

func main() {

    player_level := 1
    switch player_level {
    case 1:
        fmt.Println("勒布朗，字母歌，库里")
    case 2:
        fmt.Println("莱纳德，杜兰特，哈登")
    case 3:
        fmt.Println("欧文，利拉德，乔治")
    case 4, 5, 6:
        fmt.Println("角色群")
    default:
        fmt.Println("板凳群")
    }

    switch time.Now().Weekday() {
    case time.Saturday, time.Sunday:
        fmt.Println("来了来了，周末来了")
    default:
        fmt.Println("哭吧哭吧")
    }

    t := time.Now()
    switch {
    case t.Hour() < 12:
        fmt.Println("上午：跑步")
    default:
        fmt.Println("下午：喝茶")
    }
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
