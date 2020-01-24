---
layout: post
title: Python in a nutshell 閱讀筆記(一)
tags: [reading, python]
---

# Python in a Nutshell，閱讀筆記(一)

閱讀前已經有一定程度上對 python 的認識，所以著重於先前使用 python 時未注意的細節上進一步了解

## token

python 將程式中的每一行程式碼，依據 whitespace 來拆成一個一個的單元，而這個單元就稱為 token

```python=
x = 0 # 3個 token
if x != 0: # 4個 token
    print(f"{x} is not zero") # 1個 token
```

因此，token 就有可能是 identifier、operator、keyword、literal 等等

## hashable 與 mutable

關於 set 與 frozenset 提到了 hashable 與 mutable 的概念

hashable 來自於為了讓資料的存取更加快速地進行查找，基本上的元素包括

- key
    - 通常為查詢時輸入的關鍵字，以會員資料搜尋來說就是會員名稱
- hash function
    - 接受 key 為輸入，並產生 hash value
- hash value
    - hash table 上的 index
- hash table
    - index 與資料間 mapping 的地方

<center> 

[![](https://i.imgur.com/18B52mN.png) ](https://en.wikipedia.org/wiki/Hash_table)

</center>

- hash function 讓資料與 index 的關係與搜尋資料時所使用的 key 切開管理，假設僅有四筆資料，但卻讓 key 與 index 直接對應，直接用 key 搜尋資料，而如果 key 為一個很大的數字 (index 以數字表示) 時，如 100 ，表示 hash table 是一個相當 sparse 的狀態卻需要用到空間 100 的狀態去儲存，又或是 key 為字串或是其他不是與 index 相同表示方式時，都會帶來空間浪費或是不方便，因此利用 hash function 進行 key 與 index 的 mapping 管理會更好，而關於 hash function 的設計便不再話下，詳見[此處](http://alrightchiu.github.io/SecondRound/hash-tableintrojian-jie.html)

- 而 python 當中 immutable object 通常是 hashable，而 hash() 便是回傳 hash value，hash(x) = print(x.\_\_hash__())

- 這裡又可以探討 id、hash、==、is 以及對應的三種值 identity、value、hash value

    - id(x) 回傳一個整數，代表著 x 的 identity 的概念，所以兩個 object 為一樣的 identity 時，代表 a is b 或是 id(a) == id(b)
    ```python=
    a = 5
    b = a
    print(id(a)) # 140718980034960
    print(id(b)) # 140718980034960
    print( a is b) # True
    ```
    - hash(x) 回傳 hash value，也代表 x 為 immutable 並且能夠作為 dict key 一樣能夠在 hash table 中找出對應的 value，也因此同樣 value 的兩個不同 object 會有一樣的 hash value，而可以確認資料內容在傳遞時是否有誤
    ```python=
    a = (1,2)
    b = (1,2)
    print(hash(a)) # 3713081631934410656
    print(hash(b)) # 3713081631934410656
    print(a == b) # True
    ```

### set 與 frozenset
- set 內的 object 則必須是 hashable 而 set 本身不是 hashable，所以 set 中不能有 set，frozenset 是 immutable 所以是 hashable，基本上 frozenset 就是 immutable 版本的 set
    ```python=
    a = frozenset([5,6])
    b = frozenset([5,6,7])
    a.add(9) # immutable, has no attribute 'add'
    ---------------------------------------------------------------------------
    AttributeError                            Traceback (most recent call last)
    <ipython-input-23-ad7abbebd715> in <module>
          1 a = frozenset([5,6])
          2 b = frozenset([5,6,7])
    ----> 3 a.add(9)

    AttributeError: 'frozenset' object has no attribute 'add'
    ```
    ```python=
    a = set([5,6])
    b = set([5,6,7])
    a.add(9)
    print(a)
    # {9, 5, 6}
    ```

## callable
以下幾項是可以直接被呼叫的 object，也就是可以 function_object(arguments) 的形式執行

- built-in function
- function，以 def 定義
- generator
- built-in type
- class object
- class method，\_\_call__()

待續 ...