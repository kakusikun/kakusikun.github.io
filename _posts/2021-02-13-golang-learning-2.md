---
layout: post
title: Golang Learning 2
tags: [golang, learning]
---

看過 golang 關於基本架構的部分，把一些可能會忘記的細節整理成條列式以方便未來的記憶甦醒

關於語法的部分看 a tour of go 就非常充足了

* package 可以由一個或多個 ```.go``` 的檔案組成
* 一定要記得要有 ```package main``` 的 package
* package 的名字應該都要是小寫英文
* 只要 ```.go``` 的開頭是 ```package main```，就代表是 ```main``` 的 package 下的內容
* package 通常會用一個目錄來包含以便管理
* 如果是使用 ```./``` 的 package，會在相對目錄開始找
* 發現一個講 standard library (STL) 的好資源 [Go语言标准库](http://books.studygolang.com/The-Golang-Standard-Library-by-Example/)
* 東西都會放在，以 linux 為主要系統的話，```$GOROOT/pkg/$GOOS_$GOARCH/```
* 一個 package 內定義的 identifier 是以大寫字母為開頭，那這個 identifier 就是要做為外部使用，如同 public，小寫字母開頭則不得從外部使用，如同 private
* 通常使用 package，都是以 ```pack.method``` 的形式來說明 ```method``` 是來自 package ```pack```
* package name 也可有 alias，```import fm "fmt"```，以 ```fm``` 代替 ```fmt```
* go 會抓出根本沒在用的 package 並給編譯錯誤
* ```main``` 的 package 一定要有 ```main``` 為名稱的函數，否則會有編譯錯誤
* ```main``` 函數沒有參數也不回傳值
* 一個 package 內如果有 ```init``` 為名稱的函數，一定會在使用該 package 前先執行該函數，要不然就是 ```main```
* 函數內的程式碼會用 ```{}``` 包住，其中 ```{``` 一定要跟函數名稱在同一行，如
    ```
    func functionName(parameter_list) (return_value_list) {
    …
    }
    ```
* 承上，也可以同一行
* 函數名稱同樣是 identifier，因此開頭字母的大小寫同樣是作為是否外部使用的規則，外部使用的函數名稱就用 ```AbcdAbc``` 的方式，反之則是 ```abcdAbc``` 的方式
* package 的說明注釋會用 ```//``` 來做開頭，並且會放置於 ```package XXX``` 的定義之前
* 任何常數，變數都應該要在定義前有給予注釋
* 如果是函數的注釋，則注釋開頭就必須要用函數名稱
* 這些注釋有助於執行如 ```go doc pack``` 這樣來產生 package ```pack``` 的注釋文檔
* 不給初始值的變數定義會自動用**零值**來做初始化
* 函數若傳回多個值如，```return a, b```，多是作為判斷函數是否執行成功的方式
* 通常會以以下順序來組成基本結構
    - import package
    - 常數、變數、類型的定義
    - ```init``` 函數，如果有
    - ```main``` 函數，```main``` package 則必須有
    - 各種函數，依序是
        - 類型的
        - ```main``` 函數依序會用到的
* 執行時從 package 的 import 開始遞迴執行
* 精度大轉到精度小的型態，會有編譯錯誤
* 不用 ```GetXXX``` 的方式來命名取得物件的函數，可能會直接用 ```XXX``` 或 ```NewXXX```
* 修改物件則用，```SetXXX```

參考 : [4.2. Go 程序的基本结构和要素](https://learnku.com/docs/the-way-to-go/the-basic-structure-and-elements-of-the-go-program/3583)