# Day 19 - Common JavaScript Interview Questions for Frontend Engineers Part 1 / 前端工程師常見的 JavaScript 面試問題 Part 1

In this article, I share some common JavaScript interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## What are the differences between `==`,` ===`, and `Object.is()` in JavaScript?

在 JavaScript 當中，`==`、`===` 與 `Object.is()`的區別是？

### Example answer:

`Strict Equality (===)`:

1. If the operands are of different types, they are considered not equal.
2. For primitive types, strict equality compares their values. If the values are the same, they are considered equal.
3. For object types, strict equality compares their references. They are considered equal only if they refer to the same object/array in memory.

> of different types 是固定用法，表示「屬於不同的類型」。

`Loose Equality (==)`:

1. The loose equality operator performs type coercion before comparison.
2. For primitive types, it behaves similarly to strict equality.
3. For object types, it also compares references and checks if they point to the same object/array in memory.

`Object.is()`:

1. Similar to strict equality (===), if the operands are of different types, they are considered not equal.
2. For primitive types, it behaves mostly like strict equality, but with two differences: it treats positive and negative zero as not equal, and it treats NaN as equal to NaN.
3. For object types, it compares their references.

## Why is 0.1 + 0.2 not equal to 0.3 in JavaScript? How can we avoid related issues?

在 JavaScript 中 0.1 + 0.2 為什麼不是 0.3？如何避免相關問題？

### Example answer:

JavaScript uses the IEEE 754 double-precision format to represent numbers. When performing calculations, the computer converts decimal numbers to binary. However, some decimal fractions, such as 0.1 and 0.2, cannot be represented precisely in binary because the conversion results in repeating fractions. This is why `0.1 + 0.2` does not equal exactly `0.3`.

How can we avoid this problem? One common approach is to convert floating-point numbers to integers, perform the arithmetic, and then convert them back to floating-point numbers at the end. Another approach is to use specialized libraries designed for precise decimal arithmetic, such as decimal.js, big.js, or math.js.

```javascript
const resultAsInt = (0.1 * 10) + (0.2 * 10); // 1 + 2 = 3
const finalResult = resultAsInt / 10; // 0.3
```

在 JavaScript 一律使用浮點數來表示數值，其遵循 IEEE754 規範，使用 64 位固定長度表示(包含符號位 1 個、指數位 11 個、尾數位 52 個)，然後電腦在計算數值時會先轉成二進制進行計算，但 0.1 & 0.2 轉換成二進制表示時，計算範例如下，取整後會一直有餘數，最終超過 52 位，之後後面的會被捨棄，導致精度丟失，所以會發生預計計算結果和實際結果不符的情況。

> 十進制轉二進制是除二取整

```
5 / 2 = 2 餘  1
2 / 2 = 1 餘  0
1 / 2 = 0 餘  1
```

> 碰到小數則是乘二取整，0.1 & 0.2 取整後會一直有餘數

```
0.1 * 2 = 0.2 取整 0 剩下 0.2
0.2 * 2 = 0.4 取整 0 剩下 0.4
0.4 * 2 = 0.8 取整 0 剩下 0.8
0.8 * 2 = 1.6 取整 1 剩下 0.6
0.6 * 2 = 1.2 取整 1 剩下 0.2
0.2 * 2 = 0.4 取整 0 剩下 0.4
0.4 * 2 = 0.8 取整 0 剩下 0.8
0.8 * 2 = 1.6 取整 1 剩下 0.6
0.6 * 2 = 1.2 取整 1 剩下 0.2
```

```javascript
(0.1).toString(2) // '0.0001100110011001100110011001100110011001100110011001101'

(0.2).toString(2) // '0.001100110011001100110011001100110011001100110011001101'
```

## What are the differences between `var`, `let`, and `const` in JavaScript?

在 JavaScript 中用 `var`, `let`, 以及 `const` 有什麼差別？

### Example answer:

`var`:

* **Scope**: function-scoped. This means a variable declared with var is accessible anywhere within the function it's defined in.
* **Hoisting**: Variables declared with `var` are hoisted to the top of their function or global scope. You can use the variable before it's declared in the code, though its value will be `undefined`.
* **Reassignment & Redeclaration**: You can reassign and redeclare a `var` variable within the same scope without any errors.

`let`:

* **Scope**: block-scoped. A variable declared with `let` is only accessible within the curly braces (`{}`) where it was defined.
* **Hoisting**: `let` variables are also hoisted, but they are not initialized. This results in a "Temporal Dead Zone". Trying to access a `let` variable before its declaration will result in a `ReferenceError`.
* **Reassignment & Redeclaration**: You can reassign a `let` variable, but you can't redeclare it within the same scope.

