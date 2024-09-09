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

&emsp;函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块:
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>example of a function in JS</title>
        <script>
            function myFunction() {
                alert("Hello World!");
            }
        </script>
    </head>
    
    <body>
        <button onclick="myFunction()">click</button>
    </body>
</html>
```

### JavaScript 函数语法
&emsp;函数就是包裹在花括号中的代码块，前面使用了关键词 function：
```js
function functionname() {
    // 执行代码
}
```
&emsp;当调用该函数时，会执行函数内的代码。

&emsp;可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用

> 	JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。

### 调用带参数的函数

&emsp;在调用函数时，可以向其传递值，这些值被称为参数。

&emsp;这些参数可以在函数中使用。

&emsp;可以发送任意多的参数，由逗号 (,) 分隔：

&emsp; **Example:** `myFunction(argument1,argument2)`

&emsp;当声明函数时，把参数作为变量来声明：

```js
function myFunction(var1,var2) {
    代码
}
```
> 变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。

&emsp;**Example:**
```html
<p>点击这个按钮，来调用带参数的函数。</p>
<button onclick="myFunction('Harry Potter','Wizard')">点击这里</button>
<script>
    function myFunction(name,job){
        alert("Welcome " + name + ", the " + job);
    }
</script>
```
### 带有返回值的函数

&emsp;有时，我们会希望函数将值返回调用它的地方。

&emsp;通过使用 `return` 语句就可以实现。

&emsp;在使用 `return` 语句时，函数会停止执行，并返回指定的值。

```js
function myFunction() {

    var x=5;
    return x;
}
```

> 整个 JavaScript 并不会停止执行，仅仅是函数。JavaScript 将继续执行代码，从调用函数的地方。

&emsp;函数调用将被返回值取代：`var myVar=myFunction();`

### 局部 JavaScript 变量

&emsp;在 JavaScript 函数内部声明的变量（使用 var）是**局部变量**，所以**只能在函数内部访问它**。（该变量的作用域是局部的）。

&emsp;可以在不同的函数中使用名称相同的局部变量，因为只有声明过该变量的函数才能识别出该变量。

&emsp;只要函数运行完毕，本地变量就会被删除。

### 全局 JavaScript 变量

&emsp;在函数外声明的变量是全局变量，网页上的所有脚本和函数都能访问它。

###  JavaScript 变量的生存期

&emsp;JavaScript 变量的生命期从它们被声明的时间开始。

&emsp;局部变量会在函数运行以后被删除。

&emsp;全局变量会在页面关闭后被删除

### 向未声明的 JavaScript 变量分配值

&emsp;<strong style="color:rgb(230, 230, 250); background-color:rgb(72, 90, 205);">如果您把值赋给尚未声明的变量，该变量将被自动作为 window 的一个属性</strong>

&emsp;Example: `carname="Volvo";`

&emsp;<strong style="color:rgb(230, 230, 250); background-color:rgb(72, 90, 205);">将声明 window 的一个属性 carname。</strong>

&emsp;<strong style="color:rgb(230, 230, 250); background-color:rgb(72, 90, 205);">非严格模式下给未声明变量赋值创建的全局变量，是全局对象的可配置属性，可以删除。</strong>

```js
var var1 = 1; // 不可配置全局属性
var2 = 2; // 没有使用 var 声明，可配置全局属性

console.log(this.var1); // 1
console.log(window.var1); // 1 所有数据变量都属于 window 对象。
console.log(window.var2); // 2

delete var1; // false 无法删除
console.log(var1); //1

