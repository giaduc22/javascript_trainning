# Declarations
- **[let](#let)**
- **[var](#var)**
- **[const](#const)**
---



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

---

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

---

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

---