# 第一章 绪论

## 1.1 数据结构的基础概念

1. 数据（data）
   1. 数据是描述客观事物的数值、字符以及能输入计算机且能被处理的各种符号集合。
   2. 数据就是计算机化的信息。
2. 数据元素（data element）【记录】
   1. 数据元素是组成数据的基本单位，是数据集合的个体。
   2. 一个数据元素可由一个或多个数据项组成，数据项（data item）是有独立含义的最小单位。
3. 数据对象（data object）（数据对象是性质相同的数据元素的集合，是数据的一个子集）
   1. 数据的特点
      1. 可被计算机接收（与计算机的关联性）
      2. 可被加工（能被处理）
   2. 数据的构成
      1. 数据元素：组成数据的基本单位（是数据集合的个体）
      2. 数据对象：性质相同的数据元素的集合（是数据集合的子集）
4. 数据结构（data structure）
   1. 数据结构是指相互之间存在一种或多种特定关系的数据元素集合。
   2. 数据结构应包括数据元素集合及元素间关系的集合，即数据的组织形式。
5. 数据类型（data type）
   1. 数据类型是一组性质相同的值集合以及定义在这个值集合上的一组操作的总称。
   2. 分类：原子类型（不可再分）；结构类型
6. 抽象数据类型（抽象的本质是抽取反应问题的本质点。，而忽略非本质的细节。）
   1. 数据的抽象
   2. 抽象数据类型（abstract data type， ADT）
      1. ADT定义了一个数据对象数据对象中各元素间的结构关系以及一组处理数据的操作。
      2. 特点：数据抽象，信息隐藏。
      3. 特征：使用与实现分离，实现封装和信息隐藏。
      4. 当需要改变数据结构时，只要界面服务的使用方式不变，则仅需改变抽象数据类型的物理实现，无需修改所有使用该抽象数据类型的程序，从而提高了系统的稳定性。
      5. 包括：数据对象、数据元素间的结构关系、操作
      ```cpp
      ADT <ADT名>{
        数据对象：<数据对象的定义>
        结构关系：<结构关系的定义>
        基本操作：<基本操作的定义>
      }ADT <ADT名>;
      ```
   3. 注：
      1. 数据对象定义应在已有的数据类型或已定义的数据对象基础上，对新的数据对象进行定义。
      2. 数据对象和结构关系的定义，采用数学符号和自然语言描述。
      3. 基本操作定义，包括操作名称，参数名，操作前提（初始条件）和操作结果。
         ```cpp
         <操作名称>(参数表)
          操作前提：<操作前提描述>
          操作结果：<操作结果描述>
         ```

## 1.2 数据结构的内容

1. 数据的逻辑结构
   1. 指数据元素之间的逻辑关系描述
   2. 形式定义：数据结构是一个二元组Data-Structure=(D, R)
      1. D：数据元素的有限集
      2. R：D上关系的有限集
   3. 四类基本结构：
      1. 集合结构：同属一个集合
      2. 线性结构：一对一（线性关系）
      3. 树形结构：一对多（层次关系）
      4. 图结构或网状结构：多对多（任意关系）
   4. 逻辑结构：
      1. 线性结构：线性表、栈、队列、字符串、数组、广义表
      2. 非线性结构：树、图
2. 数据的存储结构（物理结构）
   1. 逻辑结构在计算机中的存储映像
      1. 数据元素映像
      2. 关系映像
   2. 存储结构是逻辑关系的映像与元素本身的映像
      1. 逻辑结构是数据结构的映像
      2. 存储结构是数据结构的实现。
3. 数据的运算集合：按某种逻辑关系组织起来的一批数据，按一定的映像方式，将其存放在计算机的存储器中，并在这些数据上定义一个运算的集合。

## 1.3 算法（algorithm）

1. 算法定义：规则的有限集合，是为解决特定问题而规定的一系列操作。
2. 算法的特性：
   1. 有限性：有限步骡之内正常结束,不能形成无限循环。
   2. 确定性: 每个步骤必须有确定含义，无二议性。
   3. 可行性：原则上能精确进行，操作可通过已实现的基本运算执行有限次而完成。
   4. 输入：有多个或0个输入。
   5. 输出：至少有1个或多个输出。
3. 算法设计的要求：
   1. 正确性（三个层次）
      1. 普通情况
      2. 极端情况（典型、苛刻、带有刁难性）
      3. 一切合法的输入 -> 满足要求的结果
   2. 可读性
   3. 健壮性
   4. 高效率和低存储量

## 1.4 算法描述

1. 一些关系
   1. 算法用来描述数据对象之间的关系
   2. 语言是描述算法的工具
   3. 程序是算法在计算机中的实现
2. 实现步骤：...
3. 语言选择：...

## 1.5 算法性能评价

1. 性能评价
   1. 时间耗费
   2. 空间（存储）占用
2. 问题规模：算法求解问题的输入量

### 1.5.1 算法的时间性能分析

1. 算法耗费的时间
2. 语句频度：该语句在一个算法中反复执行的次数
3. 算法的实际按复杂度
   1. T(n) = O(f(n)) //算法的渐进时间复杂度
   2. n：问题规模
   3. O：（数量级）若T(n)和f(n)是定义在正整数集合上的的两个函数，则T(n) = O(f(n))表示：存在正的常数C和n0，使当n>=n0时满足0<=T(n)<=Cf(n)
4. 渐进时间复杂度   （1. 常数阶   2. 线性阶   3. 平方阶   4. 立方阶）
5. 常用的时间复杂度：
   1. ![](imgs/2021-10-18-21-27-57.png)
   2. ![](imgs/2021-10-18-21-28-08.png)
   3. ![](imgs/2021-10-18-21-28-25.png)
   4. ![](imgs/2021-10-18-21-28-38.png)
   5. ![](imgs/2021-10-18-21-28-50.png)

### 1.5.2 算法的空间性能分析

1. 算法耗费的空间：实际占用的辅助空间总和
2. 算法的空间复杂度S(n)
   1. 所耗费的存储空间的数量级
   2. S(n) = O(f(n))
   3. 原地工作：辅助空间为O(1)

### 1.5.3 算法性能选择

1. 若程序使用次数较少，则力求算法简明易懂。
2. 对于反复使用的程序，应尽可能选用快速的算法。
3. 若待解决的问题数据量极大，计算机的存储空间较小，则相应算法主要考虑如何节省空间。

## 1.6 数据结构与C语言表示

### 1.6.1 数据结构与程序设计的关联性

### 1.6.2 结构化程序设计与函数的模块化

1. 目的：以程序良好的静态结构来保证程序动态执行的正确性
2. 构成单元：顺序、选择、重复
3. 方法：
   1. 设计思想：自顶向下，逐步求精
   2. 模块化结构：独立功能，一个入口，一个出口
   3. 设计原则：仅用三种基本控制结构

### 1.6.3 面向对象与抽象数据类型

1. 面向对象 = 对象 + 类 + 继承 + 通信
   1. 特点：
      1. 封装(Encapsulation)
      2. 继承(Inheritance)
      3. 多态(Polymorphism)
   2. 基本操作：
      1. 插入（增）：在指定位置增加元素
      2. 删除（删）：删除某个指定元素
      3. 更新（改）：改变某个元素值
      4. 查找（查）：寻找满足要求的元素
      5. 排序（排）：线性结构中重新安排元素间的逻辑顺序
   3. 分类：加工型操作、引用型操作
2. 抽象数据类型与问题求解方法
   1. 基本原则：分解、抽象和信息隐藏
   2. 规范：数据的逻辑结构和运算的定义
   3. 实现：数据的存储结构和运算算法
   4. 数据结构是基础，抽象数据类型是中枢
3. ADT的实现途径
   1. 面向过程
   2. 面向模块结构
   3. 面向对象
4. 用C语言实现ADT

### 1.6.4 算法描述规范与设计风格

1. ~
   1. 算法表示形式
      ```cpp
      [函数返回值类型] 函数名 ([形式参数及说明]){
        内部数据说明;
        执行语句组;
      } /*函数名*/
      ```
   2. 函数模块化
      ```cpp
      [包含文件]
      [宏定义]
      [自定义类型]
      [子函数原形]
      [主函数]
      [子函数定义]
      ```
2. 算法描述要点
   1. 必要的注释
   2. 避免函数返回值隐含说明（缺省int）
   3. 预定义常量和类型
   4. 有意义的函数名与变量名
   5. 避免可能出现的二义性表达`++i+++`
   6. 规范多分支转向 `switch-case`
   7. 简化输入输出表达
   8. 注意不同退出语句之间的区别
      1. return：函数结束
      2. break：结束循环或跳出情况
      3. continue：结束本次循环，进行下次循环过程
      4. exit：退出用户程序
3. 参数传递相关
   1. 变量的作用域（包含该变量定义的最小范围）
      1. 全局变量：程序中所有函数都可以访问的变量
      2. 局部变量：只能在本函数中访问的变量
   2. 参数的传递方式
      1. 值参：只为操作提供待处理的数据
      2. 变量参数：既能为操作提供待处理的数据，又能返回操作结果
4. 函数结果的带出方式
   1. 全局变量方式
   2. 数组方式
   3. 结构体方式
   4. 指针方式


# 第二章 线性表

## 2.1线性表的概念及其抽象数据类型定义

### 2.1.1 线性表的逻辑结构

1. 线性表是n个类型相同的数据元素的有限序列，对n>0，除第一个元素无直接前驱，最后一个元素无直接后继外，其余的每个元素只有一个直接前驱和一个直接后继
2. 在一般的线性表中，一个数据元素可由若干数据项组成
3. 线性表是由n(n>=0)个类型相同的数据元素组成的有限序列，记作(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>i-1</sub>, a<sub>i</sub>, a<sub>i+1</sub>, ..., a<sub>n</sub>)
4. 线性表中元素的个数n被定义为线性表的长度，n=0时称为空表
5. 线性表的特点：
   1. 同一性：线性表由同类数据元素组成，每一个a<sub>i</sub>必须属于同一数据类型
   2. 有穷性：线性表由有限个数据元素组成，表长度就是表中数据元素的个数
   3. 有序性：线性表中相邻数据元素之间存在着序偶关系`<a[i], a[i+1]>`

### 2.1.2 线性表的抽象数据类型定义

```cpp
ADT LinearList{
   数据对象：D={a[i]|a[i]∈D0，i=1,2,...,n, n>=0, D0为某一数据对象}
   结构关系：R={<a[i], a[i+1]>|a[i], a[i+1]∈D，i=1,2,...,n-1}
   基本操作：
      // 将L初始化为空表
      InitList(L);
      // 如果L为空表则返回0，否则返回表中的元素个数
      ListLength(L);
      // 返回线性表L中第i个合法元素的值
      GetData(L, i);
      // 在L中第i个位置之前插入新的数据元素e，L的长度加1
      InsList(L, i, e);
      // 删除L中第i个数据元素，并用e返回其值，L的长度减1
      DelList(L, i, e);
      // 二如果L中存在数据元素e，则返回e在L中的位置，否则返回空位置
      Locate(L, e);
      // 将L销毁
      Destory(L);
      // 将L置为空表
      ClearList(L);
      // 如果L为空表则返回TRUE，否则返回FALSE
      EmptyList(L);
}ADT LinearList;
```

## 2.2 线性表的顺序存储

### 2.2.1 线性表的顺序存储结构

顺序表：关系线性化，节点顺序存
1. 地址的计算：第i个元素的地址Loc(a<sub>i</sub>)=Loc(a<sub>1</sub>)+(i-1)*k
   1. Loc(a<sub>1</sub>)：基地址
   2. k：每个元素所占单元数
2. 线性表的顺序存储表示
   ```cpp
   typedef struct{
      ElemType elem[MAXSIZE];
      int last;
   }SeqList;
   // 类型是模板，变量才是真正的存储空间
   ```

### 2.2.2 线性表的顺序存储结构上的基本运算

1. 查找操作
   1. 按序号查找`GetData(L, i);`：
      1. 查找顺序表L中第i个（自然语言从1开始）数据元素
      2. `return L.elem[i-1]`
   2. 按内容查找`Locate(L, e);`：查找顺序表L中与给定值e相等的数据元素
      ```cpp
         size_t i;
         // 此处的不等是广义的不等
         while(i <= L.last && (L.elem[i] != e)) i++;
         return i <= L.last ? i+1 : -1;
      ```
2. 插入操作：在表得到第i(1<=i<=n+1)个位置前插入一个新元素e，使长度为n的顺序表(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>i-1</sub>, a<sub>i</sub>, a<sub>i+1</sub>, ..., a<sub>n</sub>)变成长度为n+1的顺序表(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>i-1</sub>, a, a<sub>i</sub>, a<sub>i+1</sub>, ..., a<sub>n</sub>)
   ```cpp
   InsList(SeqList* L, int i, ElemType e){
      if(i < 1 || i > L->last + 2){//位置合法检查
         // 位置不合法处理
      }
      if(L->last >= MAXSIZE - 1){
         // 表满处理
      }
      for(size_t k = L->last; k >= i-1; k--)
         L->elem[k-1] = k->elem[k];
      L->elem[i-1] = e;
      L->last++;
   }
   ```
3. 删除操作：将表的第i(1<=i<=n)个元素删去，使长度为n的顺序表(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>i-1</sub>, a<sub>i</sub>, a<sub>i+1</sub>, ..., a<sub>n</sub>)变成长度为n-1的顺序表(a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>i-1</sub>, a<sub>i+1</sub>, ..., a<sub>n</sub>)
   ```cpp
   DelList(SeqList* L, int i, ElemType* e){
      if(i < 1 || i > L->last + 1){//位置合法检查
         // 删除位置不合法
      }
      *e = L->elem[i-1];
      for(size_t k = i; k <= L->last; k++)
         L->elem[k-1] = L->elem[k];
      L->last--;
   }
   ```
4. 【A2.4 线性表的合并运算】
   ```cpp
   mergeList(SeqList* LA, SeqList* LB, SeqList* LC){
      int i=0, j=0, k=0, l=0;
      while(i <= LA->last && j <= LB->last)
         LC->elem[k++] = LA->elem[i] < LB->elem[j] ? LA->elem[i++] : LB->elem[j++];
      while(i <= LA->last)
         LC->elem[k++] = LA->elem[i++];
      while(j <= LB->last)
         LC->elem[k++] = LB->elem[j++];
      LC->last = LA->last + LB->last + 1;
   }
   ```
   ```cpp
   // 逆向思维
   int k = LA->last + LB->last + 1;
   int i = LA->last, j = LB->last;
   while(i >= 0 && j >= 0)
      LC->elem[k--] = LA->elem[i] >= LB->elem[j] ? LA->elem[i--] : LB->elem[j--];
   while(i >= 0)
      LC->elem[k--] = LA->elem[i--];
   while(j >= 0)
      LC->elem[k--] = LB->elem[j--];
   LC->last = LA->last + LB->last + 1;
   ```
5. 【将值为x的元素全部删除】
   ```cpp
   while(i <= L->last){
      if(L->elem[i] != x){
         L->elem[k++] = L->elem[i++];
         L->last--;
      }
      else{
         i++;
      } 
   }
   ```

顺序表的优点：
1. 无须为表示节点间的逻辑关系而增加额外的存储空间
2. 可方便的随机存取表中的任一元素

顺序表的缺点：
1. 除表尾外，在表的其他位置进行插入、删除运算效率低
2. 存储分配只能预先进行静态分配，难以确定合适的存储规模

## 2.3 线性表的链式存储

线性链表
- 链接方式【分类】
  - 单链表
  - 双链表
  - 循环链表
- 实现方式【分类】
  - 动态链表
  - 静态链表

### 2.3.1 单链表

1. 链表的节点（node）
   1. 数据域（data）：值
   2. 指针域（next）：直接后继的地址或位置
2. 每个节点只有一个next指针域的链表称为单链表
   ```cpp
   //





   ```
   ```cpp
   typedef struct Node{
      ElemType data;
      struct Node* next;
   }Node, *LinkList;
   ```

### 2.3.2 单链表上的基本运算

1. 初始化单链表
   ```cpp
   InitList(LinkList* L){
      *L = (LinkList)malloc(sizeof(Node));
      (*L)->next = NULL;
   }
   ```
2. 建立单链表
   1. 头插法（逆序建表法）
      ```cpp
      CreateFromHead(LinkList L){
         int flag = 1;
         while(flag){
            char c = getchar();
            if(c != '$'){
               Node *s = (Node*)malloc(sizeof(Node));
               s->data = c;
               s->next = L->next;
               L->next = s;
            }else{
               flag = 0;
            }
         }
      }
      // 初始化空表：

      // 申请新节点并赋值

      // 插入第一个节点

      // 插入第i个元素

      ```
   2. 尾插法
      ```cpp
      CreateFromTail(LinkList L){
         Node *r = L, *s;
         int flag = 1;
         while(flag){
            char c = getchar();
            if(c != '$'){
               Node *s = (Node*)malloc(sizeof(Node));
               s->data = c;
               r->next = s;
               r = s;
            }else{
               flag = 0;
               return r->next == NULL;
            }
         }
      }
      // 初始化空表：

      // 申请新节点并赋值

      // 插入第一个节点

      // 插入第二个节点
      
      ```
3. 查找
   1. 按序号查找
      ```cpp
      Node* GetData(LinkList L, int i){
         if(i <= 0)return NULL;
         int j = 0;
         Node* p = L;
         while(p->next != NULL && j < i){
            p = p->next;
            j++;
         }
         return i == j ? p : NULL;
      }
      ```
   2. 按值查找
      ```cpp
      Node* Locate(LinkList L, ElemType key){
         Node* p = L;
         while(p = p->next){
            if(p->data == key)
               break;
            // 或：if(p->data != key)continue;break;
         }
         return p;
      }
      ```
4. 求单链表长度操作
   ```cpp
   ListLength(LinkList L){
      int j = 0;
      Node* p = L;
      while(p = p->next)j++;
      return j;
   }
   ```
5. 单链表插入操作：在表得到第i(1<=i<=n+1)个位置前插入一个新元素e。
   ```cpp
   InsList(LinkList L, int i, ElemType e){
      if(i <= 0)return ERROR;
      Node* pre = L, *s;
      int k = 0;
      while((pre = pre->next) && k < i-1)k++;
      if(!pre){//插入位置不合理
      }
      s = (Node*)malloc(sizeof(Node));
      s->data = e;
      s->next = pre->next;
      pre->next = s;
   }
   // 寻找第i-1个节点

   // 申请新节点s,将s的数据域置为e

   // 插入新节点s

   ```
6. 单链表删除操作：将表的第i(1<=i<=n)个元素删去。
   ```cpp
   DelList(LinkList L, int i, ElemType *e){
      Node *pre = L, *r;
      int k = 0;
      while(pre->next && k < i-1){
         pre = pre->next;
         k++;
      }
      if(pre->next == NULL){//错误
      }
      r = pre->next;
      pre->next = r->next;
      *e = r->data;
      free(r);
   }
   // 寻找第i-1个节点

   // 删除并释放

   ```
7. 【A2.13 合并两个有序的单链表】
   ```cpp
   LinkList mergeList(LinkList LA, LinkList LB){
      Node *pa = LA->next, *pb = LB->next;
      LinkList LC = LA;
      LC->next = NULL;
      r = LC;
      while(pa && pb){
         if(pa->data <= pb->data){
            r->next = pa;
            r = pa;
            pa = pa->next;
         }else{
            r->next = pb;
            r = pb;
            pb = pb->next;
         }
      }
      // 注意：如果是逆序建表法的话，这里要用两个循环
      r->next = pa ? pa : pb;
      free(LB);
      return LC;
   }
   ```

### 2.3.3 循环链表

```cpp
// 首尾相接
// 带头结点的循环单链表
// （a）空表
// （a）
// （a）尾指针
```

| 判空条件   | 不带头结点 | 带头结点        |
| ---------- | ---------- | --------------- |
| 单链表     | `p!=NULL`  | `p->next!=NULL` |
| 单循环链表 | `p!=L`     | `p->next!=L`    |

1. 初始化循环单链表
   ```cpp
   InitCLinkList(LinkList CL){
      *CL = (LinkList)malloc(sizeof(Node));
      (*CL)->next = *CL;
   }
   ```
2. 建立循环单链表
   ```cpp
   CreateCLinkList(LinkList CL){
      Node *rear = CL, *s;
      char c = getchar();
      while(c != '$'){
         s = (Node*)malloc(sizeof(Node));
         s->data = c;
         rear->next = s;
         rear = s;
         c = getchar();
      }
      rear->next = CL;
   }
   ```
3. 【循环单链表合并】
   ```cpp
   Node *p = LA, *q = LB;
   while(p->next != LA)p = p->next;
   while(q->next != LB)q = q->next;
   q->next = LB;
   p->next = LB->next;
   free(LB);
   return LA;

   // 含尾指针
   Node *p = RA->next;// RA的头节点
   RA->next = RB->next->next;// RB的第一个元素
   free(LB->next);
   RB->next = p;
   return RB;
   ```

### 2.3.4 双向链表

