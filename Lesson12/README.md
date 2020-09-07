函数的使用
==========

## 知识点

* 函数的定义
* 多返回值函数
* 可变参数函数

## 实战演习

~~~go
package main
import "fmt"
// a+b
func plus2(a int, b int) int {
    return a + b
}
// a+b+c
func plus3(a, b, c int) int {
    return a + b + c
}
// 四则计算：计算两个值的加减乘除结果，返回多个值
func calABCD(a, b int) (int, int, int, int) {
	return a+b, a-b, a*b, a/b
}
// 可变参数函数：合计参数值
func sum(nums ...int) int {
    fmt.Print(nums, " ")
    total := 0
    for _, num := range nums {
        total += num
    }
    return total
}
// 主函数
func main() {
	// 两个数相加
    result := plus2(10, 20)
	fmt.Println("10+20=", result)
	// 三个数相加
    result = plus3(10, 20, 30)
	fmt.Println("10+20+30=", result)
	// 两个数计算加减乘除
	a, b, c, d := calABCD(200, 100)
	fmt.Println("ab四则计算=", a,b,c,d)
	// 可变参数函数计算合集
	result = sum(1,2,3,4,5,6,7,8,9,10)
	fmt.Println("1-10合计为=", result)
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
