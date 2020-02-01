---
layout: post
title: Python in a nutshell 閱讀筆記-2
tags: [reading, python]
---

# Python in a Nutshell，閱讀筆記-2

在上次的 [Python in a Nutshell，閱讀筆記-1](https://kakusikun.github.io/2020-01-24-Python-in-a-Nutshell-1/) 提到 callable 的物件，其中 generator 是比較陌生的，所以針對 generator 好好細看一下

## generator

首先要先談談 iterable 與 iterator 的概念，
### iterable 
  ```text
  An object capable of returning its members one at a time.
  ```
  根據 [python documentation](https://docs.python.org/3/glossary.html#term-iterable)，能夠一個一個慢慢從一個 objec 中去取出其內容的是 *iterable* ，也表示 iterable object 必須定義 \_\_iter__() 或 \_\_getitem__() 來負責怎麼回傳這個 object 的內容，前者會回傳 iterator (待會解說)來負責，而後者是透過 index 或 slice 的方式來呼叫該函數再回傳其內容，如
  ```python=
  class iterable_object:
    def __init__(self):
        self.a = 'a'
        self.b = 'b'
        self.c = 'c'
    def __getitem__(self, index):
        if index == 1:
            return self.a
        elif index == 2:
            return self.b
        elif index == 3:
            return self.c
        else:
            return f'{index} does not exist.'

    a = iterable_object()

    print(a[0])
    print(a[1])
    print(a[2])
    print(a[3])
    print(a[4])
    
    '''
    0 does not exist.
    a
    b
    c
    4 does not exist.
    '''
  ```
### iterator
  ```
  An object representing a stream of data.
  ```
  根據 [python documentation](https://docs.python.org/3/glossary.html#term-iterator)，iterator 是作為回傳 object 內容的媒介，所以必須定義 \_\_next__() 來達到回傳內容的效果，使用上就是透過 **next(iterator)** 來取得其內容，built-in 函數 **next()** 就是呼叫 iterator 的 \_\_next__()，而 iterable 物件並不具有 iterator 的效果，但可以透過 built-in 函數 **iter()** 來回傳一個建立在該 iterable 物件上的 iterator，**iter()** 是去呼叫 iterable 物件的 \_\_iter__()，這就是 iterable 物件需要定義 \_\_iter__() 的原因，但是如果沒定義也沒關係，iter() 這個函數會直接利用 index 與 generator (待會解說)的方式作為 iterator，但前提是該物件要已經是一個 iterable 物件，也就是有 \_\_getitem__() 的定義，才能取得物件內容並透過 IndexError 作為停止的訊號，因為 next() 就是透過回傳 StopIteration 來停止其內容的回傳。

### generator
```
It looks like a normal function except that it contains yield expressions for producing a series of values usable in a for-loop or that can be retrieved one at a time with the next() function.
```
根據 [python documentation](https://docs.python.org/3/glossary.html#term-generator)，generator 其實跟一般的函數一樣，只是定義內容包含了 **yield** 這個 keyword，generator 的效果與 iterator 相似，相同點是
- 都需要透過 next() 來執行
- 透過回傳 StopIteration 來停止

不同在於
- 不用定義 \_\_next__()
- lazy evaluation

針對 lazy evaluation 進一步說明，當呼叫 next() 時，對 generator 其定義內容的執行只會到達有 yield 的地方直接將
```python=
yield expression 
```
看到的 expression 回傳便會停止執行，直到 next() 再次被呼叫時，會從該語句繼續執行直到又碰到 yield 的執行，這麼一來便可以節省記憶體用量，不用先取得大量內容將其回傳，需要的時候才產生出來並回傳。

其中有一個 yield 的功能是在 python3 才有的，
```python=
yield from expression 
```
這個表示法中的 expression 是 iterable 物件的話，可以避免大量重複的 yield 語句，其他效果如 asynchronous 而在未來才繼續深入。

關於 yield 的改變是 yield 語句整體來說還是一個語句，也就是
```python=
def generator():
    ...
    value = yield from expression 
    ...
```
可以從 yield 語句得到一個結果，而該結果是透過 generator.send(value) 獲得的，而 next(generator) 其實就是 generator.send(None)。
```python=
def fibonacci(N):
    a, b = 0, 1
    for _ in range(N):
        v = yield a
        a, b = b, a+b
        if v is not None:
            print(f'receive {v} which means that the yielded value is larger than 5')

a = fibonacci(10)

for i in a:
    print(i)
    if i > 5:
        a.send('!')
'''
0
1
1
2
3
5
8
receive ! which means that the yielded value is larger than 5
21
receive ! which means that the yielded value is larger than 5
'''
```