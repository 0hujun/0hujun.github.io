---
title: "编码语言语法与使用对比"
permalink: /languages
---

# 编码语言语法与使用对比

【2025-02-27】

## 1 基本语法

### 1.1 变量

#### 1.1.1 变量定义和声明

| 语言   | 说明     | 定义        | 声明        |
| ------ | -------- | ----------- | ----------- |
| Go     |          | `var x int` | `x := 100`  |
| Python | 动态语言 | x = 0       | x = 100     |
| C      |          | int x       | int x = 100 |
| Java   |          | int x       | int x = 100 |
| Shell  | 脚本语言 | x=100       | x=100       |

#### 1.1.2 整型变量

#### 1.1.3 浮点型变量

#### 1.1.4 字符型变量

### 1.2 常量

#### 1.2.1 常量定义和声明

### 1.3 普通语句

#### 1.3.1 普通语句编写

| 语言   |                                          |      |
| ------ | ---------------------------------------- | ---- |
| Go     | `x := "hw"` <br/>`fmt.Println(x)`        |      |
| Python | `x = 'hw'`<br/>`print(x)`                |      |
| Shell  |                                          |      |
| C      | chars x=[]{"hw"};<br/>printf("%s\n", x); |      |
| Java   |                                          |      |





### 1.4 判断语句

#### 1.4.1 Go

```go
func main() {
    x := 100
    if x > 100 {
        fmt.Println("1000")
    } else if x == 100 {
        fmt.Println("100")
    } else {
        fmt.Println("0")
    }
}
```

#### 1.4.2 Python

```python
def main():
    x = 100
    if x > 100:
        print("1000")
    elif x == 100:
        print("100")
    else:
        print("0")

if __name__ == '__main__':
    main()
```

#### 1.4.3 Shell

```shell
function main() 
{
	x=100
	if [ $x > 100 ]; then
		echo '1000'
	elif [ $x == 100 ]; then
		echo '100'
	else
		echo '0'
	fi
}
main
```

#### 1.4.4 C

```

```



#### 1.4.5 Java

```

```



### 1.5 循环语句

#### 1.5.1 Go

```
func main() {

}
```

#### 1.5.2 Python

```

```



### 1.6 Switch语句

### 1.7 Break与Continue

## 2 集合与容器

### 2.1 数组、切片、列表

### 2.2 集合

### 2.3 Hash、Map、字典

#### 2.3.1 定义、声明、删除

#### 2.3.2 加入元素

#### 2.3.3 遍历元素

#### 2.3.3.1 Go

```

```

#### Python

```python 
def dict_demo():
	d = {}
    d['m5'] = '2018'
    d['m6'] = '2019'
    d['meta10.4'] = '2020'
    for pad_type, sell_year in pad_products.items():
        print(f"{pad_type}: {sell_year}")
    d.remove('m6')
    del pad_products
```



#### 2.3.4 删除元素

```

```

