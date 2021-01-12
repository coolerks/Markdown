# set

所有元素在插入时被自动排序，属于**关联式容器**

set容器分为**set**和**multiset**

multi(多)

### 区别

**set**不允许有重复元素

**multiset**允许重复元素

#### 用法

| 形式                          | 用途                  |
| ----------------------------- | --------------------- |
| ```set类型变量=set类型变量``` | 赋值                  |
| ```变量.insert(数据/变量)```  | 插入                  |
| ```变量.size()```             | 查看长度              |
| ```变量.swap(变量1)```        | 互换                  |
| ```变量.clear()```            | 清空                  |
| ```变量.erase(值)```          | 删除元素              |
| ```变量.find()```             | 此时为指针(迭代器)    |
| ```变量.count```              | 若为set，结果只有0或1 |



### 构造和赋值

####构造

+ ```set<类型> 变量```默认构造

+ ```set(set型变量)```拷贝构造

  + 拷贝构造示例

    ```c++
    vector<int>a{1,4,6,657,8,48,58};
    set<int>st(a.begin(),a.end());
    ```

    

#### 赋值

+ ```set类型变量=set类型变量```

#### 插入数据

```变量.insert(数据/变量)```

#### 遍历输出

#####1.方法1

```C++
#include <bits/stdc++.h>
using namespace std;
int main()
{
	set<int> st;
	st.insert(10);
	st.insert(20);
	st.insert(30);
	st.insert(40);
	int q = 50;
	st.insert(q);
	for (auto c : st)
		cout << c << endl;
	return 0;
}
```
##### 2.方法2

使用迭代器进行访问

```C++
#include<bits/stdc++.h>
int main()
{
    set<int>st;
    //插入数据
    for(set<int>::iterator i=st.begin();i<st.end();i++)
        cout<<*i;
    return 0;
}
```



#### 查看长度

```变量.size()```

#### 容器互换

```变量.swap(变量1)```

交换变量和变量1的值

#### 清空所有元素

```变量.clear()```

#### 删除某个元素

```变量.erase(值)```

#### 查找元素

```变量.find()```此时为指针(迭代器)

惯用法

```c++
set<int>a;
//插入元素
set<int>::iterator i=a.find(变量);
if(i!=a.end())
    找到元素
```

#### 统计元素的个数

```int 变量1=变量.count(数据)```

当变量为set是数据的个数只有0或者1个，因为不允许插入重复元素

当变量为multiset时，才能真正起作用

##### multiset输出方式与set一致，使用迭代器遍历输出时也一样

#### 判断set元素是否插入成功

```C++
pair<set<int>::iterator,bool> temp =变量.insert(变量/值)；
如果插入成功，则temp.second的值为true，发否则为false
```

## 对组pair

+ 功能：成对出现的数据，可以用来返回两个数据
+ **创建方式****
  + ```pair<type,type>p(v1,v2)```
  + ```pair<type,type>p=make_pair(v1.v2)```

#### 调用

```c++
pair<string,int>p("name",99);//第一种定义方式
cout<<p.first<<p.second;

pair<string,int>p=make_pair("name",99);//第二种定义方式
```

first指向第一个类型的数据，second指向第二个

