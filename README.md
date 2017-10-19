#Javascript

### Declarations
- **[let](#let)**<br>
- **[var](#var)**<br>
- **[const](#const)**<br>

### Control flow
- **[if...else](#ifelse)**<br>
- **[switch](#switch)**<br>

### Iterations
- **[for](#for)**<br>
- **[while](#while)**<br>
- **[do...while](#dowhile)**<br>
- **[for...in](#forin)**<br>
- **[for...of](#forof)**<br>

## let

- Cho phép khai báo biến và khởi tạo giá trị cho biến
- Ảnh hưởng trong toàn block mà nó được khai báo

```
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

```
var x = 'out';
function function_name() {
	console.log(x);	//out
}
console.log(x);	//out
function_name();	//out
```

```
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

```
const MY_CONST = 9;
MY_CONST = 7;	//Error
```

```
const MY_OBJECT = {key: 45};
MY_OBJECT.key = 48;	//OK
MY_OBJECT.index = 49;	//OK
MY_OBJECT = {}; //Error
console.log(MY_OBJECT);
```

## if...else

- câu lệnh rẽ nhánh

```
if(condition){
    console.log("condition = true");
} else {
    console.log("condition = false");
}
```

- nếu condition = [0, -0, null, undefined, NaN, ""] sẽ cho giá trị false.

```
if(0){
    // Câu lệnh này không được chạy
} else {
    // Câu lệnh này được chạy
}
```

## switch

### Cú pháp
```
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
```
for (let i = 0; i < 5; i++) {
	console.log(i);
}
```
Kết quả
```
0
1
2
3
4
```

## while
```
let i = 0;
while (i < 5) {
	console.log(i);
	i++;
}
```
Kết quả
```
0
1
2
3
4
```
## do...while
```
let i = 0;
do {
	console.log(i);
	i++;
} while (i<5);
```
Kết quả
```
0
1
2
3
4
```
Trong trường hợp điều kiện trong while không thoả mãn thì câu lệnh trong do vẫn được thực hiện lần đầu tiên.
```
let i = 0;
do {
	console.log(i);
	i++;
} while (i>55);
console.log(i);
```
Kết quả
```
0
1
```
## for...in

## for...of
