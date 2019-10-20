# 概率论的基本概念

## 样本空间和随机事件

### 样本空间

> 随机试验的所有可能结果构成的集合成为样本空间, 记为S={e},
>
> S中的e作为样本点

例1:

> * 一枚硬币抛一次
>
>   S = {正面, 反面}
>
> * 记录一批产品的寿命x:
>
>   S = {x : x>=0}
>
> * 记录某地一昼夜最高温度x,最低温度y
>
>   S = {(x,y) : a<=y<=x<=b}

### 随机事件

> 样本空间S的子集A成为随机事件A, 简称事件A, 当前仅当A中的某个样本点发生时 称事件A发生
>
> > 事件A的表示可以用集合, 也可以用语言表达

* 如果把S看做事件, 则每次试验S总是发生, 称S为必然事件
* 基本事件: 事件只含有一个样本
* 空集: 不包含任何样本点, 记为$\varnothing$, 则每次试验$\varnothing$都不发生, 成$\varnothing$为不可能事件

### 事件的关系(包含,相等)

1. A$\subset$B: 事件A发生一定导致事件B发生(因为A是B的子集)
2. A = B $\Leftrightarrow $ A$\subset$B 且 B$\subset$A

### 事件的运算及关系

1. 和事件, 记为A$\cup$B

   A$\cup$B = {x | x$\in$A 或 x$\in$B}, A与B至少有一个发生

2. 积事件,记为A$\cap$B, A$\cdot$B,AB

   A$\cap$B = {x | x$\in$A 且 x$\in$B}, A与B同时发生

> $\bigcup_{i=1}^{n}A_{i}$ 表示$A_{1}$,$A_{2}$,...,$A_{n}$至少有一个发生
>
> $\bigcap_{i=1}^{n}A_{i}$ 表示$A_{1}$,$A_{2}$,...,$A_{n}$同时发生

3. 不相容(互斥): AB=$\varnothing$

4. 差事件: A - B = {x | x$\in$A 且 x$\notin$B}

5. A的逆事件,记为$\overline{A}$, 也称A的互逆, 对立事件

   A$\cup$$\overline{A}$=S, A$\overline{A}$=$\varnothing$, $\overline{\overline{A}}$ = A

> A与B的差事件可以表示为:
>
> A-B = A$\overline{B}$ = A$\cup$B-B = A-AB

### 运算法则

* 交换律: A$\cup$B = B$\cup$A, A$\cap$B = B$\cap$A

* 结合律: A$\cup$(B$\cup$C) = (A$\cup$B)$\cup$C, A$\cap$(B$\cap$C) = (A$\cap$B)$\cap$C

* 分配率: A$\cup$(B$\cap$C) = (A$\cup$B) $\cap$ (A$\cup$C), A$\cap$(B$\cup$C) = (A$\cap$B) $\cup$ (A$\cap$C)

* 对偶律(德*摩根定律): $\overline{A \cup B}$ =  $\overline{A}$ $\cap$ $\overline{B}$, $\overline{A \cap B}$ =  $\overline{A}$ $\cup$ $\overline{B}$

  对偶律推广: $\bigcap_{i=1}^{n}A_{i}$= $\bigcup_{i=1}^{n}\overline{A_i}$= $\overline{A_1}\cup\overline{A_2}\cdots\cup\overline{A_n}$;

  $\bigcup_{i=1}^{n}A_{i}$= $\bigcap_{i=1}^{n}\overline{A_i}$= $\overline{A_1}\cap\overline{A_2}\cdots\cap\overline{A_n}$ = $\overline{A_1}\overline{A_2}\cdots\overline{A_n}$

## 频率和概率

### 频率

> def: $f_n(A) = \frac{n_A}{n}$; 其中$n_A$是A发生的次数(频数), n是总试验次数. 称$f_n(A) $为A在这n次试验中发生的频率.

#### 频率的性质:

