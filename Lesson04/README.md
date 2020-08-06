定义常量
========

## 知识点

* 定义Go语言中的常量

## 实战演习

~~~go
package main
import (
    "fmt"
    "math"
)
const message string = "多事之秋2020"
func main() {
    fmt.Println(message)
    //error:cannot assign to message
    // message = "明年会更好"

    const a = 100
    const b = 200 / a
    fmt.Println(a, b)
    fmt.Println(int64(a/b))

    fmt.Println(math.Pi)
    fmt.Println(math.Sin(math.Pi / 6))
    fmt.Println(math.Cos(math.Pi / 3))
    fmt.Println(math.Tan(math.Pi / 4))
}
~~~

## math

```go
const (
    E   = 2.71828182845904523536028747135266249775724709369995957496696763 // https://oeis.org/A001113
    Pi  = 3.14159265358979323846264338327950288419716939937510582097494459 // https://oeis.org/A000796
    Phi = 1.61803398874989484820458683436563811772030917980576286213544862 // https://oeis.org/A001622

    Sqrt2   = 1.41421356237309504880168872420969807856967187537694807317667974 // https://oeis.org/A002193
    SqrtE   = 1.64872127070012814684865078781416357165377610071014801157507931 // https://oeis.org/A019774
    SqrtPi  = 1.77245385090551602729816748334114518279754945612238712821380779 // https://oeis.org/A002161
    SqrtPhi = 1.27201964951406896425242246173749149171560804184009624861664038 // https://oeis.org/A139339

    Ln2    = 0.693147180559945309417232121458176568075500134360255254120680009 // https://oeis.org/A002162
    Log2E  = 1 / Ln2
    Ln10   = 2.30258509299404568401799145468436420760110148862877297603332790 // https://oeis.org/A002392
    Log10E = 1 / Ln10
)
```

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com
