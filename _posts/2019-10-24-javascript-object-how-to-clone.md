---
title: 'JS 객체를 복사하는 3가지 방법'
date: 2019-10-24
---

JavaScript의 객체는 참조 값이므로 단순히 복사 할 방법이 없다.

1. Spread 사용  

```
const obj = { a: 1, b: 2, c: 3};

const cloneObj = { ...obj };

obj.a = 0;

console.log(obj);       //{a: 0, b: 2, c: 3}
console.log(cloneObj);  //{a: 1, b: 2, c: 3}
```

2. Object.assign 사용  

```
const obj = { a: 1, b: 2, c: 3};

const cloneObj = Object.assign({}, obj);

obj.a = 0;

console.log(obj);       //{a: 0, b: 2, c: 3}
console.log(cloneObj);  //{a: 1, b: 2, c: 3}
```

3. JSON 사용  

```
const obj = { a: 1, b: 2, c: 3};

const cloneObj = JSON.parse(JSON.stringify(obj));

obj.a = 0;

console.log(obj);       //{a: 0, b: 2, c: 3}
console.log(cloneObj);  //{a: 1, b: 2, c: 3}
```