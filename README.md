# math
AI-assisted mathematical research

## 孙智伟加权二项式和整除猜想

论文研究孙智伟 [Conjecture 4.3(ii)](https://arxiv.org/html/2505.02767v4) 中的第一条整性断言。定义整数序列

$$
a_n=\sum_{i,j=0}^{n}\binom ni^2\binom nj^2\binom{i+j}{i}\,2^{i+j}3^{2n-i-j}.
$$

猜想断言：对每个正整数 $n$，都有

$$
T_n=\frac{2}{n}\sum_{k=0}^{n-1}(3k+2)a_k\in\mathbb Z.
$$

论文的证明分为三步：

1. 将 $a_n$ 写成多项式幂的对角系数，通过二项式变换和显式微分恒等式证明 $24T_n\in\mathbb Z$，使可能的分母素因子只剩 $2,3$。
2. 利用序列模 $2^s$ 的周期性和分块归纳，证明 $T_n$ 的分母不含 $2$。
3. 将三进整性问题转化为生成函数的有限奇次幂展开，通过有限原函数的分母估计与余项估计，证明 $T_n$ 的分母不含 $3$。

由此得到 $T_n\in\mathbb Z$，即证明上述整性断言。

- [阅读论文 PDF](sun猜想/sun_binomial_divisibility_advmath.pdf)
- [查看 LaTeX 源码](sun猜想/sun_binomial_divisibility_advmath.tex)
