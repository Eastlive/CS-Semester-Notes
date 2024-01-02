# 1 Sampling distributions (抽样分布)
- standardize sample mean (标准化样本均值) (z-score)
  $$Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}$$
  - 其中 $n$ 为样本容量
- standard error of the mean (标准误差)
  $$SE = \frac{\sigma}{\sqrt{n}}$$
- CLT (Central Limit Theorem) (中心极限定理)
  - 样本容量足够大时，样本均值的抽样分布近似服从正态分布
  - 样本容量足够大时，样本均值的抽样分布近似服从正态分布
  - 样本容量足够大时，样本均值的抽样分布近似服从正态分布
  - 重要的事情说三遍
- P(Z ≤ z) (标准正态分布的累积分布函数)
  - 代码：
    ```R
    # P(Z ≤ -2.5)
    pnorm(-2.5)
    # 结果：0.006209665
    ```
# 2 Point estimation (点估计)
- point estimate (点估计)：$\hat{\theta}$
  - 点估计的意思是，用样本统计量来估计总体参数
- hat notation (帽子符号)：$\hat{\theta}$
  - 用来表示样本统计量
- estimator (估计量)
- statistic (统计量)
# 3 Interval estimation (区间估计)
- interval estimate (区间估计)：$(\hat{\theta}_L, \hat{\theta}_U)$
  - 区间估计的意思是，用样本统计量来估计总体参数
  - P($\hat{\theta}_L$ ≤ θ ≤ $\hat{\theta}_U$) = 1 - α
  - 其中，α为显著性水平 (significance level)
- confidence interval (置信区间)：$\hat{\theta}_L ≤ θ ≤ \hat{\theta}_U$
  - 100(1 - α)% confidence interval (100(1 - α)% 置信区间)
  - confidence coefficient (置信系数)：1 - α
  - degree of confidence (置信度)：1 - α
  - confidence limits (置信限)：$\hat{\theta}_L$ 和 $\hat{\theta}_U$
  - CI (Confidence Interval) (置信区间) 99% CI (99% 置信区间) 此时，α = 0.01
  - we prefer a short interval with a high degree of confidence (我们更喜欢置信度高的短区间)
  - 点估计和区间估计是统计学中两种常用的参数估计方法，它们用于从样本数据推断总体参数（如均值、方差等）。
    1. **点估计（Point Estimation）**:
        - **定义**: 点估计是使用样本数据来计算一个单一值（点），作为总体参数的最佳估计。这个估计值代表了总体参数的可能取值。
        - **举例**: 如果我们想估计一个班级平均身高，我们可能会测量几个学生的身高，然后计算这些身高的平均值。这个平均值就是总体平均身高的点估计。
        - **特点**: 点估计简单直接，但它没有提供关于参数估计精确度的信息。换句话说，它不告诉我们估计值可能的误差大小。

    2. **区间估计（Interval Estimation）**:
        - **定义**: 区间估计是使用样本数据来计算一个区间，在统计意义上，我们相信这个区间内包含总体参数的真实值。区间估计不仅给出了参数的估计值，还提供了估计的不确定性。
        - **举例**: 继续上面的例子，如果我们说班级平均身高的95%置信区间是[1.65米, 1.75米]，这意味着我们有95%的信心认为真正的平均身高会落在这个区间内。
        - **特点**: 区间估计提供了更多关于估计不确定性的信息。置信区间的宽度可以反映估计的精确度，区间越宽，估计的不确定性越大。

总的来说，点估计提供了一个关于参数的具体估计值，而区间估计则提供了一个范围，表明参数可能的取值区间以及估计的可靠程度。在实际应用中，这两种估计方法通常结合使用，以获得更全面的统计推断。
# 4 Estimating the mean (估计均值)
## Single sample: Estimating the mean (单个简单随机样本估计均值)
- 公式：
  $$E(\bar{x}) = \mu$$
  $$Var(\bar{x}) = \frac{\sigma^2}{n}$$
  $$\bar{x} \sim N(\mu, \frac{\sigma}{\sqrt{n}})$$
  $$Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}} \sim N(0, 1) (\sigma \text{ is known})$$
  $$T = \frac{\bar{x} - \mu}{s / \sqrt{n}} \sim t(n - 1) (\sigma \text{ is unknown})$$
