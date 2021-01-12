# DFS与BFS

对于此图，两者的搜索方式不同

![image-20201110190810303](C:\Users\singx\AppData\Roaming\Typora\typora-user-images\image-20201110190810303.png)

#### DFS（深度搜索）

按照一条路进行搜索，搜索完一条完整的路径后，继续搜索下一条路径，常用函数递归的形式实现

对于此图，DFS搜索的过程为```A-B-D-E-C-F-D-G-H-Q```，每个节点仅搜索一次。

+ 基本框架

  ```c++
  int dfs(int shendu,int canshu2)
  {
      if(此路不通)
      {
          ...
          return...
      }
      下一种情况
  }
  ```

  

#### BFS（广度搜索）



