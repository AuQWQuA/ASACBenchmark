# 校门外的树

## 题目描述

某校大门外长度为 $l$ 的马路上有一排树，每两棵相邻的树之间的间隔都是 $1$ 米。我们可以把马路看成一个数轴，马路的一端在数轴 $0$ 的位置，另一端在 $l$ 的位置；数轴上的每个整数点，即 $0,1,2,\dots,l$，都种有一棵树。

由于马路上有一些区域要用来建地铁。这些区域用它们在数轴上的起始点和终止点表示。已知任一区域的起始点和终止点的坐标都是整数，区域之间可能有重合的部分。现在要把这些区域中的树（包括区域端点处的两棵树）移走。你的任务是计算将这些树都移走后，马路上还有多少棵树。

## 输入格式

第一行有两个整数，分别表示马路的长度 $l$ 和区域的数目 $m$。

接下来 $m$ 行，每行两个整数 $u, v$，表示一个区域的起始点和终止点的坐标。

## 输出格式

输出一行一个整数，表示将这些树都移走后，马路上剩余的树木数量。

## 样例 #1

### 样例输入 #1

```
500 3
150 300
100 200
470 471
```

### 样例输出 #1

```
298
```

## 提示

**【数据范围】**

- 对于 $20\%$ 的数据，保证区域之间没有重合的部分。
- 对于 $100\%$ 的数据，保证 $1 \leq l \leq 10^4$，$1 \leq m \leq 100$，$0 \leq u \leq v \leq l$。