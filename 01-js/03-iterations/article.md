# Iterations
- **[for](#for)**
- **[while](#while)**
- **[do...while](#dowhile)**
- **[for...in](#forin)**
- **[for...of](#forof)**
---

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

---

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

---

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

---

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

---

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

---