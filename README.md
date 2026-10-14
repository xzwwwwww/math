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

## 二进制局部模式计数的对数凹性

论文研究 Elizalde、Rivera 和 Zhuang 的 [Conjecture 4.6](https://doi.org/10.1007/s00026-026-00805-1) 中，模式避免排列类 $\mathfrak S_n(123,132)$ 与 $\mathfrak S_n(132,213)$ 的两个等价分支。原文的统计保持双射将大下降数（满足 $\pi_i>\pi_{i+1}+1$ 的位置数）转化为末位为 $1$ 的二进制字符串中连续模式 $10$ 与 $011$ 的出现次数之和。

定义计数序列

```math
b_{n,k}=\#\{w\in\{0,1\}^n:w_n=1,\ \mathrm{occ}_{10}(w)+\mathrm{occ}_{011}(w)=k\},
```

其中每个起始位置分别计数，允许模式出现相互重叠。论文证明：对每个 $n\ge1$ 和整数 $k$，都有

$$
b_{n,k}^2\ge b_{n,k-1}b_{n,k+1}.
$$

正支集恰为 $0\le k\le d_n$，其中 $d_n=\lfloor2(n-1)/3\rfloor$；当 $1\le k<d_n$ 时，上式严格成立。

论文的证明分为四步：

1. 通过零、一游程分解，得到非负二项式和 $b_{n,k}=\sum_{r\ge0}\binom{r+1}{k+1-r}\binom{n-r-1}{k}$，并用辅助变量记录游程数，将对数凹差式分成固定次数层。
2. 利用 Fibonacci 铺砖多项式的实根结构与非负线性形式乘积的系数提取，证明固定次数层中的尾词平衡不等式。
3. 利用铺砖多项式的 Cassini 恒等式、差列的单次变号及尾词权重的中央单调性，证明中央集中，从而处理全部高次层。
4. 显式计算奇数指标下唯一可能为负的最低项，证明紧邻系数足以完全补偿它，得到全参数对数凹性及正支集内部的严格对数凹性。

由统计保持双射，上述结论证明了 Conjecture 4.6 中 $\mathfrak S_n(123,132)$ 与 $\mathfrak S_n(132,213)$ 的两个等价分支。正文证明覆盖全部参数，不依赖有限范围计算。

- [阅读论文 PDF](对数凹猜想/binary_pattern_log_concavity.pdf)
- [查看 LaTeX 源码](对数凹猜想/binary_pattern_log_concavity.tex)
