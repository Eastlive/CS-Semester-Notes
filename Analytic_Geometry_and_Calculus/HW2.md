# HW8

1. 计算梯度，并求其在指定点的值，以及在某个方向上的变化率（rate of change）
2. 计算函数在某点的最大变化率，以及变化率最大的方向
3. 求函数在某点的切平面和法线方程

# HW9

1. 求函数的驻点（stationary point）
    1. 求梯度（gradient）
    2. 求梯度为0的点
    3. 计算二阶偏导数，判断是否为极值点（extremum）
        1. 计算 $D = f_{xx}f_{yy}-f_{xy}^2$
        2. 若 $D>0$，则为极值点
            1. 若 $f_{xx}>0$，则为极小值点（local minimum）
            2. 若 $f_{xx}<0$，则为极大值点（local maximum）
        3. 若 $D<0$，则为鞍点（saddle point）
        4. 若 $D=0$，则无法判断
2. 求函数在某个定义域中的极值
    1. 求梯度
    2. 求梯度为0的点
    3. 计算二阶偏导数，判断是否为极值点
        1. 计算 $D = f_{xx}f_{yy}-f_{xy}^2$
        2. 若 $D>0$，则为极值点
            1. 若 $f_{xx}>0$，则为极小值点
            2. 若 $f_{xx}<0$，则为极大值点
        3. 若 $D<0$，则为鞍点
        4. 若 $D=0$，则无法判断
    4. 求边界上的极值
    5. 比较所有极值，得出最大值和最小值
3. 求球内接长方体的最大体积

# HW10

1. 用拉格朗日乘子法（Lagrange multiplier）求函数在某个定义域中的极值
    1. 拉格朗日函数（Lagrange function）：$L(\mathbf{x},\lambda)=f(\mathbf{x})+\lambda g(\mathbf{x})$
    2. 求$L$的最值
2. 拉格朗日乘子法的不等式约束
    1. 求f的最值
    2. 求L的最值
3. 求两个约束条件的拉格朗日乘子法
4. 拉格朗日乘子法在∇𝑔=0的情况下失效
5. 求二重积分

# HW11

1. 求定义域$D$下的二重积分
2. 求二重积分
    1. type I: y的值由x决定
    2. type II: x的值由y决定
3. 计算二重积分并确定迭代顺序
    1. 画图
4. 求三重积分
5. 求二重积分转换为极坐标
    1. 公式：$dxdy=rdrd\theta$，$x=rcos\theta$，$y=rsin\theta$
6. 求三重积分转换为柱坐标
    1. 公式：$dxdydz=rdrd\theta dz$，$x=rcos\theta$，$y=rsin\theta$，$z=z$
7. 通过观察二重积分的图形，转换为极坐标

# HW12

1. 二重积分应用题
    1. 求面积
    2. 求质量：$m=\int\int_D\rho(x,y)dxdy$
    3. 求质心：
    $$\bar{x}=\frac{1}{m}\int\int_Dx\rho(x,y)dxdy$$
    $$\bar{y}=\frac{1}{m}\int\int_Dy\rho(x,y)dxdy$$
    4. 求转动惯量：
    $$I_x=\int\int_D(y-y_0)^2\rho(x,y)dxdy$$
    $$I_y=\int\int_D(x-x_0)^2\rho(x,y)dxdy$$
    $$I_z=\int\int_D(x-x_0)^2+(y-y_0)^2\rho(x,y)dxdy$$

# HW13

1. 求三重积分
    1. 柱坐标（cylindrical coordinates）：
    $$dxdydz=rdrd\theta dz$$
    $$x=rcos\theta$$
    $$y=rsin\theta$$
    $$z=z$$
    2. 球坐标（spherical coordinates）：
    $$dxdydz=\rho^2sin\phi d\rho d\theta d\phi$$
    $$x=\rho sin\phi cos\theta$$
    $$y=\rho sin\phi sin\theta$$
    $$z=\rho cos\phi$$
2. 三重积分求质心
    1. 公式
    $$\bar{x}=\frac{1}{m}\int\int\int_Dx\rho(x,y,z)dxdydz$$
    $$\bar{y}=\frac{1}{m}\int\int\int_Dy\rho(x,y,z)dxdydz$$
    $$\bar{z}=\frac{1}{m}\int\int\int_Dz\rho(x,y,z)dxdydz$$
