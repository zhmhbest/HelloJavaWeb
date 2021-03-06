<link rel="stylesheet" href="https://zhmhbest.gitee.io/hellomathematics/style/index.css">
<script src="https://zhmhbest.gitee.io/hellomathematics/style/index.js"></script>

# [Java](https://github.com/zhmhbest/HelloJava)

[TOC]

## IOStream

![stream](images/stream.png)

## Collection

![collection](images/collection.png)

### List

#### ArrayList

- 内部通过数组实现；
- 适合随机查找和遍历；
- 不适合随机插入和删除；
- 内存不够时默认扩展$50\%+1$个。

#### LinkedList

- 链表结构存储数据；
- 适合动态插入和删除；
- 随机访问速度较慢
- 提供操作表头、表尾的方法，可以当作堆栈、队列和双向队列使用。

#### Vector

- 内部通过数组实现；
- 支持线程同步；
- 访问速度慢于ArrayList；
- 内存不够时默认扩展1倍。

### Set

#### HashSet

- 基于HashMap实现；
- 非线程安全。

### Queue

#### Deque

双端队列支持在两端插入和移除元素。

#### PriorityQueue

优先队列，根据排序规则决定谁在队头，谁在队尾

## Map

![map](images/map.png)

### HashMap

- 根据键的Hash值存储数据
- 遍历时取得数据的顺序是完全随机的
- 最多只允许一条记录的Key为null，多条Value为null
- 不支持线程同步

### LinkedHashMap

- 保存了记录的插入顺序；
- 一般情况下遍历时会比HashMap慢。

### TreeMap

根据键值排序，默认按键值的升序排序。

### Hashtable

- 无论Key还是Value都不能为null；
- 线程安全的。

## JAVA参数

```txt
    -cp         目录/zip/jar搜索路径
    -classpath  目录/zip/jar搜索路径（可指定多个）

    -Xloggc:<file>  将GC状态记录在文件中(带时间戳)
    -Xms<size>      初始Heap大小（默认物理内存的1/64）
    -Xmx<size>      最大Heap大小（默认物理内存的1/4）
    -Xss<size>      每个线程的Heap大小（默认1m）

    # 堆大小 = 年轻代大小 + 年老代大小 + 持久代大小
    -Xmn<size>                  -XX:newSize=<size> + -XX:MaxnewSize==<size>
    -XX:NewSize=<size>          年轻代初始内存（应小于ms）
    -XX:MaxnewSize=<size>       年轻代最大内存（应小于mx）
    -XX:PermSize=<size>         持久代初始大小
    -XX:MaxPermSize=<size>      持久代最大大小
    -XX:NewRatio=<size>         年轻代:年老代的比值=1:<size>
```
