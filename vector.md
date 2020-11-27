# vector 
## 特性
* 序列容器中的元素按严格的线性顺序排序。各个元素按其在此序列中的位置进行访问。
* 支持随机访问，同时它的迭代器可以像指针一样进行算数运算
## 成员方法
### 迭代器相关
|    名称    | 功能        |
| --------- | ---------------- |
| iterator begin(void)   |  返回首迭代器      |
| iterator end(void)     |  返回尾后迭代器    |
| reverse_iterator rbegin(void)  |  返回反向首迭代器 |
| reverse_iterator rend(void)    |  返回反向尾后迭代器 |
### 容量相关
|    名称             | 功能        |
| ----------------- | ---------------- |
|size_type size(void)     | 返回容器大小|
|bool empty(void)    | 返回容器是否为空|
|void resize(size_type n)   |重置容器大小为n |
|void resize (size_type n, const value_type& val)     |  重置容器大小为n，并把所有元素初始化为val  |

### 访问成员
|                       名称  |           功能        |
| --------------------- | ---------------- |
|reference operator[] (size_type n)  |  返回下标为n位置的元素 |
|reference at (size_type n)     |返回下标为n位置的元素，相比[]运算符，这个方法会检查边界 |
|reference front()|返回第一个元素|
|reference back()|返回最后一个元素|
|value_type* data() |返回指向实际存放元素的数组的指针|

### 修改

|         名称          |           功能    |
| --------------------- | ---------------- |
|void push_back (const value_type& val)|在向量末尾添加元素val 常数复杂度|
|void pop_back()|删除末尾的元素 常数复杂度|
|iterator insert (const_iterator position, const value_type& val)|把val插入到position指向的位置并返回指向val的迭代器|
|iterator insert (const_iterator position, InputIterator first, InputIterator last)|插入由一对迭代器指示的范围的元素|
|iterator erase (const_iterator position)|删除迭代器指向的元素并返回后面的元素的迭代器|
|iterator erase (const_iterator first, const_iterator last);|范围删除|
|void swap (vector& x)|和另一个向量相交换|
|void clear()|清空|

## 示例
### 声明和初始化
    vector<int> a;                       //声明一个int型向量a
    vector<int> a(10);                   //声明一个初始大小为10的向量
    vector<int> a(10, 1);      //声明一个初始大小为10且初始值都为1的向量
    vector<int> b(a);                    //声明并用向量a初始化向量b
    vector<int> b(a.begin(), a.begin()+3);//将a向量中从第0个到第2个(共3个)作为向量b的初始值
    vector<int> v = {1,2,3}  //值初始化列表，c++11的新特性 
### 将输入的n个数储存到向量
    vector<int>v  ;
    int n;
    scanf("%d", &n);
    for(int i = 0; i < n; i++){
        int a;
        scanf("%d", &a);
        v.push_back(a);
    }
### 遍历
    //通过下标遍历
    for(int i = 0; i < v.size(); i++){
        v[i]++;
    }
    //通过迭代器遍历
    for(auto it = v.begin(); it != v.end(); it++){
        (*it)++;
    }
    //序列for循环，c++11新特性
    for(auto &x : v){
        x++;
    }


 