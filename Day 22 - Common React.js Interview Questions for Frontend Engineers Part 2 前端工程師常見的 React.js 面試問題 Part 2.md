# Day 22 - Common React.js Interview Questions for Frontend Engineers Part 2 / 前端工程師常見的 React.js 面試問題 Part 2

In this article, I share some common React.js interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## What is React Fiber?

React Fiber 是什麼?

### Example answer:

React Fiber is the core reconciliation algorithm in React, re-implemented from the previous stack-based approach to support incremental rendering and concurrency.

It enables splitting rendering work into smaller, interruptible chunks, allowing for higher-priority tasks like animations to be handled first and providing a smoother, more responsive user experience, especially in complex applications. Key benefits include the ability to pause, abort, or reuse work, prioritize different updates, and improve animation and complex user interactions.

## Why choose React.js / Redux for development? What are the pros and cons compared to other similar tools?

為什選擇使用 React.js / Redux 進行開發? 跟其他相似工具相比，有什麼優缺點？

### Example answer:

In the early 2000s, web pages were relatively simple and lacked complex functionalities. However, as the Internet evolved, websites became more powerful and their structures more complex. To help developers manage these complexities and improve performance, modern front-end frameworks were created. React.js is one of the most popular options, and it provides several key benefits.

First, React’s declarative approach makes it easier to reason about(思考、推論) your application. You simply describe what the UI should look like for a given state, without having to manipulate the DOM manually.
Second, React promotes building UIs with reusable and self-contained components. This modular design makes the codebase easier to manage, test, and scale.
Third, React’s Virtual DOM and reconciliation algorithm offer better performance in many cases compared to manipulating the DOM directly.

Redux provides a centralized and predictable state management. It uses an unidirectional data flow that makes state changes transparent and easy to debug.

Other front-end frameworks, such as Angular and Vue.js, also provide similar functionalities. However, if you are already familiar with JavaScript, React tends to have a gentler learning curve. Additionally, React supports multi-platform development, enabling developers to build applications that run across different browsers and device types using a single codebase.

## Why choose Redux Toolkit / RTK Query for development? What are the pros and cons compared to other similar tools?

為什選擇使用 Redux Toolkit / RTK Query 進行開發?跟其他相似工具相比，有什麼優缺點？

### Example answer:

We choose them as our tech stack because they provide several benefits.

Redux Toolkit reduces the boilerplate code that traditional Redux required. It provides built-in utilities like `createSlice` and `configureStore`, which make state logic more concise and easier to maintain. `createSlice` bundles actions and reducers into one function, so all related states can be placed in the same slice file, making our code more modular. Furthermore, Redux Toolkit integrates Immer internally, so you can write immutable state updates using a simpler, more “mutating” syntax, while it handles the immutable updates behind the scenes.

RTK Query is a powerful data fetching and caching tool. You no longer need to write manual state for loading, error, and success handling for every API call, since RTK Query manages all of that automatically. It also provides automatic caching and custom invalidation logic, which can dramatically improve application performance by preventing unnecessary network requests.

However, they may feel like overkill for very small projects or simple applications.

## What are the differences between Styled Components and other similar tools?

Styled Component 和其他相似工具的差別？

### Example answer:

Styled Components is a CSS-in-JS library that allows developers to write CSS directly inside JavaScript files using template literals.

After being compiled, it automatically generates unique class names, eliminating the problems that come with BEM or other naming conventions used to avoid conflicts. It’s also easy to pass props to components and use them to dynamically change styles. Furthermore, developers can write JavaScript conditional syntax, such as the ternary operator, directly in their styles. Styled Components also supports standard CSS functionalities, such as media queries, pseudo-classes, and pseudo-elements.

However, Styled Components injects styles into the DOM at runtime, which can be slower than using traditional, pre-compiled CSS files. Additionally, since CSS is written directly within JavaScript files, using Styled Components can lead to a larger JavaScript bundle size compared to solutions that separate CSS.

## What are the advantages and disadvantages of Next.js? Why use it?

Next.js 的優缺點?為什麼使用它?

### Example answer:

Next.js is a React framework that provides powerful features out of the box to develop websites.

First, Next.js provides the flexibility to choose the right rendering strategy for each page: SSR for dynamic content, SSG for static content, and CSR for highly interactive components. Developers can decide which rendering strategy to use depending on the requirements. If we choose SSR or SSG, the initial page load is fast and SEO-friendly. Search engine crawlers can easily read and index the pre-rendered HTML content.

Second, Next.js uses a file-system-based router. You don't need to manually configure routes with a library like React Router. The files and folders within the pages directory will automatically generate the routing.

Third, Next.js also provides optimization features such as lazy loading and image optimization, which improve web performance.
