# vector

通常称为**单端数组**

#### 与数组的区别

数组是静态空间，vector是动态空间，可以实现动态的扩展

##### 迭代器

```vector<int>::iterator i```

#### #初始化

| 形式                        | 说明                      |
| --------------------------- | ------------------------- |
| ```vector<类型>bianliang``` | 此时的```bianliang```是一个空的 |
|```vector<类型>变量(变量1)```|此时的```变量```是```变量1```的一个副本|
|```vector<类型>变量=变量1```|等价于以上定义方法|
|```vector<类型>变量(n,v)```|vector中有n个元素，且值都是v|
|```vector<类型>变量{1,2...}```|初始化的值为花括号里边的|
|```vector<类型>变量={1,2..}```|与以上作用相同，不要加[]|
| ```vector<类型>变量(n)```      |初始化为n个长度的vector|
|```vector<vector<l>>类型(n)```|初始化长度为n的空vector|
|```v.assign(v2.begin(),v2.end())```|拷贝区间数据|
|```v.resize(n1,n2)```|重新指定长度，指定长度为n1,n2为变长后填充的内容|
|v.insert(begin()+n1,n2,n3)|在n1的位置插入n2个n3，省略n2，就代表在n1位置仅插入一个数n3|
|v.swap(v2)|容器互换|

##### 相关操作

|用法|说明|
|---|---|
|```v.size()```|返回v的长度|
|```v.empty()```|若```v```为空，返回1，反之返回0|
|```v1=v2```|将```v2```拷贝到``v1``|
|```v1={1,2,3,4...}```|将花括号里的内容拷贝到```v1```|
|```v1==v2```|判断两者是否完全一样|
|```v1!=v2```|判断两者是否完全不一样|
|<、>、<=、>=|用字典顺序进行比较|
|```v.push_back(变量/值)```|将变量/值加到v的末尾|
|```v.pop_back()```|将末尾的值删掉|
|```v.begin()```|起始迭代器,指向第一个元素|
|```v.end()```|结束迭代器，指向末尾元素的下一个|
|```max_element(v.begin(),v.end()```|取最大值，返回给迭代器|
|```min_element(v.begin(),v.end()```|取最小值，返回给迭代器|
|```v.erase(v.begin()+n,v.begin+n2)```|删除n到n2-1之间的元素，若省略n2，则删除n位置的元素|

##### 常用遍历/输出元素的方法

1.
```c++
#include<bits/stdc++.h>
int main()
{
    vecotor<int>a;
    for(auto c:a)//仅引用
    {    语句
        cout<<c;
    }
    return 0;
}
```
2.

```c++
#include<bits/stdc++.h>
int main()
{
    vecotor<int>a;
    for(auto &c:a)//可使用变量c对a进行修改
        语句
    return 0;
}
```
3.迭代器1

```c++
vector<int>a;
vector<int>::iterator vbegin=a.begin();
vector<int>::iterator vend=a.end();
while(vbegin!=vend)
{
    cout<<*vbegin;
    vbegin++;
}
```

4.迭代器2

```c++
vector<int>a;
for(vector<int>::iterator i=a.begin();i!=a.end();i++)
    cout<<*i;
```






##### 非字符串去重代码

```c++
vector<int>a{........};
sort(a.begin(),a.end());
auto weizhi=unique(a.begin(),a.end());//此时weizhi指向不重复的元素之后的位置
a.erase(weizhi,a.end());//erase用来删除元素
//3.4行可以合并在一块
a.erase((unque(a.begin(),a.end()),a.end());
```

##### 字符串去重

> 字符串去重也可以采用以上的方法，但在去重过程中的效果与其他类型有所不同
```c++
vector<string>a{........};
sort(a.begin(),a.end());
auto weizhi=unique(a.begin(),a.end());//此时weizhi指向不重复的元素之后的位置
a.erase(weizhi,a.end());//erase用来删除元素
//3.4行可以合并在一块
a.erase((unque(a.begin(),a.end()),a.end());
```

在执行```unique```的时候，相邻的重复项并没有删除，只是将相邻元素进行覆盖

仅执行```unique```后再执行```a.size()```时会发现长度还是原来那些

##vector插入

```vector```可以相互进行插入，可用```insert```进行插入

#### 用法

```vector变量.insert(插入位置,插入vector的位置,插入vector的结束位置)```

#### 相关代码

```C++
vector<int>ch,ch2;
ch.insert(ch.begin(),ch2.begin(),ch2.end());
//以上代码是将ch2整体插入到ch的前端
```

----