```cpp
// 在单链表的每个节点中再增加一个指向其前驱的指针域prior
typedef struct DNode{
   ElemType data;
   struct DNode *prior, *next;
}DNode, *DoubleList;

// 设指针p指向双向链表中的某一结点，则：
p->prior->next == p;
p == p->next->prior;
```

1. 双向链表的插入操作
   ```cpp
   DLinkIns(DoubleList L, int i, ElemType e){
      DNode *s, *p;
      ...
      ...
      if(s = (DNode*)malloc(sizeof(DNode))){
         s->data = e;
         s->prior = p->prior;
         p->prior->next = s;
         s->next = p;
         p->prior = s;
      }
   }
   ```

2. 双向链表的删除操作
   ```cpp
   DLinkDel(DoubleList L, int i, ElemType e){
      DNode *p;
      // 检查合法性
      // 找到第i个节点，p指向
      p->prior->next = p->next;
      p->next->prior = p->prior;
      free(p);
   }
   ```

### 2.3.5 静态链表

```cpp
typedef struct{
   ElemType data;
   int cursor;//后继节点的相对位置
}Component, StaticList[MAXSIZE];
```

1. 初始化
   ```cpp
   initial(StaticList space, int av){
      space[0].cursor = -1;
      for(int k = i; k < MAXSIZE-1; k++)
         space[k].cursor = k+1;
      space[MAXSIZE-1].cursor = -1;
      *av = 1;//备用表头指针
   }
   ```
2. 分配节点空间
   ```cpp
   getnode(StaticList space, int *av){
      int i = *av;
      *av = space[*av].cursor;
      return i;
   }
   ```
3. 回收节点空间
   ```cpp
   freenode(StaticList space, int *av, int k){//回收k
      space[k].cursor = *av;
      *av = k;
   }
   ```

## 2.4 线性表的应用 —— 一元多项式的表示及相加

1. 表示（略）
2. 一元多项式的存储
   1. 顺序存储：适合存储非零系数较多的多项式
   2. 链式存储：
      ```cpp
      typedef struct Polynode{
         int coef, exp;
         struct Polynode* next;
      }Polynode, *Polylist;
      ```
3. 一元多项式的相加运算
   1. 指数相同项的对应系数相加，若和不为零，则构成“和多项式”的一项
   2. 指数不相同的项仍按升幂顺序复制到“和多项式”中
   3. 【A2.22 多项式相加】
      ```cpp
      PolyAdd(Polylist polya, Polylist polyb){
         Polynode *p = polya->next, *q = polyb->next;
         Polynode *tail = polya, *temp;
         int sum;
         while(p && q){
            if(p->exp < q->exp){
               tail->next = p;
               tail = p;
               p = p->next;
            }else if(p->exp == q->exp){
               if(sum = p->coef + q->coef){
                  p->coef = sum;
                  tail->next = p;
                  tail = p;
                  temp = q;
                  q = q->next;
                  free(temp);
               }else{
                  temp=p;p=p->next;free(temp);
                  temp=q;q=q->next;free(temp);
               }
            }else{
               tail->next = q;
               tail = q;
               q = q->next;
            }
         }
         tail->next = p ? p : q;
         free(polyb);
      }
      ```

【单向链表删除给定节点p（非尾节点O(1)）】
```cpp
p->data = p->next->data;
p->next = p->next->next;
free(p);
```

【单向链表删除删除倒数第k个节点O(n)】
```cpp
p = head, q = head;
while(k-- && (p = p->next));
while((p = p->next) && (q = q->next));
p->next = p->next->next;
free(p);
```

【判断链表中是否有环】
```cpp
p = head, q = head;
while(p = p->next){
   if((q = q->next) && p == q)break;
   if((q = q->next) && p == q)break;
}
return p && p == q;
```

## 2.5 顺序表与链表的综合比较

### 2.5.1 顺序表和链表的比较

1. 基于空间的考虑
   1. 存储密度：节点数据本身所占的存储量和整个节点结构所占的存储量之比
   2. 当线性表的长度变化不大，易于事先确定其大小时，为了节约存储空间，宜采用顺序表作为存储结构
2. 基于时间的考虑
   1. 若线性表的操作主要是进行查找，很少做插入或删除操作，宜采用顺序表作为存储结构
   2. 对于频繁进行插入或删除操作的线性表，宜采用链表作为存储结构
3. 基于语言考虑（略）

### 2.5.2 线性表链式存储方式比较

| 存储方式                        | 首元素节点      | 表尾节点   | p的前驱                        |
| ------------------------------- | --------------- | ---------- | ------------------------------ |
| 带头节点的单链表L               | `L->next`       | 一重循环   | 顺p节点的next域无法找到p的前驱 |
| 带头节点的循环单链表（头指针）L | `L->next`       | 一重循环   | 顺p节点的next域可以找到p的前驱 |
| 带尾指针的循环单链表R           | `R->next->next` | R          | 顺p节点的next可以找到p的前驱   |
| 带头节点的双向循环链表L         | `L->next`       | `L->prior` | `p->prior`                     |

## 2.6 总结与提高

1. 存储方式：顺序表、链表
2. 单链表操作：
   1. 顺链表操作技术：查找
   2. 指针保留技术：插入、删除
3. 相关：链表的表长并未显式保存
   1. 【R2.7 带头节点单链表的就地逆置问题】
      ```cpp
      ReverseList(LinkList L){
         p = L->next;//原链表当前处理节点
         L->next = NULL;//逆置单链表初始化为空表
         while(p){
            q = p->next;//q保留p->next
            p->next = L->next;//逆序建表
            L->next = p;
            p = q;//p后移
         }
      }
      //

      ```
   2. 【R2.8 以表中第一个元素为基准，表中小的前置，大的后置】
      ```cpp
      changelist(LinkList L){
         if(L->next == NULL){
            // 空表处理
         }
         pre = p1 = L->next;//当前操作的节点的前驱
         p = p1->next;
         while(p){
            q = p->next;
            if(p->data >= p1->data){
               pre = p;
               p = q;
            }else{
               pre->next = p->next;
               p->next = L->next;
               L->next = p;
               p = q;
            }
         }
      }
      ```
   3. 【R2.9 二进制加1】
      ```cpp
      // 二进制加法规则：实现二进制数加一运算，方向从低位往高位找到第一个值为0的位，从该位开始，对后面所有低位进行求反运算
      BinAdd(LinkList L){
         Node *q = L->next, *r = L, *s;
         while(q){
            if(q->data == 0)r=q;
            q = q->next;;
         }
         if(r != L){
            r->data = 1;
         }else{
            s = (Node*)malloc(sizeof(Node));
            s->data = 1;
            s->next = L->next;
            L->next = s;
            r = s;
         }
         while(r = r->next){
            r->data = 0;
         }
      }
      ```


# 第三章 限定性线性表 —— 栈与队列

## 3.1 栈（后进先出Last In First Out的线性表）

### 3.1.1 栈的定义

栈作为一种限定性线性表是将线性表的插入和删除操作限制在表的一端进行，通常将表中允许进行插入删除操作的一端称为栈顶，栈顶的当前位置是动态变化的，它有一个称为栈顶指针的位置指示器来指示，将表的另一端称为栈底，当栈中没有元素时称为空栈，栈的插入操作称为进站或入站，删除操作称为出栈或退栈。

```cpp
ADT Stack{
   数据对象：可以是任意类型的数据，但必须性质相同
   结构关系：栈中数据元素之间是线性关系
   基本操作：
      // 将S初始化为空栈
      InitStack(S);
      // 将栈S置成空栈
      ClearStack(S)
      // 判空
      IsEmpty(S);
      // 判满
      IsFull(S);
      // 入栈：在S的顶部插入元素x，栈满返回0
      Push(S, x);
      // 出栈：删除栈S的顶部元素，并用x带回该值，栈空返回0
      Pop(S, x);
      // 取栈顶的元素给x，栈空返回0
      GetTop(S, x);
}ADT Stack;
```

### 3.1.2 栈的表示和实现

1. 顺序栈（栈的顺序存储结构）
   ```cpp
   #define STACK_SIZE 50
   typedef struct{
      StackElementType elem[STACK_SIZE];
      int top;//栈顶元素下标，-1表空栈
   }SeqStack;
   ```
   1. 初始化
      ```cpp
      InitStack(SeqStack *S){
         S->top = -1;
      }
      ```
   2. 进栈
      ```cpp
      Push(SeqStack *S, StackElementType x){
         if(S->top == STACK_SIZE-1)return;//栈满
         S->elem[S->top++] = x;
      }
      ```
   3. 出栈
      ```cpp
      Pop(SeqStack *S, StackElementType* x){
         if(S->top == -1)return;//栈空
         *x = S->elem[S->top--];
      }
      ```
   4. 读栈顶元素
      ```cpp
      GetTop(SeqStack *S, StackElementType* x){
         if(S->top == -1)return;//栈空
         *x = S->elem[S->top];
      }
      ```
   5. 双端栈
      ```cpp
      #define M 100
      typedef struct {
         StackElementType stack[M];
         int top[2];
      }DqStack;
      InitStack(SeqStack *S){
         S->top[0] = -1;
         S->top[1] = M;
      }
      Push(SeqStack *S, StackElementType x, int i){
         if(S->top[0] + 1 == S->top[1])return;//栈满
         switch(i){
            case 0:
               S->stack[S->top[0]++] = x;
               break;
            case 1:
               S->stack[S->top[1]--] = x;
               break;
            default:break;
         }
      }
      Pop(SeqStack *S, StackElementType* x, int i){
         switch(i){
            case 0:
               if(S->top[0] == -1)return;
               *x = S->stack[S->top[0]--];
               break;
            case 1:
               if(S->top[1] == M)return;
               *x = S->stack[S->top[1]++];
               break;
            default:break;
         }
      }
      ```
2. 链栈（栈的链式存储结构）
   ```cpp
   typedef struct node{
      StackElementType data;
      struct node* next;
   }LinkStackNode, *LinkStack;
   ```
   1. 进栈
      ```cpp
      Push(LinkStack top, StackElementType x){
         LinkStackNode *temp = (LinkStackNode*)malloc(sizeof(LinkStackNode));
         if(temp){
            temp->data = x;
            temp->next = top->next;
            top->next = temp;
         }
      }
      ```
   2. 出栈
      ```cpp
      Pop(LinkStack top, StackElementType* x){
         LinkStackNode *temp = top->next;
         if(temp){
            top->next = temp->next;
            *x = temp->data;
            free(temp);
         }
      }
      ```
   3. 多栈运算
      ```cpp
      #define M 100
      typedef struct node{
         StackElementType data;
         struct node* next;
      }LinkStackNode, *LinkStack;
      LinkStack top[M];//结构体指针数组
      ```

### 3.1.3 栈的应用举例

1. 括号匹配问题
   ```cpp
   BracketMatch(char* str){
      InitStack(&S);
      while(*str){
         switch(*str){
         case '(':case '[':case '{':
            Push(&S, *str);break;
         case '(':case ']':case '}':
            if(IsEmpty(&S)){
               // 右括号多余
            }else{
               GetTop(&S, &ch);
               if(Match(ch, str)){
                  Pop(&S, &ch);
               }else{
                  // 对应的左右括号不同类
               }
            }
         }//switch
      }//while
      is(IsEmpty(&S)){
         // 匹配
      }else{
         // 左括号多余
      }
   }
   ```
2. 表达式求值
   表达式 = 运算对象 + 运算符 + 定界符
   ```cpp
   ExpEvaluation(char* exp){
      // 初始化OPTR（运算符栈）和OVS（运算数栈）；OPSet为运算符集合
      Push(&OPTR, '#');//为了便于操作，首先将定界符压入OPTR栈
      while(*exp != '#' || GetTop(OPTR) != '#'){
         if(!In(exp, OPSet)){
            Push(&OVS, GetNumber(exp));
            next(exp);
         }else{
            switch(Compare(exp, GetTop(OPTR))){
               case '>':
                  Push(&OPTR, exp);
                  next(exp);
                  break;
               case '=':
               case '<':
                  Pop(&OPTR, &op);
                  Pop(&OVS, &a);
                  Pop(&OVS, &b);
                  Push(&OVS, Execute(a, op, b));
                  break;
            }
         }
         return GetTop(OVS);
      }

   }
   ```

### 3.1.4 栈与递归的实现

- 递归：在定义自身的同时又出现了对自身的引用
- 直接递归函数：一个函数在其定义体内直接调用自己
- 间接递归函数：一个函数通过其他函数间接调用自己

1. 具有递归特性的问题
   1. 递归定义的数学函数
      1. 二阶斐波那契数列
         ```


         ```
      2. 阿克曼函数
         ```
         

         ```
   2. 递归数据结构处理：广义表、二叉树
   3. 递归求解方法：汉诺塔
   4. 使用递归的两个前提
      1. 原问题可以层层分解为类似的子问题，且子问题比原问题的规模更小
      2. 规模最小的问题具有直接解
         1. 原则：用自身的简单情况来定义自身
         2. 方法：
            1. 寻找分解方法：将原问题转化为子问题求解
            2. 设计递归出口：根据规模最小的子问题确定递归终止条件
2. 递归过程的实现
   1. 递归进层（i -> i+1层）时系统：
      1. 保留本层参数与返回地址
      2. 为被调用的函数的局部变量分配存储区，给下层参数赋值
      3. 将程序转移到被调用函数的入口
   2. 递归退层（i -> i-1层）时系统：
      1. 保存被调用函数的计算结果
      2. 释放被调用函数的数据区，恢复上层参数
      3. 依照被调用函数保存的返回地址，将控制转移回调用函数
   3. 当前正在运行的函数的数据区必在栈顶
   4. 递归工作栈：系统为了保证递归函数正确执行而设立的一个递归函数运行期间使用的数据存储区
   5. 工作记录：每层递归所需的信息（包括所有实参，局部变量以及上一层的返回地址）
3. 递归算法到非递归算法的转换（特性：分析方法有效，性能较低）
   1. 消除递归的原因
      1. 提高算法的时空性能
      2. 无应用递归语句是语言实施环境条件
      3. 递归算法中间过程对用户不可见
      4. 简单递归问题的转换：对于尾递归和单向递归的算法，可用循环结构的算法替代
      5. 基于栈的方式：将递归中隐含的栈机制转换为由用户直接控制的明显的栈，利用栈来保存参数
   2. 简单递归的消除
      1. 单向递归：递归函数中虽然有多次递归调用语句，但各次递归调用语句的参数只和主调函数有关，相互之间参数无关
      2. 尾递归：递归调用语句只有一个，而且是处于算法的最后（单向递归的特例）

## 3.2 队列

### 3.2.1 队列的定义

- 队列是另一种限定性线性表，它只允许在表的一端插入元素，而在表的另一端删除元素，所以队列具有FIFO的特性
- 队尾（rear）：允许插入的一端
- 队头（front）：允许删除的一端

```cpp
ADT Queue{
   数据对象：可以是任意类型的数据，但必须性质相同
   结构关系：队列中数据元素之间是线性关系
   基本操作：
      // 将Q初始化为一个空的队列
      InitQueue(Q);
      // 判空
      IsEmpty(Q);
      // 判满
      IsFull(Q);
      // 在队列Q的队尾插入x
      EnterQueue(Q, x);
      // 将队列Q的队头元素出队，并用x返回其值
      DeleteQueue(Q, x);
      // 将队列Q置为空队列
      ClearQueue(Q);
}ADT Queue;
```

### 3.2.2 队列的表示和实现

1. 链队列（队列的链式存储结构）
   ```cpp
   // 通常将队头指针和队尾指针封装在一个结构体中，并将该结构体类型重新命名为链队列类型
   typedef struct Node{
      QueueElementType data;
      struct Node* next;
   }LinkQueueNode;
   typedef struct{
      LinkQueueNode* front;
      LinkQueueNode* rear;
   }LinkQueue;
   ```
   【A3.16 链队列初始化】
   ```cpp
   InitQueue(LinkQueue *Q){
      Q->front = (LinkQueueNode*)malloc(sizeof(LinkQueueNode));
      if(Q->front != NULL){
         Q->rear = Q->front;
         Q->front->next = NULL;
      }
   }
   ```
   【A3.17 链队列入队】
   ```cpp
   EnterQueue(LinkQueue *Q, QueueElementType x){
      LinkQueueNode* newNode;
      if(newNode = (LinkQueueNode*)malloc(sizeof(LinkQueueNode))){
         newNode->data = x;
         newNode->next = NULL;
         Q->rear->next = newNode;
         Q->rear = newNode;
      }
   }
   ```
   【A3.18 链队列出队】
   ```cpp
   DeleteQueue(LinkQueue *Q, QueueElementType *x){
      if(Q->front == Q->rear){
         // 判空
      }
      LinkQueueNode *p = Q->front->next;
      Q->front->next = p->next;
      if(Q->rear == p){//只有一个元素，出队变空队
         Q->rear = Q->front;
      }
      *x = p->data;
      free(p);
   }
   ```
2. 循环队列（队列的顺序表示和实现方法）
   - 真正队满的条件：rear - front = MAXSIZE
   - 进队时：rear = (rear+1)%MAXSIZE
   - 出队时：front = (front+1)%MAXSIZE
   - 在非空队列中，队头指针始终指向当前的队头元素，而队尾的指针始终指向真正队尾元素后面的单元
   - front == rear：无法判断队列状态
     - 损失一个元素的存储空间，当队尾指针指向的空单元的后继单元是队头元素所在的单元时停止入队
     - 增设一个标志量以区别队列状态
   ```cpp
   #define MAXSIZE 50
   typedef struct{
      QueueElementType element[MAXSIZE];
      int front;
      int rear;
   }SeqQueue;
   ```
   【A3.19 循环队列初始化】
   ```cpp
   InitQueue(SeqQueue *Q){
      Q->front = Q->rear = 0;
   }
   ```
   【A3.20 循环队列入队】
   ```cpp
   EnterQueue(SeqQueue *Q, QueueElementType x){
      if((Q->rear + 1)%MAXSIZE == Q->front){
         // 队满
      }
      Q->element[Q->rear++] = x;
      Q->rear %= MAXSIZE;
   }
   ```
   【A3.21 循环队列出队】
   ```cpp
   DeleteQueue(SeqQueue *Q, QueueElementType *x){
      if(Q->rear == Q->front){
         // 队空
      }
      *x = Q->element[Q->front++];
      Q->front %= MAXSIZE;
   }
   ```
   - 上述的第二种标志位的方法：
     - 初始化：Q->front = Q->rear = 0;tag = 0;
     - 队空：Q->front == Q->rear = 0 && tag == 0;
     - 队满：Q->front == Q->rear = 0 && tag == 1;
3. 双端队列（不常用）

### 3.2.3 队列的应用举例

【A3.22 杨辉三角形】
```cpp
YanghuiTriangle(){
   // 初始化队列Q
   EnterQueue(&Q, 1);//行1入队
   for(n = 2; n <= N; n++){//行n入队，行n-1出队
      EnterQueue(&Q, 1);//行n第一个元素出队
      for (i = 0; i <= n-2; i++) {//利用行n-1生成行n中间n-2个元素
         DeleteQueue(&Q, &temp);//n-1行出队
         printf("%d", temp);
         GetHead(Q, &x);
         EnterQueue(&Q, temp+=x);//利用行n-1生成第n行元素
      }
      DeleteQueue(&Q, &x);//行n-1最后一个元素出队
      printf("%d", x);
      EnterQueue(&Q, 1);//行n最后一个元素入队
   }
   while(!isEmpty(Q)){
      DeleteQueue(&Q, &x);
      printf("%d"  x);
   }
}
```
【A3.23 键盘输入缓冲区问题】
```cpp
for(;;){
   //初始化队列，变量声明
   for(;;){
      printf("A");
      if(kbhit()){
         ch1 = getch();
         if(ch1 == ';' || ch1 == ',')break;
         if(!EnterQueue(&Q, ch1))break;
      }
   }
   while(!isEmpty(Q)){
      DeleteQueue(&Q, &ch2);
      putchar(ch2);
   }
   if(ch1 == ';')break;
}
```
## 3.3 总结与提高

