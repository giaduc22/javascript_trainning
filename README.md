#Javascript

### Declarations
- **[let](#let)**
- **[var](#var)**
- **[const](#const)**

### Control flow
- **[if...else](#ifelse)**
- **[switch](#switch)**

### Iterations
- **[for](#for)**
- **[while](#while)**
- **[do...while](#dowhile)**
- **[for...in](#forin)**
- **[for...of](#forof)**
### **[Function](#function)**
### **[Classes](#classes)**

## let

- Cho phép khai báo biến và khởi tạo giá trị cho biến
- Ảnh hưởng trong toàn block mà nó được khai báo

```javascript
let x = 'out';
{
	let y = 'in';
	console.log(x);	//out
	console.log(y);	//in
}
console.log(x);	//out
console.log(y);	//Error
```

## var

- Cho phép khai báo biến và khởi tạo giá trị cho biến
- Ảnh hưởng trong function bao quanh nó

```javascript
var x = 'out';
function function_name() {
	console.log(x);	//out
}
console.log(x);	//out
function_name();	//out
```

```javascript
function function_name() {
	var x = 'out';
	console.log(x);	//out
}
console.log(x);	//Error
function_name();	//out
```


## const

- Khai báo và khởi tạo giá trị hằng số
- Ảnh hưởng trong toàn block mà nó được khai báo
- Không cho phép gán lại giá trị

```javascript
const MY_CONST = 9;
MY_CONST = 7;	//Error
```

```javascript
const MY_OBJECT = {key: 45};
MY_OBJECT.key = 48;	//OK
MY_OBJECT.index = 49;	//OK
MY_OBJECT = {}; //Error
console.log(MY_OBJECT);
```

## if...else

- câu lệnh rẽ nhánh

```javascript
if(condition){
    console.log("condition = true");
} else {
    console.log("condition = false");
}
```

- nếu condition = [0, -0, null, undefined, NaN, ""] sẽ cho giá trị false.

```javascript
if(0){
    // Câu lệnh này không được chạy
} else {
    // Câu lệnh này được chạy
}
```

## switch

### Cú pháp
```javascript
switch(expression){
    case value1:
        statement1;
        break;
    case value2:
        statement2;
        break;
    default:
        default statement;
}
```

- nếu expression === value1 statement1 sẽ được chạy và thoát khỏi switch.
- nếu không có case nào === expression thì sẽ chạy default statement.

## for
```javascript
for (let i = 0; i < 5; i++) {
	console.log(i);
}

// 0
// 1
// 2
// 3
// 4
```

## while
```javascript
let i = 0;
while (i < 5) {
	console.log(i);
	i++;
}

// 0
// 1
// 2
// 3
// 4
```
## do...while
```javascript
let i = 0;
do {
	console.log(i);
	i++;
} while (i<5);

// 0
// 1
// 2
// 3
// 4
```
Trong trường hợp điều kiện trong while không thoả mãn thì câu lệnh trong do vẫn được thực hiện lần đầu tiên.
```javascript
let i = 0;
do {
	console.log(i);
	i++;
} while (i>55);
console.log(i);

// 0
// 1
```
## for...in
- Lặp qua thuộc tính đếm được của một object (enumerable: true)
```javascript
for (variable in object) {
	statement
}
```
```javascript
let obj = {
	a: 40,
	b: 30,
	c: 50
};
for (var prop in obj) {
	console.log(prop);
}

// "a"
// "b"
// "c"
```
```javascript
let obj = {
	a: 40,
	b: 30,
	c: 50
};

Object.defineProperty(obj, 'a', {
  enumerable: false
})

for (var prop in obj) {
	console.log(prop);
}

// "b"
// "c"
```



## for...of
- Lặp qua iterable objects: `Array`, `Map`, `Set`, `String`, `TypedArray`
```javascript
let string = "giaduc";
for (variable of string) {
	console.log(variable);
}

// "g"
// "i"
// "a"
// "d"
// "u"
// "c"
```

## function
**Function declarations**
- Can be hoisted
```javascript
function name([param[, param[, ... param]]]) {
   statements
}
```
**Function expressions**
- Can be name or unnamed
- Not hoisted
```javascript
var myFunction = function [name]([param1[, param2[, ..., paramN]]]) {
   statements
};
```

**Arrow function**
```javascript
([param[, param]]) => {
   statements
}
```
## classes
**Class declarations**
- Not hoisted
```javascript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```
**Class expressions**
- Can be named or unnamed
- Not hoisted
```javascript
// unnamed
var Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};

// named
var Rectangle = class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```