`const`:

* **Scope**: block-scoped.
* **Hoisting**: Variables declared with `const` must be initialized at the time of declaration. If you don't initial a value when declaring a `const` variable, it will result in a `SyntaxError`.
* **Reassignment & Redeclaration**: You can't reassign or redeclare the variable after its initial declaration, but the contents of a complex data type (like an object or an array) can be modified.

## What is a closure in JavaScript?

什麼是閉包 (Closure)？

### Example answer:

When you define a function inside another function, the inner function has access to the variables and parameters of its outer function. A closure is formed when this inner function is returned or passed to another place in your code. It keeps a live reference to the outer function's environment, allowing it to continue accessing and even modifying those variables long after the outer function has finished executing.

Key Characteristics:

1. **Lexical Scoping**: Closures rely on JavaScript's lexical scoping, which means a function's scope is determined by where it's written in the code, not where it's called.
2. **Encapsulation**: They are often used to create private variables and methods, as the variables are not directly accessible from the outside. This is a powerful way to manage state and avoid polluting the global namespace.
3. **Data Persistence**: A closure allows a function to maintain a persistent state between multiple calls, which is useful for creating things like counters or memoization functions.

### Additional information

回答中用到了 long after + [時間點/事件/名詞子句]，指的是在某個時間或事件過去很久之後。

These tools will survive long after the event concludes.

這些工具在活動結束之後很久仍然會存在。

[Day7-閉包(Closure)介紹](https://ithelp.ithome.com.tw/articles/10288362)

## Explain how the value of `this` is determined in different contexts.

解釋不同情境下 `this` 的指向?

### Example answer:

`this` is a keyword whose value is determined by the context in which a function is called.

#### 1. Global Context

In the global execution context and non–strict mode, `this` refers to the global object. In a browser environment, this is the window object. In Node.js, it is the global object.

In the global execution context and strict mode, `this` is `undefined`.

#### 2. Function Context

The value of `this` inside a function depends on **how the function is called**.

**Simple Function Call**: In non-strict mode, `this` refers to the global object.

```javascript
function showThis() {
  console.log(this);
}
showThis(); // In non-strict mode: window (or global). In strict mode: undefined.
```

**Method Call**: When a function is called as a method of an object, `this` refers to the **object that the method belongs to**.

```javascript
const person = {
  name: 'John',
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};
person.greet(); // 'Hello, my name is John'.
```

#### 3. Constructor Function / Class:

When a function is used as a constructor with the `new` keyword, `this` refers to the **newly created object instance**.

```javascript
function Person(name) {
  this.name = name; // 'this' is the new object instance.
}
const john = new Person('John');
console.log(john.name); // 'John'
```

#### 4. Arrow Functions

Arrow functions (`() => {}`) have a unique behavior: they do not have their own `this`. Instead, they **inherit `this` from the surrounding lexical scope** (the parent function or global scope). This makes them very predictable and a good choice for callbacks.

```javascript
const person = {
  name: 'John',
  // Traditional function: 'this' refers to the object itself
  showName: function() {
    setTimeout(function() {
      console.log(this.name); // 'this' is 'window' (or global) here, so it's undefined.
    }, 100);
  },
  // Arrow function: 'this' is inherited from the 'person' object
  showNameArrow: function() {
    setTimeout(() => {
      console.log(this.name); // 'this' is 'person'.
    }, 100);
  }
};
person.showName(); // undefined
person.showNameArrow(); // 'John'
```

#### 5. Explicit Binding

You can explicitly set the value of `this` using the `call()`, `apply()`, and `bind()` methods.

`call()` and `apply()`: Call the function immediately with a specified `this` value. The only difference is how they handle arguments (`call` takes them individually, `apply` takes an array).

`bind()`: Returns a new function with a permanently bound `this` value, without immediately executing it.

```javascript
function showThisName(age) {
  console.log(`${this.name} is ${age} years old.`);
}

const person1 = { name: 'John' };
const person2 = { name: 'Jane' };

showThisName.call(person1, 30); // 'John is 30 years old.'
showThisName.apply(person2, [25]); // 'Jane is 25 years old.'

const boundFunction = showThisName.bind(person1);
boundFunction(40); // 'John is 40 years old.'
```

[Day8-JavaScript this 關鍵字](https://ithelp.ithome.com.tw/articles/10288542)