- 我们用$\bar{x}$来估计$\mu$，用$s$来估计$\sigma$，其中$\bar{x}$为样本均值，$s$为样本标准差，$n$为样本容量。
1. Point estimation of the mean μ (均值的点估计)
  $$\bar{X} = \frac{1}{n} \sum_{i=1}^{n} X_i$$
2. Interval estimation (C.I.) of the mean μ (均值的区间估计)
  1. The case of σ known (已知总体标准差)
  $$\mu \in (\bar{x} - z_{\alpha/2} \frac{\sigma}{\sqrt{n}}, \bar{x} + z_{\alpha/2} \frac{\sigma}{\sqrt{n}})$$
  - Rounding principles (四舍五入原则)
    - 保留小数点后一位
  - Interval estimate errors (区间估计误差)
    - 误差范围：$z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$
    - 误差范围随着样本容量的增加而减小
    - 误差范围随着置信度的增加而增大
  - Margin of error (误差范围)
    - 标记： $MRE = z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$
  2. The case of σ unknown (未知总体标准差)
  $$\mu \in (\bar{x} - t_{\alpha/2} \frac{s}{\sqrt{n}}, \bar{x} + t_{\alpha/2} \frac{s}{\sqrt{n}})$$
    - large-sample confidence interval (大样本置信区间)
    $$\bar{x} \pm z_{\alpha/2} \frac{\sigma}{\sqrt{n}}$$
    - when normality cannot be assumed, σ is unknown and n ⩾ 30 (当不能假设正态性，σ未知且n ⩾ 30时)
3. Standard error of a point estimate (点估计的标准误差)
  - standard error of the mean (均值的标准误差)
    $$s.e.(\bar{X}) = \frac{\sigma}{\sqrt{n}}$$
  - estimate of the standard error of the mean (均值的标准误差的估计)
    $$s.e.(\bar{x}) = \frac{s}{\sqrt{n}}$$
4. Prediction intervals (预测区间)
  - value of a future observation (未来观测值的值)
  - single observation (单个观测值)
  - prediction interval (预测区间)
  1. The case of σ known (已知总体标准差)
  $$x_0 \in (\bar{x} - z_{\alpha/2} \sigma \sqrt{1+\frac{1}{n}}, \bar{x} + z_{\alpha/2} \sigma \sqrt{1+\frac{1}{n}})$$
  2. The case of σ unknown (未知总体标准差)
  $$x_0 \in (\bar{x} - t_{\alpha/2} s \sqrt{1+\frac{1}{n}}, \bar{x} + t_{\alpha/2} s \sqrt{1+\frac{1}{n}})$$
- degree of freedom (自由度)
  - $v = n - 1$
  - 不同的自由度对应不同的t分布
## Two samples: Estimating the difference between two means (两个简单随机样本估计均值之差)
- 公式
  $$\mu_{\bar{X_1} - \bar{X_2}} = \mu_1 - \mu_2 = E(\bar{X_1} - \bar{X_2})$$
  $$\sigma_{\bar{X_1} - \bar{X_2}}^2 = \frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2} = Var(\bar{X_1} - \bar{X_2})$$
  $$\sigma_{\bar{X_1} - \bar{X_2}} = \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}$$
  $$Z = \frac{(\bar{X_1} - \bar{X_2}) - (\mu_1 - \mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}} \sim N(0, 1)$$
1. Point estimation of μ1 − μ2 (均值之差的点估计)
  $$\bar{X_1} - \bar{X_2}$$
2. Interval estimation (C.I.) of μ1 − μ2 (均值之差的区间估计)
  1. The case of σ1 and σ2 known (已知总体标准差)
  $$\mu_1 - \mu_2 \in (\bar{x_1} - \bar{x_2} - z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}, \bar{x_1} - \bar{x_2} + z_{\alpha/2} \sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}})$$
  2. The case of σ1 and σ2 unknown but equal (未知总体标准差但相等)
  $$\mu_1 - \mu_2 \in (\bar{x_1} - \bar{x_2} - t_{\alpha/2} s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}}, \bar{x_1} - \bar{x_2} + t_{\alpha/2} s_p \sqrt{\frac{1}{n_1} + \frac{1}{n_2}})$$
  - pooled standard deviation (合并标准差)
    $$s_p = \sqrt{\frac{(n_1 - 1) s_1^2 + (n_2 - 1) s_2^2}{n_1 + n_2 - 2}}$$
  3. The case of σ1 and σ2 unknown and unequal (未知总体标准差且不相等)
  $$\mu_1 - \mu_2 \in (\bar{x_1} - \bar{x_2} - t_{\alpha/2} \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}, \bar{x_1} - \bar{x_2} + t_{\alpha/2} \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}})$$
  - degrees of freedom (自由度)
    $$v = \frac{(\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2})^2}{\frac{(\frac{s_1^2}{n_1})^2}{n_1 - 1} + \frac{(\frac{s_2^2}{n_2})^2}{n_2 - 1}}$$