delete var2; 
console.log(delete var2); // true
console.log(var2); // 已经删除 报错变量未定义
```

## JavaScript 作用域

&emsp;作用域是可访问变量的集合

&emsp;在 JavaScript 中, 对象和函数同样也是变量。

&emsp;在 JavaScript 中, **作用域为可访问变量，对象，函数的集合**。

&emsp;JavaScript 函数作用域: **作用域在函数内修改**。

### JavaScript 局部作用域

&emsp;变量在函数内声明，变量为局部变量，具有局部作用域。

&emsp;局部变量：只能在函数内部访问。

```js
// 此处不能调用 carName 变量
function myFunction() {
    var carName = "Volvo";
    // 函数内可调用 carName 变量
}
```

&emsp;因为局部变量只作用于函数内，所以不同的函数可以使用相同名称的变量。

&emsp;局部变量在函数开始执行时创建，函数执行完后局部变量会自动销毁。

### JavaScript 全局变量

&emsp;变量在函数外定义，即为全局变量。

&emsp;全局变量有 全局作用域: 网页中所有脚本和函数均可使用


```js
var carName = " Volvo";
// 此处可调用 carName 变量
function myFunction() {
    // 函数内可调用 carName 变量
}
```
<strong style="border:solid; border-color:gray; color:rgb(230, 230, 250); background-color:rgb(72, 90, 205);">如果变量在函数内没有声明（没有使用 var 关键字），该变量为全局变量。以下实例中 carName 在函数内，但是为<em style="color:yellow">全局变量</em>。</strong>

```js
// 此处可调用 carName 变量
function myFunction() {
    carName = "Volvo";
    // 此处可调用 carName 变量
}
```

### JavaScript 变量生命周期

&emsp;JavaScript 变量生命周期在它声明时初始化。

&emsp;局部变量在函数执行完毕后销毁。

&emsp;全局变量在页面关闭后销毁。

### ⌊函数参数

&emsp;函数参数只在函数内起作用，是局部变量。

### HTML 中的全局变量

&emsp;在 HTML 中, `全局变量是 window 对象`，所以 window 对象可以调用函数内的未声明（未加 var)的局部变量。

&emsp;**注意：** 所有数据变量都属于 `window` 对象。

> 	你的全局变量，或者函数，可以覆盖 window 对象的变量或者函数。
局部变量，包括 window 对象可以覆盖全局变量和函数。


&emsp;在 JavaScript 中，函数内部的局部变量通常不可以直接被外部作用域访问，但有几种方式可以将函数内的局部变量暴露给外部作用域，具体如下：

* 通过全局对象：在函数内部，可以通过将局部变量赋值给 window 对象的属性来使其成为全局可访问的。例如，使用 window.a = a; 语句，可以在函数外部通过 window.a 访问到这个局部变量的值。
* 定义全局变量：在函数内部不使用 var、let 或 const 等关键字声明变量时，该变量会被视为全局变量，从而可以在函数外部访问。但这种做法通常不推荐，因为它可能导致意外的副作用和代码难以维护。
* 返回值：可以通过在函数内部使用 return 语句返回局部变量的值，然后在函数外部接收这个返回值。这样，虽然局部变量本身不会被暴露，但其值可以通过函数调用传递到外部。
* 闭包：JavaScript 中的闭包特性允许内部函数访问外部函数的局部变量。即使外部函数执行完毕后，其局部变量仍然可以被内部函数引用。
* 属性和方法：定义在全局作用域中的变量和函数都会变成 window 对象的属性和方法，`因此可以在调用时省略 window，直接使用变量名或函数名。`

## JavaScript 事件

### HTML事件

&emsp;HTML事件是发生在HTML元素上的事情.

&emsp;当在HTML页面中使用 JavaScript时, JS可以触发这些事件

&emsp;HTML事件可以是浏览器的行为, 也可以是用户行为.

&emsp;一下是HTML事件的实例:

* HTML页面完成加载
* HTMLinput字段改变时
* HTML 按钮被点击

&emsp;通常, 当事件发生时, 我们可以让事件触发事执行JS代码.

&emsp;HTML元素中可以添加事件属性, 使用JS代码来添加HTML元素.

&emsp;单引号:
```js
<some-HTML-element some-event='JS code'>
```

&emsp;双引号:
```js
<some-HTML-element some-event="JS code">
```

&emsp;当点击按钮, 改变demo标签的值为Date()的返回值:
```js
<button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
```
&emsp;在这个例子中, 代码将修改自身元素的内容(使用`this`):
```js
<button onclick="this.innerHTML=Date()">现在的时间是?</button>
```

### 常见的HTML事件

&emsp;下面是一些常见的HTML事件的列表:

<table>
    <tr>
        <td>事件</td>
        <td>描述</td>
    </tr>
    <tr>
        <td>onchange</td>
        <td>HTML元素改变</td>
    </tr>
    <tr>
        <td>onclick</td>
        <td>用户点击HTML元素</td>
    </tr>
    <tr>
        <td>onmouseover</td>
        <td>鼠标指针移动到指定的元素上时发生</td>
    </tr>
    <tr>
        <td>onmouseout</td>
        <td>用户从一个HTML元素上移开鼠标时发生</td>
    </tr>
    <tr>
        <td>onkeydown</td>
        <td>用户按下键盘按键</td>
    </tr>
    <tr>
        <td>onload</td>
        <td>浏览器已完成页面的加载</td>
    </tr>
</table>

## JavaScript 字符串

&emsp;JS字符串用于存储和处理文本.

### 字符串长度

&emsp;可以直接使用内置属性`length`来计算字符串的长度`var str="test"; var len=str.length`

### 字符串可以是对象

&emsp;通常, JS字符串是原始值, 可以使用字符创建: `var firstName1 = "John"`

&emsp;我们也可以使用`new`关键字将字符串定义为一个对象: `var firstName2= new String("John")`

> 最好不要创建 `String` 对象. 它会拖慢执行速度, 并可能产生其他副作用:<br>例如上面的两个例子, 如果我们查看`(firstName1 === firstName2)`的结果, 会发现为`false` 因为**一个字符串和一个对象不相等**

> 注意: `===` 三个等号为绝对相等, 即数据类型与值必须相等

### 字符串属性和方法

&emsp;原始值字符串, 如"John", 没有属性和方法(因为他们不是对象).

&emsp;原始值可以使用 JavaScript 的属性和方法, 因为JavaScript在执行方法和属性时可以把原始值当做对象.

### 字符串属性

&emsp; constructor => 返回创建字符串属性的函数

&emsp; length => 返回字符串的长度

&emsp; prototype => 允许我们向对象添加属性和方法

### 字符串方法

&emsp; charAt() => 返回指定索引位置的字符

&emsp; charCodeAt() => 返回指定索引位置字符的 Unicode 值

&emsp; concat() => 连接两个或多个字符串, 返回连接后的字符串

&emsp; fromCharCode() => 将 Unicode 转换为字符串

&emsp; indexOf() => 返回字符串中检索指定字符第一次出现的位置

&emsp; lastindexOf() => 同上

&emsp; localCompare() => 用本地特定的顺序来比较两个字符串

&emsp; match() => 找到一个或多个正则表达式的匹配

&emsp; replace() => 替换与正则表达式匹配的字符串

&emsp; search() => 检索与正则表达式相匹配的值

&emsp; slice() => 提取字符串的片段, 并在新的字符串中返回被提取的部分

&emsp; split() => 把字符串分割为字符串数组

&emsp; substr() => 从起始索引号提取字符串中指定数目的字符

&emsp; substring() => 提取字符串中两个指定的索引号之间的字符

&emsp; toLocaleLowerCase()

&emsp; toLocaleUpperCase()

&emsp; toLowerCase() => 把字符串转换为小写

&emsp; toString() => 返回字符串对象值

&emsp; toUpperCase() => 把字符串转换为大写

&emsp; trim() => 移除字符串首位空白

&emsp; valueOf() => 返回某个字符串对象的原始值

## JavaScript 模板字符串

&emsp;JavaScript 中的模板字符串是一种方便的字符串语法, 允许我们在字符串中嵌入表达式和变量. 

&emsp;模板字符串使用**反引号**作为字符串的定界符分隔字面量

&emsp;允许多行字符串, 带嵌入表达式的字符串插值和一种叫带标签的模板的特殊结构

```js
`string text`  //普通的模板字符串

