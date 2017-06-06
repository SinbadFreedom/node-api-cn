##assert.notEqual(actual, expected[, message])
* `actual` {any}   
* `expected` {any}   
* `message` {any}   

使用不等运算符（`!=`）测试是否不相等。

```js
const assert = require('assert');

assert.notEqual(1, 2);
// 通过

assert.notEqual(1, 1);
// 抛出 AssertionError: 1 != 1

assert.notEqual(1, '1');
// 抛出 AssertionError: 1 != '1'
```

如果两个值相等，则抛出一个带有 `message` 属性的 `AssertionError`，其中 `message` 属性的值等于传入的 `message` 参数的值。
如果 `message` 参数为 `undefined`，则赋予默认的错误信息。

