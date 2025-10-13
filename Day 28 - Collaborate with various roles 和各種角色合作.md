# Day 28 - Collaborate with various roles / 和各種角色合作

In this article, I will share some common phrases and sentences you can use when collaborating with these roles.

## Collaborate with the Product Manager (PM) / 和專案經理合作

### I noticed some requirements are ambiguous. Could we refine them?

我發現有些需求不夠明確，我們可以再精確定義嗎？

### Is this feature more critical than the others on our backlog?

這個功能比 backlog 上的其他功能更重要嗎？

### What’s the priority of this task compared to others?

這個任務和其他任務比起來優先順序是什麼？

### We're on track to meet the deadline.

我們在預定的時間內，進度正常。

### I need more time to work on this bug fix.

我需要更多時間來修復這個錯誤。

### The current progress is ahead of schedule.

目前的進度超前了。

### We need to be careful about scope creep to avoid delaying the project.

我們需要小心範圍蔓延，以免延遲專案。

### Do we have flexibility on the deadline?

這個截止日期有彈性嗎？

### Key words

* requirements (需求)
* scope (範圍)
* priority (優先順序)
* trade-off (取捨)
* timeline / deadline (時程 / 截止日)
* scope creep(範圍蔓延、專案範圍在進行中不斷擴大)

## Collaborate with the UI Designer / 和介面設計師合作

### Can you share the latest design mockup?

你能分享最新的設計稿嗎？

### Does this component match the wireframe?

這個元件符合線框圖嗎？

### We need to review the user flow before implementation.

我們需要在實作前檢視使用者流程。

### Is this layout responsive across all devices?

這個版面在所有裝置上都響應式嗎？

### The font size seems a bit off on this component. Could you check the specs?

這個元件的字體大小看起來有點不對，你能檢查一下規範嗎？

> a bit off 的中文意思根據語境不同而有所差異，可以指 「有點不舒服」、「狀態不佳」、「有點不對勁」、「有點偏僻」、「有點不近人情」 等。

### This design is a bit challenging to implement due to performance issues.

這個設計因為效能問題，實作起來有點困難。

### Let's sync up to review the mobile layout.

我們約個時間一起看看手機版的佈局吧。

> sync up 的意思是進行協調同步。
> sync-up meeting 指的是讓團隊成員在任務或進度上保持一致的會議。

### Key words

* design spec (設計規格)
* wireframe / mockup / prototype (線框圖 / 模型圖 / 原型)
* pixel-perfect (像素完美)
* spacing / alignment (間距 / 對齊)
* user flow (使用流程)

## Collaborate with the Frontend Engineer / 和前端工程師合作

### Let's implement lazy loading for all images below the fold.

讓我們對所有首屏以下（不立即顯示）的圖片實施延遲載入。

### We are seeing a hydration mismatch error on the server-rendered page.

我們在伺服器渲染的頁面上看到了水合作用不匹配的錯誤。

> A hydration mismatch is when the content rendered to HTML on the server isn't the same as the content rendered in the browser.

https://vite-plugin-ssr.com/hydration-mismatch

### Can you give me a task handover before you go on vacation?

你休假前能先把任務交接給我嗎？

> task handover 工作交接、任務移交

### Please review my PR; I addressed all the comments from the last code review.

請審核我的 PR；我已經處理了上次程式碼審查中的所有評論。

### We detected a critical bug post-deployment; prepare to rollback to the previous stable version.

我們在部署後發現了一個關鍵錯誤；準備回滾到上一個穩定版本。

> Post deployment 部署後

## Collaborate with the Backend Engineer / 和後端工程師合作

### Can you provide the API endpoint for fetching user data?

你能提供取得使用者資料的 API 端點嗎？

### What’s the expected payload format?

預期的請求內容格式是什麼？

### I'm getting a `404` error when I try to hit this endpoint.

當我嘗試連這個接口時，得到一個 `404` 錯誤。

### Is this a `GET` or `POST` request?

這是 `GET` 還是 `POST` 請求？

### The payload format for this API call is not what I expected.

這個 API 請求的資料格式跟我預期的不一樣。

### The data I'm receiving from the backend is not correctly formatted.

我從後端收到的資料格式不正確。

### The API is returning a 401 status code, which means the user is unauthorized.

這個 API 回傳 401 狀態碼，代表使用者未經授權。

### Is this response format final, or will it change later?

這個回應格式是最終版嗎？還是之後會改？

### Key words

* API contract / endpoint (API 規格 / API 端點，是一個網路地址，通常是 URL)
* payload (在 API 請求或回應中傳輸的資料)

## Collaborate with the Quality Assurance Engineer / 和品質保證工程師合作

### The bug has been fixed and deployed to staging for QA verification.

這個錯誤已經修正並部署到測試環境讓 QA 驗證。

### Could you describe the steps to reproduce this bug?

你能描述一下重現這個錯誤的步驟嗎？

### I've fixed the bug you reported. Could you re-test it?

我已經修復你回報的錯誤了，你能再測試一次嗎？

### Could you confirm the environment where you found this bug?

你能確認一下你在哪個環境發現這個錯誤的嗎？

### The feature is ready for QA testing.

這個功能可以讓 QA 測試了。

### Could you provide the reproduction steps so I can debug this issue?

你能提供重現步驟，讓我能除錯這個問題嗎？

### We need to run a regression test after deploying the new fix.

部署新修復後，我們需要進行回歸測試。

### Is this bug reproducible in staging or only in production?

這個 bug 是在測試環境就能重現，還是只會出現在正式環境？

### Key words

* bug report (錯誤回報)
* reproduction steps (重現步驟)
* edge case (邊緣案例)
* regression test (回歸測試，確認新的修改沒有影響到現有功能)
