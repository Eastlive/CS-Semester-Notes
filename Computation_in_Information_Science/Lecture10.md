# 1 The SLR model (简单线性回归模型) (simple linear regression)
- straight line (直线)
- predictive linear relationship (预测线性关系)
$$Y = \beta_0 + \beta_1 X + \epsilon$$
- where
  - Y (dependent variable) (因变量)
  - X (independent variable) (自变量)
  - $\beta_0$ (intercept) (截距)
  - $\beta_1$ (slope) (斜率)
  - $\epsilon$ (error term) (误差项)
- regression line (回归线)
- regression coefficients (回归系数): $\beta_0$ and $\beta_1$
- 关于误差项$\epsilon$的假设
  - 误差项$\epsilon$的均值为0
  - 误差项$\epsilon$的方差为$\sigma^2$
  - 误差项$\epsilon$的分布为正态分布
  - 误差项$\epsilon$与因变量Y的关系是独立的
$$y_i - E(y_i) = \epsilon_i$$
- Fitted regression (拟合回归)
  - $\hat{y}_i = \hat{\beta}_0 + \hat{\beta}_1 x_i$
- Residual (残差)
  - $e_i = y_i - \hat{y}_i$
# 2 The method of least squared (最小二乘法)
- sum of squares of the errors (误差平方和)
$$SSE = \sum_{i=1}^{n} e_i^2 = \sum_{i=1}^{n} (y_i - \hat{y}_i)^2$$
$$\hat{\beta}_1 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n} (x_i - \bar{x})^2}$$
$$\hat{\beta}_0 = \bar{y} - \hat{\beta}_1 \bar{x}$$
$$SS_{xx} = \sum_{i=1}^{n} (x_i - \bar{x})^2$$
$$SS_{yy} = \sum_{i=1}^{n} (y_i - \bar{y})^2$$
$$\hat{\beta}_1 = \frac{SS_{xy}}{SS_{xx}}$$
$$\hat{\beta}_0 = \bar{y} - \hat{\beta}_1 \bar{x}$$

# 3 Properties of the least-squared fit (最小二乘法的性质)
- 列表：

| x | y | $\hat{y}$ | $\hat{e}$ |
| - | - | - | - |
| $x_1$ | $y_1$ | $\hat{y}_1$ | $\hat{e}_1$ |
| $x_2$ | $y_2$ | $\hat{y}_2$ | $\hat{e}_2$ |
| ... | ... | ... | ... |
- 性质：
  - 拟合线必过$(\bar{x}, \bar{y})$
  - 观测值的平均值与拟合值的平均值相等
  - 残差的平均值为0
  - 残差$\hat{e}_i$与拟合值$\hat{y}_i$的相关系数为0
  - 误差项$\epsilon_i$是独立的
  - 误差项$\epsilon_i$的方差为$\sigma^2$
  - constant variance (恒定方差)
    $$s^2 = \frac{SSE}{n-2} = \frac{SS_{yy} - \hat{\beta}_1 SS_{xy}}{n-2}$$
# 4 Regression with R (R语言中的回归)
- R语言中的回归函数：
  - lm() (linear model) (线性模型)
  - summary() (摘要)
  - predict() (预测)
  - plot() (绘图)
  - abline() (画线)
# 5 Residual plots (残差图)
- scatter plot (散点图)
# 6 Prediction intervals (预测区间)