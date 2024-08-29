# JS 语法
## JavaScript 字面量
&emsp; **Number:**

* 3.14
* 1001
* 123e5

&emsp; **String**

* "This is a string"
* 'This is also a string'

&emsp; **表达式字面量**

* 5 + 6
* 5 * 10

&emsp; **Array**

* [40, 100, 1, 5, 25]

&emsp; **Object**

* {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}

&emsp; **Function**

* function myFunction(a, b) { return a * b;}

## JavaScript 变量
&emsp;JavaScript 使用关键字 var 来定义变量， 使用等号来为变量赋值:

```js
var x, length
x = 5
length = 6
```
&emsp;**变量可以通过变量名访问。在指令式语言中，变量通常是可变的。字面量是一个恒定的值。**
> 变量是一个名称。字面量是一个值。

### JavaScript 操作符

&emsp;JavaScript使用 算术运算符 来计算值:
```js
(5 + 6) * 10
```
&emsp;JavaScript使用赋值运算符给变量赋值：

```js
x = 5;
y = 6;
z = (x + y) * 10;
```
### JavaScript 语句

&emsp;在 HTML 中，JavaScript 语句用于向浏览器发出命令。
&emsp;语句是用分号分隔：
```js
x = 5 + 6;
y = x * 10;
```

### JavaScript 注释

&emsp;不是所有的 JavaScript 语句都是"命令"。双斜杠 // 后的内容将会被浏览器忽略：
```js
// this is a comment
```
### JavaScript 数据类型

&emsp;JavaScript 有多种数据类型：数字，字符串，数组，对象等等：
```js
var length = 16;                                  // Number 通过数字字面量赋值 
var points = x * 10;                              // Number 通过表达式字面量赋值
var lastName = "Johnson";                         // String 通过字符串字面量赋值
var cars = ["Saab", "Volvo", "BMW"];              // Array  通过数组字面量赋值
var person = {firstName:"John", lastName:"Doe"};  // Object 通过对象字面量赋值
```
### JavaScript 字母大小写

&emsp;JavaScript 对大小写是敏感的。

&emsp;当编写 JavaScript 语句时，留意是否关闭大小写切换键。

&emsp;函数 getElementById 与 getElementbyID 是不同的。

&emsp;同样，变量 myVariable 与 MyVariable 也是不同的

