# STL总结

- ### **集合类**：`set`, `multiset`, `unordered_set`，适用于存储并查找唯一元素。

- ### **映射类**：`map`, `multimap`, `unordered_map`，适用于存储键值对。

- ### **序列类**：`vector`, `deque`, `list`, `array`, `forward_list`，适用于存储线性结构的数据。

- ### **栈、队列与优先队列**：`stack`, `queue`, `priority_queue`，适用于不同的存取模式。



### 集合类：

- **set** 和 **multiset**：
  - `insert(value)`：插入一个元素，返回一个pair，包含迭代器和布尔值（表示是否插入成功）
  - `erase(value)`：删除指定元素，返回删除的元素个数（0或1）
  - `find(value)`：查找元素，返回元素的迭代器（若未找到，返回end()）
  - `count(value)`：返回元素出现的次数（set中为0或1，multiset中可能大于1）
  - `size()`：返回集合的大小（类型：size_t）
  - `empty()`：判断集合是否为空，返回布尔值（true或false）
  - `clear()`：清空集合，返回void
- **unordered_set**：
  - `insert(value)`：插入一个元素，返回一个pair，包含迭代器和布尔值（表示是否插入成功）
  - `erase(value)`：删除指定元素，返回删除的元素个数（0或1）
  - `find(value)`：查找元素，返回元素的迭代器（若未找到，返回end()）
  - `count(value)`：返回元素出现的次数（在unordered_set中为0或1）
  - `size()`：返回集合的大小（类型：size_t）
  - `empty()`：判断集合是否为空，返回布尔值（true或false）
  - `clear()`：清空集合，返回void

### 映射类：

- **map** 和 **multimap**：
  - `insert({key, value})`：插入键值对，返回一个pair，包含迭代器和布尔值（表示是否插入成功）
  - `erase(key)`：删除指定键值对，返回删除的元素个数（0或1）
  - `find(key)`：查找键，返回键值对的迭代器（若未找到，返回end()）
  - `count(key)`：返回键的出现次数（map中为0或1，multimap中可能大于1）
  - `operator[]`：访问或插入键值对，返回值类型为value的引用
  - `size()`：返回映射的大小（类型：size_t）
  - `empty()`：判断映射是否为空，返回布尔值（true或false）
  - `clear()`：清空映射，返回void
- **unordered_map**：
  - `insert({key, value})`：插入键值对，返回一个pair，包含迭代器和布尔值（表示是否插入成功）
  - `erase(key)`：删除指定键值对，返回删除的元素个数（0或1）
  - `find(key)`：查找键，返回键值对的迭代器（若未找到，返回end()）
  - `count(key)`：返回键的出现次数（在unordered_map中为0或1）
  - `operator[]`：访问或插入键值对，返回值类型为value的引用
  - `size()`：返回映射的大小（类型：size_t）
  - `empty()`：判断映射是否为空，返回布尔值（true或false）
  - `clear()`：清空映射，返回void

### 序列类：

- **vector**：
  - `push_back(value)`：在末尾插入元素，返回void
  - `pop_back()`：删除末尾元素，返回void
  - `insert(position, value)`：在指定位置插入元素，返回插入位置的迭代器
  - `erase(position)`：删除指定位置的元素，返回删除元素的下一个位置的迭代器
  - `at(index)`：访问指定位置的元素，返回该位置的元素引用
  - `size()`：返回容器的大小（类型：size_t）
  - `empty()`：判断容器是否为空，返回布尔值（true或false）
  - `clear()`：清空容器，返回void
  - `resize(n)`：调整容器大小，返回void
- **deque**：
  - `push_back(value)`：在末尾插入元素，返回void
  - `push_front(value)`：在头部插入元素，返回void
  - `pop_back()`：删除末尾元素，返回void
  - `pop_front()`：删除头部元素，返回void
  - `at(index)`：访问指定位置的元素，返回该位置的元素引用
  - `size()`：返回容器的大小（类型：size_t）
  - `empty()`：判断容器是否为空，返回布尔值（true或false）
  - `clear()`：清空容器，返回void
- **list**：
  - `push_back(value)`：在末尾插入元素，返回void
  - `push_front(value)`：在头部插入元素，返回void
  - `pop_back()`：删除末尾元素，返回void
  - `pop_front()`：删除头部元素，返回void
  - `insert(position, value)`：在指定位置插入元素，返回插入位置的迭代器
  - `erase(position)`：删除指定位置的元素，返回删除元素的下一个位置的迭代器
  - `size()`：返回容器的大小（类型：size_t）
  - `empty()`：判断容器是否为空，返回布尔值（true或false）
  - `clear()`：清空容器，返回void

### 栈、队列与优先队列：

- **stack**：
  - `push(value)`：在栈顶插入元素，返回void
  - `pop()`：删除栈顶元素，返回void
  - `top()`：访问栈顶元素，返回栈顶元素的引用
  - `empty()`：判断栈是否为空，返回布尔值（true或false）
  - `size()`：返回栈的大小（类型：size_t）
- **queue**：
  - `push(value)`：在队尾插入元素，返回void
  - `pop()`：删除队头元素，返回void
  - `front()`：访问队头元素，返回队头元素的引用
  - `back()`：访问队尾元素，返回队尾元素的引用
  - `empty()`：判断队列是否为空，返回布尔值（true或false）
  - `size()`：返回队列的大小（类型：size_t）
- **priority_queue**：
  - `push(value)`：插入元素，保持堆的性质，返回void
  - `pop()`：删除堆顶元素，返回void
  - `top()`：访问堆顶元素，返回堆顶元素的引用
  - `empty()`：判断优先队列是否为空，返回布尔值（true或false）
  - `size()`：返回优先队列的大小（类型：size_t）