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

   若$X$的概率分布律为(随机变量只可能取0，1两个值):

   | $X$  | 0     | 1    |
   | ---- | ----- | ---- |
   | $P$  | $1-p$ | $p$  |

   其中$0<p<1,就成X服从参数为p的0-1分布(或两点分布),记为X \sim 0-1(p)或X\sim B(1,p)$,其分布律还可以写为: $P(X=k)=p^k(1-p)^{1-k},k=0,1$

   $(X服从退化分布：若P(X=c)=1)$
   
   只有两个可能结果的试验，成为贝努利试验， 故亮点分布有时也被称为贝努利分布
   
2. 二项分布(基于n重贝努利分布)

   设$X$表示$n$重贝努利试验中结果A发生的次数，则$X$的可能取值为$0,1,\cdots,n$,且$P\{X=k\}=C_n^kp^k(1-p)^{(n-k)}$

   定义：

   若X的概率分布律为$P\{X=k\}=C_n^kp^k(1-p)^{(n-k)}, k=0,1,\cdots,n,其中n\geq1,0<p<1,就称X服从参数为n,p的二项分布(Binomial)，记作 X\sim B(n,p)$

3. 泊松分布(Poisson)

   $若X的概率分布律为P(X=k)=\frac {\lambda^ke^{-\lambda}} {k!},k=0,1,2,\cdots,其中\lambda>0,就称X服从参数为\lambda的泊松分布,记作X\sim \pi(\lambda)或X\sim P(\lambda)$

   Note: 根据泰勒展开式可得: $e^{\lambda}=\sum_{k=0}^{+\infty}\frac {\lambda^k} {k!}$

| 二项分布和泊松分布有以下近似公式：                           |
| ------------------------------------------------------------ |
| $当n>10,p<0.1时, C_n^kp^k(1-p)^{n-k}\approx \frac {e^{-\lambda}\lambda^k}{k!},其中\lambda=np.$ |

即当n>10,p<0.1时，二项分布B(n,p)可以用泊松分布$\pi(np)$来近似

4. 几何分布

   若X的概率分布律为$P(X=k)=p(1-p)^{k-1},k=1,2,3,\cdots,其中0<p<1,称X服从参数为p的几何分布，记为X\sim Geom(p)$

   用途: 在重复多次的贝努利试验中，试验进行到某种结果出现第一次位置，此时的试验总次数服从几何分布。

## 分布函数

### 定义：

$随机变量X,对任意实数x,称函数$

​		$F(x) = P(X\leq x), 有时也写作F_X(x)=P(X\leq x)$

$为X的概率分布函数，简称分布函数$

### 用途：

可以给出随机变量落入任意一个范围的可能性。

| $X的分布函数为F(x), a,b为两个实数，a<b, 则$                  |
| ------------------------------------------------------------ |
| $P(a<x\leq b)=P(X\leq b)-P(X\leq a)=F(b)-F(a)$ <br />$P(a<X<b)=P(a<X\leq b-0)=F(b-0)-F(a)$<br />$P(X=b)=P(X\leq b)-P(x<b)=F(b)-F(b-0)$ <br />$P(a<X<b)=P(a<X\leq b)-P(X=b)$ |

| 一般地，离散型随机变量的分布函数为阶梯函数                   |
| ------------------------------------------------------------ |
| 设离散型随机变量$X$的分布律为$P\{X=x_k\}=p_k,k=1,2,\cdots$<br />$X$的分布函数为$F(X=\sum_{x_k\leq x}p_k)$<br />$F(x)$在$x=x_k,(k=1,2,\cdots)$处有跳跃，其跳跃值为$p_k=P\{X=x_k\}$ |

### 性质：

1. $0\leq F(x)\leq 1$
2. $F(x)$单调不减      因为 对于任意$x_1<x_2,有0\leq P(x1<X\leq x_2)=F(x_2)-F(x_1)$
3. $F(-\infty)=0, F(+\infty)=1$
4. $F(x)$是右连续函数，即$F(x+0)=F(x)$

## 连续型随机变量及其概率密度

### 定义

对于随机变量$X$的分布函数$F(x)$,若存在非负的函数f(x),使对于任意实数$x$有：

$F(x)=\int_{-\infty}^{x}f(t)dt$

则称$X$为<font color=Blue>连续型随机变量</font>, 其中$f(x)$成为$X$的<font color=Blue>概率密度函数</font>,简称概率密度。有时也写为$f_X(x)$

### $f(x)$的性质

1. $f(x)\geq0$

2. $\int_{-\infty}^{+\infty}f(x)dx=1$

