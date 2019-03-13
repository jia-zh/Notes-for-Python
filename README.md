# Notes for Python
[![](https://img.shields.io/badge/update-anytime-success.svg)](https://github.com/jia-zh/Program-Notes-for-Python)
  
Some small code knowledge points I often encounter
  
- [Some Code for List](#some-code-for-list)
- [Some Code for Dict](#some-code-for-dict)

  
### Some Code for List
  
1. 字符串list按照长度排序
```python
my_list = ['青海省', '内蒙古自治区', '西藏自治区', '新疆维吾尔自治区', '广西壮族自治区']  
order_list = sorted(my_list, key = lambda i:len(i),reverse=True)  
print(order_list) 
******************
['新疆维吾尔自治区', '广西壮族自治区', '内蒙古自治区', '西藏自治区', '青海省']  
******************
```

2. 数字list连续分片
```python
from itertools import groupby
my_list = [1, 2, 3, 5, 6, 7, 9, 11, 12, 13, 14]
fun = lambda x: x[1] - x[0]
for k, g in groupby(enumerate(my_list), fun):
    cont_list = [j for i, j in g]
    print(cont_list)
******************
[1, 2, 3]
[5, 6, 7]
[9]
[11, 12, 13, 14]
******************
```

### Some Code for Dict
1. dict排序
```python
my_dict = {'am': 5, 'is': 7, 'are': 3}
my_list = sorted(my_dict.items(), key=lambda d: d[1], reverse=True)
for word in my_list:
    print(word[0] + "\t" + str(word[1]))
print("******")
my_list = sorted(my_dict.items(), key=lambda d: d[0], reverse=True)
for word in my_list:
    print(word[0] + "\t" + str(word[1]))
******************
is	7
am	5
are	3
******
is	7
are	3
am	5
******************
```
