# List 链表

将数据进行链式存储

## 方法

| 方法                          | 含义                                                         |
| ----------------------------- | ------------------------------------------------------------ |
| ```list<int>l```              | 默认构造                                                     |
| ```l.push_back(value)```      | 尾插                                                         |
| ```l.assign(begin,end)```     | 区间复制                                                     |
| ```swap(l1,l2)```             | 交换链表                                                     |
| ```l.assign(n,element)```     | 复制```n```个```element```到```l```                          |
| ```l.resize(num)```           | 指定大小                                                     |
| ```l.size()```                | 返回长度                                                     |
| ```l.empty()```               | 是否为空                                                     |
| ```l.pop_back()```            | 删除最后的                                                   |
| ```l.pop_front()```           | 删除最前面的                                                 |
| ```l.push_front(element)```   | 头插                                                         |
| ```l.insert(pos,n,element)``` | pos位置插入n个元素，n可省略，省略后代表插入一个              |
| ```l.clear()```               | 清除所有元素                                                 |
| ```l.erase(begin,end)```      | 清除[begin,end]之间的元素，如果省略end，代表删除begin位置的元素 |
| ```l.remove(value)```         | 清除与value的值匹配的元素                                    |
| ```l.front()```               | 返回最开头的元素                                             |
| ```l.back()```                | 返回末尾元素                                                 |
|                               |                                                              |
|                               |                                                              |