【辗转相除法（求最大公约数）】
```cpp
int f(int m, int n){
   int r;
   do{
      r = m % n;
      m = n;
      n = r;
   }while(r);
   return m;
}
```
【模拟排队】
```cpp
#include <stdio.h>
#include <stdlib.h>
typedef struct customer{// 顾客
   int come; //顾客到来的时间
   int use;  //办理业务需要的时间
} customer;
typedef struct window{// 窗口
   int time;      //窗口恢复空闲的时间
   int wait_time; //所有客户在该窗口等待的总时间
   int counter;   //办理的客户数量
} window;
typedef struct cqnode{
   customer *customer;
   struct cqnode *next;
} cqnode;
typedef struct customerQueue{
   cqnode *front;
   cqnode *rear;
} * customerQueue;
customerQueue initQueue(){
   customerQueue queue = (customerQueue)malloc(sizeof(struct customerQueue));
   queue->front = (cqnode *)malloc(sizeof(struct cqnode));
   queue->rear = queue->front;
   queue->front->next = NULL;
   return queue;
}
int enterQueue(customerQueue queue, customer *cstm){
   cqnode *newNode = (cqnode *)malloc(sizeof(struct cqnode));
   newNode->customer = cstm;
   newNode->next = NULL;
   queue->rear->next = newNode;
   queue->rear = newNode;
   return 1;
}
int deleteQueue(customerQueue queue, customer **cstm){
   if (queue->front == queue->rear){
      return 0;
   }
   cqnode *p = queue->front->next;
   queue->front->next = p->next;
   if (queue->rear == p){
      queue->rear = queue->front;
   }
   *cstm = p->customer;
   free(p);
   return 1;
}
int isEmpty(customerQueue queue){
   return queue->front == queue->rear;
}
void show_window_count(window *windows, int windowsNumber){
   for (size_t i = 0; i < windowsNumber; i++){
      printf("%d", windows[i].counter);
      if (i != windowsNumber - 1){
         printf(" ");
      }
   }
}
double finder(window *windows, int windowsNumber, int *maxWaitTime){
   double avg = 0.0;
   for (int i = 0; i < windowsNumber; i++){
      avg += windows[i].wait_time;
      if (windows[i].time > *maxWaitTime){
         *maxWaitTime = windows[i].time;
      }
   }
   return avg;
}
int main()
{
   /*
   N(customerNumber):顾客总人数 <=1000
   每行给出一位顾客的到达时间T和事务处理时间P,已经按到达时间先后排好了顺序
   K(windowsNumber)：开设的营业窗口数 <=10
   */
   int customerNumber, windowsNumber;
   // 初始化参数
   customer *tempCustomer;                           //存储单个客户信息
   customerQueue wait;                               //客户等待队列
   window *windows;                                  //模拟 k 个窗口
   int i, flag;                                      //循环控制变量,受理标志
   int min_time, num, max_waittime = 0, maxtime = 0; //最快可办理窗口时间、最快可办理窗口编号、最大等待时间、最后办理结束时间
   double avg = 0.0;
   // 初始化客人队列
   scanf("%d", &customerNumber);
   wait = initQueue();
   for (i = 0; i < customerNumber; i++){
      tempCustomer = (customer *)malloc(sizeof(customer));
      scanf("%d %d", &tempCustomer->come, &tempCustomer->use);
      if (tempCustomer->use > 60)
         tempCustomer->use = 60;
      enterQueue(wait, tempCustomer);
   }
   // 初始化窗口
   scanf("%d", &windowsNumber);
   windows = (window *)malloc(windowsNumber * sizeof(window));
   for (i = 0; i < windowsNumber; i++){ //制造 k 个窗口
      windows[i].counter = 0;
      windows[i].time = 0;
      windows[i].wait_time = 0;
   }
   // 主控逻辑
   while (!isEmpty(wait)){ //等待队列不为空
      flag = 0;
      min_time = 9999; //一个理论极大值
      // 出队一个顾客
      tempCustomer = (customer *)malloc(sizeof(customer));
      deleteQueue(wait, &tempCustomer);
      for (i = 0; i < windowsNumber; i++){
         if (windows[i].time <= tempCustomer->come){ //有空闲窗口
            windows[i].time = tempCustomer->come;
            windows[i].time += tempCustomer->use;
            windows[i].counter++;
            flag++;
            break;
         }
         if (windows[i].time < min_time){ //记录最先可办理窗口
            num = i;
            min_time = windows[i].time;
         }
      }
      if (flag) //已经在空闲窗口办理
         continue;
      if (tempCustomer->come > windows[num].time) //到最先可办理窗口办理
         windows[num].time = tempCustomer->come;
      else{
         windows[num].wait_time += (windows[num].time - tempCustomer->come);
         if ((windows[num].time - tempCustomer->come) > max_waittime) //更新最大等待时间
            max_waittime = windows[num].time - tempCustomer->come;
      }
      windows[num].time += tempCustomer->use;
      windows[num].counter++;
   } // end while
   // 数据输出
   avg = finder(windows, windowsNumber, &maxtime) / customerNumber;
   printf("%.1f %d %d\n", avg, max_waittime, maxtime);
   show_window_count(windows, windowsNumber);
   return 0;
}
```


# 第四章 串

## 4.1 串的基本概念

- 字符串：由零个或多个字符组成的有限序列，记为S='a<sub>1</sub>a<sub>2</sub>a<sub>3</sub>...a<sub>n</sub>'(n>0)
  - n=0时的串称为空串
  - 引号是定界符，不属于串，作用是避免串值与变量名或常量混淆
- 子串：串中任意连续的字符组成的子序列
- 主串：包含子串的串
- 子串在主串中的位置：子串的第一个字符在主串中的位置
- 串相等：两个串的值相等（长度相同且对应位置的字符都相等）
- 空格串：由一个或多个空白字符组成的串

```cpp
ADT String{
  数据对象：D={a[i]|a[i]∈characterSet, i=1,2,...,n,n>=0}
  结构关系：R={<a[i],a[i+1]>|a[i],a[i+1]∈D,i=1,2,...,n-1,n>=1}
  基本操作：
    // 生成一个值等于chars的串S
    StrAssign(S, chars);
    // 在串S的第pos个字符之前插入串T
    StrInsert(S, pos, T);
    // 从串S中删除第pos个字符起长度为len的子串
    StrDelete(S, pos, len);
    // 由串T复制得串S
    StrCopy(S, T);
    // 判断串S是否为空串
    StrEmpty(S);
    // S>T 返回正值，S=T 返回0，S<T 返回负值
    StrCompare(S, T);
    // 返回串S的长度（字符个数）
    StrLength(S);
    // 将S清为空串
    StrClear(S);
    // 将串T的值连接在串S的后面
    StrCat(S, T);
    // 用Sub返回串S的第pos个字符起长度为len的子串
    SubString(Sub, S, pos, len);
    // 若串S中存在和串T相同的子串，则返回它在串S中第pos个字符之后第一次出现的位置，否则返回0
    StrIndex(S, pos, T);
    // 用v替换串S中出现的所有与T相等的不重叠的子串
    StrReplace(S, T, v);
    // 销毁串S
    StrDestory(S);
}ADT String;
```

## 4.2 串的存储实现

### 4.2.1 定长顺序串

将串设计成一种静态结构类型，串的存储方面已是在编译时完成的

1. 定长顺序串的存储结构
   ```cpp
   #define MAXLEN 40
   typedef struct {
     char ch[MAXLEN];
     int len;
   }SString;
   ```
2. 定长顺序串基本操作的实现（注：本节位置与下标均从零开始）
   1. 串插入
      ```cpp
      StrInsert(SString* s, int pos, SString t){
        int i;
        if(pos < 0 || pos > s->len)return;//插入位置不合法
        if(s->len + t.len <= MAXLEN){//插入后串长<=MAXSIZE
          for(i = s->len + t.len-1; i >= t.len + pos; i--)
            s->ch[i] = s->ch[i-t.len];//后移
          for(i = 0; i < t.len; i++)
            s->ch[i+pos] = t.ch[i];//插入
          s->len += t.len;
        }else if(pos + t.len <= MAXLEN){//插入后串长>MAXSIZE，但t也可以完全插入
          for(i = MAXLEN - 1; i > t.len + pos - 1; i--)
            s->ch[i] = s->ch[i-t.len];//部分丢弃
          for(i = 0; i < t.len; i++)
            s->ch[i+pos] = t.ch[i];//t插入
          s->len = MAXLEN;
        }else{//t只能插入部分
          for(i = 0; i < MAXLEN - pos; i++)
            s->ch[i+pos] = t.ch[i];//直接插入，多余舍弃
          s->len = MAXLEN;
        }
      }
      ```
   2. 串删除
      ```cpp
        StrDelete(SString* s, int pos, int len){//从pos起删len个字符
          if(pos < 0 || pos > s->len - len)return;//删除参数不合法
          for(i = pos + len; i < s->len; i++)
            s->ch[i-len] = s->ch[i];
          s->len - = len;
        }
      ```
   3. 串比较
      ```cpp
        StrCompare(SString s, SString t){
          for(i = 0; i < s.len && i < t.len; i++)
            if(s.ch[i] != t.ch[i])return s.ch[i] - t.ch[i];
          return s.len - t.len;//谁长谁大
        }
      ```
   4. 定位函数
      1. 模式匹配：在主串（目标串）中寻找子串（模式串）的过程
3. 串的简单模式匹配Brute-Force算法
   ```cpp
    StrIndex(SString s, int pos, SString t){
      if(t.len == 0)return 0;//空串是任意串的匹配串
      start = pos; i = start; j = 0;//主串从pos开始，模式串从0开始
      while(i < s.len && j < t.len){
        if(s.ch[i] == t.ch[j]){//对应字符相等
          i++; j++;//推进
        }else{//对应字符不等
          start++; i = start; j = 0;//回溯:主串从start+1开始,模式串从0开始
        }
      }
      return j >= t.len ? start : -1;//匹配成功时，返回匹配起始位置
    }
   ```
4. KMP
   ```cpp
   //









   ```

### 4.2.2 堆串

- 符号表：所有串名的存储映像构成一个符号表。借助此结构可以在串名和串值之间建立一个对应关系，称为串名的存储映像。
- 堆串：以一组地址连续的存储单元顺序存放串中的字符，但他们的存储空间是在程序执行过程中动态分配的。

```cpp
typedef struct {
  char* ch;//串的起始地址
  int len;
}HString;
// 堆串插入
StrInsert(HString* s, int pos, HString* t){
  int i;
  char* temp;
  if(pos < 0 || pos > s->len || s->len == 0)return 0;//负值上溢，空串处理
  if((temp = (char*)malloc(s->len+t->len)) == NULL)return 0;//未产生足够的空间
  for(i = 0; i < pos; i++)
    temp[i] = s->ch[i];//原来前半部分
  for(i = 0; i < t->len; i++)
    temp[i+pos] = t->ch[i];//插入部分
  for(i = pos; i < s->len; i++)
    temp[i+t->len] = s->ch[i];//原来后半部分
  s->len += t->len;
  free(s->ch);
  s->ch = temp;
}
StrAssign(HString* s, char* tval){
  int len, i = 0;
  if(s->ch != NULL)free(s->ch);//置s未空串
  while(tval[i] != '\0')i++;//求tval长度
  len = i;
  if(len){
    if((s->ch = (char*)malloc(len)) == NULL)return;//开辟空间
    for(i = 0; i < len; i++)
      s->ch[i] = tval[i];//按位复制
  }else{
    s->ch == NULL;
  }
  s->len = len;
}
```

### 4.2.3 块链串

```cpp
typedef struct Block{
  char ch[BLOCK_SIZE];//值域
  struct Block* next;//指针域
}Block;
typedef struct BLString{//块链结构
  Block* head;
  Block* tail;
  int len;//asdf
};
// 存储密度：值域所占字节数/(值域所占字节数+指针域所占字节数)
// 当BLOCK_SIZE = 1时：
typedef struct chBlock{
  char ch;//值域
  struct chBlock* next;//指针域
}chBlock;
// 当BLOCK_SIZE > 1时，每个节点存放多个字符，最后一个节点未存满时，不足处可用特定字符补齐。
```

## 4.3 串的应用举例：简单的行编辑器（略）

页表

| 页号 | 起始位置 | 长度 |
| ---- | -------- | ---- |
| 1    | 1        | 106  |

行表

| 行号 | 起始位置 | 长度 |
| ---- | -------- | ---- |
| 1    | 1        | 31   |
| 2    | 32       | 15   |
| 3    | 47       | 6    |
| ...  | ...      | ...  |
| 7    | 102      | 5    |

## 4.4 总结与提高

【带头节点的单链表实现串的模式匹配】
```cpp
Link* StrIndex(LKString* s, LKString*t){
  Link *sp, *tp, *start;
  if(t->len == 0)return s->head->next;//空串是任意串的子串
  start = s->head->next;//主串起始点
  sp = start; tp = t->head->next;//主串从start开始，模式串从第一个节点开始
  while(sp && tp){//有一个为空就结束
    if(sp->ch == tp->ch){
      sp = sp->next;
      tp = tp->next;
    }else{
      start = start->next;//主串从start的下一个开始
      sp = start;
      tp = t->head->next;//模式串从第一个节点重新开始
    }
  }
  // tp不为NULL，则主串读到结尾，证明没有匹配的子串
  // tp为NULL，则模式串读完，即匹配成功，start即为主串匹配位置的地址
  return tp ? NULL : start;
}
```


# 第五章 数组与广义表

## 5.1 数组的定义与运算

1. 数组的定义：
   1. ...
   2. N维数组是数据元素为N-1维数组的线性表
2. 数组的运算（数据元素的定位）
   1. 数组是一组有确定个数的元素的集合
   2. 获得特定位置的元素值；
   3. 修改特定位置的元素值；
3. 数组的抽象数据类型定义
   ```cpp
   ADT Array{
      数据对象：D={a[j1j2...jn]|n>0， 称为数组的维数，ji是数组的第i维下标，1<=ji<=bi，bi为数组第i维的长度，a[j1j2...jn]∈ElementSet}
      结构关系：R={R[1],R[2],...R[n]}; R[i]={<a[j1j2...jn],a[j1j2...jn]>|1<=j[k]<=b[k],1<=k<=n,且k≠i,1<=j[i]<=b[i-1],a[j1j2...jn],a[j1j2...jn]∈D,i=1,2,...,n, n>=0}
      基本操作：
         // 若维数n和各维的长度合法，则构造相应的数组A，并返回TRUE
         InitArray(A, n, bound1, bound2, ..., boundn);
         // 销毁数组A
         DestoryArray(A);
         // 若下标合法，则用e返回数组A中相应位置的元素的值
         GetValue(A, e, index1, index2, ..., indexn);
         // 若下标合法，则将数组A中相应位置的元素的值置为e
         SetValue(A, e, index1, index2, ..., indexn);
   }ADT Array;
   // 此处的数组下标从1开始
   ```

## 5.2 数组的顺序存储实现

数组的基本操作不涉及数组结构的变化，因此对于数组而言，采用顺序存储比较合适

1. 一维数组地址计算：`Loc(A[i])=Loc(A[1])+(i−1)∗size`
2. 二维数组地址计算：`Loc(A[i][j])=Loc(A[1][1])+(n*(i−1)+j-1)∗size`
3. 三维数组地址计算：`Loc(A[i][j][k])=Loc(A[1][1][1])+(m*n*(i−1)+n*(j-1)+k-1)∗size`
4. n维数组地址计算：![](imgs/2021-10-19-21-20-56.png)

## 5.3 特殊矩阵的压缩存储

### 5.3.1 规律分布的特殊矩阵

1. 三角矩阵（下三角矩阵、上三角矩阵、对角矩阵）
   1. 下三角矩阵：当i\<j时，有a\[i\]\[j\]=c（典型情况c=0）
   2. 上三角矩阵：当i\>j时，有a\[i\]\[j\]=c（典型情况c=0）
   3. 对角矩阵：矩阵中所有元素均满足`a[i][j]=a[j][i];`
   4. 下三角矩阵A中的元素a<sub>ij</sub>(i>=j)在一维数组B中的存储单元的地址为
      1. `Loc(A[i][j])=Loc(A[1][1])+(前i-1行非零元素个数+第i行中A[i][j]前非零元素个数)`
      2. `Loc(A[i][j])=Loc(A[1][1])+(i*(i-1)/2+j-1)`
2. 带状矩阵
   1. 矩阵中所有非零元素都在集中以主对角线为中心的带状区域中
   2. 三角带状矩阵特点：在以下条件下`a[i][j]`非零，其他元素均为零
      1. 当`i=1`时，j=1,2
      2. 当`1<i<n`时，j=i-1,i,i+1
      3. 当`i=n`时，j=n-1,n
   3. 三角带状矩阵压缩存储方法
      1. 原则：将带状区域上的非零元素按行序存储
      2. 存储该矩阵所需的一维向量空间的大小：3n-2
      3. 确定非零元素在一维数组空间中的地址：`Loc(A[i][j])=Loc(A[1][1])+(前i-1行非零元素个数+第i行中A[i][j]前非零元素个数)*size`
      4. `=Loc(A[1][1])+(3*(i-1)-1+j-i+1)*size`
      5. `=Loc(A[1][1])+(2*(i-1)+j+1)*size`

### 5.3.2 稀疏矩阵

矩阵中大多数（70%以上）元素为0的矩阵
1. 三元组表示法
   1. row：行；col：列；e：值
   2. 类型定义
      ```cpp
      #define MAXSIZE 1000
      typedef struct{
         int row, col;
         ElementType e;
      }Triple;
      typedef struct{
         Triple data[MAXSIZE + 1];//data[0]未用
         int m, n, len;//矩阵的行数，列数，非零元素个数
      }TSMatrix;
      ```
   3. 三元组表实现矩阵的转置
      1. 经典算法
         ```cpp
         TransMatrix(ElementType source[m][n], ElementType dest[m][n]){
            for(i = 0; i < m; i++)
               for(j = 0; j < n; j++)
                  dest[j][i] = source[i][j];
         }
         ```
      2. 三元组表实现稀疏矩阵的转置
         1. 列序递增转置法
            ```cpp
            TransposeTSMatrix(TSMatrix A, TSMatrix *B){
               int i, j, k;
               B->m = A.n;
               B->n = A.m;
               B->len = A.len;
               if (B->len > 0){
                  j = 1;
                  for (k = 1; k <= A.n; k++){
                     for (i = 1; i < A.len; i++){
                        if (A.data[i].col == k){
                           B->data[j].row = A.data[i].col;
                           B->data[j].col = A.data[i].row;
                           B->data[j].e = A.data[i].e;
                           j++;
                        }
                     }
                  }
               }
            }
            ```
         2. 一次定位快速转置法
            ```cpp
            FastTransposeTSMatrix(TSMatrix A, TSMatrix *B){
               int col, t, p, q, i;
               int num[MAXSIZE]; //, position[MAXSIZE];
               B->len = A.len;
               B->n = A.m;
               B->m = A.n;
               if (B->len > 0){
                  for (col = 1; col <= A.len; col++)
                     num[col] = 0;
                  for (t = 1; t <= A.len; t++)
                     num[A.data[t].col]++;
                  num[0] = 1; // position[i] = 1;
                  for (col = 2; col <= A.len; col++)
                     //  position[col] = position[col - 1] + num[col - 1];
                     num[col] += num[col - 1];
                  for (p = 1; p <= A.len; p++){
                     col = A.data[p].col;
                     q = num[col]; //  q = position[col];
                     B->data[q].row = A.data[p].col;
                     B->data[q].col = A.data[p].row;
                     B->data[q].e = A.data[p].e;
                     num[col]++; //  position[col]++;
                  }
               }
            }
            ```
2. 十字链表
   1. 存储表示（节点结构）：row：行；col：列；value：值；down：同一列的下一个非零元；right：同一行的下一个非零元
   2. 类型定义
      ```cpp
      typedef struct OLNode{
         int row, col;
         ElementType value;
         struct OLNode *right, *down;
      }OLNode, *OLink;
      typedef struct{
         OLink *row_head, *col_head;
         int m, n, len;
      }CrossList;
      ```
   3. 十字链表算法实现
      1. 建立步骤：
         1. 行数、列数、非零元个数
         2. 行链表的头指针向量，列链表的头指针向量
         3. 逐个读入非零元素，分别插入行链表，列链表
         ```cpp
         CreateCrossList(CrossList *M){
            int m, n, t, i, j, e;
            OLink p, q;
            scanf(&m, &n, &t);
            M->m = m;
            M->n = n;
            M->len = t;
            if (!(M->row_head = (OLink *)malloc((m + 1) * sizeof(OLNode))))
               exit(1);
            if (!(M->col_head = (OLink *)malloc((n + 1) * sizeof(OLNode))))
               exit(1);
            // M->row_head[] = M->col_head[] = NULL;
            for (scanf(&i, &j, &e); i; scanf(&i, &j, &e)){
               if (!(p = (OLink)malloc(sizeof(OLNode))))
                  exit(1);
               p->row = i;
               p->col = j;
               p->value = e;
               if (M->row_head[i] == NULL)
                  M->row_head[i] = p;
               else if (p->row < M->row_head[i]->row){
                  p->right = M->row_head[i];
                  M->row_head[i] = p;
               }
               else{
                  for (q = M->row_head[i]; q->right && q->right->row < j; q = q->right);
                  p->right = q->right;
                  q->right = p;
               }
               if (M->col_head[i] == NULL)
                  M->col_head[j] = p;
               else if (p->row < M->row_head[j]->row){
                  p->down = M->col_head[i];
                  M->col_head[i] = p;
               }
               else{
                  for (q = M->col_head[i]; q->down && q->down->row < i; q = q->down);
                  p->down = q->down;
                  q->down = p;
               }
            }
         }
         ```

## 5.4 广义表

### 5.4.1 广义表的概念

- GL=(d<sub>1</sub>, d<sub>2</sub>, d<sub>3</sub>, ..., d<sub>n</sub>)
- 通常广义表的名字用大写字母表示，单个元素用小写字母表示，n是广义表长度
- D=()：空表，其长度为0
- A=(a, (b, c))：长度为2的广义表，其中第一个元素是单个数据a，第二个元素是一个子表(b, c)
- B=(A, A, D)：长度为3的广义表，其中前两个元素是表A，第三个元素是空表D
- C=(a, C)：长度为2的广义表，C相当于无穷表(a, (a, (a, ...)))

