# 1.基本数据类型

## 1.typeof运算符

​	来检查一个变量的类型

语法：   	

```js
typeof 变量
```

检查字符串时，会返回string。

## 2.Number.MAX_VALUE

显示数字的最大值（即取值范围）

1.

如果使用Number表示的数字超过了最大值，则会返回一个Infinity（无穷）

使用typeof检查infinity时也会返回Number

2.

```js
a = "abc" *"abc"
```

返回NaN

NaN是一个特殊字面量，表示No one Number。

## 3.Number.MIN_VALUE

返回"5e-324"。

如果使用js进行浮点元素，可能会得到一个不精确的结果。

例子：

```js
var c= 0.1+0.2
```

返回0.300000000004。



## 4.null类型

只有一个值，就是null，专门用来表示一个为空的对象。



## 5.undefined类型

当声明一个变量，但是并不给变量赋值时，他的值就是undefined。

## 总结

一共有六种数据类型。

String    字符串

Number     数值

Boolean      布尔值

Null       空值

Undefined      未定义

||上述是五种基本数据类型

object    对象

# 2.强制类型转换

 类型转换主要是指，将其他的数据类型，转换为  String Number Boolean

### 调用为String

方法一：

调用被转换数据类型的toString（）方法。

```js
//调用a的toString（）方法，

//即xxx的yyy()方法，就是xxx.yyy()方法
```

该方法不会影响到原变量，它会将转换的结果返回。

但是注意：null和undefined这两个值没有toString方法，如果调用他们的方法，会报错。



方法二：

调用String()函数，并将被转换的数据作为参数传递给函数。

```js
let a = String(a);
```

null和undefined这两个值可以转换，直接转出（null）和（undefined）；



### 调用为number

转换方式一：

使用Number（）函数；如String（）函数。	

​		若是纯数字字符串，则可以直接转换为数字。

​		若有非数字内容，则输出为NaN。

​		若字符串是空串或这为空格，输出为0。

布尔-->数字

​		true--> 1

​		false --> 0

​		

​		null -- > 0

​		undefined -- > NaN



转换方式二；

专门对付字符串

​		parseInt（）把字符串转换为一个整数。

将一个字符串中的有效的整数内容取出来，然后转换为number

​		parseFloat（）把一个字符串转换为浮点数。

它可以去除有效的小数内容，然后转出来。

对非String使用，会先转换为String然后在操作。

## 自增和自减

### 自增：

分为a++和++a；变量会 立即加一。

不同的是，a++和++a的值不同。

a++等于原变量的值（自增前的值）。

++a的值等于新值（自增后的值）。

### 自减：

通过自减可以是变量在自身的基础上减一。

同上，自增的变化。 