# Day 20 - Common JavaScript Interview Questions for Frontend Engineers Part 2 / 前端工程師常見的 JavaScript 面試問題 Part 2

In this article, I share some common JavaScript interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## Can you explain the event loop in the browser?

請說明瀏覽器中的事件循環 (Event Loop)

### Example answer:

The Event Loop in JavaScript is a mechanism that allows asynchronous code to be executed without blocking the main thread.

In the JavaScript runtime environment, there are some key components:

#### 1. Call Stack

It is a place to store the functions that are to be executed. After a function is executed, it is popped off the call stack. The JavaScript engine can only execute one function at a time. If a function takes a long time to run, it "blocks" the stack, making the user interface unresponsive.

#### 2. Web APIs

Web APIs are built into the browser, such as DOM events, `setTimeout`, `setInterval`, and `fetch`.

#### 3. Macro-task Queue (or Task Queue, Callback Queue)

It stores tasks that are waiting to be executed after the call stack is empty. These tasks are queued by `setTimeout`, `setInterval`, or other APIs.

#### 4. Micro-task Queue (or Job Queue)

It is a higher-priority queue for `Promise` and `MutationObserver` callbacks. Microtasks are executed before tasks in the macro-task queue.

#### 5. Event Loop

The event loop continuously checks if the call stack is empty and pushes tasks from the microtask queue or macro-task queue to the call stack for execution.

In the JavaScript runtime environment, the following steps are followed to execute the code:

1. Execute all synchronous tasks on the call stack.
2. Check whether there is any microtask in the Job Queue. If there is, move it to the call stack and execute it.
3. Check whether there is any macrotask in the Task Queue. If there is, move it to the call stack and execute it.

### Additional information

[JavaScript Visualized - Event Loop, Web APIs, (Micro)task Queue](https://youtu.be/eiC58R16hb8)

[Day4-JavaScript Runtime Environment 觀念](https://ithelp.ithome.com.tw/articles/10287730)

be + to V，表示「預定要 / 應該要」發生的動作。

* are to be executed 偏向「定義性的說法」，用來解釋「它的用途是...」。
* will be executed 偏向「時間未來式」，強調「它之後會被執行」。

## What do synchronous and asynchronous mean in JavaScript?

JavaScript 中的同步和非同步是指什麼？

### Example answer:

Synchronous means that tasks are performed one after another, in sequence. Each task must finish before the next one starts. If a synchronous task is time-consuming, it will "block" the main thread.

It's like standing in a single-file line at a bank. You can't start your transaction until the person in front of you is finished.

Asynchronous means that a task can start and run in the background without blocking the main thread. The program can continue to execute other tasks while it waits for the asynchronous task to complete.

It's like ordering food at a restaurant. You place your order and then go sit down. You don't stand at the counter and wait for your food to be made. The kitchen prepares the food while you're free to do other things.

## What is the difference between passing by value and passing by reference in JavaScript?

JavaScript 中 by value 和 by reference 的區別是什麼?

### Example answer:

Primitive data types (such as `number`, `string`, `boolean`, `null`, `undefined`, and `symbol`) are passed by value.

When you assign a primitive value to a new variable or pass it to a function, you are creating a direct copy of the value. The two variables are completely independent. Changes made to one will not affect the other.

Object data types (including `object`, `arrays` and `functions`) are passed by reference.

When you assign a non-primitive value to a new variable or pass it to a function, you are not copying the value itself, but rather a reference (or memory address) to the object. Both variables point to the same object in memory.

Reassigning the object reference: If you reassign the function's parameter to a new object, this will not affect the original variable outside the function. The parameter will then point to a different object, while the original variable still points to the initial object.

```javascript
let myObject = { value: 10 };

function changeObject(obj) {
  obj.value = 20; // This works (modifying a property)
  console.log('Inside function (after modification):', obj); // { value: 20 }
  
  obj = { value: 30 }; // This does NOT affect the original 'myObject'
  console.log('Inside function (after reassignment):', obj); // { value: 30 }
}

changeObject(myObject);
console.log('Outside function:', myObject); // Output: { value: 20 }
// The original object's property was changed, but the re-assignment did not work.
```

## What is the difference between shallow copy and deep copy in JavaScript?

JavaScript 中的淺拷貝 (shallow copy) 和深拷貝 (deep copy) 差別是什麼？

### Example answer:

The difference between shallow copy and deep copy lies in how nested objects are handled.

A shallow copy creates a new object or array, but it only duplicates the top-level properties. If the original object or array contains nested objects or arrays, the shallow copy will still reference the same nested objects or arrays as the original. In this case, updating a nested property in the copied object will also affect the original object.

Common Shallow Copy Methods:

1. Spread Syntax (`...`): The most common and modern way.
2. `Object.assign()`
3. `Array.prototype.slice()`
4. `Array.from()`

A deep copy creates a completely independent copy of an object or array, including all nested objects and arrays. It recursively duplicates all levels of the data structure, ensuring that no shared references remain between the original and the copied object. In this case, updating a property in the copied object will not affect the original object.

Common Deep Copy Methods:
1. `JSON.parse(JSON.stringify())`: The simplest and most common method for plain objects.
2. Specialized Libraries: For more complex objects (with functions, undefined, Map, Set, etc.), you should use libraries like `lodash.cloneDeep`.

[Day26-瞭解 JS 的淺拷貝(Shallow Copy) & 深拷貝(Deep Copy)](https://ithelp.ithome.com.tw/articles/10298831)
