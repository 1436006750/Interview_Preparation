# Python知识点
## 1、Python基本数据类型

Python3 中有六个标准的数据类型：

Number（数字）
String（字符串）
List（列表）
Tuple（元组）
Set（集合）
Dictionary（字典）





List（列表）：
    删除元素：
        a.pop(index):删除列表a中index处的值,并且返回这个值.
        del(a[index]):删除列表a中index处的值,无返回值. del中的index可以是切片,所以可以实现批量删除.
        a.remove(value):删除列表a中第一个等于value的值,无返回.
```python
a = [0, 2, 3, 2]
a.remove(2)
print(a)  # [0, 3, 2]

a = [3, 2, 2, 1]
del a[1]
print(a)  # [3, 2, 1]


a = [4, 3, 5]
a.pop(1)  # 3
print(a)  # [4, 5]

# 错误信息也不一样
a = [4, 5, 6]
a.remove(7)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: list.remove(x): x not in list
>>> del a[7]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list assignment index out of range
>>> a.pop(7)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: pop index out of range
```
Dictionary（字典）：
    合并字典：
        