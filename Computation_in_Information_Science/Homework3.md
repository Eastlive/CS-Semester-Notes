# 1 汉明码的weight和Hamming Distance

- weight: 1的个数
- Hamming Distance: 两个码字不同的位数

# 2

- The maximum weight of a word in $Z^n_2$ is $n$.
- The maximum Hamming distance of two words in $Z^n_2$ is $n$.

# 3 汉明码

- distance = 3
- detect = distance - 1 = 2
- correct = (distance - 1) / 2 = 1

- 正常是(7,4)汉明码，(N,k)
- $$overhead or redundancy = \frac{N-k}{k}$$
- $$Coding rate = \frac{k}{N}$$

- 作业给了一个假的汉明码 (7,3)汉明码
- dist = 4
- dependent vector in G 指的是单位向量后面的那些向量

# 4 奇偶校验

- 单词： parity check word
- even parity: 偶校验： 1的个数是偶数
- odd parity: 奇校验： 1的个数是奇数
- $dist_{min}$ = 2
- $$Coding Rate = \frac{k}{N} = \frac{n-1}{n}$$

# 56离散

- $-D-$ 表示 `AND`
- $-)>-$ `OR`
- ))> XOR