# Day 15 - 開發相關單字 Part 3 / Development-related vocabulary Part 3

In this article, I have compiled some words that might be used in software development.

### back-and-forth

來回的，在交流情境通常指「反覆討論」「多次往返的溝通」。

#### 範例：

There was a lot of back-and-forth between the frontend and backend teams before we finalized the API contract.

在前端與後端團隊之間，經過了許多次反覆的討論後，我們才最終確定 API 的格式。

### case sensitive

區分大小寫。

#### 範例：

Passwords are case sensitive, so "Apple123" is different from "apple123".

密碼是區分大小寫的，所以「Apple123」和「apple123」是不一樣的。

### case-insensitive

不區分大小寫。

#### 範例：

The search function is case-insensitive, so "User" and "user" will return the same results.

搜尋功能不區分大小寫，所以「User」和「user」會得到相同的結果。

### fixed value

固定值。

#### 範例：

Hardcoding a fixed value in the code may cause issues when requirements change.

在程式裡硬編一個固定值，可能在需求變更時造成問題。

#### Fixed value vs. Constant

* Fixed value：固定值，但可能只是目前寫死在程式中。
* Constant：常數，在程式語言層面上明確宣告不可變。

### dropped frames

掉幀。

#### 範例：

Using requestAnimationFrame helps synchronize rendering with the display refresh rate, which prevents dropped frames.

使用 requestAnimationFrame 可以讓渲染與螢幕刷新率同步，避免掉幀。

### rule of thumb

經驗法則。

#### 範例：

A good rule of thumb in web performance is to keep image sizes under 200KB.

在網頁效能上的一個經驗法則是保持圖片大小低於 200KB。

### best practice

最佳實務。

#### 範例：

Using semantic HTML tags is considered a best practice for accessibility.

使用語意化的 HTML 標籤被視為無障礙設計的最佳實務。

### task prioritization

任務優先排序。

#### 範例：

Effective task prioritization helps the development team focus on critical features first.

有效的任務優先順序可以幫助開發團隊先專注於關鍵功能。

### user flow

使用者流程。

#### 範例：

Before designing the interface, we mapped out the user flow to ensure a smooth onboarding experience.

在設計介面之前，我們先繪製了使用者流程圖，以確保新手使用者體驗順暢。

### self-contained

獨立的、自給自足的。

在軟體開發中，這個詞通常用來形容一個元件、模組或系統，它包含了自己運作所需的所有東西，不需要依賴外部的複雜配置或資源。

#### 範例：

Each microservice is a self-contained unit with its own database.

每個微服務都是一個獨立的單元，擁有自己的資料庫。

### out of the box

開箱即用、原生就支援、不需要額外設定。

在軟體開發中，通常用來形容某個框架、工具或套件本身就提供某些功能，不需要開發者再額外安裝或手動設定。

#### 範例：

Next.js provides server-side rendering out of the box, so developers don’t need to set it up manually.

Next.js 原生就支援伺服器端渲染，開發者不需要再手動設定。

### technical jargon

專業術語、技術術語。

#### 範例：

When writing documentation, I try to avoid using too much technical jargon so that non-technical stakeholders can understand it.

撰寫文件時，我盡量避免使用過多的技術術語，讓非技術相關的利害關係人也能理解。

## Word comparisons / 單字比較

### Wireframe vs. mockup vs. prototype

* Wireframe(線框圖)：用來表示網頁或應用程式的基本結構和布局，通常不包含顏色、字型或圖形等詳細設計元素。
* Mockup (模型圖)：展示更詳細的視覺設計，包含顏色、字型、圖片等元素，接近最終產品的外觀，但還不具備互動功能。
* Prototype (原型)：比 mockup 更進一步，提供可互動的元素（如按鈕、導航等），讓用戶可以體驗到基本的操作流程。

#### 參考文章

[Wireframe、Mockup與Prototype的差異？來看看完整的產品UI設計流程](https://kopu.chat/wireframe%E3%80%81mockup%E8%88%87prototype%E7%9A%84%E5%B7%AE%E7%95%B0%EF%BC%9F%E4%BE%86%E7%9C%8B%E7%9C%8B%E5%AE%8C%E6%95%B4%E7%9A%84%E7%94%A2%E5%93%81ui%E8%A8%AD%E8%A8%88%E6%B5%81%E7%A8%8B/)

### functionality 和 feature 在軟體開發上的差異

這兩個單字在軟體開發的中文意思都和功能有關，也常能互換使用，但實際上指的功能又有點不同。

#### feature

指在一個軟體產品中，使用者可以看到、操作的具體功能，常會在軟體文件或產品規則說明書看到。

例如：

* Login/Signup feature
* Search feature
* Auto-save feature

#### functionality

比較偏向描述軟體可以做到的事情、能力，或是這個功能如何運作的。例如一個社群應用程式擁有和他人交流的功能，這個"功能"就是 functionality，而其中的發送訊息、發送貼文、按讚等"功能"就是 feature。

### document 和 documentation 的差別

document 為可數名詞，表示單一文件，可以是 Word、PDF、Markdown、Google Doc 等形式。

documentation 為不可數名詞，一整套文件的總稱，通常是系統化的資料，幫助使用者或開發者理解與使用某個系統、API、程式碼。

#### 範例：

Please upload the design **document** to the project folder.

請把設計文件上傳到專案資料夾。

The API **documentation** provides details about all available endpoints.

API 文件提供了所有可用端點的詳細資訊。

### goal 的 target 的差別

goal 比較是指抽象、長期、不一定有明確數字的目標，通常是想達到的最終成果或方向。

target 比較是指具體、可衡量的短期目標，通常有明確數字或期限。

#### 範例：

Our goal is to improve the overall user experience of the platform.

我們的目標是提升整體的使用者體驗。

Our target is to reduce page load time to under 2 seconds.

我們的目標是把頁面載入時間降到 2 秒以下。

### fault tolerance 和 fault tolerant 的差別

fault tolerance 為名詞，意思是容錯能力、容錯性。

fault tolerant 為形容詞，意思是具備容錯性的、能容錯的。

#### 範例：

Our system was designed with high fault tolerance to handle unexpected server crashes.

我們的系統設計有高度的容錯能力，以應對意外的伺服器崩潰。

We built a fault-tolerant microservice architecture to ensure continuous availability.

我們建立了一個具備容錯性的微服務架構，以確保持續可用。