1. 广义表的元素可以是子表，而子表还可以是子表
2. 广义表可以被其他广义表共享
3. 广义表具有递归性
4. 广义表操作：
   1. 求表头head(A)=a，表A的表头是a
   2. 求表尾tail(A)=((b, c))，表A的表尾是((b, c))，广义表的表尾一定是一个表

### 5.4.2 广义表的存储结构

1. 广义表的头尾链表存储结构
   1. 任何一个非空的广义表都可以将其分解成表头和表尾两部分，反之，一对确定关系的表头和表尾可以唯一地确定一个表
   2. 节点结构
      1. 表节点：tag=1：标志域；hp：表头；tp：表尾；
      2. 原子节点：tag=0：标志域；atom：值
   ```cpp
   typedef enum{ATOM, LIST} ElemTag;
   typedef struct GLNode{
      union{
         AtomType atom;
         struct{
            struct GLNode *hp, *tp;
         } htp;
      } atom_htp;
      ElemTag tag;
   } GLNode, *GList;
   ```
2. 广义表的同层节点存储结构
   1. 节点结构
      1. 表节点：tag=1：标志域；hp：表头；tp：同层下一个节点的指针域；
      2. 原子节点：tag=0：标志域；atom：值；tp：同层下一个节点的指针域
   ```cpp
   typedef struct GLNode{
      ElemTag tag;
      union{
         AtomType atom;
         struct GLNode *hp;
      } atom_htp;
      struct GLNode *tp;
   } GLNode, *GList;
   ```
   ```cpp
   // 头尾链表




   // 同层节点




   ```

### 5.4.3 广义表的操作实现（头尾链表）

【A5.5 求表头】
```cpp
GList Head(GList L){
   if (L == NULL)
      return NULL;
   if (L->tag == ATOM)
      exit(1);
   else
      return L->atom_htp.htp.hp;
}
```
【A5.6 求表尾】
```cpp
GList Tail(GList L){
   if (L == NULL)
      return NULL;
   if (L->tag == ATOM)
      exit(1);
   else
      return L->atom_htp.htp.tp;
}
```
【A5.7 求表长】
```cpp
int Length(GList L){
   int k = 0;
   GLNode *s;
   if (L == NULL)
      return NULL;
   if (L->tag == ATOM)
      exit(1);
   s = L;
   while (s){
      k++;
      s = s->atom_htp.htp.tp;
   }
   return k;
}
```
【A5.8 求深度】
```cpp
int Depth(GList L){
   int d, max;
   GLNode *s;
   if (L == NULL)
      return 1;
   if (L->tag == ATOM)
      return 0;
   s = L;
   while (s){
      d = Depth(s->atom_htp.htp.hp);
      if (d > max)
         max = d;
      s = s->atom_htp.htp.tp;
   }
   return max + 1;
}
```
【A5.9 原子节点个数】
```cpp
int CountAtom(GList L){
   int n1, n2;
   if (L == NULL)
      return 0;
   if (L->tag == ATOM)
      return 1;
   n1 = CountAtom(L->atom_htp.htp.hp);
   n2 = CountAtom(L->atom_htp.htp.tp);
   return n1 + n2;
}
```
【A5.10 复制广义表（深复制）】
```cpp
int copyGList(GList S, GList *T){
   if (S == NULL){
      *T = NULL;
      return 1;
   }
   *T = (GLNode *)malloc(sizeof(GLNode));
   if (*T == NULL)
      return -1;
   (*T)->tag = S->tag;
   if (S->tag == ATOM)
      (*T)->atom_htp.atom = S->atom_htp.atom;
   else{
      copyGList(S->atom_htp.htp.hp, &((*T)->atom_htp.htp.hp));
      copyGList(S->atom_htp.htp.tp, &((*T)->atom_htp.htp.tp));
      return 1;
   }
}
```

## 5.5 总结与提高

【R5.4 上三角矩阵地址】