`string text line 1
 string text line 2` //多行模板字符串

`string text ${expression} string text` //带嵌入表达式的字符串

tagFunction`string text ${expression} string text`  //带标签的模板字符串
```

* string text：将成为模板字面量的一部分的字符串文本。几乎允许所有字符，包括换行符和其他空白字符。但是，除非使用了标签函数，否则无效的转义序列将导致语法错误。
* expression：要插入当前位置的表达式，其值被转换为字符串或传递给 tagFunction。
* tagFunction：如果指定，将使用模板字符串数组和替换表达式调用它，返回值将成为模板字面量的值。

> 模板字符串中可以同时使用单引号和双引号<br>模板字符串还支持多行文本, 而不需要特殊的转义字符.

## JavaScript 运算符

&emsp;**同 C 和 C++**

## JavaScript 比较 和 逻辑运算符

&emsp;`===` => 绝对等于(值和类型均相等)

&emsp;`!==` => 绝对不等于(值和类型有一个不相等, 或者两个都不相等)

> 其余同 C 和 C++

## JavaScript if...Else 语句

&emsp;**同 C 和 C++**


## JavaScript switch 语句

&emsp;**同 C 和 C++**

## JavaScript 循环

&emsp;**For/In循环**:

```js
var txt = "";
var person={fname:"Bill",lname:"Gates",age:56}; 
 
