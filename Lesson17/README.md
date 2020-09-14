接口的使用
==========

## 知识点

* 接口的使用, 实现对象的多态性

## 实战演习

~~~go
package main
import (
    "fmt"
    "math"
    "reflect"
)
// 定义一个几何图形接口
type geometry interface {
    area() float64
    perim() float64
}
// 定义一个矩形结构体
type rect struct {
    width, height float64
}
// 定义一个圆形结构体
type circle struct {
    radius float64
}
// 矩形计算面积
func (r rect) area() float64 {
    return r.width * r.height
}
// 矩形计算周长
func (r rect) perim() float64 {
    return 2 * (r.width * r.height)
}
// 圆形计算面积
func (c circle) area() float64 {
    return math.Pi * c.radius * c.radius
}
// 圆形计算周长
func (c circle) perim() float64 {
    return 2 * math.Pi * c.radius
}
// 计算函数，参数为几何图形接口类型
func measure(g geometry) {
    fmt.Println(reflect.TypeOf(g), g)
    fmt.Println(g.area())
    fmt.Println(g.perim())
}

func main() {
    // 声明一个矩形
    r := rect{width: 4, height: 5}
    // 声明一个圆形
    c := circle{radius: 10}
    // 用measure函数计算矩形面积和周长
    measure(r)
    // 用measure函数计算圆形面积和周长
    measure(c)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