3. 对于任意的实数$x_1,x_2(x_1<x_2)$

   $P(x_1<X\leq x_2)=\int_{x_1}^{x_2}f(t)dt$;

   $\Rightarrow$对任意的实数a，$P(X=a)=0$. 且$P(x_1<X\leq x_2)=P(x_1<X<x_2)$

   对于连续型的随机变量$X$,有$P(X\in D)=\int_{D}f(x)dx,任意D\sub R.$

4. 在$f(x)$连续点$x,F'(x)=f(x)$.

   即在$f(x)$的连续点，

   $f(x)=F'(x)=\lim_{\Delta x\rightarrow0}\frac{F(x+\Delta x)-F(x)}{\Delta x}=\lim_{\Delta x\rightarrow 0}\frac{P(x<X\leq x+\Delta x)}{\Delta x}$

   $P(x<X\leq x+\Delta x)\approx f(x)\cdot\Delta x$

   这表示X落在点x附近$(x,x+\Delta x]$的概率近似等于$f(x)\Delta x$

### 说明

1. $f(x)$值的含义：

   当$\Delta x$充分小时，$P(x<X\leq x+\Delta x)\approx f(x)\cdot\Delta x$

2. $f(x)$的值是可以大于1的

3. $F(x)=\int_{-\infty}^{x}f(t)dt$

   $f(x)=\frac{d}{dx}F(x)$

## 均匀分布和指数分布

### 均匀分布

#### 定义

若$X$的概率密度函数为
$$
f(x)=
\begin{cases}
\frac{1}{b-a},&&x\in (a,b); \\
0,&&其他.
\end{cases}
$$
其中$a<b$,就称$X$服从$(a,b)$上的<font color=Blue>均匀分布(Uniform)</font>,记为$X \sim U(a,b)$或$X \sim Unif(a,b)$.

#### 性质

均匀分布具有等可能性

即，对于任意的$a<k<k+l<b$,均有$P(k<X<k+l)=\int_k^{k+l}\frac{1}{b-a}dt=\frac{l}{b-a}$,与$k$无关，仅与$l$有关。

即，服从$U(a,b)$上的均匀分布的随机变量X落入$(a,b)$中的任意自取件上的概率只与其区间长度有关， 与区间所处的位置无关

#### 均匀分布的概率计算

若$X\sim U(a,b)$,则对于$\forall I\sub R$,有

法一： $P(X\in I)=\int_{I}f(x)dx$

法二：$P(X\in I)=\frac{I\bigcap (a,b) 的长度}{(a,b)的长度}$

### 指数分布

#### 定义

若$X$的概率密度函数为
$$
f(x)=
\begin{cases}
\lambda e^{-\lambda x},&&x>0;\\
0,&&x\leq0,
\end{cases}
$$
其中$\lambda>0$,就称$X$服从参数为$\lambda$的<font color=Blue>指数分布(Exponential)</font>,记为$X\sim E(\lambda)$或$X\sim Exp(\lambda)$

分布函数为：
$$
F(x)=
\begin{cases}
1-e^{-\lambda x},&&x>0;\\
0,&&x\leq0.
\end{cases}
$$

#### 性质

<font color=Blue>指数分布具有无记忆性</font>

对于$t_0>0,t>0$,

$P(X>t_0+t|X>t_0)=\frac{P(X>t_0+t,X>t_0)}{P(X>t_0)}=\frac{P(X>t_0+t)}{P(X>t_0)}=\frac{1-F(t_0+t)}{1-F(t_0)}=\frac{e^{-\lambda(t_0+t)}}{e^{-\lambda t_0}}=e^{-\lambda t}=P(X>t)$

#### 指数分布的用途

1. 可以用来表示独立随机事件发生的时间间隔，比如旅客进机场的时间间隔、中文维基百科新条目出现的时间间隔等等；
2. 在排队论中，一个顾客接受服务的时间长短也可以用指数分布来近似
3. 无记忆性的现象(连续时)

## 正态分布

### 定义

若$X$的概率密度函数为$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-u)^2}{2\sigma ^2}},-\infty<x<+\infty$,其中$-\infty<\mu<\infty,\sigma>0$,就称$X$服从参数为$\mu,\sigma$的<font color=Blue>正态分布</font>(或高斯分布),记为$X\sim N(\mu,\sigma^2)$

### 特征

1. $f(x)$关于$x=\mu$对称；
2. 当$x\leq\mu$时，$f(x)$时严格单调递增函数；
3. $f_{max}=f(\mu)=\frac{1}{\sqrt{2\pi}\sigma}$;
4. $\lim_{|x-\mu|\rightarrow\infty}f(x)=0$

### 两个参数的含义：

1. 当固定$\sigma$，改变$\mu$的大小时，$f(x)$图形的形状不变，只是沿着$x$轴作平移变换；$\color{blue}\mu$<font color=Blue>称为位置参数</font>(决定对称轴位置)
2. 当固定$\mu$,改变$\sigma$大小时,$f(x)$图形的对称轴不变，而形状在改变,$\sigma$越小,图形越高越瘦,$\sigma$越大，图形越胖越矮。$\color{blue} \sigma$<font color=Blue>称为尺度参数</font>(决定曲线分散程度)

