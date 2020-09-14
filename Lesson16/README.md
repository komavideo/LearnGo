结构体方法
==========

## 知识点

* 为结构体定义专用的方法

## 实战演习

~~~go
package main
import "fmt"
// 定义矩形结构体
type rect struct {
    width, height int
}
// 为 rect 结构体定义计算面积方法 area(), 参数为指针类型
func (r *rect) area() int {
	return r.width * r.height
}
// 为 rect 结构体定义计算周长的方法 perim(), 参数为值类型
func (r rect) perim() int {
	return 2 * (r.width + r.height)
}

func main() {
    // 定义一个矩形结构体变量
	r := rect{width: 10, height: 4}
	// 分别调用计算面积和周长的方法
	fmt.Println("area: ", r.area())
	fmt.Println("perim:", r.perim())

    // 指针方式调用
	rp := &r
	fmt.Println("area: ", rp.area())
	fmt.Println("perim:", rp.perim())
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
