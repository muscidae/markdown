# 算法（algorithm）

## 1. 数据结构（data structure）
**概述**: 是数据的组织、管理和存储格式，其使用目的是为了高效地访问和修改数据。

### 1.1 常见的数据结构
- **线性结构**: 线性结构是最简单的数据结构，包括数组、链表，以及由它们衍生出来的栈、队列、哈希表。

- **树**: 树是相对复杂的数据结构，其中比较有代表性的是二叉树，由它又衍生出了二叉堆之类的数据结构。

- **图**: 图是更为复杂的数据结构，因为在图中会呈现出多对多的关联关系。

- **其他数据结构**: 除上述所列的几种基本数据结构以外，还有一些其他的千奇百怪的数据结构。它们由基本数据结构变形而来，用于解决某些特定问题，如跳表、哈希链表、位图等。

### 1.2  数组（array）
**概述**: 由相同类型的元素（element）的集合所组成的数据结构，分配一块连续的内存来存储利用元素的下标（index）可以计算出该元素对应的存储地址。  
**特点**: 物理存储方式为顺序存储，访问方式为随机访问。
利用下标查找数组元素的时间复杂度是 **O(1)**，中间插入、删除数组元素的时间复杂度是 **O(n)**。  
**优势**: 数组拥有非常高效的随机访问能力，只要给出下标，就可以用常量时间找到对应元素。  
**劣势**: 由于数组元素连续紧密地存储在内存中，插入、删除元素都会导致大量元素被迫移动，影响效率。

### 1.3  链表（linked list）
**概述**: 是一种线性表，但是并不会按线性的顺序存储数据，而是在每一个节点里存到下一个节点的指针(Pointer)。  
**特点**: 在插入的时候可以达到 **O(1)** 的复杂度，查找一个节点或者访问特定编号的节点则需要 **O(n)** 的时间。  
**优势**: 可以克服数组链表需要预先知道数据大小的缺点，链表结构可以充分利用计算机内存空间，实现灵活的内存动态管理。允许插入和移除链表上任意位置上的节点，所以拥有非常高效的插入和删除能力。  
**劣势**: 由于增加了节点的指针域，空间开销比较大。不允许随机存取，读取效率低。

### 1.4 数组和链表时间复杂度对比

|  数据结构 / 时间复杂度  |          |   更新   |   插入   |   删除   |
| :---------------------: | :------: | :------: | :------: | :------: |
|    **数组（array）**    | **O(1)** | **O(1)** | **O(n)** | **O(n)** |
| **链表（linked list）** | **O(n)** | **O(1)** | **O(1)** | **O(1)** |

### 1.5 栈
**概述**:  栈中的元素只能先入后出（First In Last Out，简称FILO）。最早进入的元素存放的位置叫作栈底（bottom），最后进入的元素存放的位置叫作栈顶（top）。
**特点**: 先入后出，后入先出。除头尾节点之外，每个元素有一个前驱，一个后继。

​	压栈（push）：将数据放入堆栈顶端，堆栈顶端移到新放入的数据。

​	出栈（pop）：将堆栈顶端数据移除，堆栈顶端移到移除后的下一笔数据。

#### 1.51 物理结构和逻辑结构

|              |         线性结构         |   非线性结构   |
| :----------: | :----------------------: | :------------: |
| **逻辑结构** | **例：顺序表、栈、队列** | **例：树、图** |
| **物理结构** |       **例：数组**       |  **例：链表**  |


### 1.6 队列
**概述**:  
**特点**:  
**优势**:  
**劣势**:  
### 1.7 散列
**概述**:  
**特点**:  
**优势**:  
**劣势**:  

## 2. 时间复杂度
**概述**: 若存在函数f(n)，使得当n趋近于无穷大时，T(n) / f(n)的极限值为不等于零的常数，则称f(n)是T(n) 的同数量级函数。记作T(n) =O( f(n) )，称为O( f(n) )，O为算法的渐进时间复杂度，简称为时间复杂度。

### 2.1 时间复杂度推导

- 如果运行时间是**常数**量级，则用常数1表示。
- 只保留时间函数中的**最高阶项**。
- 如果最高阶项存在，则省去**最高阶项前面的系数**。

## 3. 空间复杂度
**概述**: 时间复杂度是对一个算法运行时间长短的量度，用大O表示，记作T（n）=O（f（n））。
### 3.1 空间复杂度的计算
1. **常量空间**: 当算法的存储空间大小固定，和输入规模没有直接的关系时，空间复杂度记作O（1）
2. **线性空间**: 当算法分配的空间是一个线性的集合（如数组），并且集合大小和输入规模n成正比时，空间复杂度记作O（n）。
3. **二维空间**: 当算法分配的空间是一个二维数组集合，并且集合的长度和宽度都与输入规模n成正比时，空间复杂度记作O（n2）。 
4. **递归空间**: 递归是一个比较特殊的场景。虽然递归代码中并没有显式地声明变量或集合，但是计算机在执行程序时，会专门分配一块内存，用来存储“方法调用栈”。“方法调用栈” 包括进栈和出栈两个行为。当进入一个新方法时，执行入栈操作，把调用的方法和参数信息压入栈中。当方法返回时，执行出栈操作，把调用的方法和参数信息从栈中弹出。