- 矩阵上三角中共有n*(n+1)/2个元素，下三角中所有元素相同，使用一维数组B
- 上三角中第t行共有n-t+1个元素，对于上三角任意元素a<sub>ij</sub>
  - 其前i-1行中共有：$\sum_{t=1}^{i-1} (n-t+1) = \frac {(i-1)(2n-i+2)} {2}$
  - 第i行a<sub>ij</sub>前共有：$j-(i-1)-1=j-i$
  - 综上对于任意元素a<sub>ij</sub>，前有 $\sum_{t=1}^{i-1} (n-t+1) = \frac {(i-1)(2n-i+2)} {2} + j-i$ 个元素，其在一维数组B中的位置
   $$
   k=f(i,j)=\left\{\begin{aligned}
   \sum_{t=1}^{i-1} (n-t+1) = \frac {(i-1)(2n-i+2)} {2} + j-i\\   m   \end{aligned}\right.
   $$


# 第六章 树与二叉树

## 6.1 树的定义及基本术语

1. 树的基本概念
   1. 树：n(n>=0)个节点的有限集合T
   2. n=0：空树
   3. n>0：
      1. 其中必有一个称为根（root）的特定节点，他没有直接前驱，但有零个或多个直接后继
      2. 其中n-1个节点可以划分成m(m>=0)个互不相交的有限集T<sub>1</sub>,T<sub>2</sub>,...T<sub>m</sub>
         1. 其中T<sub>i</sub>又是一棵树，称为根的子树
         2. 每棵子树的根节点有且仅有一个直接前驱，但有零个或多个直接后继
2. 树的图解表示法
   1. 倒置树结构（树形表示法）
   2. 文氏图表示法（嵌套集合表示法）
   3. 广义表形式（嵌套括号表示法）
   4. 凹入表示法
3. 树的相关属术语
   1. 结点：包括一个数据元素及若干指向其他节点的分支信息
   2. 结点的度：该结点的子树个数
   3. 叶结点：度为0的结点，即无后继结点，又称终端结点
   4. 分支结点：度不为0的结点，又称非终端结点
   5. 结点的层次：从根结点开始定义，根结点的层次为1，根的直接后继的层次为2...
   6. 结点的层序编号：将树中的结点按从上层到下层，同层从左到右的次序排成一个线性序列，依次给他们编以连续的自然数
   7. 树的度：树中所有结点度的最大值
   8. 树的高度（深度）：树中所有结点的层次的最大值
   9. 有序树：在树T中，如果各子树T<sub>i</sub>之间是有先后次序的，则称为有序树
   10. 森林：m(m>=0)棵互不相交的树的集合。将一棵非空树的根结点删去，树就变成一个森林；给森林增加一个统一的根结点，森林就变成一棵树。一棵树也可以称为森林
   11. 同构：对两棵树，通过对结点适当地重命名，就可以使两棵树完全相等（结点对应相等，对应结点的相关关系页也相等）
   12. 孩子结点：该结点的直接后继
   13. 双亲结点：该结点的直接前驱
   14. 兄弟结点：同一双亲结点的孩子结点之间互称
   15. 堂兄弟：父亲是兄弟关系或堂兄弟关系的结点
   16. 祖先结点：从根结点至该结点的路径上的所有结点
   17. 子孙结点：该结点的直接后继和间接后继
   18. 前辈：层号比某结点小的结点
   19. 后辈：层号比某结点大的结点
4. 树的抽象数据类型
   ```cpp
   ADT Tree{
      数据对象：一个集合D，该集合中的所有元素具有相同的特性
      结构关系：若D为空集，则为空树；若D中仅含有一个元素，则关系R为空树，否则R={H}，H是如下的二元关系
         在D中存在唯一的称为根的数据元素root，它在关系H下没有前驱
         除root外，D中每个节点在关系H下都有且仅有一个前驱
      基本操作：
         // 将Tree初始化为一棵空树
         InitTree(Tree);
         // 销毁树Tree
         DestroyTree(Tree);
         // 创建树Tree
         CreateTree(Tree);
         // 判空
         TreeEmpty(Tree);
         // 返回树Tree的根
         Root(Tree);
         // 若x为非根结点，返回他的双亲，否则返回空
         Parent(Tree, x);
         // 若x为非叶子结点，返回他的第一个孩子结点，否则返回空，
         FirstChild(Tree, x);
         // 若x不是其双亲的最后一个孩子结点，则返回其下一个兄弟结点，否则返回空
         NextSibling(Tree, x);
         // 将child插入Tree中，作为p所指向结点的子树
         InsertChild(Tree, p, child);
         // 删除Tree中p所指向结点的第i棵子树
         DeleteChild(Tree, p, i);
         // 按照某种次序，对Tree每个结点调用Visit函数访问一次且最多访问一次，若Visit失败则操作失败
         TraverseTree(Tree, Visit());
   }ADT Tree;
   ```

## 6.2 二叉树

### 6.2.1 二叉树的定义与基本操作

二叉树（binary tree）【位置二元有序树】：
- 每个结点的度都不大于2
- 每个节点的孩子结点次序不能任意颠倒

二叉树的基本操作：
```cpp
// 将bt初始化为空二叉树
InitBiTree(bt);
// 创建一棵非空二叉树bt
CreateBiTree(bt);
// 销毁二叉树bt
DestroyBiTree(bt);
// 判空
Empty(bt);
// 求二叉树bt的根结点，若二叉树bt为空二叉树，返回NULL
Root(bt);
// 求二叉树bt中结点x的双亲结点，若结点x是二叉树的根结点或二叉树bt中无结点x，返回NULL
Parent(bt, x);
// 求二叉树bt中结点x的左孩子，若结点x无左孩子或x不在bt中，返回NULL
LeftChild(bt, x);
// 求二叉树bt中结点x的右孩子，若结点x无右孩子或x不在bt中，返回NULL
RightChild(bt, x);
// 按某个次序依次访问二叉树bt中每个节点一次且仅一次
Traverse(bt);
// 将二叉树bt置为空树
Clear(bt);
```

### 6.2.2 二叉树的性质

1. 在二叉树的第i层上至多有2<sup>i-1</sup>个结点（i>=1）
2. 深度为k的二叉树至多有2<sup>k</sup>-1个结点（k>=1）
3. 对任意一棵二叉树T，若终端结点数为n<sub>0</sub>，而其度数为2的结点数为n<sub>2</sub>，则n<sub>0</sub>=n<sub>2</sub>+1
   1. 满二叉树：深度为k，且有2<sup>k</sup>-1个结点的二叉树。
   2. 满二叉树的顺序表示：从二叉树的根开始，按层间从上到下，层内从左到右的顺序逐层进行编号（1，2，...，n）
   3. 完全二叉树：深度为k，结点数为n的二叉树，如果其结点`1~n`的位置序号分别与等高的满二叉树的结点`1~n`的位置序号一一对应，则为完全二叉树。
      1. 叶子结点只可能出现在 最后两层
      2. 度为1的结点个数为0或1
4. 具有n个结点的完全二叉树的深度为$[log_2 n]+1$
5. 对于具有n个结点的完全二叉树，如果按照从上到下、从左到右的顺序对二叉树中的所有结点从1考试顺序编号，则对任意序号i的结点有：
   1. 如果i=1，则序号为i的结点是根结点，无双亲结点；如i>1，则序号为i的结点的双亲结点序号为$[i/2]$
   2. 如果2i>n，则序号为i的结点无左孩子；如2i<=n，则序号为i的结点的左孩子结点的序号为2i
   3. 如果2i+1>n，则序号为i的结点无右孩子；如2i+1<=n，则序号为i的结点的右孩子结点的序号为2i+1

### 6.2.3 二叉树的存储结构

1. 顺序存储结构
2. 链式存储结构
   1. 二叉链表
      ```cpp
      typedef struct Node{
         DataType data;
         struct Node* LChild;
         struct Node* RChild;
      }BiTNode, *BiTree;
      // 若一个二叉树含有n个结点，则其二叉链表中必含有2n个指针域，其中必有n+1个空的指针域
      ```
   2. 三叉链表
      ```cpp
      typedef struct Node{
         DataType data;
         struct Node* Parent;
         struct Node* LChild;
         struct Node* RChild;
      }BiTNode, *BiTree;
      ```

## 6.3 二叉树的遍历与线索化

### 6.3.1 二叉树的遍历

根据对根访问先后顺序不同，分别称DLR为先序遍历或先根遍历，LDR为中序遍历（对称遍历），LRD为后序遍历

先序、中序、后序遍历时递归定义的，即在其子树中仍按上述规律进行遍历

【A6.1 先序遍历二叉树】
```cpp
void PreOrder(BiTree root){
   // 先序遍历二叉树，root为某二叉树或子树根结点的指针
   if (root != NULL){
      Visit(root->data);
      PreOrder(root->LChild);
      PreOrder(root->RChild);
   }
}
```

【A6.2 中序遍历二叉树】
```cpp
void InOrder(BiTree root){
   // 中序遍历二叉树，root为某二叉树或子树根结点的指针
   if(root != NULL){
      InOrder(root->LChild);
      Visit(root->data);
      InOrder(root->RChild);
   }
}
```

【A6.3 后序遍历二叉树】
```cpp
void PostOrder(BiTree root){
   // 后序遍历二叉树，root为某二叉树或子树根结点的指针
   if(root != NULL){
      PostOrder(root->LChild);
      PostOrder(root->RChild);
      Visit(root->data);
   }
}
```

### 6.3.2 遍历算法的应用

1. 输出二叉树中的结点
   【A6.4 先序遍历输出二叉树中的结点】
   ```cpp
   void PreOrder(BiTree root){
      // 先序遍历输出二叉树结点，root为某二叉树或子树根结点的指针
      if (root != NULL){
         print(root->data);
         PreOrder(root->LChild);
         PreOrder(root->RChild);
      }
   }
   ```
2. 输出二叉树中的叶子结点
   【A6.5 先序遍历输出二叉树中的叶子结点】
   ```cpp
   void PreOrder(BiTree root){
    // 先序遍历输出二叉树叶子结点，root为某二叉树或子树根结点的指针
      if (root != NULL){
         if (root->LChild==NULL && root->RChild==NULL)
            print(root->data);
         PreOrder(root->LChild);
         PreOrder(root->RChild);
      }
   }
   ```
3. 统计叶子结点的数目
   1. 方法一：遍历
      【A6.6(a) 后序遍历统计二叉树中的叶子结点数目】
      ```cpp
      void leaf(BiTree root){
         // leafCount为保存叶子节点数目的全局变量，调用之前初始化值为0
         if(root != NULL){
            leaf(root->LChild);
            leaf(root->RChild);
            if (root->LChild==NULL && root->RChild==NULL)
               leafCount++;
         }
      }
      ```
   2. 方法二：分治
      【A6.6(b) 后序遍历统计二叉树中的叶子结点数目】
      ```cpp
      int leaf(BiTree root){
         int leafCount;
         if(root == NULL)
            leafCount = 0;
         else if(root->LChild==NULL && root->RChild==NULL)
            leafCount = 1;
         else leafCount = leaf(root->LChild) + leaf(root->RChild);
         return leafCount;
      }
      ```
4. 建立二叉链表方式存储的二叉树
   【A6.7 用扩展的先序遍历序列创建二叉树】
   ```cpp
   CreateBiTree(BiTree *bt){
      char ch = getchar();
      if(ch=='.')*bt=NULL;
      else{
         *bt = (BiTree)malloc(sizeof(BiTNode));
         (*bt)->data = ch;
         CreateBiTree(&((*bt)->LChild));
         CreateBiTree(&((*bt)->RChild));
      }
   }
   ```
5. 求二叉树的高度：二叉树的高度（深度）为二叉树中结点层次的最大值，也可以视为其左右子树高度的最大值加一
   1. 分沿法
      1. 若bt为空，则高度为0
      2. 若bt非空，其高度应为其左右子树高度的最大值加一
      ```cpp
      int PostTreeDepth(BiTree bt){
         if(bt){
            int hl = PostTreeDepth(bt->LChild);
            int rl = PostTreeDepth(bt->RChild);
            return (hl > rl ? hl : rl) + 1;
         }else{
            return 0;
         }
      }
      ```
   2. 先序遍历
      1. 先序遍历，求二叉树bt高度的遍历算法，h为bt指向结点所在的层次，初值为1
      2. depth为当前求得的最大层次，为全局变量，初值为0
      ```cpp
      PreTreeDepth(BiTree bt, int h){
         if(bt){
            if(h>depth)depth = h;
            PreTreeDepth(bt->LChild,h+1);
            PreTreeDepth(bt->RChild,h+1);
         }
      }
      ```
6. 按横向树形显示二叉树
   ```cpp
   PrintTree(BiTree bt, int nLayer){
      if(bt){
         PrintTree(bt->RChild, nLayer+1);
         for(int i = 0; i < nLayer; i++)printf(" ");
         printf("%c\n", bt->data);
         PrintTree(bt->LChild, nLayer+1);
      }
   }
   ```

### 6.3.3 基于栈的递归消除

1. 中序遍历二叉树的非递归算法
   【A6.11(a) 中序遍历二叉树的非递归算法（goto实现（略））】
   【A6.11(a) 中序遍历二叉树的非递归算法（直接实现栈操作（略））】
   【A6.11(a) 中序遍历二叉树的非递归算法（调用栈操作的函数）】
   ```cpp
   // 从根结点开始,只要当前结点存在或栈不空,则重复下面操作。
   // ①如果当前结点存在,则进栈并遍历左子树。
   // ②否则退栈并访问,然后遍历右子树。
   InOrder(BiTree root){
      InitStack(&S);
      p = root;
      while(p != NULL || !IsEmpty(S)){
         if(p != NULL){
            Push(&S, p);//根指针进栈
            p = p->LChild;//遍历左子树
         }else{
            Pop(&S, &p);//根指针退栈
            Visit(p->data);//访问根结点
            p = p->RChild;//遍历右子树
         }
      }
   }
   ```
2. 先序遍历二叉树的非递归算法
   ```cpp
   PreOrder(BiTree root){
      InitStack(&S);
      p = root;
      while(p != NULL || !IsEmpty(S)){
         if(p != NULL){
            Visit(p->data);//访问根结点
            Push(&S, p);//根指针进栈
            p = p->LChild;//遍历左子树
         }else{
            Pop(&S, &p);//根指针退栈
            p = p->RChild;//遍历右子树
         }
      }
   }
   ```
3. 后序遍历二叉树的非递归算法
   ```cpp
   // 从根结点开始,只要当前结点存在或栈不空,则重复下面操作。
   // ①从当前结点开始,进栈并遍历左子树,直到左子树为空。
   // ②如果栈顶结点的右子树为空,或栈顶结点的右孩子为刚访问过的结点,则退栈并访问,然后将当前结点指针置为空。
   // ③否则,遍历右子树。
   void PostOrder(BiTree root){
      BiTNode *p=root, *q=NULL;
      Stack S;
      InitStack(&S);
      while(p!=NULL || !IsEmpty(S)){
         if(p != NULL){
            Push(&S, p);
            p = p->LChild;//遍历左子树
         }else{
            GetTop(&S, &p);
            if(p->RChild == NULL || p->RChild == q){//栈顶结点的右子树为空,或栈顶结点的右孩子为刚访问过的结点
               Visit(p->data);//访问
               q = p;
               Pop(&S, &p);//退栈
               p = NULL;// 当前结点指针置为空。
            }else
               p = p->RChild;//遍历右子树。
         }
      }
   }
   ```

### 6.3.4 线索二叉树

1. 基本概念
   1. 若结点有左子树,则其 LChid 域指向其左孩子,否则 LChild 域指向其前驱结点;若结点有右子树,则其 RChild 域指向其右孩子,否则 RChild 域指向其后继结点。为了区分孩子结点和前驱、后继结点,可以为结点结构增设两个标志域 Ltag 和 Rtag(付出的空间代价)。
   2. 线索：指向前驱和后继结点的指针。
   3. 线索链表：以这种结构组成的二叉链表作为二叉树的存储结构。
   4. 线索化：对二叉树以某种次序进行遍历并且加上线索的过程。
   5. 线索二叉树：线索化了的二叉树。
2. 二叉树的线索化
   - 中序线索化采用中序递归遍历算法框架。
   - 加线索操作就是访问结点的操作。
   - 加线索操作需要利用刚访问过的结点与当前结点的关系,因此设置一个指针(pre始终记录刚访问过的结点)其操作如下：
     - 如果当前遍历结点 root 的左子域为空,则让左子域指向 pre
     - 如果前驱 pre 的右子域为空,则让右子域指向当前遍历结点 root。
     - 为下次做准备,当前访问结点 root 作为下一个访问结点的前驱 pre。
   【A6.13 建立中序线索树】
   ```cpp
   Inthread(BiTree root){
      // 对root所指的二叉树进行中序线索化，其中pre始终指向刚刚访问过的结点，其初值为NULL
      if (root != NULL){
         InThread(root->LChild); // 线索化左子树
         if (root->LChild == NULL){//置前驱线索
            root->LChild = pre;
            root->Ltag = 1;
         }
         if (root->RChild == NULL){//置后继线索
            root->RChild = root;
            root->Rtag = 1;
         }
         pre = root;
         InThread(root->RChild); // 线索化右子树
      }
   }
   ```
3. 在线索二叉树中寻找前驱、后继结点
   1. 在中序线索树中找前驱结点
      【A6.14 在中序线索树中找前驱结点】
      ```cpp
      BiTNode* InPre(BiTNode *p){
         // 在中序线索二叉树中查找p的前驱结点，并用pre指针返回结果
         if(p->Ltag==1)pre=p->LChild;
         else{
            // 在p的左子树中查找“最右下端”结点
            for(q=p->LChild; q->Rtag==0; q=q->RChild);
            pre = q;
         }
         return pre;
      }
      ```

   2. 在中序线索树中找后继结点
      【A6.15 在中序线索树中找后继结点】
      ```cpp
      BiTNode* InNext(BiTNode *p){
         // 在中序线索二叉树中查找p的前驱结点，并用Next指针返回结果
         if(p->Rrag==1)Next=p->RChild;
         else{
            // 在p的右子树中查找“最左下端”结点
            for (q=p->RChild; q->Ltag==0; q=q->LChild);
            Next = q;
         }
         return Next;
      }
      ```
4. 遍历中序线索树
   1. 在中序线索树中求中序遍历的第一个结点
      ```cpp
      BiTNode *InFirst(BiTree bt){
         if (bt)return NULL;
         while (bt->Ltag == 0)bt = bt->LChild;
         return bt;
      }
      ```
   2. 遍历中序二叉线索树
      ```cpp
      void TInOrder(BiTree bt){
         bt = InFirst(bt);
         while (bt){
            Visit(bt);
            bt = InNext(bt);
         }
      }
      ```

### 6.3.5 由遍历序列确定二叉树
根据遍历序列确定二叉树，至少需要知道两种遍历序列，且其中一种是中序遍历序列
```cpp
// 通过后序、中序遍历确定二叉树
BiTree createBinaryTreeByPostInOrder(int *post, int *in, int n){
   int i = 0, k = 0, root = 0;
   if (n == 0) //空树
      return NULL;
   BiTree T = (BiTree *)malloc(sizeof(BiTNode));
   root = post[n - 1]; //根节点就是后序遍历的最后一位
   T->data = root;
   for (i = 0; i < n; i++){
      if (in[i] == root){ //通过中序遍历，确定左右子树的长度
         k = i;
         break;
      }
   }
   T->LChild = createBinaryTreeByPostInOrder(post, in, k); //递归左右子树
   T->RChild = createBinaryTreeByPostInOrder(post + k, in + k + 1, n - k - 1);
   return T;
}
```

## 6.4 树、森林和二叉树的关系

### 6.4.1 树的存储结构
1. 双亲表示法：用一组连续的存储空间来存储树中的结点，在保存每个结点的同时附设一个指示器来指示其双亲的结点在表中的位置。
   ```cpp
   // 结点结构
   typedef struct TNode{
      DataType data;
      int parent;
   } TNode;
   // 树
   typedef struct{
      TNode tree[MAXSIZE];
      int r;
   } ParentTree;
   ```
2. 孩子（链表）表示法 -> 图的邻接表表示法
   ```cpp
   typedef struct ChildNode{   // 孩子结点的结构
      int child;              // 孩子结点在线性表中的位置
      struct ChildNode *next; // 指向下一个孩子结点的指针
   } ChildNode;
   typedef struct{            // 顺序表结点的结构
      DataType data;         // 数据域
      ChildNode *firstchild; // 指向第一个孩子结点的指针
   } DataNode;
   typedef struct{              // 树的定义
      DataNode nodes[MAXSIZE]; // 数据域（结点数组）
      int root;                // 根结点的位置，若约定nodes[0]为根结点，则可以省略该域
      int num;                 // 树中结点的个数
   } ChildTree;
   ```
3. 孩子兄弟表示法（★）：又称树的二叉链表表示法
   ```cpp
   typedef struct CSNode{// 存储结构定义
      DataType data;    // 数据域
      int FirstChild;   // 第一个孩子结点的位置（父子关系）
      int NextSibling;  // 下一个兄弟结点的位置（兄弟关系）
   } CSNode, *CSTree;
   /*访问结点x的第i个孩子
   1. 从FirstChild域找到第1个孩子结点n
   2. 沿着n的NextSibling域走i-1步
   */
   ```

### 6.4.2 树、森林与二叉树的相互转换
1. 树转换为二叉树（将一棵树转化为二叉树的方法）
   1. 树中所有相邻兄弟之间加一条连线
   2. 对树中每个结点，只保留其与第一个孩子结点之间的连线，删去其与其他孩子结点之间的连线
   3. 以树的根结点为轴心，将整棵树顺时针旋转一定角度，使之结构层次分明
2. 森林转换为二叉树
   1. 将森林中的每棵树转换成相应的二叉树
   2. 第一棵树不动，从第二棵二叉树开始，依次把后一棵二叉树的根结点在作为前一棵二叉树根结点的右孩子，将所有二叉树连在一起
3. 递归描述（将森林F看作树的有序集F={T1, T2, ..., Tn}， 他对应的二叉树为B(F)）
   1. 若n\=0，则B(F)为空
   2. 若n\>0，二叉树B(F)的根为森林中第一棵树T1的根；B(F)的左子树为B({T11, ..., T1m})，其中{T11, .., T1m}是T1的子树森林；B(F)的右子树是B({T2, ..., Tn})
4. 二叉树还原为树或森林
   1. 若某结点是其双亲的左孩子，则把该结点的右孩子、右孩子的右孩子......都与该结点的双亲结点用线连起来
   2. 删掉原来二叉树中所有双亲结点与右孩子结点的连线
   3. 整理使之层次分明
5. 4的递归描述（若B是一棵二叉树, T是B的根结点, L是B的左子树, R为B的右子树,且B对应的森林F(B)中含有的n棵树为T1, T2 , ..., Tn
   1. B为空, 则F(B)为空的森林(n=0)。
   2. B非空, 则 F(B)中第一棵树T1的根为二叉树B的根T; T1中根结点的子树森林由B的左子树L转换而成, 即F(L)={T11, ..., T1m}; B的右子树R转换为F(B)中其余树组成的森林, 即F(R)={T2, T3, ..., Tn}

### 6.4.3 树与森林的遍历

1. 树的遍历
   1. 先根遍历 => 转换后二叉树的先序遍历
      1. 访问根节点
      2. 从左到右，依次先根遍历根结点的每一棵子树
   2. 后根遍历 => 转换后二叉树的中序遍历
      1. 从左到右，依次后根遍历根结点的每一棵子树
      2. 访问根节点
2. 树的遍历算法实现
   ```cpp
   RootFirst(CSTree root){ // 法一
      if(root){
         Visit(root->data); // 访问根节点
         p = root->FirstChild;
         while(p){
            RootFirst(p); // 访问以p为根的子树
            p = p->NextSibling;
         }
      }
   }
   RootFirst(CSTree root){ // 法二
      if (root)
      {
         Visit(root->data);       // 访问根节点
         RootFirst(root->lchild); // 先根遍历首子树
         RootFirst(root->rchild); // 先根遍历兄弟树
      }
   }
   RootLast(CSTree root){
      if(root){
         RootLast(root->FirstChild); // 后根遍历首子树
         Visit(root->data);          // 访问根节点
         RootLast(root->NextSibling); // 后根遍历兄弟树
      }
   }
   ```
3. 森林的遍历
   1. 先序遍历（若森林非空,则遍历方法为）
      1. 访问森林中第一棵树的根结点；
      2. 先序遍历第一棵树的根结点的子树森林;
      3. 先序遍历除去第一棵树之后剩余的树构成的森林。
   2. 中序遍历（若森林非空,则遍历方法为）
      1. 中序遍历森林中第一棵树的根结点的子树森林；
      2. 访问第一棵树的根结点；
      3. 中序遍历除去第一棵树之后剩余的树构成的森林。
   3. 后序遍历（若森林非空,则遍历方法为）
      1. 后序遍历森林中第一棵树的根结点的子树森林；
      2. 后序遍历除去第一棵树之后剩余的树构成的森林；
      3. 访问第一棵树的根结点。
4. 求树的高度
   ```cpp
   Depth(CSTree root, int h){
      if(root){
         if(depth < h)
               depth = h;
         Depth(root->FirstChild, h+1);
         Depth(root->NextSibling, h);
      }
   }
   ```
5. 树的层序遍历

## 6.5 哈夫曼树及其应用

### 6.5.1 哈夫曼树
1. 哈夫曼树的基本概念
   1. 路径：从一个结点到另一个结点的分支序列
   2. 路径长度：一个结点到另一个结点所经过的分支数目
   3. 树的路径长度：从根结点到每个结点的路径长度之和
   4. 结点的权：赋予结点的一个具有某种实际意义的实数
   5. 带权路径长度：从树根到某一结点的路径长度与该结点的权的乘积
   6. 树的带权路径长度：树中从根到每个叶子结点的带权路径长度之和，通常记作 $WPL=\sum_{i=1}^n w_i * l_i$ 其中，n为叶子结点的个数， w<sub>i</sub>为第i个叶子结点的权值，l<sub>i</sub>为第i个叶子结点的路径长度
   7. 哈夫曼树：由n个带权节点组成的所有二叉树中带权路径长度最短的二叉树，又称为最优二叉树，
2. 构建哈夫曼树
   1. 初始化：用给定的n个权值{w1,w2,...,wn}构建n棵二叉树并构成森林F={T1,T2,...,Tn}，其中每一二叉树Ti(1<=i<=n)都只有一个权值为wi的根结点，其左右子树结点为空。
   2. 找最小树：在森林F中选择两棵根结点权值最小的二叉树Ti1和Ti2
   3. 删除与加入：构造一棵新的二叉树T(i+1)，其左右子树分别为Ti1和Ti2，其根结点的权值为Ti1和Ti2的根结点的权值之和，然后将Ti1和Ti2从森林F中删除。
   4. 重复2-4，直到森林F中只剩一棵树为止。此时得到的这颗二叉树就是哈夫曼树。
3. 哈夫曼树的类型定义
   1. 存储结构
   2. 哈夫曼树的类型定义
      ```cpp
      #define N 20 // 叶子结点的最大值
      #define M 2*N-1 // 所有结点的最大值
      typedef struct {
         int weight; // 权值
         int parent, lchild, rchild; // 双亲结点，左孩子，右孩子
      } HTNode, HuffmanTree[M+1]; // HuffmanTree是一个结构体数组，0号单元不用
      ```
4. 哈夫曼树的算法实现
   ```cpp
   【A6.18 构建哈夫曼树】
   HuffmanTree_Create(HuffmanTree ht, int w[], int n){
      // 构建哈夫曼树ht[M+1]， w[]是权值数组，n是数组的长度
      int m = 2 * n - 1, s1, s2;          //哈夫曼树的结点数
      for (int i = 1; i < n; i++) // 初始化叶子结点，1-n号单元
         ht[i] = (HTNode){w[i], 0, 0, 0};
      for (int i = n + 1; i <= m; i++) // 初始化非叶子结点，n+1-m号单元
         ht[i] = (HTNode){0, 0, 0, 0};
      // 初始化叶子结点后，构造哈夫曼树
      for (int i = n+1; i < m; i++){
         // 找出最小的两个结点
         select(ht, i-1, &s1, &s2);
         ht[i].weight = ht[s1].weight + ht[s2].weight;
         ht[s1].parent = i;ht[s2].parent = i;
         ht[i].lchild = s1;ht[i].rchild = s2;
      }
   }
   ```

### 6.5.2 哈夫曼编码
1. 概念
   1. 前缀编码：任何一个字符的编码都不能是其他字符编码的前缀的编码系统中的编码
   2. 哈夫曼编码：对一棵具有n个叶子结点的哈夫曼树，若对树中的每个左分支赋予1，右分支赋予0（可以互换），则从根结点到每个叶子结点的通路上，各分支的赋值分别构成一个二进制串。
   3. 定理6.1：哈夫曼编码是前缀编码
   4. 定理6.2：哈夫曼编码是最优前缀编码
2. 应用
3. 算法实现
   ```cpp
   typedef char *HuffmanCode[N + 1]; //存储哈夫曼编码串的头指针数组
   // 【A6.19 求哈夫曼树的哈夫曼编码】
   CrtHuffmanCode(HuffmanTree ht, HuffmanCode hc, int n){
      // 从叶子结点到根，逆向求每个叶子结点对应的哈夫曼编码
      char *cd = (char *)malloc(sizeof(char) * n); //分配求当前编码的空间
      cd[n - 1] = '\0';                            //从右向左逐位存放编码，首先存放编码串的结束符
      for (int i = 1; i <= n; i++){
         int start = n - 1;           //编码串的起始指针
         int c = i, p = ht[i].parent; //当前结点
         while (p){                    // 当前结点不是根结点
            cd[--start] = ht[p].lchild == c ? '1' : '0'; //左1，右0
            c = p;
            p = ht[p].parent; // 向上查找
         }
         hc[i] = (char *)malloc(sizeof(char) * (n - start)); //分配第i个编码串的空间
         strcpy(hc[i], &cd[start]);                          //将编码复制到hc[i]中
      }
   }
   ```

## 6.6 并查集

### 6.6.1 并查集定义
并查集：
1. 确定一个元素所在的子集：任给一个结点，只需沿着父指针找到根结点，就可以确定所在的子集
2. 合并两个子集：只要让一棵子树的根指向另外一棵子树的根，即可实现两个子集的并操作。

```cpp
ADT MFSet{
   数据对象：假设集合S有n个元素，每个元素属于同一个数据对象。
      S0, S1, ..., Sm-1是m个互不相交的子集，
      SS是以S0, S1, ..., Sm-1为元素构成的集合。
   数据关系：S0∪S1∪...∪Sm-1=S, S0∩S1∩...∩Sm-1=∅, Si包含于S， Si包含于SS。
   基本操作：
   // 用S中的n个元素构造n个单元素集合，再以这n个单元素集合为元素生成集合SS
   Initial(SS, S)
   // 确定x属于SS中哪个集合
   Find(SS, x)
   // 将第j个集合并入第i个集合
   Merge(SS, i, j)
}ADT MFSet;
```

### 6.6.2 并查集存储与基本操作实现
【A6.20 初始化并查集O(集合S中元素数目n)】
```cpp
void Initial(MFSet *SS, SeqList *S){
   // 用S中的n个元素构建n个单根树，代表n个单元素集合S0，S1，...，Sn-1,，这n个单根树构成一个森林，代表并查集SS
   SS->nodenum = S->last+1;
   for(int i = 0; i < SS->nodenum; i++){
      SS->tree[i].data = S->elem[i];
      SS->tree[i].parent = -1;
   }
}
```
【A6.21(a) 在并查集中查找某个元素O(x所在子集树的高度h)】
```cpp
int Find_1(MFSet *SS, DataType x){
   // 确定x属于并查集SS中哪个集合。如果不属于SS中任何一个子集则返回-1，否则返回所在子集树的根结点下标
   pos = Locate(SS, x); //确定x在SS->tree[]中的下标
   if(pos < 0) return -1; // 如果x不属于SS中任一子集，返回-1
   i = pos; // 从pos开始，沿双亲指针查找根结点
   while(SS->tree[i].parent > 0)
      i = SS->tree[i].parent;
   return i; //返回子集树的根结点下标
}
```
【A6.22(a) 合并并查集中的子集树O(1)】
```cpp
int Merge_1(MFSet *SS, int root1, int root2){
   // root1和root2是并查集SS中两个互不相交的非空子集树的根，将子集树root2并入子集树root1
   if(root1 < 0 || root1 > SS->nodenum-1) return ERROR;
   if(root2 < 0 || root2 > SS->nodenum-1) return ERROR;
   SS->tree[root2].parent = root1;
   return OK;
}
```
【A6.22(b) 合并并查集中的子集树（改进算法）】
```cpp
int Merge_2(MFSet *SS, int root1, int root2){
   // root1和root2是并查集SS中两个互不相交的非空子集树的根，根结点parent域存放树中结点数目的负值（绝对值越大数目越大，值越小）。本算法将结点数目少的子集树并入结点数目多的子集树
   if(root1 < 0 || root1 > SS->nodenum-1) return ERROR;
   if(root2 < 0 || root2 > SS->nodenum-1) return ERROR;
   if(SS->tree[root1].parent < SS->tree[root2].parent){// 第一棵子集树中结点数目较多。
      SS->tree[root2].parent = root1;
      SS->tree[root1].parent += SS->tree[root2].parent;
   }else{// 第二棵子集树中结点数目较多。
      SS->tree[root1].parent = root2;
      SS->tree[root2].parent += SS->tree[root1].parent;
   }
   return OK;
}
```
【A6.21(b) 在并查集中查找某个元素（改进算法）】
```cpp
int Find_2(MFSet *SS, DataType x){
   // 确定x属于并查集SS中哪个集合，同时调整子集树，降低其高度。如果不属于SS中任何一个子集则返回-1，否则首先找到x所在子集树的根root，然后将x及x的所有祖先（除了root）均改为root的子结点，最后返回root
   pos = Locate(SS, x); //确定x在SS->tree[]中的下标
   if(pos < 0) return -1; // 如果x不属于SS中任一子集，返回-1
   i = pos; // 从pos开始，沿双亲指针查找根结点
   while(SS->tree[i].parent > 0)
      i = SS->tree[i].parent;
   root = i; // 记录x所在子集树的根结点下标
   i = pos; // 从pos开始，将x及x的所有祖先（除了root）均改为root的子结点
   while(i != root){
      temp = SS->tree[i].parent;
      SS->tree[i].parent = root;
      i = temp;
   }
   return root; // 返回x所在子集树的根结点下标
}
```

### 6.6.3 应用实例：等价类划分
···

## 6.7 总结与提高

1. 二叉树的相似性判断
   1. 若二叉树1与二叉树2均为空树，返回相似
   2. 否则，若二叉树1和二叉树2其中之一为空树，返回不相似
   3. 否则，返回（二叉树1的左子树和二叉树2的左子树是否相似）与（二叉树1的右子树和二叉树2的右子树是否相似）
2. 求二叉树根结点到r结点之间的路径
   ```cpp
   // 求二叉树根结点到r结点之间的路径，并输出。使用非递归后序遍历
   void path(BiTree root, BiTNode *r){
      if(root == NULL || r == NULL)return;
      BiTNode *p = root, *q = NULL;
      BiTNode *stack[MAXSIZE];
      int top = 0;
      while(p != NULL || top != 0){
         while(p != NULL){
            // 栈满处理
            stack[++top] = p;
            p = p->lchild; // 遍历左子树
         }
         if (top > 0){// 栈不空
            p = stack[top];
            if (p->rchild == NULL || p->rchild == q){
               if (p == r){// 到达r结点
                  for(int i = 1; i <= top; i++)
                     printf("%d", stack[i]->data);
                  return;
               }else{
                  q = p; // 用q保存刚刚访问过的结点
                  top--;
                  p = NULL; // 跳过前面左遍历，继续推栈
               }
            }else p = p->rchild; // 遍历右子树
         }
      }
   }
   ```
3. 层序遍历二叉树
   1. 初始化空队列Q
   2. 若二叉树bt为空树，则直接返回
   3. 将二叉树的根结点指针bt放入队列Q
   4. 若队列非空，重复如下操作：
      1. 队头元素出队并访问该元素
      2. 若该结点的左孩子不为空，则将其左孩子指针放入队列Q
      3. 若该结点的右孩子不为空，则将其右孩子指针放入队列Q
   ```cpp
   int LayerOrder(BiTree bt){
      SeqQueue Q;
      BiTree p;
      InitQueue(&Q); // 初始化空队列Q
      if(bt == NULL)        return 0; // 若二叉树bt为空树，则直接返回
      EnterQueue(&Q, bt); // 二叉树的根结点指针bt入队，开始层序遍历
      while(!isEmpty(Q)){
         DeleteQueue(&Q, &p); // 队头元素出队并访问该元素
         Visit(p->data);
         if(p->lchild != NULL)  EnterQueue(&Q, p->lchild); // 若该结点的左孩子不为空，则将其左孩子指针放入队列Q
         if(p->rchild != NULL)  EnterQueue(&Q, p->rchild); // 若该结点的右孩子不为空，则将其右孩子指针放入队列Q
      }
      return 1;
   }
   ```


# 第七章 图

## 7.1 图的定义与基本术语

### 7.1.1 图的定义
（略，仅给出抽象数据类型定义）
```cpp
ADT Graph{
   数据对象 V：一个非空集合，该集合中所有的元素具有相同的特性
   数据关系 R：R={VR={<x, y>| P(x, y)且(x, y)∈V}}
   基本操作：
      // 创建图
      CreateGraph(G);
      // 销毁图
      DestroyGraph(G);
      // 若图中存在顶点v，则函数返回值为顶点v在图G中的位置，否则返回值为“空”
      LocateVertex(G, v);
      // 返回图中第i个顶点的值，若i大于图中顶点数，则返回“空”
      GetValue(G, i);
      // 返回图中顶点v的第一个邻接顶点的位置，若v不在图中或没有邻接顶点，则返回“空”
      FirstAdjVertex(G, v);
      // 返回图中顶点v的下一个邻接顶点的位置，若v不在图中或没有下一个邻接顶点，则返回“空”
      NextAdjVertex(G, v);
      // 在图中增加一个顶点u
      InsertVertex(G, u);
      // 删除图中的顶点v及与顶点v相关联的弧
      DeleteVertex(G, v);
      // 在图中增加一条从顶点v到顶点w的弧<v, w>
      InsertArc(G, v, w);
      // 删除图中从顶点v到顶点w的弧<v, w>
      DeleteArc(G, v, w);
      // 按照某种次序，对图中的每个顶点访问一次且仅访问一次
      TraverseGraph(G, visit);
}ADT Graph;
```

### 7.1.2 基本术语
（详见离散数学）
1. 完全图、稀疏图、稠密图
2. 子图
3. 邻接点
4. 度、入度、出度
5. 权与网
6. 路径与回路
7. 连通图、连通分量

## 7.2 图的存储结构

### 7.2.1 邻接矩阵（数组）表示法
```cpp
#define MAX_VERTEX_NUM 20 /*最多顶点个数*/
#define INFINITY 32768 /*无穷*/
/*图的种类：DG表示有向图、DN表示有向网、UDG表示无向图、UDN表示无向网*/
typedef enum{DG, DN, UDG, UDN} GraphKind;
typedef char VertexData;
typedef struct ArcNode{
   AdjType adj; //对于无权图，用1或0表示是否相邻；对于带权图，则为权值类型
   OtherInfo info;
} ArcNode;
typedef struct {
   VertexData vertex[MAX_VERTEX_NUM]; //顶点向量
   ArcNode arcs[MAX_VERTEX_NUM][MAX_VERTEX_NUM]; //邻接矩阵
   int vexnum, arcnum; //图的顶点数和弧数
   GraphKind kind; //图的种类标志
} AdjMatrix;
```
1. 存储空间
   无向图的邻接矩阵是对称矩阵，可以采用特殊矩阵的压缩存储法
2. 运算
   【A7.1 用邻接矩阵表示法创建有向网】
   ```cpp
   int LocateVertex(AdjMatrix *G, VertexData v) {
      int j = Error, k;
      for(k = 0; k < G->vexnum; k++) {
         if(G->vertex[k] == v) {
            j = k; break;
         }
      }
      return j;
   }
   int CreateDN(AdjMatrix *G) {
      int i, j, k, weight;
      VertexData v1, v2;
      scanf("%d,%d", &G->vexnum, &G->arcnum);
      for(i = 0; i < G->vexnum; i++)
         for(j = 0; j < G->vexnum; j++)
            G->arcs[i][j].adj = INFINITY;
      for(i = 0; i < G->vexnum; i++)
         scanf("%c", &G->vertex[i]);
      for(k = 0; k < G->arcnum; k++){
         scanf("%c,%c,%d", &v1, &v2, &weight);
         i = LocateVertex(G, v1);
         j = LocateVertex(G, v2);
         G->arcs[i][j].adj = weight;
      }
      G->kind = DN;
      return 1;
   }
   ```

### 7.2.2 邻接表
表头结点表：数据域vexdata、链域firstarc  
边表：邻接点域adjvex、链域nextarc、数据域info
```cpp
typedef struct ArcNode{
   int adjvex; //该边、弧指向顶点的位置
   struct ArcNode *nextarc; //指向下一条边、弧的指针
   OtherInfo info; //与该边、弧相关的信息
}ArcNode; //边结点
typedef struct VertexNode{
   VertexData data; //顶点数据
   ArcNode *firstarc; //指向该顶点第一条边、弧的指针
}VertexNode; //表头结点
typedef struct{
   VertexNode vertex[MAX_VERTEX_NUM];
   int vexnum, arcnum; //图的顶点数和边、弧数
   GraphKind kind; //图的种类标识
}AdjList;
```
1. 存储空间
2. 无向图的度：顶点i的度恰好为第i个单链表上结点的个数
3. 有向图的度：有向图中第i个单链表上结点的个数仅为顶点i的出度，要求入度须遍历整个邻接表，在所有边表中查找邻接点域值为i的结点并计数。法二：逆邻接表，存储两份边表，邻接表计算出度，逆邻接表计算入度。

### 7.2.3 十字链表（有向图）
```cpp
typedef struct ArcNode{
   int tailvex, headvex;
   struct ArcNode *hlink, *tlink;
}ArcNode; //弧结点
typedef struct VertexNode{
   VertexData data; //顶点信息
   ArcNode *firstin, *firstout;
}VertexNode; //顶点结点
typedef struct{
   VertexNode vertex[MAX_VERTEX_NUM];
   int vexnum, arcnum; //图的顶点数和弧数
   GraphKind kind; //图的种类
}OrthList; //图的十字链表表示法
```
【A7.2 创建图的十字链表】
```cpp
void CrtOrthList(OrthList *g){
   scanf("%d,%d", &n, &e); //顶点个数和弧的个数
   g->vexnum = n;
   g->arcnum = e;
   for(i = 0; i < n; i++){
      scanf("%c", &(g->vertex[i].data));
      g->vertex[i].firstin = NULL;
      g->vertex[i].firstout = NULL;
   }
   for(k = 0; k < e; k++){
      scanf("%c,%c", &vt, &vh);
      i = LocateVertex(G, vt);
      j = LocateVertex(G, vh);
      p = (ArcNode *)malloc(sizeof(ArcNode));
      p->tailvex = i; p->headvex = j;
      p->tlink = g->vertex[i].firstout;
      g->vertex[i].firstout = p;
      p->hlink = g->vertex[j].firstin;
      g->vertex[j].firstin = p;
   }
}
```

### 7.2.4 临界多重表（无向图）
```cpp
typedef struct EdgeNode{
   int mark, ivex, jvex;
   struct EdgeNode *ilink, *jlink;
}EdgeNode; //边结点
typedef struct{
   VertexData data;
   EdgeNode *firstedge;
}VertexNode; //顶点结点
typedef struct{
   VertexNode vertex[MAX_VERTEX_NUM];
   int vexnum, arcnum; //图的顶点数和弧数
   GraphKind kind; //图的种类
}AdjMultiList; //临界多重表表示法
```

## 7.3 图的遍历

访问标志数组visited\[n\]，用于标示图中每个顶点是否被访问过。

### 7.3.1 深度优先搜索

深度优先搜索（depth-first search, DFS）是按照深度方向搜索，类似于树的先根遍历，是树的先根遍历的推广。

基本思想：
1. 从图中某个顶点v0出发，首先访问v0。
2. 找出刚访问过的顶点的第一个未被访问的邻接点，然后访问该邻接点。以该邻接点为顶点重复此步骤，直到刚访问过的顶点没有未被访问的邻接点为止。（访问方向使用实线箭头表示）
3. 返回前一个访问过且仍有未被访问的邻接点的顶点，找出该顶点的下一个未被访问的邻接点并访问，然后执行步骤2。（回溯方向使用虚线箭头表示）

深度优先搜索树：所有顶点加上标有实线箭头的边，构成一棵以第一个访问节点为根的树。

【A7.3 深度优先遍历图g】
```cpp
int visited[MAX_VERTEX_NUM]; //访问标志数组
void TraverseGraph(Graph g){
   for(vi = 0; vi < g.vexnum; vi++)
      visited[vi] = 0; //初始化访问标志数组
   for(vi = 0; vi < g.vexnum; vi++)
      if(!visited[vi]) DepthFirstSearch(g, vi);
}
```
【A7.4 深度优先遍历v0所在的连通子图】
```cpp
void DepthFirstSearch(Graph g, int v0){
   Visit(v0); visited[v0] = 1;
   w = FirstAdjVertex(g, v0);
   while(w != -1){// 邻接点存在
      if(!visited[w]) DepthFirstSearch(g, w);
      w = NextAdjVertex(g, v0, w); //找下一个邻接点
   }
}
```
【A7.5 采用邻接矩阵的DepthFirstSearch】
```cpp
void DepthFirstSearch(AdjMatrix g, int v0){
   Visit(v0); visited[v0] = 1;
   for(vj = 0; vj < g.vexnum; vj++)
      if(!visited[vj] && g.arcs[v0][vj].adj)
         DepthFirstSearch(g, vj);
}
```
【A7.6 采用邻接表的DepthFirstSearch】
```cpp
void DepthFirstSearch(AdjList g, int v0){
   Visit(v0); visited[v0] = 1;
   p = g.vertex[v0].firstarc;
   while(p != NULL){
      if(!visited[p->adjvex])
         DepthFirstSearch(g, p->adjvex);
      p = p->nextarc;
   }
}
```
【A7.7 非递归形式的DepthFirstSearch】
```cpp
void DepthFirstSearch(Graph g, int v0){
   InitStack(&S);
   Push(&S, v0);
   while(!isEmpty(S)){
      Pop(&S, &v);
      if(!visited[v]){
         Visit(v); visited[v] = 1;
         w = FirstAdjVertex(g, v);
         while(w != -1){
            if(!visited[w]) Push(&S, w);
            w = NextAdjVertex(g, v, w);
         }
      }
   }
}
```

### 7.3.2 广度优先搜索

广度优先搜索（breadth-first search, BFS）是按照广度方向搜索，类似于树的层次遍历，是树的层次遍历的推广。

基本思想：
1. 从图中某个顶点v0出发，首先访问v0。
2. 依次访问v0的各个未被访问的邻接点。
3. 分别从这些邻接点（端结点）出发，依次访问他们的各个未被访问的邻接点（新的端结点）。访问时应保证：如果vi和vk为当前端结点，且vi在vk之前被访问，则vi的所有未被访问的邻接点应在vk的所有未被访问的邻接点之前访问。
4. 重复3，直到所有端结点均没有未被访问的邻接点为止。若此时还有顶点未被访问，则选一个未被访问的顶点作为起始点，重复上述过程，直至所有顶点均被访问过为止。

广度优先搜索树：所有顶点加上标有箭头的边，构成一棵以第一个访问节点为根的树。

【A7.8 广度优先搜索图g中v0所在的连通子图】
```cpp
void BreadthFirstSearch(Graph g, int v0){
   Visit(v0); visited[v0] = 1;
   InitQueue(&Q);
   EnterQueue(&Q, v0);
   while(!isEmpty(Q)){
      DeleteQueue(&Q, &v);
      w = FirstAdjVertex(g, v);
      while(w != -1){
         if(!visited[w]){
            Visit(w); visited[w] = 1;
            EnterQueue(&Q, w);
         }
         w = NextAdjVertex(g, v, w);
      }
   }
}
```

## 7.4 图的应用

### 7.4.1 图的连通性问题

1. 无向图的连通分量：可以利用利用图的遍历过程来判断一个图是否连通。如果在遍历的过程中不止一次调用搜索过程，则说明该图就是一个非连通图。调用搜索过程几次，就表明该图有几个连通分量
2. 图中两个顶点之间的简单路径
   【A7.9 深度优先找出从顶点u到顶点v的简单路径】
   ```cpp
   int pre[MAX_VERTEX_NUM] = {-1};
   void Path(Graph g, int u, int v){
      pre[u] = u;
      DFS(G, u, v);
   }
   void DFS(Graph g, int u, int v){
      if(u == v){
         print_path(pre, v); return;
      }
      w = FirstAdjVertex(g, u);
      while(w != -1){
         if(!visited[w]){
            pre[w] = u; DFS(g, w, v);
         }
         w = NextAdjVertex(g, u, w);
      }
   }
   ```
3. 图的生成树与最小生成树
   1. 生成树：一棵有N个顶点的生成树，有且仅有N-1条边，如果他多于N-1条边则一定有回路，但是有N-1条边的图并非一定连通，不一定存在生成树，如果一个图有N个顶点且边数小于N-1条，则该图一定是非连通图。
   2. 最小生成树：在一个连通图的所有生成树中，各边代价之和最小的那棵生成树称为该连通图的最小代价生成树，简称最小生成树（minimal spanning tree MST）性质：设N={V, {E}}是一个连通图，U是顶点集V的一个非空子集。若(u, v)是一条具有最小权值的边，其中u∈U，v∈V-U，则存在一棵包含边(u, v)的最小生成树。
   3. 普利姆算法【加点法】：假设N=(V, {E})是连通图，TE为最小生成树中边的集合。
      1. 算法
         1. 初始U={u<sub>0</sub>}(u<sub>0</sub>∈V),TE=Ø。
         2. 在所有u∈U，v∈V-U的边中，选一条代价最小的边(u, v)并入集合TE，同时将v并入U。
         3. 重复2，直到U=V为止。
      2. 此时，TE中必含有n-1条边，则T={V, {TE}}为N的最小生成树。
      3. 注意：选择最小边时，条件是边的一个顶点属于U而另一个顶点不属于U，即保证加点不构成回路。在有多条同样权值的边可选时，可任选其一。
      4. 辅助数组：closedge\[\]，对于每个顶点v∈V-U，closedge\[v\]记录所有与v邻接的，从U到V-U的那组边中的最小边信息。closedge\[v\]包含两个域：adjvex记录最小边在U中的那个顶点；lowcost存储最小边的权值。`closedge[v].lowcost = Min({cost(u, v)|u∈U})`
      5. 思想：
         1. 首先将初始顶点u加入到U中，对其余的每一个顶点i，将closedge\[i\]均初始化为i到u的边信息。
         2. 循环n-1次，做如下处理：
            1. 从各组最小边closedge\[\]中选出最小的最小边closedge\[v\](v∈V-U)。
            2. 将v加入U中。
            3. 更新剩余的每组最小边信息closedge\[i\](i∈V-U)。对于以i为中心的那组边，新增加了一条从v到i的边，如果新边的权值比closedge\[i\].lowcost小，则将closedge\[i\].lowcost更新为新边的权值
      6. 【A7.10 普里姆算法】
         ```cpp
         struct {
            int adjvex;
            int lowcost;
         } closedge[MAX_VERTEX_NUM+1]; //求最小生成树时的辅助数组，0号单元不用
         MiniSpanTree_Prim(AdjMatrix gn, int u){
            //从顶点u出发，按普利姆算法构造连通网gn的最小生成树，并输出生成树的每条边
            closedge[u].lowcost = 0; //初始化，U={u}
            for(i = 1; i <= gn.vexnum; i++)
               if(i != u){ //对V-U中的顶点i，初始化closedge[i]
                  closedge[i].adjvex = u;
                  closedge[i].lowcost = gn.arcs[u][i].adj;
               }
            for(e = 1; e <= gn.vexnum-1; e++){//找n-1条边
               v = Minium(closedge); //closedge[v]中存有当前最小边(u, v)的信息
               u = closedge[v].adjvex; //u∈U
               printf("(%d, %d)"u, v); //输出生成树的当前最小边(u, v)
               closedge[v].lowcost = 0; //将顶点v纳入集合U
               for(i = 1; i <= gn.vexnum; i++) //在顶点v纳入集合U之后，更新closedge[i]
                  if(gn.arcs[v][i].adj < closedge[i].lowcost){
                     closedge[i].lowcost = gn.arcs[v][i].adj;
                     closedge[i].adjvex = v;
                  }
            }
         }
         ```
   4. 普里斯卡尔算法【加边法】（并查集）：假设N=(V, {E})是连通图，将N中的边按权值升序排列
      1. 将n个顶点看成n个集合。
      2. 按权值升序选择边，所选的边应满足两个顶点不在同一个顶点集合内，将该边放到生成树边的集合中，同时将该边的两个顶点所在的顶点集合合并。
      3. 重复2直到所有的顶点都在同一个顶点集合内。

### 7.4.2 有向无环图（directed acyclic graph，DAG）的应用

1. 拓扑排序
   1. 顶点表示活动的网（activity on vertex network，AOV网）：用顶点表示活动，用弧表示活动间的优先关系的有向无环图。
   2. 拓扑序列：在有向图G={V, {E}}中，V中顶点的线性序列(v<sub>i1</sub>, v<sub>i2</sub>, v<sub>i3</sub>, ..., v<sub>in</sub>)。如果该序列满足条件：对序列中任意两个顶点vi/vj，在G中有一条从vi到vj的路径，则序列中vi必排在vj之前。
   3. AOV网的特性
      1. 若vi为vj的先行活动，vj为vk的先行活动则vi为vk的先行活动，即先行关系具有可传递性。
      2. AOV网的拓扑序列不是唯一的
   4. 求一个有向无环图的拓扑排序的思想
      1. 从有向图中选一个无前驱的节点输出
      2. 将此节点和以它为起点的边删除
      3. 重复一二，直到不存在无前驱的节点。
      4. 若此时输出的节点数小于有向图中的顶点数，则说明有向图中存在回路，否则输出的顶点的顺序即为一个拓扑序列。
   5. 辅助数组indegree\[\]存放各顶点的入度
      1. 找到G中无前驱的节点，即查找indegree\[i\]为0的顶点。
      2. 删除以i为起点的所有弧，及对链在顶点i后的所有邻接顶点k将对应的indegree减1。
   6. 【A7.11 拓扑排序算法】
      ```cpp
      int TopoSort(AdjList G){
         Stack S;
         int indegree[MAX_VERTEX_NUM];
         int i, count, k;
         ArcNode *p;
         FindID(G ,indegree); // 求出各顶点的入度
         InitStack(&S); // 初始化辅助栈
         for(i = 0; i < G.vexnum; i++){
            if(indegree[i] == 0) 
               Push(&S, i); //将入度为0的顶点入栈
         }
         count = 0; // 输出的节点数
         while(!isEmpty(S)){ // 只要栈不空
            Pop(&S, &i) // 将栈顶元素出栈并打印
            printf("%c", G.vertex[i].data);
            count++;
            p = G.vertex[i].firstarc; // 第一条临界边
            while(p != NULL){
               k = p->adjvex;
               indegree[k]--; // i号顶点的每个临界点的入度减一
               if(indegree[k] == 0){
                  Push(&S, k); // 若入度减为0，则入栈
               }
               p = p->nextarc;
            }
         }
         return count < G.vertex ? Error : OK;
      }
      ```
   7. 【A7.11 求入度算法】
      ```cpp
      void FindID(AdjList G, int indegree[MAX_VERTEX_NUM]){
         int i; ArcNode *p;
         for(i = 0; i < G.vexnum; i++){
            indegree[i] = 0; // 全部初始化为0
         }
         for(i = 0; i < G.vexnum; i++){
            p = G.vertex[i].firstarc;
            while(p != NULL){
               indegree[p->adjvex]++;
               p = p->nextarc;
            }
         }
      }
      ```
2. 关键路径
   1. AOV网：用顶点表示活动，用有向弧表示活动间的优先关系的网
   2. AOE网：用顶点表示事件，用弧表示活动，弧的权值表示活动所需要的时间
   3. 源点：在AOE网中存在唯一的、入度为0的顶点
   4. 汇点：存在唯一的、出度为0的顶点
   5. 关键路径：从源点到汇点的最长路径的长度即为完成整个工程任务所需的时间。
   6. 关键活动：关键路径上的活动。
   7. 事件vi的最早发生时间ve(i)：从原点到顶点vi的最长路径的长度。
   8. 事件vi的最晚发生时间vl(i)：在保证汇点按其最早发生时间发生这一前提下，求事件vi的最晚发生时间。
   9. 活动ai的最早开始时间e(i)：如果活动ai对应的弧为\<j,k\>，，则e(i)等于从原点到顶点j的最长路径长度，即e(i)=ve(j)
   10. 活动ai的最晚开始时间l(i)：如果活动ai对应的弧为\<j,k\>，其持续时间为dut(\<j,k\>)，则有l(i)=vl(k)-dut(\<j,k\>)>。即在保证事件vk的最晚发生时间为vl(k)的前提下。活动ai的最晚开始时间vl(i)。
   11. 活动ai的松弛时间（时间余量）：ai的最晚开始时间与ai的最早开始时间之差，即l(i)-e(i)。显然松弛时间为零的活动为关键活动。
   12. 基本步骤：
       1. 对图中顶点进行拓扑排序，在排序过程中按拓扑序列求出每个事件的最早发生事件。
       2. 按逆拓扑序列求每个事件的最晚发生时间
       3. 求出每个活动的最早发生时间e(i)和最晚发生时间l(i)。
       4. 找出最早发生时间等于最晚发生时间的活动。

【A7.13 修改后的拓扑排序算法】
```cpp
int ve[MAX_VERTEX_NUM];
int TopoOrder(AdjList G, Stack *T）{
    int count,i,j,k;ArcNode *p;
    int indegree[MAX_VERTEX_NUM]; //各顶点入度数组
    Stack S; // S为存放入度为0的顶点的栈
    InitStack(T); InitStack(&S);
    FindID(G, indegree); // 求各顶点入度
    for(i=0;i<G.vexnum;i++)
        if(indegree[i]==0)
            Push(i, &S);
    count = 0;
    for(i=0;i<G.vexnum;i++)
        ve[i] = 0; // 初始化最早发生时间
    while(!IsEmpty(&S)){
        Pop(&S, &j);
        Push(T, j); //按拓扑序列存入栈中
        count++;
        p = G.vertex[j].firstarc;
        while(p){
            k = p->adjvex;
            if(--indegree[k]==0)
                Push(&S, k); // 入度为0的顶点入栈
            if(ve[j]+p->Info.weight>ve[k])
                ve[k] = ve[j]+p->Info.weight; // 更新最早发生时间
            p = p->next;
        }
    return count < G.vexnum ? 0 : 1;
}
```

【A7.14 关键路径算法】
```cpp
int CriticalPath(AdjList G){
    ArcNode *p;
    int i,j,k,dut,ei,li; char tag;
    int vl[MAX_VERTEX_NUM]; //每个顶点的最迟发生时间
    Stack T;
    if(!TopoOrder(G, &T)) // 求时间最早发生时间和逆拓扑序列栈T
        return 0;
    for(i=0; i<G.vexnum; i++) // 将各顶点事件的最迟发生时间初始化为汇点的最早发生时间
        vl[i] = ve[G.vexnum-1];
    while(!isEmpty(&T)){ // 按逆拓扑序列求各顶点的vl值
        Pop(&T, &j);
        p = G.vertex[j].firstarc;
        while(p){
            k = p->adjvex;
            dut = p->weight;
            if(vl[k]-dut < vl[j]) // 如果某个顶点的vl值小于等于其出度的最迟发生时间
                vl[j]=vl[k]-dut; // 则更新该顶点的vl值
            p = p->nextarc;
        }
    }
    for(j=0;j<G.vexnum;j++){ // 求每个顶点的最早发生时间
        p = G.vertex[j].firstarc;
        while(p){
            k = p->adjvex;
            dut = p->weight;
            ei = ve[j];
            li = vl[k]-dut;
            tag = (ei==li) ? '*' : ' ';
            printf("%c,%c,%d,%d,%d,%c\n", G.vertex[j].data, G.vertex[k].data, dut, ei, li, tag);
            p = p->nextarc;
        }
    }
    return 1;
}
```

### 9.4.3 最短路径问题

1. 求某一顶点到其他各顶点的最短路径
```cpp





























/* 【A7.15 图的最短路径算法】 */
#define INFINITY 32768 // 表示极大值
typedef unsigned int WeightType;
typedef WeightType AdjType;
typedef SeqList VertexSet;
ShortestPath_DJS(AdjMatrix g, int v0, WeightType dist[MAX_VERTEX_NUM]),VertexSet path[MAX_VERTEX_NUM]){
    // path[i]存放顶点i的当前最短路径。dist[i]中存放顶点i的当前最短路径长度
    VertexSet S; // S为已找到最短路径的终点集合
    for(int i=0; i<g.vexnum; i++){
        InitList(&path[i]);
        dist[i] = g.arcs[v0][i].adj;
        if(dist[i] < INFINITY){
            AddTail(&path[i], g.vertex[v0]);
            AddTail(&path[i], g.vertex[i]);
        }
    }
    InitList(&S);
    AddTail(&S, g.vertex[v0]); // 将v0看成第一个已找到最短路径的终点
    for(int t = 1; t < g.vexnum; t++){
        int k = -1;
        WeightType min = INFINITY;
        for(int i=0; i<g.vexnum; i++){
            if(!IsInList(&S, g.vertex[i]) && dist[i] < min){
                min = dist[i];
                k = i;
            }
        }
        AddTail(&S, g.vertex[k]);
        for(int t=0; t<=g.vexnum-1; t++){ // 求v0到各个顶点的最短路径
            min = INFINITY;
            for(int i=0; i<g.vexnum; i++){
                if(!Member(g.vertex[i],S) && dist[i] < min){
                    k = i;
                    min = dist[i];
                }
            }
            if(min < INFINITY) return;
            AddTail(&S, g.vertex[k]);
            for(int i=0; i<g.vexnum; i++){ // 修正dist[i]，i∈V-S
                if(!Member(g.vertex[i],S) && g.arcs[k][i].adj!=INFINITY && dist[i] > dist[k] + g.arcs[k][i].adj){
                    dist[i] = dist[k] + g.arcs[k][i].adj;
                    path[i] = path[k];
                    AddTail(&path[i], g.vertex[i]); // path[i]=path[k]∪v[i]
                }
            }
        }
    }
}
```
3. 求任意一对顶点间的最短路径
```cpp






























/* 【A7.16 弗洛伊德算法】 */
ShortestPath_Floyd(AdjMatrix g, WeightType dist[MAX_VERTEX_NUM][MAX_VERTEX_NUM], VertexSet path[MAX_VERTEX_NUM][MAX_VERTEX_NUM]){
    // g为有向网的邻接矩阵表示法，path[i][j]为vi到vj的当前最短路径，dist[i][j]为vi到vj的当前最短路径的长度
    for (i = 0; i < g.vexnum; i++){ //初始化dist[][]和path[][]
        for (j = 0; j < g.vexnum; j++){
            InitList(&path[i][j]);
            dist[i][j] = g.arcs[i][j].adj;
            if (dist[i][j] < INFINITY){
                AddTail(&path[i][j], g.vertex[i]);
                AddTail(&path[i][j], g.vertex[j]);
            }
        }
    }
    for (k = 0; k < g.vexnum; k++){
        for (i = 0; i < g.vexnum; i++){
            for (j = 0; j < g.vexnum; j++){
                if (dist[i][k] + dist[k][j] < dist[i][j]){
                    dist[i][j] = dist[i][k] + dist[k][j];
                    path[i][j] = JoinList(path[i][k], path[k][j]); // 合并线性表
                }
            }
        }
    }
}
```



# 第八章 查找

## 8.1 查找的基本概念

1. 列表：由同一类型的数据元素（或记录）构成的集合，可利用任意数据结构实现。
2. 关键字：数据元素的某个数据项的值，用它可以标识列表中的一个或一组数据元素。如果一个关键字可以唯一标识列表中的一个数据元素，则称其为主关键字，否则为次关键字。当数据元素仅有一个数据项时，数据元素的值就是关键字。
3. 查找：根据给定的关键字值，在特定的列表中确定一个其关键字与给定值相同的数据元素，并返回该数据元素在列表中的位置。
4. 分类：静态查找，在查找过程中只是对数据元素进行查找；动态查找，在实施查找的同时插入未找到的元素，或从查找表中删除已查到的某个元素。
5. 涉及参量：查找对象、查找范围、查找结果
6. 平均查找长度ASL<sub>succ</sub> = P<sub>1</sub>C<sub>1</sub>+P<sub>2</sub>C<sub>2</sub>+...+P<sub>n</sub>C<sub>n</sub>
7. 查找的基本方法：比较式查找法{基于线性表的查找法{顺序查找法、折半查找法、分块查找法}、基于树的查找法}、计算式查找法（哈希法）

## 8.2 基于线性表的查找法

### 8.2.1 顺序查找法
```cpp
#define LIST_SIZE 20
typedef struct{
   KeyType key;
   OtherType other_data;
} RecordType;
typedef struct {
   RecordType r[LIST_SIZE + 1]; // r[0]为工作单元
   int length;
} RecordList;
```
【A8.1 设置监视哨的顺序查找法】
```cpp
int SeqSearch(RecordList l, KeyType k){
   l.r[0] = k; i = l.length;
   while(l.r[i].key != k) i--;
   return i;
}
```
【A8.2 不设置监视哨的顺序查找法】
```cpp
int SeqSearch(RecordList l, KeyType k){
   i = l.length;
   while(i >= 1 && l.r[i] != k) i--;
   // i >= 1 防止越界
   return i >= 1 ? i : 0;
}
```

### 8.2.2 折半（二分）查找法
前提：必须采用顺序存储结构、必须按关键字大小有序排列

【A8.3 折半查找法】
```cpp
int BinSrch(RecordType l, KeyType k){
   low = 1; high = l.length;
   while(low <= high){
      mid = (low + high) / 2;
      if(k == l.r[mid].key) return mid;
      else if(k < l.r[mid].key) high = mid-1;
      else low = mid+1;
   }
   return 0;
}
```

### 分块查找法
1. 将列表分成若干个块，一般情况下，块的长度均匀，最后一块可以不满，每一块中的元素任意排列，即块内无序，但块之间有序。
2. 构造一个索引表，其中每个索引项对应一个块，记住每块的起始位置以及每块中最大的关键字，索引表按关键字有序排列

## 8.3 基于树的查找法

### 8.3.1 二叉排序树

1. 二叉排序树的定义与描述
   1. 二叉排序树或者是一棵空树，或者是具有如下性质的二叉树。
   2. 若它的左子树非空，则左子树上所有节点的值均小于根节点的值。
   3. 若他的右子树非空，则右子树上所有结点的值均大于等于根节点的值。
   4. 它的左右子树也分别为二叉排序树。
   ```cpp
   typedef struct node{
      KeyType key; // 关键字的值
      struct node *lchild, *rchild;
   } BSTNode, BSTree;
   ```
2. 二叉排序树的插入与创建
   1. 【A8.4 二叉排序树插入的递归算法】
      ```cpp
      void InsertBST(BSTree *bst, KeyType key){
         BiTree s;
         if(*bst == NULL){
            s = (BSTree)malloc(sizeof(BSTNode));
            s->key = key;
            s->lchild = s->rchild = NULL;
            *bst = s;
         }else if(k < (*bst)->key)
            InsertBST(&((*bst)->lchild), key);
         else if(k > (*bst)->key)
            InsertBST(&((*bst)->rchild), key);
      }
      ```
   2. 【A8.5 创建二叉排序树】
      ```cpp
      void CreateBST(BSTree *bst){
         KeyType key;
         *bst = NULL；
         scanf("%d", &key);
         while(key != ENDKEY){
            InsertBST(bst, key);
            scanf("%d", &key);
         }
      }//具有相同元素的序列，输入顺序不同，则所创建的二叉排序树的形态不同
      ```
3. 二叉排序树的查找
   1. 【A8.6 二叉排序树查找的递归算法】
      ```cpp
      BSTree SearchBST(BSTree bst, KeyType key){
         if(!bst) return NULL;
         else if(bst->key == key) return bst;
         else if(bst->key > key) return SearchBST(bst->lchild, key);
         else return SearchBST(bst->rchild, key);
      }
      ```
   2. 【A8.7 二叉排序树查找的非递归算法】
      ```cpp
      BSTree SearchBST(BSTree bst, KeyType key){
         BSTree q = bst;
         while(q){
            if(q->key == key) return q;
            else if(q->key > key) q = q->lchild;
            else q = q->rchild;
         }
         return NULL;
      }
      ```
4. 二叉排序树的删除
   1. 若p为叶子节点，则可直接将其删除f->lchild=NULL;free(p);
   2. 若p节点只有左子树，或只有右子树，则可将p的左子树或右子树直接改为其双亲结点f的左子树f->lchild=p->lchild(f->lchild=p->rchild);free(p);
   3. 若p节点既有左子树又有右子树
      1. 法一：首先找到p结点在中序序列中的直接前驱s结点，然后将p的左子树改为f的左子树，而将p的右子树改为s的右子树: f->lchild=p->lchild;s->rchild=p->rchild;tree(p);
      2. 法二：首先找到p结点在中序序列中的直接前驱s结点，然后用s结点的值替代p结点的值，再将s结点删除，原s结点的左子树改为s的双亲结点q的右子树:p->data=s->data;q->rchild=s->lchild;free(s);
   【A8.8 在二叉排序树中删除节点】
   ```cpp
   BSTNode* DelBST(BiTree t, KeyType key){
      BSTNode *p = t, *f = NULL, *s, *q;
      while(p){
         if(p->key == key) break; // 找到待删除的节点p，跳出循环
         f = p;
         p = (p->key > k) ? p->lchild : p->rchild;
      }
      if(p == NULL) return t; // 找不到，返回原来的二叉树
      if(p->lchild == NULL){ // p无左子树
         if(f == NULL) t = p->rchild; // p是原二叉排序树的根
         else if(f->lchild == p) f->lchild=p->rchild; // p是f的左孩子，将p的右子树链到f的左链上
         else f->rchild=p->rchild; // p是f的右孩子，将p的右子树链到f的右链上
         free(p);
      }else{ // p有左子树
         q = p; s = p->lchild;
         while(s->rchild){ // 在p的左子树中查找最右下节点
            q = s; s = s->rchild;
         }
         if(q==p) q->lchild = s->lchild; //将s的左子树链到q上
         else q->rchild = s->lchild;
         p->key = s->key; //
         free(s);
      }
      return t;
   }
   ```
5. 二叉排序树的特性：中序遍历二叉排序树可以得到一个升序有序序列，反之逆中序遍历可以得到一个降序有序序列。

### 8.3.2 平衡二叉排序(AVL)树
- 左子树与右子树的高度之差的绝对值小于等于一
- 左子树与右子树也是平衡二叉排序树
- 平衡因子：节点的左子树深度与右子树深度之差

一般情况下,只有新插入结点的祖先结点的平衡因子受影响,即以这些祖先结点为根的子树有可能失衡。下层的祖先结点恢复平衡,将使上层的祖先结点恢复平衡,因此应调整最下面的失衡子树。因为平衡因子为0的祖先不可能失衡,所以从新插入结点开始,向上遇到的第一个平衡因子不等于0的祖先结点为第一个可能失衡的结点,如果失衡,则应调整以该结点为根的子树。失衡的情况不同,调整的方法也不同.失衡类型及相应的调整方法可归纳为 LL 型、LR 型、RR 型和 RL 型4种。

1. LL型
   ```cpp










   ```
2. LR型
   ```cpp












   ```
3. RR型
   ```cpp










   ```
4. RL型
   ```cpp












   ```
【A8.9 平衡二叉排序树的插入】
```cpp
// ①查找应插位置,同时记录离插人位置最近的可能失衡结点A(看的平衡因子不等于0)。
// ②插入新结点S。
// ③确定结点B,并修改A的平衡因子。
// ④修改从B到S路径上各结点的平衡因子(原值必为0,否则A将下移)。
// ⑤根据A、B的平衡因子判断是否失衡以及失衡类型,并做相应处理。
void ins_AVLtree(AVLTree *avlt, KeyType k){
   S = (AVLTree)malloc(sizeof(AVLTNode));
   S->key = k;
   S->lchild = S->rchild = NULL;
   S->bf = 0;
   if(*avlt == NULL) *avlt = S;
   else{
      // 首先查找S的插入位置fp，同时记录距S的插入位置最近且平衡因子不等于零的节点A，A为可能的失衡节点
      A = *avlt; FA = NULL;
      p = *avlt; fp = NULL;
      while(p != NULL){
         if(p->bf != 0){
            A = p; FA = fp;
         }
         fp = p;
         if(K < p->key) p = p->lchild;
         else p = p->rchild;
      }
      // 插入S
      if(K < fp->key) fp->lchild = S;
      else fp->rchild = S;
      // 确定节点B，并修改A的平衡因子
      if(K < A->key){
         B = A->lchild;
         A->bf++;
      }else{
         B = A->rchild;
         A->bf--;
      }
      // 修改B到S路径上各节点的平衡因子（原值均为0）
      p = B;
      while(p != S){
         if(K < p->key){
            p->bf = 1;
            p = p->lchild;
         }else{
            p->bf = -1;
            p = p->rchild;
         }
      }
      // 判断失衡类型并做出相应调整
      if(A->bf == 2 && B->bf == 1){//LL
         A->lchild = B->rchild;
         B->rchild = A;
         A->bf = B->bf = 0;
         if(FA == NULL) *avlt = B;
         else if(A == FA->lchild) FA->lchild = B;
         else FA->rchild = B;
      }else if(A->bf == 2 && B->bf == -1){//LR
         C = B->rchild;
         B->rchild = C->lchild;
         A->lchild = C->rchild;
         C->lchild = B; C->rchild = A;
         if(S->key < C->key){
            A->bf = -1; B->bf = 0; C->bf = 0;
         }else if(S->key > C->key){
            A->bf = 0; B->bf = 1; C->bf = 0;
         }else{
            A->bf = B->bf = 0;
         }
         if(FA == NULL) *avlt = C;
         else if(A == FA->lchild) FA->lchild = C;
         else FA->rchild = C;
      }else if(A->bf == -2 && B->bf = 1){//RL
         C = B->lchild;
         B->lchild = C->rchild;
         A->rchild = C->lchild;
         C->lchild = A; C->rchild = B;
         if(S->key < C->key){
            A->bf = 0; B->bf = -1; C->bf = 0;
         }else if(S->key > C->key){
            A->bf = 1; B->bf = 0; C->bf = 0;
         }else{
            A->bf = B->bf = 0;
         }
         if(FA == NULL) *avlt = C;
         else if(A == FA->lchild) FA->lchild = C;
         else FA->rchild = C;
      }else if(A->bf == -2 && B->bf = -1){//RR
         A->rchild = B->lchild;
         B->lchild = A;
         A->bf = B->bf = 0;
         if(FA == NULL) *avlt = B;
         else if(A == FA->lchild) FA->lchild = B;
         else FA->rchild = B;
      }
   }
}
```

### 8.3.3 B树
1. m路查找树
   1. 节点最多有m棵子树，m-1个关键字
   2. K<sub>i</sub>\<K<sub>i+1</sub>, 1 <= i <= n-1
   3. 子树P<sub>i</sub>中的所有关键字均大于K<sub>i</sub>，小于K<sub>i+1</sub>, 1 <= i <= n-1
   4. 子树P<sub>0</sub>中的关键字均小于K<sub>1</sub>，而子树P<sub>n</sub>中的所有关键字均大于K<sub>n</sub>
   5. 子树P<sub>i</sub>也是m路查找树，0 <= i <= n
2. B树及其查找
   1. 一棵B树是一颗平衡的m路查找树
   2. 树中每个节点最多有m棵子树
   3. 根节点至少有两棵子树
   4. 除根节点之外的所有非叶子节点至少有\[m/2\]棵子树
   5. 所有的叶子节点出现在同一层上，并且不含信息，通常称为失败节点。失败节点为虚节点，在B树中并不存在，指向他们的指针为空指针，引入失败节点是为了便于分析B树的查找性能

【A8.10 在B树中查找关键字为k的元素】
   ```cpp
   #define m <阶数>
   typedef int Boolean;
   typedef struct Mbtnode{
      struct Mbtnode *parent;
      int keynum;
      KeyType key[m+1];
      struct Mbtnode *ptr[m+1];
   } Mbtnode, *Mbtree;
   Boolean srch_mbtree(Mbtree mbt, KeyType key, Mbtree *np, int *pos){
      //在根为mbt的B树中查找关键字k,如果查找成功,则将所在结点地址放入np,将结点内位置序号放入pos,并返回true;否则,将上应被插人的结点地址放入np,将结点内应插位置序号放人pos,并返回false
      p = mbt; fp = NULL; found = false; i = 0;
      while(p != NULL && !found){
         i = search(p, k);
         if(i > 0 && p->key[i] == k) found = true;
         else {
            fp = p; p = p->ptr[i];
         }
      }
      if(found){
         *np = p; *pos = i; return true;
      }else{
         *np = fp; *pos = i; return false;
      }
   }
   ```
【A8.11 在B树中查找关键字为k的元素】
   ```cpp
   int search(Mbtree mbt, KeyType key){
      // 在 mbt 指向的结点中,寻找小于等于 key 的最大关键字序号
      n = mbt->keynum;
      i = 1;
      while(i <= n && mbt->key[i] <= key) i++;
      return i-1;// 返回小于等于 key 的最大关键字序号,为0时表示应到最左分支找,越界时表示应到最右分支找
   }
   ```
3. B树插入
   ```









   ```
   【A8.12 B树的插入算法】
   ```cpp
   void ins_mbtree(Mbtree mbt, KeyType key, Mbtree q, int i){
      // 在m阶B树t中插入k:如果mbt=NULL,则生成初始根(此时q=NULL,i=0);否则q指向某个最下层非终端结点,k应插在该结点中q->key[i+1]处,插入后如果q->keynum>m-1,则进行分裂处理
      Mbtree ql, ap;
      if(*mbt == NULL){
         *mbt = (Mbtree)malloc(sizeof(Mbtnode));
         (*mbt)->keynum = 1; (*mbt)->parent = NULL;
         (*mbt)->key[1] = k; (*mbt)->ptr[0] = NULL;
         (*mbt)->ptr[1] = NULL;
      }else{
         x = k; // 将x插到q->key[i+1]处
         ap = NULL; //将ap插到q->key[i+1]处
         finished = NULL; //
         while(q != NULL && !finished){ //q=NULL标识已经分裂到根
            Insert(q, i, x, ap);
            if(q->keynum < m) finished = TRUE; //不在分裂
            else{
               s = ceil((float)m / 2);
               split(q, &q1); //分裂
               x = q->key[s];
               ap = q1;
               q = q->parent;
               if(q != NULL) i = search(q, x);
            }
         }
         if(!finished){ //根节点要分裂并产生新根
            new_root = (Mbtnode)malloc(sizeof(Mbtnode));
            new_root->keynum = 1;
            new_root->parent = NULL;
            new_root->key[1] = x;
            new_root->ptr[0] = *mbt;
            new_root->ptr[1] = ap;
            *mbt = new_root;
         }
      }
   }
   ```
   【A8.13 在mbp->key\[ipos+1\]处插入key】
   ```cpp
   void insert(Mbtree mbt,int pos, KeyType key, Mbtree rp){
      // 在mbp->key[ipos+1]处插入key，在mbp->ptr[ipos+1]处插入rp
      for(j = bmp->keynum; j >= ipos+1; j--){
         bmp->key[j+1] = bmp->key[j];
         bmp->ptr[j+1] = bmp->ptr[j];
      }
      bmp->key[ipos+1] = key;
      bmp->ptr[ipos+1] = rp;
      bmp->keynum++;
   }
   ```
   【A8.14 】
   ```cpp
   void split(Mbtree oldp, Mbtree *newp){
      s = ceil((float)m / 2);
      n = m-s;
      *newp = (Mbtree)malloc(sizeof(Mbtnode));
      (*newp)->keynum = n;
      (*newp)->parent = oldp->parent;
      (*newp)->ptr[0] = oldp->ptr[s];
      for(i = 1; i <= n; i++){
         (*newp)->key[i] = oldp->key[s+i]
         (*newp)->ptr[i] = oldp->ptr[s+i];
      }
      oldp->keynum = s-1;
   }
   ```

4. 在B树中删除一个关键字
   1. 在最下层节点中删除一个关键字
      ```cpp
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      ```
   2. 在非最下层节点中删除一个关键字
      ```cpp






      ```

## 8.4 计算式查找法——哈希法

哈希法又称散列法,杂凑法或关键字地址计算法,相应的表称为哈希裁,散列表或杂凑表等。哈希法的基本思想:首先在元素的关键字k和存储位置p之间建立一个对应关系H,使得p=H(k),H()称为哈希函数。创建哈希表时,把关键字为k的元素直接存入地址为H(k)的单元,以后当查找关键字为石的元素时,再利用哈希函数p=H(h)计算出该元素的存储位置,从而达到按关键字直接存取元素的目的。

冲突问题：当关键字集合很大时，关键字值不同的元素可能会映像到哈希表的同一地址上，即k1≠k2，但H(k1)=H(k2)的现象，称k1、k2为同义词

### 8.4.1 哈希函数的构造方法
原则：函数本身便于计算、计算结果分布均匀

1. 数字分析法
2. 平方取中法
3. 分段叠加法
4. 除留余数法
5. 伪随机数法

实际应用需考虑因素：
1. 计算哈希函数所需的时间(简单)。
2. 关键字的长度。
3. 哈希表的大小。
4. 关键字分布的情况。
5. 记录查找的频率

### 8.4.2 处理冲突的方法
1. 开放地址法
2. 再哈希法
3. 链地址法（☆）
4. 建立公共溢出区法

### 8.4.3 哈希表的查找过程
1. 首先计算h0=hash(K)。
2. 如果单元h0为空,则所查元素不存在。
3. 如果单元h0中元素的关键字为K,则找到所查元素。
4. 否则重复下述解决冲突的过程：
   1. 按解决冲突的方法,找出下一个哈希地址h;
   2. 如果单元h,为空,则所查元素不存在;
   3. 如果单元h,中元素的关键字为K,则找到所查元素。

【A8.15 哈希表的查找算法（用线性探测再散列处理冲突）】
   ```cpp
   #define m <哈希表长度>
   #define NULLKEY <代表空记录的关键字值>
   typedef int KeyType；/*假设关键字为整型*/
   typedef struct {
      KeyType key;
      ... /*记录中其他分量按需求确定*/
   } RecordType;
   typedef RecordType HashTable[m];
   int HashSearch(HashTable ht, KeyType K)
      h0 = hash(K)；
      if(ht[h0].key == NULLKEY) return -1;
      else if(ht[h0].key == K) return h0;
      else {/*用线性探测再散列解决冲突*/
         for (i=1; i<=m-1; i++){
            hi = (h0+i) % m;
            if(ht[hi].key == NULLKEY) return -1;
            else if(hi[hi].key == K) return hi;
         }
      return -1;
      }
   }
   ```

## ...

```cpp









```



# 第九章 内部排序

## 9.1 排序的基本概念

1. 排序：...得到一个按关键字有序的记录序列{R<sub>p<sub>1</sub></sub>, R<sub>p<sub>2</sub></sub>, ..., R<sub>p<sub>n</sub></sub>}。
2. 内部排序与外部排序
   1. 内部排序：整个排序过程完全在内存中进行
   2. 外部排序：由于待排序记录数据量太大，内存无法容纳全部数据，排序需要借助外部存储设备才能完成
3. 主关键字与次关键字
   1. 主关键字：
   2. 次关键字：
4. 排序方法的稳定性
   1. 稳定：排序前的序列中R<sub>i</sub>领先于R<sub>j</sub>（即`i<j`），经过排序后得到的序列中R<sub>i</sub>仍领先于R<sub>j</sub>
   2. 不稳定：相同关键字的领先顺序在排序过程中发生变化
   3. 证明一种排序方法是稳定的,要通过算法本身的步骤加以证明。证明排序方法是不稳定的，只需给出一个反例说明即可。
5. 排序的两种基本操作
   1. 比较两个关键字的大小
   2. 将记录从一个位置移动到另一个位置
6. 待排序序列常见的存储表示
   1. 向量结构
   2. 链表结构
   3. 记录向量与地址向量结合
   ```cpp
   // 向量结构定义：
   typedef int KeyType;
   typedef struct{
      KeyType key;
      OtherType other_data;
   }RecordType;
   ```

## 9.2 插入排序

插入类排序的基本思想是在一个已排好序的记录子集的基础上,每一步将下一个待排序的记录有序插入已排好序的记录子集,直到将所有待排记录全部插人为止。

### 9.2.1 直接插入排序

【A9.1 直接插入排序】
```cpp
void InsSort(RecordType r[], int n){
   // 对记录数组r做直接插入排序，n为数组中待排序记录的数目
   for(i = 2; i <= n; i++){
      // 监视哨r[0]：备份待插入的记录，防止越界
      r[0] = r[i];
      j = i - 1;
      while(r[0].key < r[j].key){//寻找插入位置
         r[j+1] = r[j];
         j--;
      }
      r[j+1] = r[0];//将待插入记录插入已排序的序列
   }
}
```

### 9.2.2 折半插入排序

【A9.2 折半插入排序】
```cpp
void BinSort(RecordType r[], int n){
   // 对记录数组r做折半插入排序，n为数组长度
   for(i = 2; i <= n; i++){
      x = r[i];
      low = 1;high = i-1;
      while(low < high){//寻找插入位置
         mid = (low + high)/2;
         if(x.key < r[mid].key)high = mid-1;
         else low = mid+1;
      }
      for(j = i-1; j >= low; j--){
         r[j+1] = r[j];//记录以此向后移动
      }
      r[low] = x;//插入记录
   }
}
```

### 9.2.3 希尔排序

希尔排序：又称缩小增量排序

算法在具体实现时,并不是先对一个子序列完成插入排序,再对另一个子序列进行插入排序,而是从第一个子序列的第二个记录开始,顺序扫描整个待排序记录序列,当前记录属于哪一个子序列,就在哪一个子序列中进行插入排序。

【A9.2 折半插入排序】
```cpp
void ShellInsert(RecordType r[], int n, int delta){
   // 对记录数组r做一次希尔插入排序，n为数组长度，delta为增量
   for(i = 1 + delta; i <= n; i++){
      if(r[i].key < r[i-delta].key){
         r[0] = r[i];//备份r[i]，不做监视哨
         for(j = i-delta; j>0 && r[0].key < r[j].key; j-=delta)
            r[j+delta] = r[j];
         r[j+delta] = r[0];
      }
   }
}

void ShellSort(RecordType r[], int n, int delta[], int m){
   // 对记录数组r做希尔插入排序，n为数组长度，delta为增量数组，m为delta长度
   for(i = 0; i <= m-1; i++){
      ShellInsert(r, n, delta[i]);
   }
}
```

1. 增量的取法：
2. 逆转数：在它之前比此关键字大的关键字的个数（逆序数）
3. 时间复杂度：

### 9.2.4 小结

插入类排序算法的简单总结

| 排序算法     | 改进思路                                                       | 时间复杂度                                 | 最好情况                  | 最坏情况         | 空间复杂度       |
| ------------ | -------------------------------------------------------------- | ------------------------------------------ | ------------------------- | ---------------- | ---------------- |
| 直接插入排序 | ——                                                             | O(n<sup>2</sup>)                           | O(n)：n较小或元素基本有序 | O(n<sup>2</sup>) | O(n<sup>1</sup>) |
| 折半插入排序 | 改进了确定插入位置的方法，利用折半思想确定在有序表中的插入位置 | O(n<sup>2</sup>)：比较时间复杂度为O(nlogn) | O(nlogn)                  | O(n<sup>2</sup>) | O(n<sup>1</sup>) |
| 希尔排序     | 利用了直接插住的最好情况：n比较小，基本有序                    | O(n<sup>1.5</sup>)                         | ——                        | ——               | O(n<sup>1</sup>) |

插入类排序算法的稳定性证明

| 排序算法     | 稳定性 | 证明                                                                                     |
| ------------ | ------ | ---------------------------------------------------------------------------------------- |
| 直接插入排序 | 稳定   | 排序比较从后向前进行：算法中`while(r[0].key < r[j].key)`保证了相同的后面元素不会排到前面 |
| 折半插入排序 | 稳定   | `if(x.key < r[mid].key)high = mid-1;else low = mid+1;`保证了相同的后面元素不会排到前面   |
| 希尔排序     | 不稳定 | 给出反例{2，4，1，2}                                                                     |

## 9.3 交换类排序

交换类排序的基本思想是通过一系列交换逆序元素进行排序。

### 9.3.1 冒泡排序

冒泡排序（相邻比序）是一种简单的交换类排序方法，它是通过对相邻的数据元素进行交换，逐步将待排序序列变成有序序列的过程，若在某一趟冒泡排序过程中没有发现一个逆序，则可直接结束整个排序过程。

```cpp
void BubbleSort(RecordType r[], int n){
   // 对记录数组r做冒泡排序，n为数组长度
   change = 1;
   for(i = 1; i <= n-1 && change; i++){
      change = 0;
      for(j = 1; j <= n-1; j++){
         if(r[j].key > r[j+1].key){
            x = r[j];
            r[j] = r[j+1];
            r[j+1] = x;
            change = 1;
         }
      }
   }
}
```

### 9.3.2 快速排序

【A9.5 快速排序算法】
```cpp
void QKSort(RecordType r[], int low, int high){
   // 对记录数组r用快速排序算法进行排序
   if(low < high){
      pos = QKPass(r, low, high);// 调用一次快速排序，以基准记录为界划分两个子表
      QKSort(r, low, pos-1);// 对左部子表快速排序
      QKSort(r, pos+1, high);// 对右部子表快速排序
   }
}
```

【A9.6 一趟快速排序算法】
```cpp
int QKPass(RecordType r[], int low, int high){
   // 用基准记录对r[low]~r[high]部分进行一趟排序，得到基准记录的新位置，使得基准记录之前的所有记录的关键字均小于基准记录关键字，而基准记录之后的所有记录的关键字均大于或等于基准记录的关键字
   x = r[low];// 选择基准记录
   while(low < high){
      // high从右到左找到小于x.key的记录
      while(low < high && r[high].key >= x.key)high--;
      // 找到小于x.key的记录，送入空单元r[low]
      if(low < high)r[low++] = r[high];
      // low从左到右找到大于或等于x.key的记录
      while(low < high && r[low].key < x.key)low++;
      // 找到大于或等于x.key的记录，送入空单元r[high]
      if(low < high)r[high--] = r[low];
   }
   r[low] = x;//将基准记录保存到low=high的位置
   return low;//返回基准记录的位置
}
```

### 9.3.3 小结

交换类排序算法的简单总结

| 排序算法 | 改进思路                           | 时间复杂度           | 最好情况             | 最坏情况         | 空间复杂度          |
| -------- | ---------------------------------- | -------------------- | -------------------- | ---------------- | ------------------- |
| 冒泡排序 | ——                                 | O(n<sup>2</sup>)     | O(n)                 | O(n<sup>2</sup>) | O(1)                |
| 快速排序 | 交换不相邻的两个元素，消除多个逆序 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n<sup>2</sup>) | O(log<sub>2</sub>n) |