for (x in person) {  // x 为属性名 
    txt=txt + person[x];
}
```

### JavaScript 标签

&emsp;如同 switch 语句, 我们可以对 JavaScript 语句进行标记

> 这种标签的方式和 **C语言** 大体相同, 但是要加花括号

&emsp;1. 默认标签的情况（除了默认标签情况，其他时候必须要有名标签，否则会有惊喜）
当 break 和 continue 同时用于循环时，没有加标签，此时默认标签为当前"循环"的代码块。当 break 用于 switch 时，默认标签为当前的 switch 代码块:

```js
cars=["BMW","Volvo","Saab","Ford"];
list:
{
    document.write(cars[0] + "");
    document.write(cars[1] + "");
    document.write(cars[2] + "");
    break list;
    document.write(cars[3] + "");
    document.write(cars[4] + "");
    document.write(cars[5] + "");
}
```

> 有了标签，可以使用break和continue在多层循环的时候控制外层循环。

```js
outerloop:
for (var i = 0; i < 10; i++)
{
    innerloop:
    for (var j = 0; j < 10; j++)
    {
        if (j > 3)
        {
            break;
        }
        if (i == 2)
        {
            break innerloop;
        }
        if (i == 4)
        {
            break outerloop;
        }
        document.write("i=" + i + " j=" + j + "");
    }
}
```

## JavaScript typeof, null, 和 undefined

### typeof 操作符

```js
typeof "John"                // 返回 string 
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
```
> 在JavaScript中, 数组是一种特殊的对象类型. 因此上面的那个数组返回 object

### null

&emsp;在JavaScript中, null是一个只有一个值的特殊类型. 表示`一个空对象的引用`

> 我们可以通过 `console.log(typeof null)` 来查看null的类型

&emsp;我们可以通过设置`undefined`来清空对象

> `var person = undefined` 这种情况下, 值为`undefined`, 类型为`undefined`

### undefined 和 null 的区别

&emsp;**null 和 undefined 的值相等, 但类型不等**

```js
typeof undefined             // undefined
typeof null                  // object
null === undefined           // false
null == undefined            // true
```

1. 定义:
    (1). undefined: 是所有没有赋值变量的默认值, 自动赋值
    (2). null: 主动释放一个变量引用的对象, 表示一个变量不再指向任何对象地址
2. 什么时候应该使用 **null**
    * 当使用完一个比较大的对象时, 需要对其进行释放内存时间, 设置为null
3. null 与 undefined 的异同点
    * 共同点: 都是原始类型, 保存在栈中
    * 不同点:<br>
        &emsp;1> undefined 表示变量声明过, 但是并未赋值. **它是所有未赋值变量的默认值**<br>
        &emsp;2> null 表示一个变量将来可能指向一个对象. **一般用于主动释放指向对象的引用** 


## JavaScript 类型换换

### JavaScript 数据类型

&emsp;在 JavaScript 中有六种不容的数据类型:

* string
* number
* bollean
* object
* function
* symbol

&emsp;有三种对象类型:

* Object
* Date
* Array

&emsp;不包含任何值的数据类型:

* null
* undefined

### typeof 操作符

```js
typeof "John"                 // 返回 string 
typeof 3.14                   // 返回 number
typeof NaN                    // 返回 number
typeof false                  // 返回 boolean
typeof [1,2,3,4]              // 返回 object
typeof {name:'John', age:34}  // 返回 object
typeof new Date()             // 返回 object
typeof function () {}         // 返回 function
typeof myCar                  // 返回 undefined (如果 myCar 没有声明)
typeof null                   // 返回 object
```

&emsp;**注意:**

* NaN 的数据类型是 number
* 数组 (Array) 的数据类型是 object
* 日期 (Date) 的数据类型是 object
* null 的数据类型是 object
* 未定义变量的数据类型为 undefined

### constructor 属性

&emsp;`constructor`属性返回所有 JavaScript 变量的构造函数
```js
"John".constructor                 
// 返回函数 String()  { [native code] }
(3.14).constructor                 
// 返回函数 Number()  { [native code] }
false.constructor                 
// 返回函数 Boolean() { [native code] }
[1,2,3,4].constructor             
// 返回函数 Array()   { [native code] }
{name:'John', age:34}.constructor 
// 返回函数 Object()  { [native code] }
	new Date().constructor            
