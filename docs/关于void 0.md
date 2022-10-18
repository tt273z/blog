代码中看到过很多次 `void 0` 的写法，比较好奇，了解了一下总结在这里。

## void expression

> **void 运算符**对给定的表达式进行求值，然后返回 [`undefined`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/undefined)。

我对 `void` 的理解是，他把后面的表达式正常执行一遍，再返回一个 `undefined` 给我们。

## 常见用法

- 替代 `undefined`

  ```js
  let bob = void 0; 
  ```

- 判断对象是否为 `undefined`

  ```js
  if (bob == void 0){}
  ```

## 为什么替代 undefined ?

- 局部作用域里面的 `undefined` 是可以被重写的

- `void 0` 短小精悍，省流助手

## 其他使用

如果想执行一个函数（或者任何表达式）又想确保没有任何副作用的话，可以这样使用：

```js
function meow(){ /*...*/ }
btn.onclick = () => void meow()
```

