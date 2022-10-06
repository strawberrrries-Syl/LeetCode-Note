# 1  `PSNR`
Peak Signal-to-Noise Ratio - 峰值信噪比
# 1.1 算法：
* 计算原图与编码后图像的`MSE`（均方差）-Mean Square Error.
* 带公式：
$$
10 \times log_{10}(\frac{MAX_I^{2}}{MSE})
$$

**数值越高，效果越好**

# 2. `SSIM` 
Structural Similarity. 结构相似性.
# 2.1 原理：
SSIM公式基于样本$x$和$y$之间的三个比较衡量，亮度`luminance`，对比度`contrast`，和结构`structure`。

$$
l(x,y) = \frac{2 \mu _x\mu_y + c_1 }{\mu_x^2 + \mu_y^2 + c_1} c(x,y) = \frac{2 \sigma_x\sigma_y + c_2 }{\sigma_x^2 + \sigma_y^2 + c_2} s(x,y) = \frac{\sigma_{xy} + c_3 }{\sigma_x\sigma_y + c_3}

$$

$c_1, c_2$为常数，避免除零

$$SSIM(x,y) = [l(x,y)^{\alpha} \cdot c(x,y)^{\beta} \cdot s(s,y)^{\gamma}]$$

一般 $\alpha, \beta, \gamma$都取1， 故
$$SSIM = \frac{(2\mu_x\mu_y + c_1)(2\sigma_{x,y}+c_2)}{(\mu_x^2 + \mu_y^2 + c_1)(\sigma_x^2 + \sigma_y^2 + c_2)}$$

一般是取NxN的窗口，滑动计算，取均值

**接近1，效果最好**

