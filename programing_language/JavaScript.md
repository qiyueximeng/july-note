# JavaScript

JavaScript 是一种具有函数优先的轻量级，解释型（即时编译型）的编程语言。

是一种基于原型编程、多范式的动态脚本，支持面向对象、命令式及函数式（声明式）编程风格。

主要依赖于浏览器的 JS 解释器（如：V8）解释并执行，所以在浏览器的支持下，有很强的的跨平台特性；


## 特性

1. 解释型脚本语言：在程序运行的过程中逐行进行解释（V8 是所有解释完才执行）
2. 基于对象：JavaScript 中一切皆为对象，对象可通过原型关联
3. 弱类型：变量类型为弱类型，未对数据类型做严格要求，变量比较时有隐式类型转换的特点
4. 动态性：采用事件驱动，不需要通过服务器即可对用户输入做出响应
5. 跨平台：仅依赖浏览器的解释器，不依赖操作系统


## 组成

[ECMAScript](https://baike.baidu.com/item/ECMAScript)：描述了该语言的语法和基本对象；

[文档对象模型（DOM）](https://baike.baidu.com/item/%E6%96%87%E6%A1%A3%E5%AF%B9%E8%B1%A1%E6%A8%A1%E5%9E%8B)：描述处理网页内容的方法和接口；

[浏览器对象模型（BOM）](https://baike.baidu.com/item/BOM/1801)：描述与浏览器进行交互的方法和接口；


## 语法

### 变量声明

1. 不允许重复声明
2. 变量名限制为 字母、数字、下划线、$，且不能以数字开头
3. 关键词无法作为变量名

**let, const：**

1. 不存在变量提升
2. const 声明为常量，声明必须赋值，后值不可改变，对引用属性保留的是指针

**var：**

1. 存在声明提升，不存在赋值提升


### 顶层对象

浏览器环境中为 `window`，nodejs 中为 `global`


### 数据类型

string, number, boolean, null, undefined, object, symbol


### 关键词

1. if ... else ...
2. var, function, let, const, class
3. for ... in ... , for ... of , for ...
4. continue
5. break
6. debugger
7. while ... , do ... while ...
8. return
9. try ... catch ...
10. switch
11. // ... , /* ... */
12. this
13. throw
14. void

### 特殊字符

1. \b：退格键
2. \f：换页
3. \n：新行
4. \r：回车
5. \t：水平（Tab）制表符
6. \v：垂直制表符
7. \\'：单引号
8. \\"：双引号
9. \\\：反斜杠
10. \\xXX：由从00和FF的两位十六进制数字XX表示的Latin-1字符。例如，\ xA9是版权符号的十六进制序列
11. \\uXXXX：由四位十六进制数字XXXX表示的Unicode字符。例如，\ u00A9是版权符号的Unicode序列。见Unicode escape sequences (Unicode 转义字符)
12. \\u{XXXXX}：Unicode代码点 (code point) 转义字符。例如，\u{2F804} 相当于Unicode转义字符 \uD87E\uDC04的简写

### 运算符

多个运算符一起使用时要注意优先级，可通过小括号改变优先级

**赋值运算符：**

```
=, +=, -=, *=, **=, /=, %=,
&=, |=, ~=, ^=, <<=, >>=, >>>=
```

**算数运算符：**

`+, ++, -, --, *, **, /, %`

**比较运算符：**

`==, ===, !=, !==, >, >=, <, <=, ? ... :`

**逻辑运算符：**

`&&, ||, !`

**类型运算符：**

`typeof, instanceof`

通过 typeof 运算符得出的特殊值：
```
NaN - 'number'
array - 'object'
function - 'function'
null - 'object'
```

**位运算符：**

`&, |, ~, ^, <<, >>, >>>`

[位运算巩固](https://www.w3school.com.cn/js/js_bitwise.asp)

### 正则表达式

[正则表达式巩固](https://www.w3school.com.cn/js/js_regexp.asp)

## 内置对象

常用的几个为：

```
String, Number, Boolean, Symbol, Date, Math, RegExp, Promise, Proxy, Function, Array, Object, Error, JSON, Map, Set, parseInt, parseFloat, encodeURI, encodeURIComponent, decodeURI, decodeURIComponent, 
```


## 模块

```
export
export default
import
import ... from ...
import ... as ... from ...
import { ... as ... } from ...
import(...).then(Module => {})
```

## 要点

### this 关键词

1. 默认绑定：全局对象（如 window）或 undefined （严格模式）
2. 隐式绑定：函数所属对象
3. 显式绑定：通过 call 和 apply 将 this 指定到某个对象
4. 固定绑定：如箭头函数，call 和 apply 都不可改变

### 原型链

#### 继承

### 闭包

### 事件循环
