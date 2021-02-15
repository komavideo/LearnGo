构造体与集合
==========

## 知识点

* 建立构造体和构造体的集合属性

## 实战演习

~~~go
package main

import (
	"fmt"
)

type Book struct {
	title  string
	author string
	price  int
}

type BookStore struct {
	BookList []*Book
}

// 主函数
func main() {
	fmt.Println("Helo Go.")

	book1 := Book{title: "Vue的心得", author: "尤大婶", price: 20}
	book2 := Book{title: "Node.js入门", author: "小马", price: 25}
	book3 := Book{title: "高性能Go语言", author: "Koma", price: 22}

	bookStore := BookStore{}
	bookStore.BookList = append(bookStore.BookList, &book1, &book2, &book3)

	fmt.Println(bookStore)
	for i, book := range bookStore.BookList {
		fmt.Println(i, book)
	}
}
~~~

## 课程文件

https://github.com/komavideo/LearnGo

## 小马视频频道

http://komavideo.com