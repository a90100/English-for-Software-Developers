# Day 29 - LeetCode problem-solving phrases / LeetCode 解題相關用語

In this article, I will share some common phrases and sentences you can use when solving LeetCode problems during a whiteboard interview.

> 確認需求的句子，可以參考 溝通合作用語。

## Ask about the input range and consider edge cases / 詢問 input 範圍和考慮 edge cases

### Number

* What is the range of the value?
* Are there rounding requirements?

### String

* What is the maximum length of the string?
* What character the string may contain?
* Are there case sensitivity or whitespace constraints?

### Array / Matrix

* What is the size of the array/matrix?
* What is the range of values in the array/matrix?
* Does the array contain negative numbers, duplicates, or can it be empty?

### Lnked List

* What is the length of the linked list?
* What is the range of node values?

### Tree

* How many nodes are in the tree?
* What is the range of node values?
* Is it a perfect, full, or complete binary tree?

> * 滿二元樹 (Full binary tree): 除了樹葉以外，每個節點都有兩個小孩。
> * 完全二元樹 (Complete binary tree): 各層節點全滿，除了最後一層，最後一層節點全部靠左。
> * 完美二元樹 (Perfect binary tree): 各層節點全滿。同時也是 full binary tree 和 complete binary tree 。

### Graph

* How many nodes and edges are there?
* What is the range of node/edge values?

### To ensure we are on the right track, could you please confirm that this input/output example matches your expectations?

為了確保我們方向正確（步調一致），您能否確認這個輸入/輸出範例是否符合您的期望？

> be on the right track 做法、方法適當/正確

### I want to make sure I understand the scope fully. What are the definitive constraints or specifications I need to adhere to before I begin coding?

我想確保我完全理解範圍。在我開始寫程式之前，有哪些明確的限制或規格是我需要遵守的？

### Based on my understanding,  I'm anticipating that cases like ... will be key edge cases. Is that accurate?

基於我的理解，我預期像 ... 這樣的案例會是關鍵的極端案例。請問這樣理解準確嗎？

### What’s the input range?

輸入的範圍是多少？

### Can the input be empty or null?

輸入會是空的或 null 嗎？

### Can the numbers be negative?

數字可能是負的嗎？

### Should I handle duplicates?

需要處理重複的值嗎？

### What should I return if the input is invalid?

若輸入無效，應該回傳什麼？

### The expected output is...

預期輸出是...

## Provide test cases / 舉測試案例

### If I have an array like [2,7,11,15] and the target is 9, the two indices would be 0 and 1, right?

如果我有一個像 `[2, 7, 11, 15]` 這樣的陣列，而目標值是 9，那麼這兩個索引應該是 0 和 1，對吧？

### Am I to assume that each input would only have one solution?

我可以假設每個輸入只有一個解嗎？

> Am I to assume... 我是不是該假設...?

### If we run the test with the functoin, the result is 10.

如果我們用這個函式執行測試，結果是 10。

### Let's walk through a simple example to confirm our understanding.

讓我們走過一個簡單的範例來確認我們的理解。

## Explain the solution approach and ideas / 解題方向、想法說明

### To solve this problem, I plan to use a data structure called a hashmap, because it uses a key-value format and allows quick access to the value we want, thereby reducing time complexity.

為了解決這個問題，我打算使用一種稱為哈希表（hashmap）的資料結構，因為它採用鍵值對的格式，能夠快速存取我們想要的值，從而降低時間複雜度。

> I plan to use...

### My approach would be implementing Dijkstra's algorithm to optimize for time complexity in finding the shortest path.

我的方法是實作 Dijkstra 演算法，以優化尋找最短路徑時的時間複雜度。

> My approach would be...

### I think the Union-Find algorithm would be suitable here, as it efficiently handles dynamic connectivity problems in a graph.

我認為 Union-Find 演算法在這裡會很合適，因為它能有效處理圖中的動態連通性問題。

> would be suitable here...

### Although a brute force approach is feasible, it would lead to a Time Limit Exceeded error.

雖然暴力法可行，但它會導致超時錯誤。

### For efficient prefix searching, a Trie is the optimal data structure.

為了高效的前綴搜尋，前綴樹是最佳的資料結構。

### A greedy algorithm can find the solution by making the locally optimal choice at each step.

貪婪演算法可以透過在每一步做出局部最佳選擇來找到解。

### I'm using backtracking to explore all possible combinations and prune invalid paths."

我正在使用回溯法來探索所有可能的組合並修剪無效路徑。

### We can prune the search space by sorting the input first.

我們可以透過先對輸入進行排序來修剪搜尋空間。

### My initial thought process was to use recursion, but that led to redundant calculations.

我最初的思考過程是使用遞迴，但那導致了重複計算。

> My initial thought process was...

### Before writing the recursive function, let's first establish a base case: if the array is empty, return zero.

在撰寫遞迴函數之前，我們先確定一個基本情況（或基本條件）：如果陣列為空，則回傳零。

> Let's first establish a base case. 我們首先確定一個基本案例。

### I’ll keep track of the frequency using a hash map.

我需要記錄出現次數。