1. $0 \leqslant f_n(A) \leqslant 1$
2. $f_n(S) = 1$
3. 设$A_1, A_2, \cdots, A_k$两两互不相容, 则$f_n(\bigcup_{i=1}^{k}A_{i}) =  \sum_{i=1}^{k}f_n(A_i)$
4. $f_n(A)$随n的增大渐趋稳定, 稳定值为p.

### 概率

#### 定义

##### 统计性定义

当试验的次数增加时, 随机时间A发生的频率的稳定值p成为概率, 记为P(A) = p.

##### 公理化定义

设随机试验对应的样本空间为S, 对每个时间A定义P(A),满足

1. 非负性: $P(A) \geq 0$;
2. 规范性: P(S) = 1;
3. 可列可加性: $A_1, A_2,\cdots$两两互斥,即$A_iA_j=\varnothing, i \neq j$, 称$P(\bigcup_{i=1}^{\infty}A_i) = \sum_{i=1}^{\infty}P(A_i)$

称P(A)为事件A的概率.

#### 性质

1. P($\varnothing$) = 0

2. $P(A) = 1- P(\overline{A})$

3. 有限可加性: $A_1,A_2,\cdots,A_n, A_IA_j = \varnothing, i \neq j \Rightarrow P(\bigcup_{i=1}^{n}A_i) = \sum_{i=1}^{n}P(A_i)$

4. 若$A\subset B$, 则有P(B-A) = P(B) -P(A)

5. 概率的加法公式: $P(A \cup B) = P(A) + P(B) + P(AB)$

   #5的推广1:

   $P(A \cup B \cup C) = P(A) +P(B) +P(C) - P(AB) - P(AC) - P(BC) +P(ABC)$

   #5的推广2(一般情形):

   $P(\bigcup_{i=1}^{n}A_i) = \sum_{i=1}^{n}P(A_i) - \sum_{1\leq i < j \leq n}P(A_iA_j) + \sum_{1 \leq i < j < k \leq n}P(A_iA_jA_k) + \cdots + (-1)^{n-1}P(A_1A_2 \cdots A_n)$

## 等可能概型(古典概型)

> 若试验满足:
>
> * 样本空间S中样本点有限(有限性)
> * 出现每一个样本点的概率相等(等可能性)
>
> 称这种试验为等可能概型(或古典概型)
>
> $P(A) = \frac {A中包含的样本点数} {S中的样本点数}$

例子: n次抽奖, 不论先后, 概率都是一样的

## 条件概率

### 定义

$P(B | A) = \frac {P(AB)} {P(A)}, P(A) \neq 0$

性质:

1.  非负性: $P(B|A) \geq 0$

2. 规范性: $P(S|A) = 1$

3. 可列可加性: $B_1,B_2,\cdots, B_iB_j = \varnothing, i \neq j, 则 P(\bigcup_{i=1}^{\infty}B_i | A) = \sum_{i=1}^{\infty}P(B_i | A)$

4. 具有概率的所有性质

   $P(B | A) = 1 - P(\overline{B} | A)$

   $P(B \cup C | A) = P(B | A) + P(C | A) - P(BC | A)$

   $B \supset C \Rightarrow P(B | A) \geq P(C | A)$

### 乘法公式

当下面的条件概率都有意义时:

$P(AB) = P(A) \cdot P(B | A) = P(B) \cdot P(A | B)$

$P(ABC) = P(A) \cdot P(B | A) \cdot P(C | AB)$

$P(A_iA_j \cdots A_n) = P(A_1) \cdot P(A_2 | A_1) \cdot P(A_3 | A_1A_2) \cdots P(A_n | A_1 \cdots A_{n-1})$

## 全概率公式和贝叶斯公式

### 全概率公式定理: 
设$B_1,B_2,\cdots,B_n为S的一个划分$, 满足如下条件, 且$P(B_i) > 0$, 则有全概率公式: $P(A) = \sum_{j=1}^{n}P(B_j) \cdot P(A | B_j)$

  1. 不漏 $B_1 \cup B_2 \cup \cdots \cup B_n = S$

  2. 不重复 $B_iB_j = \varnothing, i \neq j$