交换类排序算法的稳定性证明

| 排序算法 | 稳定性 | 证明                                                                                        |
| -------- | ------ | ------------------------------------------------------------------------------------------- |
| 冒泡排序 | 稳定   | 排序比较从前向后进行，算法中语句`if(r[j].key > r[j+1].key)`保证了相同的后面元素不会排到前面 |
| 快速排序 | 不稳定 | 给出反例{3，3，2}                                                                           |

## 9.4 选择类排序

选择类排序的基本思想是，每一趟在n-i+1（i=1，2，...，n-1）个记录中选取关键字最小的记录作为有序序列中第i个记录

### 9.4.1 简单选择排序

```cpp
void SelectSort(RecordType r[], int n){
   for(int i = 1; i <= n-1; i++){
      int k = i;
      for(int j = i+1; j <= n; j++){
         if(r[j].key < r[k].key)k=j;
      }
      if(i != k){
         RecordType x = r[i];
         r[i] = r[k];
         r[k] = x;
      }
   }
}
```

### 9.4.2 树形选择排序

```cpp




```

### 9.4.3 堆排序

堆定义：称各结点的关键字值满足条件`r[i].key >= r[2i].key`并且`r[i].key >= r[2i+1].key`（`i=1，2，...，[n/2]`）的完全二叉树称为大根堆

