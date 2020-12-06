# 预备知识: C语言指针

对指针熟悉的读者建议直接跳过,本小节只是对通过Python等类脚本语言入门, 对指针概念不是非常了解的读者做一个科普, 否则难以入门MPI.

## 指针是什么 - 在Python背景下的理解

在使用Python进行一些简单编程(爬虫, excel处理等)任务时大都不涉及指针概念. 但是有一个著名大坑想必90%初学者都踩过: 列表的复制

尝试以下代码:
```python
a = [1, 2, 3]
b = a
b[1] = 3
print(a)
print(b)
```
结果:
```
a = [1, 3, 3]
b = [1, 3, 3]
```
改变b的第二个元素(位置1)时a的第二个元素也跟着改变了