### 贝叶斯公式定理: 

设$B_1,B_2,\cdots,B_n$为S的一个划分切$P(B_i) > 0$, 对$P(A) > 0$有Bayes公式: $P(B_i | A) = \frac {P(B_i)P(A | B_i)} {\sum_{j=1}^{n}P(B_j)P(A | B_j)} = \frac {p_iq_i}{\sum_{j=1}^{n}p_jq_j}$

## 事件独立性

### 定义

设A,B是两随机事件, 如果$P(AB) = P(A)P(B)$. 则称A,B相互独立

### 推论

1. $若P(A) > 0, P(B) > 0$, 则$P(AB) = P(A)P(B) \Leftrightarrow P(B|A) = P(B) \Leftrightarrow P(A|B) = P(A)$
2. $A,B相互独立\Leftrightarrow \overline A,B相互独立\Leftrightarrow A,\overline B相互独立\Leftrightarrow \overline A, \overline B相互独立$

### 相互独立

定义: 设$A_1,A_2,\cdots,A_n为n个随机事件, 若对2\leq k \leq n, 均有P(A_{i_1}A_{i_2}\cdots A_{i_n}) = \prod_{j=1}^{k} P(A_{i_j}), 则称A_1,A_2,\cdots,A_n相互独立$

特别地, 对与事件A,B,C相互独立的定义为:

1. 两两独立: $P(AB) = P(A)P(B), P(AC) = P(A)P(C), P(BC)=P(B)P(C)$

2. $P(ABC) = P(A)P(B)P(C)$

   以上1,2才能构成相互独立(即, 两两独立不能推到出相互独立)

# 随机变量及其分布

## 随机变量

### 定义:

被随机试验的样本空间为S,若$X = X(e)$为定义在S上的实值单值函数,则称$X(e)$为随机变量, 简写为$X$.

### 说明:

1. 随机变量$X(e): S\rightarrow R为一映射, 其自变量具有随机性$

2. $随机时间可以表示为A=\{ e:X(e)\in I\} = \{X\in I\}, I \subset R$

   如: 将一枚均匀的硬币抛掷3次, 样本空间为:

   $S=\{正正正,正正反,正反正,正反反,反正正,反正反,反反正,反反反\}$ 

   $ 若X表示3次中出现正面的次数$, 

   $则随机事件A=\{正面出现了一次\}=\{正反反, 反正反, 反反正\}=\{e: X(e) = 1\} = \{X = 1\}$

   $随机事件B=\{3次出现的情况相同\}=\{正正正,反反反\}=\{X=0或3\}$

   $随机事件C=\{正面至少出现了一次\} = \{X \geq 1\}$

3. $对于i \neq j,则必有\{X=i\} \cap \{X=j\}=\varnothing$, 一一映射,不可以一对多, 可以多对一

### 离散型和连续型随机变量

#### 离散型

##### 定义:

若随机变量X的取值为有限个或可数个, 则称X为离散型随机变量

##### 概率分布律

分布律: 1. 随机变量的所有可能取值; 2. 取每个可能取值对应的概率

性质: $p_k \geq 0, \sum_{k=1}^{\infty}p_k=1$, 另一种表示形式: $P(X=x_k)=p_k, k=1,2,\cdots.$

#### 常见的离散型随机变量

1. 0-1分布

   若$X$的概率分布律为:

   | $X$  | 0     | 1    |
   | ---- | ----- | ---- |
   | $P$  | $1-p$ | $p$  |

   其中$0<p<1,就成X服从参数为p的0-1分布(或两点分布),记为X \sim 0-1(p)或X\sim B(1,p)$,其分布律还可以写为: $P(X=k)=p^k(1-p)^{1-k},k=0,1$

   

