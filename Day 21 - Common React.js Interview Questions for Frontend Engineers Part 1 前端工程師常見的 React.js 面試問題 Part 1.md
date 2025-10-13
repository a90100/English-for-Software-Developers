# Day 21 - Common React.js Interview Questions for Frontend Engineers Part 1 / 前端工程師常見的 React.js 面試問題 Part 1

In this article, I share some common React.js interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## What is JSX? Why do we use JSX?

什麼是 JSX? 為什麼要用 JSX？

### Example answer:

JSX is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file. When we write JSX in React components, we are actually writing the `React.createElement()` syntax that is built into React.js. JSX provides syntactic sugar that lets us write the structure of React elements more easily.

Therefore, JSX is highly integrated with React.js. It provides a declarative way to define what the UI should look like based on the current state and props. We don't have to manipulate the DOM manually; instead, we update state and props so React.js will re-render the UI.

[Writing Markup with JSX](https://react.dev/learn/writing-markup-with-jsx)

## What is Virtual DOM?

什麼是 Virtual DOM？

### Example answer:

The Virtual DOM is a mechanism that uses JavaScript objects to describe what the Real DOM should look like. It provides several benefits.

First, we don’t need to update the entire Real DOM whenever the webpage re-renders. React applies changes to the Virtual DOM first, then runs a diffing algorithm to compare the new Virtual DOM with the previous one and calculates the minimal set of updates required. Finally, it updates only the affected parts of the Real DOM.

Second, the Virtual DOM also enhances the development experience. With declarative programming, developers don’t have to manipulate the DOM manually. Instead, they simply update data, state, and props, and React takes care of updating the Real DOM accordingly. This allows developers to focus on managing data changes rather than worrying about DOM operations, saving both time and effort.

[网上都说操作真实 DOM 慢，但测试结果却比 React 更快，为什么？](https://www.zhihu.com/question/31809713)

## Why are there some restrictions on using Hooks, such as not being able to call them inside loops, conditionals, or nested functions?

為什麼使用 Hook 有些限制，不能在迴圈、條件式或是巢狀的 function 內呼叫 Hook？

### Example answer:

The core reason you can't call Hooks in loops, conditionals, or nested functions is to ensure a consistent and predictable order of execution. Internally, React stores Hooks as a linked list on the Fiber node's `memoizedState` field. When a functional component renders, React creates a Fiber node for it. This node contains a `memoizedState` property, which represents the first Hook. Each Hook's state object has a `next` property that points to the next Hook in the list.

If a Hook is skipped—for example, by being placed in a conditional statement—the linked list's structure breaks. When the component re-renders, React expects the Hooks to be in the same order. If the order is disrupted, React will fetch the wrong state for the wrong Hook, leading to bugs and unpredictable behavior. This is why React enforces these usage limitations.

## Why should we use immutable patterns when updating state in React?

為什麼更新 React 中的 state 要用 immutable 的寫法?

### Example answer:

React relies on shallow comparison to detect whether states and props have changed. The first benefit is that it only needs to check whether the reference of a state or prop has changed. In contrast, checking the actual values could be more time-consuming, especially when the data is large.

The second benefit is that it ensures predictable state management. If multiple state objects share the same reference, side effects may occur — a change in one place can unexpectedly affect another. By using an immutable approach, each change creates a new version of the state, which prevents these side effects.

## What is the difference between a controlled component and an uncontrolled component?

controlled component 和 uncontrolled component 的區別是？

### Example answer:

The distinction between a controlled component and an uncontrolled component in React boils down to how they manage their form data.

In a controlled component, every value of the form fields is managed by React state. Any changes to the input are handled by an event handler. This gives developers full control over the form’s behavior and makes it easier to validate or manipulate data.

In an uncontrolled component, the values of the form fields are managed by the DOM itself. We usually access the values using refs. Uncontrolled components require less code but provide less control, which can make complex form handling more difficult.

## Can you explain the difference between Client-Side Rendering (CSR) and Server-Side Rendering (SSR)?

你能解釋一下 CSR（Client-Side Rendering）與 SSR（Server-Side Rendering）的差異嗎？

### Example answer:

Client-Side Rendering and Server-Side Rendering are two distinct approaches for rendering web pages.

Client-Side Rendering means that the server sends a minimal HTML file and a bundle of JavaScript to the browser. The browser then executes the JavaScript to build and render the content dynamically.

**Pros**: It provides a highly interactive and fluid user experience after the initial load. Once the JavaScript is loaded, subsequent page navigations are very fast because they only involve fetching new data and updating the DOM, without a full page reload.

**Cons**: The initial load time can be slower, as the browser has to download, parse, and execute the JavaScript before anything is visible. This also negatively impacts SEO, as search engine crawlers might see a blank page before the content is rendered.

Server-Side Rendering means that when a user requests a page, the server fetches the necessary data, renders the complete HTML page, and then sends this fully constructed HTML file to the browser. The browser receives a page that is ready to be displayed immediately.

**Pros**: The initial page load is very fast since the user sees the content right away. This is great for user experience and is highly beneficial for SEO, as search engine crawlers can easily index the fully rendered content.

**Cons**: It can put a heavier load on the server since it's responsible for rendering the entire page for every request.
