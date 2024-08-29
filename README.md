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

### 对代码行进行折行

&emsp;您可以在文本字符串中使用反斜杠对代码行进行换行。下面的例子会正确地显示：
```js
document.write("你好 \
世界!");
```

## JavaScript 数据类型

&emsp;**值类型(基本类型):** 字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）、Symbol。
&emsp;**引用数据类型（对象类型）：** 对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）。

![DataType](./images/Javascript-DataType.png)

> **注：** Symbol 是 ES6 引入了一种新的原始数据类型，表示独一无二的值。


### JavaScript 拥有动态类型

&emsp;JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：
```js
var x;               // x 为 undefined
var x = 5;           // 现在 x 为数字
var x = "John";      // 现在 x 为字符串
```

&emsp;变量的数据类型可以使用 `typeof` 操作符来查看：
```js
typeof "John"                // 返回 string
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
```
&emsp;**More example**
```js
//sring
var carname1 = "example1";
var carname2 = 'example2';
//number
var x1 = 10.20;
var x2 = 123e-5;
//bool
var situation1 = true;
var situation2 = false;
//array
var cars1 = new Array();
cars1[0] = "element1";
cars1[1] = "element2";
cars1[2] = "element3";
var cars2 = ["element1", "element2", "element3"];
var cars3 = new Array("element1", "element2", "element3");
//object
var person={firstname:"John", lastname:"Doe", id:5566};
var person2 = {
        firstname : "John",
        lastname  : "Doe",
        id        :  5566
};
cars1 = null;
```
### JavaScript 对象

&emsp;**JavaScript 对象是拥有属性和方法的数据。**

<table style="border:solid; background-color:white; color:black">
    <tr style="border:solid; background-color:gray; color:white;border-color:black">
        <td style = "border:solid; border-color:black;">对象</td>
        <td style = "border:solid; border-color:black;">属性</td>
        <td style = "border:solid; border-color:black;">方法</td>
    </tr>
    <tr>
        <td rowspan="4" style = "border:solid; border-color:black;"><img src="./images/car.gif"></td>
        <td style = "border:solid; border-color:black;">car.name = Flat</td>
        <td style = "border:solid; border-color:black;">car.start()</td>
    </tr>
    <tr>
        <td style = "border:solid; border-color:black;">car.model = 500</td>
        <td style = "border:solid; border-color:black;">car.drive()</td>
    </tr>
    <tr>
        <td style = "border:solid; border-color:black;">car.weight = 850kg</td>
        <td style = "border:solid; border-color:black;">car.brake()</td>
    </tr>
    <tr>
        <td style = "border:solid; border-color:black;">car.color = white</td>
        <td style = "border:solid; border-color:black;">car.stop()</td>
    </tr>
</table>

&emsp;所有汽车都有这些属性，但是每款车的属性都不尽相同。

&emsp;所有汽车都拥有这些方法，但是它们被执行的时间都不尽相同。


### JavaScript 几乎所有的事物都是对象

> JavaScript 对象是变量的容器。

### 对象定义

&emsp;你可以使用字符来定义和创建 JavaScript 对象:

```js
var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```
&emsp;
```js
var person = {
    firstName:"John",
    lastName:"Doe",
    age:50,
    eyeColor:"blue"
};
```

### 对象属性

&emsp;可以说 "JavaScript 对象是变量的容器"。

&emsp;但是，我们通常认为 "JavaScript 对象是键值对的容器"。

&emsp;键值对通常写法为 name : value (键与值以冒号分割)。

&emsp;键值对在 JavaScript 对象通常称为 **对象属性**。

> 	JavaScript 对象是属性变量的容器

### 访问对象属性

```js
person.lastName; // first way to access an attribute of an object
person["lastName"]; //second way to access an attribute of an object
```

### 对象方法

&emsp;对象的方法定义了一个函数，并作为对象的属性存储。

&emsp;对象方法通过添加 () 调用 (作为一个函数)。

&emsp;该实例访问了 person 对象的 fullName() 方法:
```html
<p id="demo"></p>
<script>
var person = {
    firstName: "John",
    lastName : "Doe",
    id : 5566,
    fullName : function() {
       return this.firstName + " " + this.lastName;
    }
};
document.getElementById("demo").innerHTML = person.fullName();
```

> 	JavaScript 对象是属性和方法的容器。

### 访问对象方法

&emsp;可以使用以下语法创建对象方法：
```js
methodName : function() {
    // 代码 
}
```

&emsp;可以使用以下语法访问对象方法：
```js
objectName.methodName()
```

## JavaScript 函数
