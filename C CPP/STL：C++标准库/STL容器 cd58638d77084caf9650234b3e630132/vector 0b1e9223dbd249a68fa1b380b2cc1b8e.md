# vector

头文件：<vector>

是一种有序集合，支持随机访问，在末尾操作元素时效率很高，但是不擅长插入操作

# **大小和容量**

如果超越容量就有必要重新分配内部内存，导致相关的reference, pointer, iterator失效，且内存重新分配相当耗时

可以使用reserve( )保留适量容量（无法用reserve( )缩减容量）

```c
vector<int> v;
v.reserve(80);
```

另一个方法是初始化时就向构造函数传额外实参构建足够空间

```c
vector<int> v(5);
```

C++11引入了新函数：shrink_to_fit( )可以缩减容量以符合当前元素个数

# 操作

[非更易型操作](vector%200b1e9223dbd249a68fa1b380b2cc1b8e/%E9%9D%9E%E6%9B%B4%E6%98%93%E5%9E%8B%E6%93%8D%E4%BD%9C%20e9c1ffee84914ed3bde283b0b09ea8b2.csv)

[赋值](vector%200b1e9223dbd249a68fa1b380b2cc1b8e/%E8%B5%8B%E5%80%BC%200b179d811db242eea5a8b1dba97a38da.csv)

[元素访问](vector%200b1e9223dbd249a68fa1b380b2cc1b8e/%E5%85%83%E7%B4%A0%E8%AE%BF%E9%97%AE%20f30adac4020b498bb09fe5a5178d115d.csv)

[安插和移除](vector%200b1e9223dbd249a68fa1b380b2cc1b8e/%E5%AE%89%E6%8F%92%E5%92%8C%E7%A7%BB%E9%99%A4%208fd5e279d890421fa36987b9dbba0f7f.csv)