1. 重建堆
   ```cpp
   // 筛选法


   【A9.8 重建堆过程】
   void sift(RecordType r[], int k, int m){
      // 假设r[k..m]是以r[k]为根的完全二叉树，且分别以r[2k]和r[2k+1]为根的左右子树为大根堆，调整r[k]，使整个序列r[k..m]满足堆的性质
      RecordType t = r[k]; //暂存根记录r[k]
      int x = r[k].key;
      i = k, j = 2 * i;
      finished = false;
      while (j<=m && !finished){
         if(j+1 <= m && r[j].key < r[j+1].key)
            j++;//若存在右子树，且右子树的关键字大，则沿右分支筛选
         if(x >= r[j].key)
            finished = true;//筛选完毕
         else{//继续筛选
            r[i] = r[j];
            i = j;
            j = 2 * i;
         }
      }
      r[i] = t;//填入恰当的位置
   }
   ```
2. 建初始堆
   【A9.9 建初始堆算法】
   ```cpp
   void crt_heap(RecordType r[], int n){
      // 对记录数组r建堆，n为数组的长度
      for(i = n/2; i >= 1; i--){
         sift(r, i, n);
      }
   }





   ```
3. 堆排序算法实现
   1. 将待排序记录按照堆的定义建初始堆(算法 9.9),并输出堆顶元素。
   2. 调整剩余的记录序列,利用筛选法将前n-i个元素重新筛选建成一个新堆,再输出堆顶元素。
   3. 重复执行步骤2,进行 n-1 次筛选,新筛选成的堆会越来越小,而新堆后面的有序关键字会越来越多,最后使待排序记录序列成为一个有序的序列,这个过程称为堆排序。
   【A9.10 堆排序算法】
   ```cpp
   void HeapSort(RecordType r[], int n){
      // 对r[1..n]进行堆排序
      crt_heap(r, n);
      for(i = n; i >= 2; i--){
         // 将堆顶记录和队尾记录互换
         b = r[1];
         r[1] = r[i];
         r[i] = b;
         // 进行调整，使r[1...i-1]变成堆
         sift(r, 1, i-1);
      }
   }
   （1）建立初始堆
   （2）排序反复调整堆
   ```

