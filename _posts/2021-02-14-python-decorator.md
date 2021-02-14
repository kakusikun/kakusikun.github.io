---
layout: post
title: Python 上一些用於 classmethod 的 decorator 使用方法
tags: [python, research]
---

關於 python 的 decorator 的一般使用方式已經相當熟悉，但有時需要一種模式是希望新增的類別（稱為 ```Tool```）是向某個類別（稱為 ```A```）註冊，讓 ```A``` 是能夠直接找到 ```Tool```，如果用繼承的方式也不太適合，因此考慮用一個類別在別的類別上的 decorator。

有時也需要繼承的類別可以在格式或是參數上，使用通用的規則來呈現或檢查等等，因此考慮用父類別在子類別 method 上的 decorator


```python=
class A:

    @classmethod
    def decorator_for_other_cls(cls, *args, **kwargs):
        print('decorator_for_other_cls, args', args)
        print('decorator_for_other_cls, kwargs', kwargs)
        def wrap(other_cls):
            print('other_cls', other_cls.__name__)
        return wrap

    @classmethod
    def decorator_for_other_cls_method(cls, *args, **kwargs):
        print('decorator_for_other_cls_method, args', args)
        print('decorator_for_other_cls_method, kwargs', kwargs)
        def wrap(method):
            def wrap2(ins, *wargs, **wkwargs):
                print('method', method.__name__)
                print('method, args', wargs)
                print('method, kwargs', wkwargs)
            return wrap2
        return wrap

@A.decorator_for_other_cls('ToolForA', kwargs='ToolForA_kwargs')
class ToolForA:
    def __init__(self):
        self.name = 'ToolForA'

# decorator_for_other_cls, args ('ToolForA',)
# decorator_for_other_cls, kwargs {'kwargs': 'ToolForA_kwargs'}
# other_cls ToolForA

```

根據上面的程式，**一個類別在別的類別上的 decorator**，與一般的 decorator 差不多，最外層的參數是取得 decorator 的參數，內部包的另一層 function 所取得的參數就是需要拿到的類別

一旦執行程式，在 python 找到 ```ToolForA``` 的定義後就會第一步傳入 decorator 的參數，然後取得類別 ```ToolForA```

```python=
class ChildA(A):
    @A.decorator_for_other_cls_method('ChildForAMethod', kwargs='ChildForAMethod_kwargs')
    def child_a_method(self, method_args, wkwargs='method_kwargs'):
        print('ChildA method')
        print(method_args)

# decorator_for_other_cls_method, args ('ChildForAMethod',)
# decorator_for_other_cls_method, kwargs {'kwargs': 'ChildForAMethod_kwargs'}


child_a = ChildA()
child_a.child_a_method('method_args', wkwargs='method_kwargs')

# method child_a_method
# method, args ('method_args',)
# method, kwargs {'wkwargs': 'method_kwargs'}
```

根據上面的程式，**父類別在子類別 method 上的 decorator**，在傳入參數的部分並沒有太大差異，但需要包住兩層 function（wrap 與 wrap2），wrap 取得需要拿到的子類別 method，而 wrap2 才是進一步取得外部向子類別 method 傳入的參數

以上是使用 decorator 上的一些自己需要的特殊需求




