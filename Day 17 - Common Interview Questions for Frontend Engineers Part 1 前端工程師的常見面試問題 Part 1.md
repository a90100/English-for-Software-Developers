# Day 17 - Common Interview Questions for Frontend Engineers Part 1 / 前端工程師的常見面試問題 Part 1

In this article, I share some common interview questions for frontend engineers.

**The best way to use this article is to try answering these questions in English.**

## List several common frontend performance optimization techniques and explain how they improve page load speed.

請列舉幾個常見的前端效能優化技巧，並說明它們如何提升網頁載入速度。

### Example answer:

There are several ways to optimize our website's performance.

First, we minify and compress all project files to reduce their size. Smaller files mean faster download times for the browser, which directly improves page rendering speed.

Second, we use lazy loading for images or code splitting so that content is loaded only when needed, which significantly decreases the initial page load time.

Third, our backend engineers set Cache-Control, Last-Modified, or ETag in the HTTP headers to enable resource caching. This allows repeat visitors to experience faster load times when they return to our website.

Of course, there are still many ways to improve performance. But I would say that understanding when to optimize and which techniques to apply is even more important than simply knowing all the methods. Different scenarios require different approaches, and there is no one-size-fits-all solution.

> I would say that 用來表達個人看法、觀點，語氣比較 謙虛、柔和，帶有「依我看來」或「如果要說的話」的感覺。
> I have to say that 表達強烈的意見或驚訝，語氣比較 直接、帶點情緒，像是「老實說」、「不得不說」。

## Explain what happens from the moment a user types a URL into a browser's address bar to the point where the page is fully rendered.

請解釋當使用者在瀏覽器網址列輸入網址後，到頁面完全顯示出來，這之間發生了什麼事。

### Example answer:

When a user enters a URL in the browser's address bar and presses Enter, the browser will find the correct IP address through a DNS (Domain Name System) lookup. After that, the browser establishes a connection with the server using the TCP/IP three-way handshake. If the site uses HTTPS, it also performs a TLS handshake to create a secure channel.

The browser sends an HTTPS request to the server to ask for the resources of the website. The server processes the request and returns an HTTP response with the resources.

After receiving the resources, the browser parses the HTML, builds the DOM and CSSOM trees. The DOM and CSSOM trees are then combined to form the Render Tree, followed by layout and painting. The browser also executes JavaScript and applies styles, and finally renders everything on the screen.

## Can you explain what CORS (Cross-Origin Resource Sharing) is and how you handle related issues?

請解釋 CORS（跨來源資源共享）是什麼，以及你如何解決相關問題。

### Example answer:

In browsers, the same-origin policy ensures the security of data transmission. It limits websites to only accessing resources from the same origin. If we want to access responses from a different origin, we need Cross-Origin Resource Sharing (CORS), a security mechanism that determines whether websites from different origins can exchange data.

To solve CORS issues, backend engineers can configure specific HTTP response headers to inform browsers which origins are allowed to access the resources. The most common one is the `Access-Control-Allow-Origin` header. Other common headers include` Access-Control-Allow-Methods`, `Access-Control-Allow-Headers`, and `Access-Control-Allow-Credentials`.

> At the end of this article, I included additional explanations of these headers.

## How do you conduct code reviews with frontend engineers?

和前端工程師之間進行 code review，是怎麼進行的?

### Example answer:

After a frontend engineer creates a merge request, the assigned reviewer checks the following things:
First, the code should follow the team's established coding standards and be consistent with the existing codebase.
Second, the code should be easy to understand so that other developers can maintain it easily in the future.
Third, we also need to check whether the feature has any bugs.

We can leave comments directly on the merge request. The most important thing is comments should be constructive, follow the team’s rules, and avoid being subjective or based on personal preferences.

After all suggestions and bugs are fixed, we can merge the branch into the target branch.

## How do you handle disagreements during a code review?

如果 code review 意見不同，怎麼處理呢?

### Example answer:

The first step is to understand both the committer’s and the reviewer’s perspectives. We need to identify the differences between their viewpoints and understand why the committer wants to make certain changes.

After that, we should discuss and try to reach a consensus. We can use official documentation or technical articles to support our perspective and avoid being subjective or relying on personal preferences. The key goal is to make the project better in the long run, so we should choose the solution that improves maintainability and extensibility.

## Supplementary information

### Access-Control-Allow-Origin:

This response header specifies the origin(s) permitted to access the resource. It can be set to a specific origin (e.g., https://example.com) or, for requests without credentials, to the wildcard `*` to allow any origin. If credentials are included in the request, a specific origin must be provided, and the wildcard `*` cannot be used.

### Access-Control-Allow-Methods:

This response header, typically sent in response to a preflight OPTIONS request, indicates the HTTP methods (e.g., GET, POST, PUT, DELETE) allowed when accessing the resource. The browser uses this information to determine if the requested method is permitted for the cross-origin request.

### Access-Control-Allow-Headers:

This response header, also typically sent in response to a preflight OPTIONS request, lists the custom HTTP headers that are allowed in the actual cross-origin request. If a client attempts to send a custom header not listed in this header, the request will be blocked by the browser.

### Access-Control-Allow-Credentials:

This response header indicates whether the client is allowed to send credentials (like cookies, HTTP authentication, or client-side SSL certificates) with the cross-origin request. If this header is present and set to true, the browser will allow the inclusion of credentials. If omitted or set to false, credentials will not be sent. When Access-Control-Allow-Credentials is true, Access-Control-Allow-Origin cannot be set to `*`.

[[Day21] 跨來源資源共用 CORS 基本介紹](https://ithelp.ithome.com.tw/articles/10323953)

[跨域資源共用（CORS）https://www.alibabacloud.com/](https://www.alibabacloud.com/help/tc/api-gateway/traditional-api-gateway/user-guide/cross-origin-resource-sharing)

[深入了解 CORS (跨來源資源共用): 如何正確設定 CORS？](https://www.shubo.io/what-is-cors/)