> keep track of 追蹤、記錄、掌握某人或某事的動態或情況。

### The key idea is to...

核心想法是...

### Let’s break the problem down.

我們先把問題拆解。

### Based on my understanding...

根據我的理解。

## Write the code / 撰寫程式碼

### I first define a function called fourSum. This function takes two parameters: the first is an array, and the second is a number representing the target value for the four-number sum.

我先定義一個函式，叫做 fourSum。這個函式接收兩個參數：第一個是陣列，第二個是一個數字，代表四個數相加的目標值。

> define a function called(named) 定一個叫 ? 的函式

> take ? parameter(s) 接收 ? 個參數

### I’ll start by writing a helper function.

我會先寫一個輔助函式。

### Let's initialize the DP table with a size of N+1.

我們用 N+1 的大小來初始化 DP 表。

### We need to loop through the array from i equals zero to N minus one.

我們需要從 i 等於零循環遍歷陣列到 N 減一。

### I’ll check if my logic works for all cases.

我會確認邏輯是否適用所有情況。

### This condition serves as our base case for the recursion.

這個條件充當我們遞迴的基本情況。

### Let’s dry run the code.

我們手動跑一次程式看看。

### I might have a bug here.

這裡我可能有 bug。

### Let’s debug this part.

我們來除錯這一段。

### The code looks good to me.

程式看起來沒問題。

### I’ll optimize it later if needed.

若有需要，我之後會優化它。

### I need a moment to re-evaluate the approach.

我需要一點時間來重新評估這個方法。

### This is where we could potentially have an **off-by-one error**.

這可能是我們可能會出現**差一錯誤**的地方。

> 差一錯誤（英語：Off-by-one error，縮寫OBOE）是在計數時由於邊界條件判斷失誤導致結果多了一或少了一的錯誤，通常指電腦編程中迴圈多了一次或者少了一次的程式錯誤，屬於邏輯錯誤的一種。比如，程式設計師在迴圈中進行比較的時候，本該使用「小於等於」，但卻使用了「小於」，或者是程式設計師沒有考慮到一個序列是從0而不是1開始（許多程式語言的陣列下標都是這樣）。

[差一錯誤 WIKI](https://zh.wikipedia.org/zh-tw/%E5%B7%AE%E4%B8%80%E9%94%99%E8%AF%AF)

### We must handle integer overflow if the numbers are too large.

如果數字太大，我們必須處理整數溢位。

## Discuss time and space complexity / 討論時間、空間複雜度

| Big O 表示法  | 英文說法 |
| ---------- | -------- |
| O(1) | Big O of one / Constant time |
| O(log n) | Big O of log n / Logarithmic time |
| O(n) | Big O of n / Linear time |
| O(n log n) | Big O of n log n / Linearithmic time |
| O(n²) | Big O of n squared / Quadratic time |
| O(n³) | Big O of n cubed / Cubic time |
| O(2^n) | Big O of two to the power n / Exponential time |
| O(n!) | Big O of factorial n / Factorial time |

* constant space => 常數空間
* requires additional linear space => 需要額外的線性空間
* space complexity is proportional to the input size => 空間複雜度與輸入大小成正比

### We need to optimize the algorithm to achieve Big O of n time instead of n squared.

我們需要優化這個演算法，讓時間複雜度從 O(n²) 降到 O(n)。

### Accessing an element in an array is a Big O of one operation.

存取陣列中的元素是 O(1) 的操作。

### The space complexity is Big O of n because we are using a hash map to store up to n elements.

空間複雜度是 O(n)，因為我們使用了一個雜湊映射來儲存最多 n 個元素。

### There's a time-space trade-off: we use extra space (Big O of n) to achieve a faster runtime (Big O of n).

這裡存在一個時間與空間的權衡取捨：我們使用額外的空間 (O(n)) 來實現更快的運行時間 (O(n))。

> time-space trade-off 時間與空間的權衡取捨

### This approach trades space for time.

這個方法是以空間換取時間。

### This is the optimal time complexity we can achieve for this problem.

這是我們針對這個問題可以達到的最佳時間複雜度。

## Other expressions that can be used during the problem-solving process / 其他可以用在解題過程的用語

### Since

因為。

#### 範例：

Since this problem is similar to a previous one I solved on LeetCode.

### Next

接下來。

#### 範例：

Next, I will use a hash map to optimize the solution for this LeetCode problem and reduce the time complexity.

接下來，我會使用雜湊表來優化這題 LeetCode 的解法，並降低時間複雜度。

### And finally

最後。

#### 範例：

And finally, I analyzed the time complexity of my solution and confirmed that it runs in O(n log n) time.

最後，我分析我的解法的時間複雜度，並確認它的執行時間為 O(n log n)。

### to verify that...

驗證...是否...。

#### 範例：

To verify that my code handles edge cases, I added custom test inputs with empty arrays and large numbers.

為了確認我的程式能處理邊界情況，我加入了空陣列與大數字的自訂測資。

### in some cases

在某些情況下...。

#### 範例：

In some cases, a problem might look like dynamic programming, but a greedy approach works better.

在某些情況下，問題看起來像是動態規劃，但其實用貪心法更有效。
