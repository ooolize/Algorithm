# 链表是什么?
> 链表是一种线性数据结构，由一些节点相连而成的逻辑上的连续序列，节点包含`值`与`指针`。
# 为什么需要链表
> 数组作为一种常见的数据结构，其局限性至少包含两各方面：① 编译期就要知道大小 ②空间上是连续的。 
> 而链表是动态分配内存的，删除和插入元素仅仅影响局部，无须整块横移。
>
> 相对于链表而言，数组也有自身的优点：允许随机访问。这在大部分排序算法中是必须的.而在那些只是需要访问
固定位置而对结构改变要求很高的算法，常常需要用到链表，例如队列.数组的另一个优势是空间，对于较大的链表
而言，如果数据移动不是很频繁，有剩余空间的数据并不算浪费空间

# STL中的链表
> 头文件加入`#include<list>`就可以使用STL的双向链表了。下面是成员函数节选： 

|成员函数|行为以及返回值|
|:---|:--|
|T& back()|返回链表最后一个节点的元素|
|T& front()|返回链表第一个节点的元素|
|iterator begin()|返回指向第一个节点的迭代器|
|iterator end()|返回指向最后一个节点的迭代器|
|void pop_back()|删除最后一个节点|
|void pop_front()|删除第一个节点|
|void push_back()|向尾部添加节点|
|void push_front()|向首部添加节点|
|iterator erase(iterator i)|删除迭代器所指的节点并返回其**后**的第一个迭代器|
|iterator erase(iterator first,iterator last)|删除所指范围的节点并返回其**后**的迭代器|
|iterator insert(iterator i, const T&el)|向迭代器i所指位置**前**一个值为el的节点并返回该新节点的迭代器|
|void insert(iterator i,size_type n, const T&el)|向迭代器i所指位置**前**插入n个值为el的节点
|void insert(iterator i,iterator first,iterator last)|向迭代器i所指位置**前**插入 迭代器first与last之间的元素|
|void clear()|删除所有节点|
|void reverse()|翻转链表|
|void unique()|**在有序链表中**删除所有重复节点|
|bool empty()|链表为空返回TRUE，否则返回FALSE|
|size_type size() const|返回节点数|

   
# Todo
* 跳跃链表
+ 稀疏表
- 自组织链表