### 9.4.4 小结

选择类排序算法的简单总结

| 排序算法     | 改进思路                                               | 时间复杂度           | 最好情况             | 最坏情况             | 空间复杂度 |
| ------------ | ------------------------------------------------------ | -------------------- | -------------------- | -------------------- | ---------- |
| 简单选择排序 | 基本排序方法                                           | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(n<sup>2</sup>)     | O(1)       |
| 树形选择排序 | 排序过程中记录元素大小关系                             | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(n)       |
| 堆排序       | 将存储在向量中的数据看成一棵完全二叉树，减少了辅助空间 | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(nlog<sub>2</sub>n) | O(1)       |

选择类排序算法的稳定性证明

| 排序算法     | 稳定性 | 证明                                                               |
| ------------ | ------ | ------------------------------------------------------------------ |
| 简单选择排序 | 不稳定 | 给出反例{3，3，2}                                                  |
| 树形选择排序 | 稳定   | 当左右子树相等时，优先选择左子树，保证了相同的后面元素不会移到前面 |
| 堆排序       | 不稳定 | 给出反例{5，5，3}                                                  |

## 9.5 归并排序

【A9.11 合并相邻的两个有序子序列】
```cpp
void Merge(RecordType r[], int low, int mid, int high){
   // r数组中，low到mid单元为一有序序列，mid+1到high为另一有序序列，将二者合并为一个新的有序序列，并放入r数组的low到high单元
   int i, j, k;
   RecordType *A = (RecordType *)malloc(sizeof(RecordType) * (high - low + 1));
   i = low;
   j = mid + 1;
   k = 0;
   while (i < mid && j < high){
      if (r[i] <= r[j]){
         A[k++] = r[i++];
      }
      else{
         A[k++] = r[j++];
      }
   }
   while (i < mid){
      A[k++] = r[i++];
   }
   while (j < high){
      A[k++] = r[j++];
   }
   // 合并好的数据放在辅助空间中，平移到原数组r中，并释放辅助空间
   for (i = low, k = 0; i < high; i++, k++)
      r[i] = A[k];
   free(A);
}
```

## 9.6 分配类排序

### 9.6.1 多关键字排序

```


```

### 9.6.2 链式基数排序

```cpp
#define RADIX 10
#define KEY_SIZE 6
#define LIST_SIZE 20
typedef int KeyType;
typedef struct {
    KeyType keys[KEY_SIZE];//子关键字数组
    OtherType other_data;//其他数据项
    int next;//静态链域
}RecordType;
typedef struct {
    RecordType r[LIST_SIZE+1];//r[0]为头结点
    int length;
    int keynum;
}SLinkList;//静态链表
typedef int PVector;[RADIX];

【A9.13 链式基数排序算法】
void Distribute(RecordType r[], int i, PVector f, PVector e){
   /*记录数组r中的记录已按低位关键字 key[i+1],…,key[d]进行“低位优先”排序。本算法按第i位关键字key[i]建立 RADIX 个队列,同一个队列中记录的key[i]相同。f[j]和e[j]分别指向各队列中第一个和最后一个记录(j=0,1,2,…,RADIX-1)。f[j]=0 表示相应队列为空队列*/
   for (size_t j = 0; j <= RADIX - 1; j++)
      f[j] = 0;/*将 RADIX 个队列初始化为空队列*/
   p = r[0].next;/* p指向链表中的第一个记录*/
   while (p != 0){
      j = Order(r[p].key[i]);/*用记录中第 i位关键字求相应队列号*/
      if (f[j] == 0)
         f[j] = p;/*将p所指向的结点加入第j个队列*/
      else
         r[e[j]].next = p;
      e[j] = p;
      p = r[p].next;
   }
}
void Collect(RecordType r[], PVector f, PVector e){
   /*本算法从 0 到 RADIX-1 扫描各队列,将所有非空队列首尾相接,重新链接成一个链表*/
   j = 0;
   while (f[j] == 0)
      j++;
   r[0].next = f[j];
   t = e[j];
   while (j < RADIX - 1){/*找第一个非空队列*/
      j++;
      while (j < RADIX - 1 && f[j] == 0)
         j++;/*寻找并串接所有非空队列*/
      if (f[j] != 0){/*链接非空队列*/
         r[t].next = f[j];
         t = e[j];
      }
   }
   r[t].next = 0;/*t 指向最后一个非空队列中的最后一个结点*/
}
void RadixSort(RecordType r[], int n, int d){
   /*n个记录存放在数组r中,d为关键字位数,执行本算法进行基数排序后,链表中的记录将按关键字从小到大的顺序相链接*/
   n = length;
   for (i = 0; i <= n - 1; i++)
      r[i].next = i + 1;/*构造静态链表*/
   r[n].next = 0;
   for (i = d - 1; i >= 0; i--){/*从最低位子关键字开始，进行d趟分配和收集*/
      Distribute(r, i, head, tail);/*第i趟分配*/
      Collect(r, head, tail);/*第i趟收集*/
   }
}
```

## 9.7 各种排序方法的综合比较

```


```

## 9.8 总结与提高

```








```


# 第十章 外部排序

## 10.1 外排序的基本方法

### 10.1.1 磁盘排序

1. 一个例子（略）
2. 初始顺串的生成
   1. 待排序文件：FI；存放初始顺串：FO；WA：可以容纳m个记录的内存工作区
   2. 过程：
      1. 从FI输入m个记录到内存工作区WA
      2. 从WA中选出关键字最小的记录Min，其关键字为MinKey
      3. 将Min输出到FO中
      4. 若FI不为空，则从FI读入下一个记录，送到WA中
      5. 从WA中所有关键字大于MinKey的记录中，重新选出关键字最小的记录Min，其关键字为MinKey
      6. 重复3-5，直到在WA中选不出新的Min记录为止，此时已得到一个初始顺串，所以输出一个结束标志到FO中
      7. 重复2-6，直到WA为空。此时，FO中将顺次存放所有初始顺串

### 10.1.2 磁带排序

## 10.2 总结与提高

