# Grammar

## 标识符 identifier

* 所有基本数据类型的名称
* 接口类型 error
* 常量 true, false 和 iota
* 所有内建函数的名称: 
append, cap, close, complex, copy, delete, imag, len
make, new, panic, print, println, real, recover, _(空占位符)

## 关键字 keyword
* 程序声明关键字：import, package
* 程序实体声明和定义: chan(channel), const, func, interface，map, struct, type and var
* 程序流程控制:
go, select, break, case, continue, default, defer, else, fallthrough, for, goto, if, range, return and switch

## 字面量 literal
字面量是值的一种标记法

* 用于表示基础数据类型值的各种字面量， 例如 12E-3
* 用于构造各种自定义的复合数据类型的类型字面量， 例如

```
type User struct {
    Username string
    Password string
}
```

* 用于表示复合数据类型的值的复合字面量， 它可以用来构造 struct, array, slice, and map 类型的值
复合字面量一般由字面类型以及被花括号包裹的复合元素的列表组成， 字面类型指的就是复合数据类型的名称

```
User { Username: "walter", Password: "pass"}
```

## 表达式 Expression

* 选择表达式: `context.Speaker`
* 索引表达式: `array1[1]`
* 切片表达式: `slice1[0:2]`
* 类型断言: v1.(I1) // v1 是否符合接口 I1
* 调用表达式: v1.M1 // 调用 v1 的 M1 方法

## 操作符 operator

也称运算符， 共有 21 个, 分为
* 算术运算符: +, -, *, /
* 比较运算符: ==, !=, <, <=, >, >=
* 逻辑操作符: ||, &&, ...
* 地址操作符
* 接收操作符： <-

## 基本类型
1. bool
1. byte
1. rune: 存储 unicode 字符，可以看作一个 32 位有符号整数 int32, 亦可表示一些特殊的转义符
1. int: int8/uint8 ~ int64/uint64 
1. float32, float64
1. complex64, complex128
1. string

## 高级类型

1. 数组

```
var ipv4 [4]uint8{1, 2, 3, 4}
```

2. 切片

切片可以看作是一种对数组的包装形式， 它包装的数组称为该切片的的底层数组

```
var ips = []string{"Alice", "Bob", "Carl"}
```

3. 字典

例如声明一个 map, key是string 类型， value 是 bool 类型
```
var featureToggles = map[string]bool{}
```

4. 函数和方法

```
func divide(dividend int divisor int)(result int, err error) {
    if divisor == 0 {
        err = errors.New("division by zeor")
        return
    }

    result = dividend/divisor
    return
}
```

方法是函数的一种， 实际上是与某个数据类型关联在一起的函数， 分为值方法和指针方法
这个要仔细看看

5. 接口

接口用于定义一组行为， 其中每个行为都由一个方法声明表示

```
type Talk interface {
    Hello(username string) string
}
```

6. 结构体

```

```

## 流程控制

if, switch, 
for, break, continue
defer
select
go