3. Paired observations (成对观测)
  - paired observations (成对观测)
  $$\mu_D \in (\bar{d} - t_{\alpha/2} \frac{s_D}{\sqrt{n}}, \bar{d} + t_{\alpha/2} \frac{s_D}{\sqrt{n}})$$
# 5 Estimating a proportion (估计比例)
- Single sample: Estimating a proportion (单个简单随机样本估计比例)
- 公式
  $$\hat{p} = \frac{x}{n}$$
  $$E(\hat{p}) = p$$
  $$Var(\hat{p}) = \frac{p(1-p)}{n}$$
  $$\hat{p} \sim N(p, \sqrt{\frac{p(1-p)}{n}})$$
  $$Z = \frac{\hat{p} - p}{\sqrt{\frac{p(1-p)}{n}}} \sim N(0, 1)$$
1. Point estimation of p (比例的点估计)
  $$\hat{p} = \frac{x}{n}$$
2. Interval estimation (C.I.) of p (比例的区间估计)
  $$p \in (\hat{p} - z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}, \hat{p} + z_{\alpha/2} \sqrt{\frac{\hat{p}(1-\hat{p})}{n}})$$
# 6 Estimating the variance (估计方差)
- Single sample: Estimating the variance (单个简单随机样本估计方差)
$$X^2 = \frac{(n-1)s^2}{\sigma^2} \sim \chi^2(n-1)$$
$$\frac{(n-1)s^2}{\chi^2_{\alpha/2}(n-1)} \leq \sigma^2 \leq \frac{(n-1)s^2}{\chi^2_{1-\alpha/2}(n-1)}$$
$$v = n - 1$$
- Two samples: Estimating the ratio of two variances (两个简单随机样本估计方差之比)
$$F = \frac{\sigma_2^2 S_1^2}{\sigma_1^2 S_2^2}$$
$$\frac{S_1^2}{S_2^2} \frac{1}{F_{\alpha/2}(v_1, v_2)} \leq \frac{\sigma_1^2}{\sigma_2^2} \leq \frac{S_1^2}{S_2^2} F_{\alpha/2}(v_2, v_1)$$
$$v_1 = n_1 - 1, v_2 = n_2 - 1$$
# 7 Statistical hypotheses (统计假设)
- hypothesis (假设)
  - null hypothesis (零假设)
  - alternative hypothesis (备择假设)
- hypothesis testing (假设检验)
# 8 Level of significance (显著性水平)
- level of significance (显著性水平)
  - α (alpha)
  - 1 - α (confidence coefficient)
  - 1 - α (degree of confidence)
# 9 One- and Two-tailed tests (单尾和双尾检验)
- one-tailed test (单尾检验)
  - $H_0: \theta = \theta_0, H_1: \theta > \theta_0$
  - $H_0: \theta = \theta_0, H_1: \theta < \theta_0$
- two-tailed test (双尾检验)
  - $H_0: \theta = \theta_0, H_1: \theta \neq \theta_0$
# 10 P-values (P值)
- P-value (P值)
  - P-value < α (reject $H_0$)
  - P-value > α (do not reject $H_0$)
$$P-value = P(\theta < -\theta_{obt}) + P(\theta > \theta_{obt})$$
# 11 Hypothesis tests concerning the mean (关于均值的假设检验)
- Single sample: Tests concerning a single mean (单个简单随机样本检验均值)
# 12 Hypothesis tests concerning a proportion (关于比例的假设检验)
- One sample: Test on a single proportion (large samples) (单个简单随机样本检验比例)