# Day 13 - 開發相關單字 Part 1 / Development-related vocabulary Part 1

In Chinese, many words can represent different meanings depending on the context. For example:

* 他打了我一巴掌。Here, “打” means “to hit or attack with the hand or an object.”
* 你會打籃球嗎？Here, “打” means “to participate in an activity.”
* 她在打電話。Here, “打” means “to dial or connect to a communication device.”

English words are no exception. Below, I’ve compiled some words, explained their meanings in the context of development, and provided example sentences to demonstrate their usage.

---

### escape (v)

escape 有逃走、逃脫的意思，在軟體開發上意思是「轉義」，指的是在程式碼或字串中，將某些有特殊意義的字元進行處理，使它們被當作一般字元來看待，避免誤解或錯誤執行。

例如，我們在 HTML 輸入 `<div></div>`，在瀏覽器上執行 HTML 時，會生成 DOM 元素，但假如我們的目的就是要顯示 `<div></div>` 這個字串內容，那 `<` 和 `>` 要 escape 成 `&lt;` 和 `&gt;`。

#### 範例：

The user input should be escaped before inserting it into the HTML to prevent XSS attacks.

在將使用者輸入插入到 HTML 之前，應該先進行轉義，以防止 XSS 攻擊。

### call、invoke (v)

兩者都有呼叫函式的意思，主要差別在 call 通常用於直接呼叫一個函式的情境，invoke 則比較偏向透過某個機制來觸發函式執行的意思。

#### 範例：

JavaScript allows you to **call** a function with a different `this` context using `.call()`.

JavaScript 允許你使用 `.call()` 以不同的 `this`上下文去呼叫函式。

The event handler is automatically **invoked** when the user clicks the button.

當使用者點擊按鈕時，事件處理器會自動被觸發執行。

### crawl (v)

中文有緩慢移動、爬行的意思，在軟體開發中，則和自動蒐集資料有關。

#### 範例：

Our bot will crawl the website every day to collect the latest news articles.

我們的機器人每天會爬這個網站，收集最新新聞。

### serialize (v)

中文有連載、連播的意思，在軟體開發中，則指序列化。

序列化（Serialization） 是指將資料結構或物件轉換成一個可以儲存或傳輸的格式的過程，通常是轉換成字串（如 JSON、XML、二進位格式）。

#### 範例：

Before sending data to the frontend, the backend will serialize the data object into JSON format.

在將資料傳送到前端之前，後端會先將資料物件序列化成 JSON 格式。

### upscale (v / adj)

它可以當作形容詞，意思是指（商品、產品）高檔的，高級的，也可以當作動詞，意思指提高、提升品質。

軟體開發中，則和提升應用程式或系統的處理能力有關。

#### 範例：

We need to upscale our backend server to handle the growing user base.

我們需要升級後端伺服器，以應對越來越多的使用者。

### compatibility (n)

中文意思是和睦相處、共存性，軟體開發情境中，則比較貼近**不同版本或不同環境之間能不能正常運作、不出錯**的意思。

#### 範例：

We need to perform thorough browser compatibility testing to ensure our website works smoothly on Chrome, Firefox, and Safari.

我們需要進行完整的瀏覽器相容性測試，以確保我們的網站在 Chrome、Firefox 和 Safari 上都能順利運作。

### maintainability (n)

可維護性，意思是系統或程式在未來維護、修正錯誤或擴充功能時的難易程度。

#### 範例：

To improve the maintainability of the code, we will refactor this complex logic and add unit tests.

為了提高程式的可維護性，我們將重構這段複雜的邏輯，並加入單元測試。

### traffic (n)

常見中文意思可以指交通、交通流量、運輸量，但和網路相關時，指的是資料流量或使用者請求量。

#### 範例：

We can give you advice on how to improve your site traffic and generate sales.

我們可以為您提供有關如何增加網站流量和提升銷售量的建議。

### statement (n)

中文意思為陳述，說明，用在寫程式中，意思是代表程式碼執行的指令，它告訴程式要做一件事情。

#### 範例：

This statement tells the browser to write "Hello Dolly." inside an HTML element with id="demo".

這個語句告訴瀏覽器在 id 為 'demo' 的 HTML 元素中寫入『Hello Dolly.』

`document.getElementById("demo").innerHTML = "Hello Dolly.";`

### truncate (v)

中文意思為截斷、縮短 或刪減。開發情境多指將資料（如文字、檔案、資料表）截斷到指定長度。

#### 範例：

We used a custom function to truncate the user input to 50 characters before displaying it on the screen.

我們使用自訂函式將使用者輸入截斷為 50 個字元再顯示在畫面上。

### indices (n)

為 index 的複數，中文意思為索引，用在程式設計中常指陣列的索引。

#### 範例：

In most programming languages, array indices start at zero.

在大多數程式語言中，陣列索引是從零開始的。

### comment (n)

中文意思為評論、意見，用在寫程式中，意思是註解。

#### 範例：

Good comments can make your code much easier to maintain.

良好的註解可以讓你的程式碼更容易維護。

### accessibility (n)

中文意思為可及性、可訪問性，在前端開發中，則指無障礙性。

#### 範例：

Improving accessibility ensures that users with disabilities can navigate and interact with the website effectively.

提升無障礙性可以確保有障礙的使用者也能有效瀏覽與操作網站。

### robust (adj)

中文意思是強健的、穩健的、耐用的，在軟體開發中指系統或程式穩定性強、不易出錯。

#### 範例：

We need to design a robust API that can handle high traffic and unexpected errors.

我們需要設計一個穩健的 API，能夠應對高流量與突發錯誤。

### practical (adj)

實際的、可行的。

在軟體開發中，通常用來表示某個解決方案不只是理論上正確，而是實際上可行、有效率，並能解決問題。

#### 範例：

Instead of building a complex custom framework, we chose a more practical solution by using an existing open-source library.

我們沒有自行建立一個複雜的客製化框架，而是選擇使用現有的開源函式庫，這是一個更實際可行的解決方案。

### under the hood

字面是「引擎蓋底下」，在軟體開發裡比喻背後的運作機制 / 底層原理。

#### 範例：

React handles DOM updates efficiently under the hood, so developers don’t need to manipulate the DOM directly.

React 在底層會有效率地處理 DOM 更新，所以開發者不需要直接操作 DOM。

### wrap something in/into something

把某個東西「包裹在」另一個東西裡。

在軟體開發中，常指將功能、邏輯或元件放進另一個結構/函式/容器裡。

#### 範例：

We can wrap the API call in a try-catch block to handle errors gracefully.

我們可以把 API 呼叫包在 try-catch 區塊裡，以更優雅地處理錯誤。

---

### JavaScript-related terms / JavaScript 相關單字

* declare a constant 常數宣告
* block scope 區塊作用域
* function scope 函式作用域
* destructuring assignment 解構賦值
* template literals	樣板字串
* reference type vs primitive type 參考型別 vs 原始型別
* variable hoisting 變數提升
* self-invoking functions、immediately invoked function expressions (IIFEs) 立即(調用)函式
* spread operator 展開運算符
* rest operator 其餘運算符
* implicit Type Coercion 隱性型別轉換
* type coercion 強制類型轉換
* event bubbling / capturing 事件冒泡 / 捕獲
