错误处理
========

## 知识点

* Go语言的错误处理方式

## 实战演习

~~~go
package main
import (
    "fmt"
    "errors"
)
//-------------------------------------//
// 带错误返回值的函数
func f1(num int) (int, error) {
    if num < 0 {
        return -1, errors.New("参数错误")
    }
    return 2 * num, nil
}
//-------------------------------------//
// 定义一个错误结构体
type argError struct {
    arg  int
    msg string
}
// 定义结构体的错误函数(实现错误接口)
func (e *argError) Error() string {
    return fmt.Sprintf("%d -> %s", e.arg, e.msg)
}
func f2(num int) (int, error) {
    if num < 0 {
        return -1, &argError{num, "参数不能为负值"}
    }
    return 2 * num, nil
}
//-------------------------------------//
// 主函数
func main() {
    // f1
    result, err := f1(10)
    fmt.Println(result, err)
    result, err = f1(-10)
    fmt.Println(result, err)
    // f2
    result, err = f2(10)
    fmt.Println(result, err)
    result, err = f2(-10)
    fmt.Println(result, err)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
