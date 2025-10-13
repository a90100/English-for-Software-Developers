# Day 16 - Common Interview Questions for Different Types of Software Engineers / 各種專長的軟體工程師的常見面試問題

In this article, I’ve collected some important interview questions for different types of software engineers. Since my expertise is in frontend development, I’ve separated the frontend questions into another article, where I answer each of them.

**The best way to use this article is to try answering these questions in English.**

## Software Engineer Common Questions / 軟體工程師通用問題

### Why did you decide to become a software engineer?

為什麼你會決定成為一位軟體工程師？

#### Example answer:

I think being a software engineer gives me a great sense of accomplishment.

With your skills, you can create many interesting and useful tools that make people’s lives easier. That’s why there are so many open-source projects on GitHub. Many maintainers are willing to contribute to these projects even though they don’t get paid. I guess one of the reasons is that the sense of accomplishment gives them the motivation.

### How do you ensure code quality and maintainability?

你如何確保程式碼的品質與可維護性？

#### Example answer:

The first question is: why do we need to ensure code quality and maintainability? I think it’s because we want our colleagues and future maintainers to easily understand our code.

So, first of all, I always follow consistent naming conventions, making sure that variable and function names are easy to understand. I also keep each function focused on doing only one thing.

Second, I participate in code reviews with other engineers to ensure clarity and maintain consistency across the team.

Third, I write documentation and add clear comments when necessary.

Finally, I refactor code when requirements or features change significantly, in order to prevent accumulating too much technical debt.

### Please explain the Gitflow workflow your team follows.

請說明你所在的團隊的 Gitflow 流程。

#### Example answer:

We have three core branches: develop, release, and master, and they correspond to three deployment environments: dev, stage, and production.

The dev environment is mainly for software engineers, and it gets updated most frequently. The stage environment is used by QA engineers for testing, and the production environment is for real users.

For each new feature, we create a feature branch from develop. After completing the feature, we submit a merge request and go through a code review with other engineers. Once approved, the feature branch is merged back into develop.

When we are preparing for a new release, we create a release branch from develop and let QA engineers run tests on it. If new bugs are found, we create bugfix branches from develop to fix them. Once all bugs are resolved, we update the latest release branch and let QA engineers test again.

If all tests pass, the release branch is merged into master, making the latest features available to end users.

For urgent production issues, we create hotfix branches directly from master to fix the bugs. After applying the fix, we also merge master back into develop to ensure the bug is resolved in the dev environment as well.

## Backend Engineer Interview Questions / 後端工程師面試問題

### How would you design a system to handle high concurrency?

你如何設計一個高併發的系統？

### Can you explain the differences between REST and GraphQL and when to use them?

請解釋 REST 與 GraphQL 的差異與使用情境。

### Compare the pros and cons of SQL and NoSQL databases, and explain in which scenarios you would choose to use a NoSQL database.

請比較 SQL 和 NoSQL 資料庫的優缺點，並說明在什麼情境下會選擇使用 NoSQL 資料庫。

### Explain how to design a scalable system and describe the difference between horizontal and vertical scaling.

請說明如何設計一個可擴展的系統，並解釋水平擴展（horizontal scaling）和垂直擴展（vertical scaling）的差異。

### Explain the advantages and disadvantages of a microservices architecture and describe how services can communicate with each other (e.g., synchronously or asynchronously).

請說明微服務架構的優點和缺點，並解釋服務間如何溝通（如同步或非同步）。

## Full-stack Engineer Interview Questions / 全端工程師面試問題

### Explain why data validation should be performed on both the frontend and the backend.

請說明為什麼資料驗證（data validation）應該同時在前端和後端進行。

### Explain the difference between authentication and authorization, and describe how you would implement user authentication using JSON Web Token (JWT).

請解釋認證（authentication）和授權（authorization）的區別，並說明如何使用 JSON Web Token (JWT) 實現使用者認證。

## QA Engineer Interview Questions / 測試工程師面試問題

### Describe how you would write a test plan for a new feature, including the design of test cases.

請說明你會如何為一個新功能撰寫測試計畫，包含測試案例的設計。

### What is your process when you discover a bug? How do you communicate with the development team?

當發現一個 bug 時，你的處理流程是什麼？你會如何與開發團隊溝通？

### Explain how you would decide which test cases are suitable for automation, and briefly describe the advantages and challenges of test automation.

請說明你會如何決定哪些測試案例適合進行自動化，並簡述自動化測試的優點和挑戰。

## Mobile App Engineer Interview Questions / 行動裝置 APP 工程師面試問題

### How do you ensure an app works properly across different devices and screen sizes?

你如何確保 App 在不同裝置與螢幕大小上都能正常運作？

### List several techniques you would use to optimize battery consumption and memory usage when developing a mobile application.

請列舉幾個在開發行動裝置應用程式時，用來優化電池消耗和記憶體使用的技巧。

### Explain how you would handle different screen sizes and devices on mobile platforms to ensure a consistent UI/UX.

請說明如何在行動裝置上處理不同尺寸的螢幕和裝置，以確保一致的 UI/UX。

## Data Engineer Interview Questions / 資料工程師面試問題

### Explain the difference between ETL and ELT, and describe in which scenarios each would be a better choice.

請解釋 ETL 和 ELT 的區別，並說明它們各自適合在什麼情境下使用。

### Explain how a distributed computing framework (e.g., Hadoop or Spark) processes big data, and describe the basic concept of MapReduce.

請說明分散式運算框架（如 Hadoop 或 Spark）是如何處理大數據的，並解釋 MapReduce 的基本概念。

### Describe the components that a robust data pipeline should include and discuss how to ensure data quality and consistency.

請說明一個健壯的資料管道應該包含哪些組成部分，並討論如何確保資料的品質和一致性。

## Security Engineer Interview Questions / 安全工程師面試問題

### Can you provide an example of a security vulnerability you have handled?

請舉例說明你處理過的一次安全漏洞。

### How do you integrate security checks into a CI/CD pipeline?

你如何在 CI/CD pipeline 中導入安全檢查？

### Describe how to design a secure authentication system and discuss the importance of multi-factor authentication (MFA).

請說明如何設計一個安全的認證系統，並討論多重驗證（MFA）的重要性。

## DevOps Engineer Interview Questions / DevOps 工程師面試問題

### Explain the stages of a typical CI/CD (Continuous Integration/Continuous Deployment) pipeline and describe its benefits.

請說明一個典型的 CI/CD (持續整合/持續部署) 流程包含哪些階段，並解釋其優點。

### Explain what Infrastructure as Code (IaC) is, compare it with manually configuring servers, and describe the advantages of using IaC.

請解釋什麼是 IaC，並與手動配置伺服器的方式進行比較，說明 IaC 的優勢。

### How do you handle troubleshooting and recovery when a system fails?

當系統出現故障時，你會如何進行故障排除與恢復？
