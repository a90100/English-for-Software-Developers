# Day 18 - Common Interview Questions for Frontend Engineers Part 2 / 前端工程師的常見面試問題 Part 2

In this article, I share some common interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## How do you handle cross-browser compatibility issues in a frontend project?

在前端專案中，你如何處理跨瀏覽器相容性問題？

### Example answer:

There are several ways to handle cross-browser compatibility.

First, before using specific browser APIs or JavaScript syntax—especially bleeding-edge features—I check MDN and caniuse.com to ensure they are supported on the browsers our users rely on.

Second, I use automated polyfills, necessary CSS prefixes, and Babel to transpile the code into a more universally compatible version.

Third, I test our website across different browsers to make sure all features work properly.

## How do you coordinate with backend engineers to confirm the data exchange format of an API?

你是如何和後端工程師協調，來確認 API 的資料交換格式？

### Example answer:

When discussing an API data exchange format with backend engineers, I always make sure we both consistently understand the feature requirements. After that, I open the web design mockup to explain what data I need to present on the webpage and why specific fields are necessary. We also share our perspectives on the request and response structures, including data types, required fields, and error handling. If we don’t have a shared understanding, we adjust the data format until we reach a consensus.

As development progresses, if I encounter an unexpected data format or realize that an additional field is needed, I immediately notify the backend engineers. This iterative feedback loop is crucial for adapting to unforeseen challenges and ensuring a successful integration.

## Why do you choose JSON as the data exchange format for APIs?

為什麼選擇用 JSON 做為 API 的資料交換格式?

### Example answer:

The most important reason is that JSON is supported by many popular programming languages and tools. Furthermore, it is lightweight, human-readable, and easy to parse, which makes integration and debugging much simpler.

## Could you give an example of collaborating with backend engineers to discuss the data exchange format of an API?

能否舉一個前端與後端討論 API 資料交換格式合作案例?

### Example answer:

I participated in a project where one of the functionalities was for our system to read circuit board-related files, such as pcbdoc and schematic documents.

I was responsible for reading the content of these files and transforming them into JSON format, which our algorithm engineers needed. However, since circuit boards usually contain many types of information, such as board details, layers, components, vias, tracks, and clearance, I faced a problem: should I split the information into several JSON files or consolidate it into one large JSON file?

To resolve this, I discussed the options with a backend engineer who was also involved in the project. Both approaches had pros and cons. Sending a single large JSON file through one API request reduces the number of requests and simplifies the data-handling logic. Sending multiple JSON files through multiple APIs offers higher fault tolerance. If part of the data fails to upload, we only need to re-upload that portion. It also allows us to provide more detailed upload status to users, since we can show success messages as each file completes.

After evaluating both approaches, we decided to send one large JSON file because the file size was manageable—it only contained diverse types of data. We just needed to ensure that the data structure was clear and easy for algorithm engineers to understand.

The lesson I learned from this collaboration is that when facing multiple ways to implement a feature, it’s important to analyze the pros and cons first and then choose the solution that best fits the project’s needs.

## How do you collaborate with UI designers?

和 UI 設計師合作，是怎麼進行的?

### Example answer:

During the design phase, when the mockups are not yet finalized, I evaluate the feasibility of each feature. If there is a complex animation or special effect, I provide technical feedback about potential challenges and performance concerns.

Once the UI designer has finished the mockups, I conduct a detailed review of interactive behaviors, responsive layouts, and edge cases, making sure my understanding is aligned with the designer.

During development, I maintain constant communication with the UI designer to ask questions or clarify details. This continuous back-and-forth ensures that the implemented UI closely matches the designer’s vision.

## Can you share an experience where you optimized performance in the past?

過去做過效能優化的經驗？

### Example answer:

I developed a feature that displayed the net data of a circuit board on our webpage. The number of records ranged from over ten thousand to nearly one hundred thousand. If all the data were rendered directly in a limited area on the webpage, the list would become extremely long. When scrolling, the page often dropped frames because the browser had to constantly handle too many DOM elements. Rendering new DOM nodes consumes memory, CPU, and GPU resources, especially when their positions change during user interactions such as scrolling. The initial loading time was also longer since a large amount of data had to be loaded at once.

To solve this, I implemented a virtualized list using a third-party library called react-window. It rendered only the DOM elements visible on the screen and removed those that were no longer in view. As a result, the browser didn’t need to manage so many DOM nodes at the same time. I also applied lazy loading to fetch more data only when the user scrolled to the bottom of the list, which further optimized the initial load time.

After these optimizations, scrolling through the list became smooth, and the overall performance of the page improved significantly.
