##assert.notDeepEqual(actual, expected[, message])
* `actual` {any}   
* `expected` {any}   
* `message` {any}   

测试是否不深度相等。
与 [`assert.deepEqual()`] 相反。

```js
const assert = require('assert');

const obj1 = {
  a : {
    b : 1
  }
};
const obj2 = {
  a : {
    b : 2
  }
};
const obj3 = {
  a : {
    b : 1
  }
};
const obj4 = Object.create(obj1);

assert.notDeepEqual(obj1, obj1);
// 抛出 AssertionError: { a: { b: 1 } } notDeepEqual { a: { b: 1 } }

assert.notDeepEqual(obj1, obj2);
// 通过，obj1 与 obj2 不深度相等

assert.notDeepEqual(obj1, obj3);
// 抛出 AssertionError: { a: { b: 1 } } notDeepEqual { a: { b: 1 } }

assert.notDeepEqual(obj1, obj4);
// 通过，obj1 与 obj4 不深度相等
```

如果两个值深度相等，则抛出一个带有 `message` 属性的 `AssertionError`，其中 `message` 属性的值等于传入的 `message` 参数的值。
如果 `message` 参数为 `undefined`，则赋予默认的错误信息。

