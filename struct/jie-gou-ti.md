# 结构体

Go语言中的基础数据类型可以表示一些事物的基本属性，但是当我们想表达一个事物的全部或部分属性时，这时候再用单一的基本数据类型，就无法满足需求了。

Go语言提供了一种自定义数据类型：**结构体** `struct` ，可以封装多个基本数据类型。&#x20;

Go语言中通过`struct`来实现面向对象。

#### 结构体的定义

使用 `type` 和 `struct` 关键字来定义结构体：

```go
type 类型名 struct {
    字段名 字段类型
    字段名 字段类型
    …
}
```

例如我们定义一个 `Person` 结构体。同样类型的字段可以写在一行。

```go
type person1 struct {
	name, city string
	age        int8
}
```



#### 结构体的基本使用

```go
package main

import "fmt"

// 结构体

type person struct {
	name, gender string
	age          int
	hobby        []string
}

func main() {
	// 声明一个person类型的变量p
	var p person

	// 通过字段赋值
	p.name = "bingo"
	p.age = 9000
	p.gender = "男"
	p.hobby = []string{"🏀", "⚽️", "双色球"}
	fmt.Println(p)

	// 访问变量p的字段
	fmt.Printf("%T\n", p)
	fmt.Printf(p.name)
}
```
