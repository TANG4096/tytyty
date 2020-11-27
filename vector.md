#vector
##特性
* 序列容器中的元素按严格的线性顺序排序。各个元素按其在此序列中的位置进行访问。
* 支持随机访问，同时它的迭代器可以像指针一样进行算数运算
##成员方法
###迭代器相关
|    名称    | 功能        |
| --------- | ---------------- |
| iterator begin(void)   |  返回首迭代器      |
| iterator end(void)     |  返回尾后迭代器    |
| reverse_iterator rbegin(void)  |  返回反向首迭代器 |
| reverse_iterator rend(void)    |  返回反向尾后迭代器 |
###容量相关
|    名称             | 功能        |
| ----------------- | ---------------- |
|size_type size(void)     | 返回容器大小|
|bool empty(void)    | 返回容器是否为空|
|void resize(size_type n)   |重置容器大小为n |
|void resize (size_type n, const value_type& val)     |  重置容器大小为n，并把所有元素初始化为val  |

###访问成员
|    名称             | 功能        |
| ----------------- | ---------------- |

 
 