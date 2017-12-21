# Control flow

- **if...else**
- **switch**
- **Ternary operator ‘?’**

---

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

---

## switch
Cú pháp

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

---

## Ternary operator ‘?’

```javascript
    let result = condition ? value1 : value2
```