![正态分布图像](https://github.com/cosedahe/Math/blob/terry/ProbabilityAndStatistics/images/正态分布图形.png?raw=true)

### 正态分布的用途

1. 自然界和人类社会中很多现象可以看做正态分布

   如： 人的胜利尺寸(身高、体重);

   ​		医学检验指标(红细胞数、血小板);

   ​		测量误差等等

2. 多个随机变量的和可以用正态分布来近似

   如: 注册MOOC的某位同学完成所有作业的时间;二项分布;等等(By 中心极限定理)

### 标准正态分布

若$Z\sim N(0,1)$,称$Z$服从标准正态分布。

$Z$的概率密度函数:$\varphi(z)=\frac{1}{\sqrt{2\pi}}e^{-\frac{z^2}{2}}$.

$Z$的分布函数:$\phi(z)=\int_{-\infty}^z\frac{1}{\sqrt{2\pi}}e^{-\frac{t^2}{2}}dt$.

重要性质: $\color{blue}{\phi(-z_0)=1-\phi(z_0)}$,对于任意的实数$z_0$都成立。  因为关于y轴对称。

![标准正态分布表](https://github.com/cosedahe/Math/blob/terry/ProbabilityAndStatistics/images/标准正态分布表.jpeg?raw=true)

### 正态分布转换成标准正态分布

性质： 当$X\sim N(\mu,\sigma^2)$时, $\frac{X-\mu}{\sigma}\sim N(0,1)$.

即：当$X\sim N(\mu,\sigma^2)$时，对于任意实数$a$,有$F_X(a)=P(X\leq a)=P(\frac{X-\mu}{\sigma}\leq\frac{a-\mu}{\sigma})=\Phi(\frac{a-\mu}{\sigma})$

## 随机变量函数的分布

一般，若已知$X$的概率分布, $Y=g(x)$, 求$Y$的概率分布的过程为：

<font color=Blue>先给出Y的可能取值，再利用等价事件来给出概率分布</font>

- 若$X$为离散型随机变量，则先写出$Y$的可能取值: $y_1,y_2,\cdots,y_j,\cdots;$

  再找出$\{Y=y_j\}$的等价事件$\{X\in D\}$, 得$P(Y=y_j)=P(X\in D)$

- 若$X$为连续型随机变量，先根据$X$的取值范围，给出$Y$的取值范围; 然后写出$Y$的概率分布函数: $F_Y(y)=P(Y\leq y)$, 找出$\{Y\leq y\}$的等价事件$\{X\in D\}$, 得$F_Y(y)=P(X\in D)$; 再求出$Y$的概率密度函数$f_Y(y)$.

### 定理

设随机变量$X\sim f_X(x),-\infty<x<+\infty, Y=g(x),g'(x)>0(或g'(x)<0)$, 则$Y$具有概率密度为:
$$
f_Y(y)=
\begin{cases}
f_X(h(y))\cdot |h'(y)|,&&\alpha<y<\beta,\\
0,&&其他
\end{cases}
$$
<font color=Blue>**注意：**</font>

- 这里$(\alpha,\beta)$是$Y$的取值范围，其中: $\alpha=g(-\infty),\beta=g(+\infty)$.

  当$g'(x)<0时, \alpha=g(+\infty), \beta=g(-\infty)$

- $h$是$g$的反函数， 即$h(y)=x\Leftrightarrow y=g(x)$

# 多维随机变量

## 二元随机变量

设$E$是一个随机试验，样本空间$S=\{e\}$; 设$X=X(e)$ 和 $Y=Y(e)$ 是定义在$S$上的随机变量，由他们构成的向量$(X,Y)$成为二维随机向量或二维随机变量。

## 二元离散型随机变量

若二元随机变量$(X,Y)$全部可能取到的不同值是有限对或可列无限对，则称$(X,Y)$是二元离散型随机变量。

### 离散型随机变量的联合概率分布律

设$(X,Y)$所有可能取值为$(x_i,y_j)$, 称$P(X=x_i,Y=y_j)=P_{ij}; i,j=1,2,\cdots$为二元离散型随机变量$(X,Y)$的联合概率分布律。也可建成$(X,Y)$的分布律

#### 联合分布律的性质

1. $P_{ij}\geq0$
2. $\sum_{i=1}^{\infty}\sum_{j=1}^{\infty}p_{ij}=1$
3. $P((X,Y)\in D)=\sum_{(x_i,y_j)\in D}p_{ij}$

其中$P_{ij}=P(X=x_i,Y=y_j); i,j=1,2,\cdots$