// 返回函数 Date()    { [native code] }
function () {}.constructor        
// 返回函数 Function(){ [native code] }
```

&emsp;例如, 我们也可以用这个函数来查看对象是否为数组, 同理也可以查看是否为日期(包含字符串"Date")

```js
function isArray(myArray) {
    return myArray.constructor.toString().indexOf("Array") > -1;
}
```

### JavaScript 类型转换

&emsp; JavaScript 变量可以转换为新变量或其他数据类型:

* 通过使用 JavaScript 函数
* 通过 JavaScript 自身自动转换

### 将数字转换为字符串

&emsp;全局方法`String()`可以将数字转换为字符串

&emsp;该方法可以用于任何类型的数字, 字母, 变量, 表达式:

```js
String(x)         // 将变量 x 转换为字符串并返回
String(123)       // 将数字 123 转换为字符串并返回
String(100 + 23)  // 将数字表达式转换为字符串并返回
```

&emsp;Number方法`toString()`也有同样的效果:
```js
x.toString()
(123).toString()
(100 + 23).toString()
```
* toExponential() => 把对象的值转换为指数计数法
* toFixed() => 把数字转换为字符串, 结果的小数点后有指定位数的数字
* toPrecision => 把数字格式化为指定的长度

### 将布尔值转换为字符串

&emsp;全局方法`String()`

```js
String(false) //返回"false"
String(true)  //返回"true"
false.toString()
true.toString()
```

### 将日期转换为字符串

&emsp;可以直接用`Date()`方法, 该函数直接返回字符串

&emsp;全局方法`String()`可以将日期对象转换为字符串

```js
String(new Date())
```

&emsp;Date方法`toString()`也有同样的效果
```js
obj = new Date()
obj.toString()
```
### 将字符串转换为数字

&emsp;全局方法 `Number()` 可以将字符串转换为数字.

&emsp;空字符串会被转换为 0

&emsp;其他字符串会转换为 `NaN`

```js
Number("3.14")    // 返回 3.14
Number(" ")       // 返回 0 
Number("")        	// 返回 0
Number("99 88")   // 返回 NaN
```

### 一元运算符 "+"

&emsp; `+` 可用于将变量转换为数字

```js
var y = "3";
var x = +y;
```
> 注意上面不是`+=` 而是 `=+`<br>此外, y的类型是 String, 而x的类型是 Number

&emsp;如果变量无法转换, 结果仍为数字(类型), 值为NaN(不是数字)

```js
var y = "jajaja"
var x = +y;
```
### 将布尔值转换为数字

&emsp;全局方法`Number()`可将布尔值转换为数字

```js
Number(true); //返回 1
NUmber(false);//返回 0
```
### 将日期转换为数字
&emsp;全局方法 `Number()` 可将日期转换为数字.
```js
d = new Date();
Number(d);
```
&emsp;日期方法 `getTime()` 也有同样的效果

```js
d = new Date();
d.getTime();
```
### 自动转换类型

&emsp;当 JavaScript 尝试操作一个"错误"的数据类型时, 会自动转换为"正确"的数据类型

```js
5 + null    // 返回 5         null 转换为 0
"5" + null  // 返回"5null"    null 转换为 "null"
"5" + 1     // 返回 "51"      1 转换为 "1"  
"5" - 1     // 返回 4         "5" 转换为 5
 ```
 
### 自动转换为字符串

&emsp;当你尝试输出一个对象或一个变量时 JavaScript 会自动调用变量的 toString() 方法:

```js
document.getElementById("demo").innerHTML = myVar;

