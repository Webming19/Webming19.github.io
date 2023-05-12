# JS隐式类型转换

由于JS是解释型语/即时编译型语言，并且具有灵活、宽容的写法，所以在一些操作符下其数据类型会做一下类型转换再计算而不是报错。

if(xxx)判断、==、+ 都是比较常见的存在隐式类型转换的操作

🌰 ：
```js
var a = true + false;
console.log(a);// 1 (true转化为1，false转化为0)

if (" ") {
    console.log("true");
} else {
    console.log("false");
}// true 非空字符串转化为true

if ("") {
    console.log("true");
} else {
    console.log("false");
}// false 空字符串转化为false

var a = {
  valueOf: function () {
     return 1;
  },
  toString: function () {
     return '123'
  }
}
true == a // true;
```

## 1. if 判断

对于括号里的表达式，会被强制转换为布尔类型

| 类型            | 结果                                |
|---------------|-----------------------------------|
| undefined     | false                             |
| Null          | false                             |
| Boolean       | 直接判断                              |
| Number        | +0, −0, 或者 NaN 为 false, 其他为 true  |
| String        | 空字符串为 false,其他都为 true          |
| Object        | true                              |

```js
if ("hello") {
  // true
  console.log("hello")
} 

if ("") {
  // false
  console.log('empty')
}

if (" ") {
  // true
  console.log('blank')
}

var obj = {};
if (obj) {
  // true
  console.log(obj)
}
```

## 2. + 操作符

- 在两个操作数都是数字的时候，会做加法运算
- 两个参数都是字符串或在有一个参数是字符串的情况下会把另外一个参数转换为字符串做字符串拼接
- 在参数有对象的情况下会调用其valueOf或toString方法
- 在只有一个字符串参数的时候会尝试将其转换为数字
- 在只有一个数字参数的时候返回其正数值

```js
console.log(2+4); // 6
console.log("2"+"4"); // "24"
console.log(2+"4"); // "24"
console.log(2+new Date()); // "2Mon Jan 20 2014 17:15:01 GMT+0800 (China Standard Time)"
console.log(+"4"); // 4 
```

## 3. == 操作符

对于x == y ，js做如下处理

| x         | y                | 结果                  |
|-----------|------------------|---------------------|
| null      | undefined        | true                |
| Number    | String           | x == toNumber(y)    |
| Boolean   | (any)            | toNumber(x) == y    |
| Object    | String or Number | toPrimitive(x) == y |
| otherwise | otherwise        | false               |

toNumber规则

| type      | Result                     | 
|-----------|----------------------------|
| Undefined | NaN                        |
| Null      | 0                          |
| Boolean   | ture -> 1, false -> 0      |
| String    | 'abc' -> NaN, '123' -> 123 |

toPrimitive规则

对于 Object 类型，先尝试调用`.valueOf`方法获取结果。
如果没定义，再尝试调用`.toString`方法获取结果。
都没有则报错
