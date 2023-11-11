# 1

# 2

- `sample_space <- expand.grid(S1=x, S2=y)`

# 3 贝叶斯

# 4 二项分布 Binomial

- dbinom(3, size=10, prob=0.5) 表示二项分布的概率质量函数
  - $$P(X=3)=\binom{10}{3}0.5^3(1-0.5)^{10-3}$$
- pbinom(3, size=10, prob=0.5) 表示二项分布的累积分布函数
  - $$P(X\leq3)=\sum_{i=0}^3\binom{10}{i}0.5^i(1-0.5)^{10-i}$$
- qbinom(0.5, size=10, prob=0.5) 表示二项分布的分位数函数
  - $$P(X\leq5)=0.5$$

# 5 泊松分布 Poisson

- dpois(3, lambda=2) 表示泊松分布的概率质量函数
  - $$P(X=3)=\frac{2^3}{3!}e^{-2}$$
- ppois(3, lambda=2) 表示泊松分布的累积分布函数
  - $$P(X\leq3)=\sum_{i=0}^3\frac{2^i}{i!}e^{-2}$$
- 泊松分布证明
  - $$P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}$$
  - $$E(X) = Var(X) = \lambda$$

# 6 指数分布 Exponential

- dexp(3, rate=2) 表示指数分布的概率密度函数
  - $$f(x)= \frac{1}{\lambda}e^{-\frac{x}{\lambda}}$$
  - $$rate = \lambda$$
- pexp(3, rate=2) 表示指数分布的累积分布函数
  - $$F(x)=1-e^{-\lambda x}$$

# 7 正态分布 Normal

- dnorm(3, mean=2, sd=1) 表示正态分布的概率密度函数
  - $$f(x)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
- pnorm(3, mean=2, sd=1) 表示正态分布的累积分布函数
  - $$F(x)=\frac{1}{\sqrt{2\pi}\sigma}\int_{-\infty}^xe^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
- pnorm(3) - pnorm(-3) = 0.9973002

# 8 泊松分布

- rpois(100, lambda=2) 表示泊松分布的随机数
  - $$P(X=k)=\frac{e^{-\lambda}\lambda^k}{k!}$$
  - $$E(X) = Var(X) = \lambda$$