`
myVar = {name:"Fjohn"}  // toString 转换为 "[object Object]"
myVar = [1,2,3,4]       // toString 转换为 "1,2,3,4"
myVar = new Date()      // toString 转换为 "Fri Jul 18 2014 09:08:55 GMT+0200"
myVar = 123             // toString 转换为 "123"
myVar = true            // toString 转换为 "true"
myVar = false           // toString 转换为 "false"
`
```

## JavaScript 正则表达式

### 语法

```js
/正则表达式主体/修饰符(可选)
```

例如:
```js
var patt = /test/i;
```
&emsp;其中:

* `/test/i` 是一个正则表达式
* `test` 是一个`正则表达式主体`(用于检索)
* `i`是一个**修饰符**(搜索不区分大小写)

&emsp;在 JavaScript 中，正则表达式通常用于两个字符串方法 : search() 和 replace()。

## JavaScript 错误 - throw, try 和 catch

* `try`, `catch`, `throw` 语句的使用方法和在c++中很相似
* `finally` 语句在 `try`和`catch`语句之后, 无论是否触发异常, 该语句都会被执行

### JavaScript try 和 catch

```js
try {
    ...    //异常的抛出
} catch(e) {
    ...    //异常的捕获与处理
} finally {
    ...    //结束处理
}
```
## JavaScript 声明提升

&emsp; JavaScript中, 函数以及变量的声明都将被提升到函数的最顶部

&emsp; JavaScript中, 变量可以在使用后声明, 也就是变量可以先使用再声明

```js
x = 5; // 变量 x 设置为 5

elem = document.getElementById("demo"); // 查找元素 
elem.innerHTML = x;                     // 在元素中显示 xvar x; // 声明 x
```

```js
var x; // 声明 x
x = 5; // 变量 x 设置为 5
elem = document.getElementById("demo"); // 查找元素 
elem.innerHTML = x;                     // 在元素中显示 x
```

> 声明提升(hoisting): 函数声明和变量声明总是会被解释器悄悄地"提升"到方法体的最顶部

### JavaScript 初始化不会提升

&emsp;JavaScript 初始化不会提升, JavaScript 只有声明变量部分会提升, 初始化部分不会. 

### 在头部声明变量

&emsp;如果不能很好的理解声明提升, 程序就容易出现一些问题

&emsp;为了避免这些问题, 通常我们在每个作用域开始前声明这些变量, 这也是正常的JavaScript解析步骤, 易于我们的理解 

> JavaScript 严格模式(strict mode)不允许使用未声明的变量

## JavaScript 严格模式(use strict)

### 严格模式声明
&emsp;严格模式通过在脚本或函数的头部添加`use strict`表达式来声明

```js
"use strict";
x = 3.14;       // 报错 (x 未定义)
```
&emsp;注意: 在函数内部声明是局部作用域(只在函数内部使用严格模式)

```js
x = 3.14;       // 不报错
myFunction();

function myFunction() {
   "use strict";
    y = 3.14;   // 报错 (y 未定义)
}
 ```

&emsp;为什么使用严格模式:

* 消除JavaScript语法的一些不合理, 不严谨之处, 减少一些怪异行为
* 消除代码运行的一些不安全之处, 保证代码运行的安全
* 提高编译器效率, 增加运行速度
* 为未来新版本的JavaScript做好铺垫

## JavaScript 表单

&emsp; HTML 表单验证可以通过JS来完成.

&emsp; 下面的代码用来判断表单字段(fname)的值是否存在, 如果不存在, 就弹出信息, 阻止表单提交:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <script>
            function validateForm() {
                var x = document.forms["myForm"]["fname"].value;
                if (x == null || x == "") {
                    alert("需要输入名字。");
                    return false;
                }
            }
        </script>
    </head>
    <body>

        <form name="myForm"
            onsubmit="return validateForm()" method="post">
            名字: <input type="text" name="fname">
            <input type="submit" value="提交">
        </form>

    </body>
</html>
```

### HTML表单自动验证

```js
<form action="demo_form.php" method="post">
  <input type="text" name="fname" required="required">
  <input type="submit" value="提交">
</form>
```

&emsp;HTML表单验证也可以通过浏览器来自动完成.

&emsp;如果表单字段(fname)的值为空, **required**属性会阻止表单提交

### 数据验证

&emsp;数据验证用于确保用户输入的数据是有效的

&emsp;典型的数据验证有:

* 必须字段是否有输入
* 用户是否输入了合法的数据
* 在数字字段是否输入了文本

> **服务端数据验证**是在数据提交到服务器上后再验证<br>**客户端数据验证**是在数据发送到服务器钱, 在浏览器上完成验证




