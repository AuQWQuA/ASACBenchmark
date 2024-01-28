# 双栈排序

## 题目描述

Tom 最近在研究一个有趣的排序问题。如图所示，通过 $2$ 个栈 $S_1$ 和 $S_2$，Tom 希望借助以下 $4$ 种操作实现将输入序列升序排序。

![](https://cdn.luogu.com.cn/upload/image_hosting/gwxu91ud.png)

- 操作 $\verb!a!$：将第一个元素压入栈 $S_1$。
- 操作 $\verb!b!$：将 $S_1$ 栈顶元素弹出至输出序列。
- 操作 $\verb!c!$：将第一个元素压入栈 $S_2$。
- 操作 $\verb!d!$：将 $S_2$ 栈顶元素弹出至输出序列。

如果一个 $1\sim n$ 的排列 $P$ 可以通过一系列合法操作使得输出序列为 $(1,2,\cdots,n-1,n)$，Tom 就称 $P$ 是一个“可双栈排序排列”。例如 $(1,3,2,4)$ 就是一个“可双栈排序序列”，而 $(2,3,4,1)$ 不是。下图描述了一个将 $(1,3,2,4)$ 排序的操作序列：$\texttt {a,c,c,b,a,d,d,b}$。

![](media/image2.jpeg)

当然，这样的操作序列有可能有几个，对于上例 $(1,3,2,4)$，$\texttt{a,b,a,a,b,b,a,b}$ 是另外一个可行的操作序列。Tom 希望知道其中字典序最小的操作序列是什么。

## 输入格式

第一行是一个整数 $n$。

第二行有 $n$ 个用空格隔开的正整数，构成一个 $1\sim n$ 的排列。

## 输出格式

共一行，如果输入的排列不是“可双栈排序排列”，输出 `0`。

否则输出字典序最小的操作序列，每两个操作之间用空格隔开，行尾没有空格。

## 样例 #1

### 样例输入 #1

```
4
1 3 2 4
```

### 样例输出 #1

```
a b a a b b a b
```

## 样例 #2

### 样例输入 #2

```
4
2 3 4 1
```

### 样例输出 #2

```
0
```

## 样例 #3

### 样例输入 #3

```
3
2 3 1
```

### 样例输出 #3

```
a c a b b d
```

## 提示

$30\%$ 的数据满足：$n\le10$。

$50\%$ 的数据满足：$n\le50$。

$100\%$ 的数据满足：$n\le1000$。