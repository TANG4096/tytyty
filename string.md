# string

## 特性
* string 是一个以char为具体类型的basic_string类的实例
## 成员方法

### 迭代器

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
|size_type length(void)   | 返回字符串长度（字符串长度不一定等于其实际大小）|
|bool empty(void)    | 返回容器是否为空|
|void resize(size_type n)   |重置容器大小为n |
|void resize (size_type n, char c)     |  重置容器大小为n，并把所有元素初始化为c  |

### 访问成员
|                       名称  |           功能        |
| --------------------- | ---------------- |
|reference operator[] (size_type n)  |  返回下标为n位置的元素 |
|reference at (size_type n)     |返回下标为n位置的元素，相比[]运算符，这个方法会检查边界 |
|reference front()|返回第一个元素|
|reference back()|返回最后一个元素|

### 修改

|         名称          |           功能    |
| --------------------- | ---------------- |
|string operator +=|把字符或字符串拼接到该字符串后面|
|void push_back (const value_type& val)|在string末尾添加元素val 常数复杂度|
|void push_back (char c)|在向量末尾添加字符c,常数复杂度|
|void pop_back()|删除末尾的元素 常数复杂度|
|iterator insert (const_iterator position, const string& s)|把s插入到position指向的位置并返回指向val的迭代器|
|iterator insert (const_iterator position, char c)|把c插入到position指向的位置并返回指向val的迭代器|
|iterator insert (const_iterator position, InputIterator first, InputIterator last)|插入由一对迭代器指示的范围的元素|
|iterator erase (const_iterator position)|删除迭代器指向的元素并返回后面的元素的迭代器|
|iterator erase (const_iterator first, const_iterator last);|范围删除|
|void clear()|清空|

### 字符串操作

|         名称          |           功能    |
|---------------------  | ---------------- |
|const char* c_str()|返回一个字符指针，指向实际存储的末尾有终止字符的字符串|
|size_t find (const string& str, size_t pos = 0) <br> size_t find (const char* str, size_t pos = 0)   |返回str在字符串中第一次出现的位置，<br>当有参数pos从pos开始匹配，找不到返回string::npos|  
|size_t rfind (const string& str, size_t pos = 0) <br> size_t find (const char* str, size_t pos = 0)   |返回str在字符串中最后一次出现的位置，<br>当有参数pos从pos之前开始匹配，找不到返回string::npos|  
|string substr (size_t pos = 0, size_t len = npos) |返回字符串pos位置开始长度为len的子串|
|int compare (const string& str)<br>int compare (const char* s)|比较字符串，返回值等于0表示相等，大于0或小于0表示大于或小于|

## 示例

### 创建

    string s;  //初始化一个空字符串
    string s("aaa"); //用字符串常量初始化
    string s2(s); //用另一个string初始化
    
### 读入

    cin >> s; //读入字符串，遇到空格或换行停止
    getline(cin,s);//读取一行，可以读空格
    
