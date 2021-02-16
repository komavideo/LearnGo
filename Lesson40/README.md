Go语言的测试 - test
==================

## 知识点

* 编写Go语言的测试代码，提高整体程序的健壮性

## 使用工具包

https://github.com/cweill/gotests

## 实战演习

```bash
$ go mod init komavideo.com/mywork
$ go get -u github.com/cweill/gotests/...
```

## 语言代码

### /utils/math.go

```go
package utils
func Add(x, y int) int {
	return x + y
}
```

### /main.go

```go
package main
import (
	"fmt"
	"komavideo.com/mywork/utils"
)
func main() {
	fmt.Println(utils.Add(10, 20))
}
```

```bash
$ go run main.go
```

## 编写测试代码 - /utils/math_test.go

### 手动编写

```go
package utils
import "testing"
func TestAdd1(t *testing.T) {
	val := Add(10, 20)
	if val != 0 {
		t.Error("计算错误", val)
	}
}
```

```bash
$ go test -v ./utils
```

### 自动编写

```
>Command+Shift+P
>Go:Generate Unit Tests For Function
```

```go
...
// TODO: Add test cases.
{
	name: "正常处理",
	args: args{x: 10, y: 20},
	want: 30,
},
// {
// 	name: "错误处理",
// 	args: args{x: 10, y: 20},
// 	want: 40,
// },
...
```
## 测试代码

```bash
# 测试当前文件夹
$ go test -v ./
# 测试指定文件夹
$ go test -v ./utils
# 测试当前所有子文件夹
$ go test -v ./...
# 测试输出包含代码覆盖率
$ go test -v -cover ./...
```

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com