# GAMES101

## 线性代数基础

### 定义与基本
- 向量定义：$\vec{AB} = B - A$
- 向量相加可以通过两种表示：三角形相加法、平行四边形相加法
- x和y可以为任何向量，一般采用正交向量
$A = \begin{pmatrix} x\\ y\\ \end{pmatrix}$  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $A^T = \begin{pmatrix} x&y\\ \end{pmatrix}$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $|\!|\vec{A}|\!| = \sqrt{x^2 + y^2}$

### 点乘（Dot product）
- 点乘基本公式
    - $\vec{a}\cdot\vec{b} = |\!|a|\!||\!|b|\!|cos\theta$
    - $cos\theta = \frac{\vec{a}\cdot\vec{b}}{|\!|a|\!||\!|b|\!|}$
    - $cos\theta = \widehat{a}\cdot\widehat{b}$ 对于单位向量
- 点乘基本运算规则
    - $\vec{a}\cdot\vec{b}=\vec{b}\cdot\vec{a}$
    - $\vec{a}\cdot(\vec{b}+\vec{c})=\vec{a}\cdot\vec{b}+\vec{a}\cdot\vec{c}$
    - $(k\vec{a})\cdot\vec{b} = \vec{a}\cdot(k\vec{b})=k(\vec{a}\cdot\vec{b})$
- 笛卡尔坐标系表示点乘
    - 二维
      $\vec{a}\cdot\vec{b}=\begin{pmatrix} x_a\\ y_a\\ \end{pmatrix}\cdot\begin{pmatrix} x_b\\ y_b\\ \end{pmatrix} = x_ax_b+y_ay_b$
    - 三维
      $\vec{a}\cdot\vec{b}\cdot\vec{c}=\begin{pmatrix} x_a\\ y_a\\ z_a\\ \end{pmatrix}\cdot\begin{pmatrix} x_b\\ y_b\\ z_b\\ \end{pmatrix} = x_ax_b+y_ay_b+z_az_b$
- 用途
    - 点乘相当于一个向量投影到另一个向量上的长度向乘法
    <img src="./image/dot_projection.png" alt="点乘投影图像" width="300px"></img>
    - 可用于判断一个向量与另一个向量的前后或者垂直关系

### 叉乘（Cross prduct）
- 基本运算
    - $\vec{a}\times\vec{b} = -\vec{b}\times\vec{a}$
    - $|\!|\vec{a}\times\vec{b}|\!| = |\!|\vec{a}|\!||\!|\vec{b}|\!|sin\theta$
    - 采用右手定则
- 特性
    - $\vec{x}\times\vec{y}=\vec{z}$
    - $\vec{y}\times\vec{x}=-\vec{z}$
    - $\vec{y}\times\vec{z}=\vec{x}$
    - $\vec{z}\times\vec{y}=-\vec{x}$
    - $\vec{x}\times\vec{z}=\vec{y}$
    - $\vec{z}\times\vec{x}=-\vec{y}$
    - $\vec{a}\times\vec{b}=-\vec{b}\times\vec{a}$
    - $\vec{a}\times\vec{a}=0$
    - $\vec{a}\times(\vec{b}+\vec{c})=\vec{a}\times\vec{b}+\vec{a}\times\vec{c}$
    - $\vec{a}\times(k\vec{b})=k(\vec{a}\times\vec{b})$