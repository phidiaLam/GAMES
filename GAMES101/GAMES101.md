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
    <img src="./image/dot_forward.png" alt="判断向量前后" width="300px"></img>


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

### 正交坐标系与矩阵
- 三条互相垂直的单位坐标
    - $|\!|\vec{u}|\!|=|\!|\vec{v}|\!|=|\!|\vec{w}|\!|=1$
    - $\vec{u}\cdot\vec{v}=\vec{v}\cdot\vec{w}=\vec{w}\cdot\vec{u}=0$
    - $\vec{w}=\vec{v}\times\vec{u}$
    - $\vec{p}=(\vec{p}\cdot\vec{u})\vec{u}+(\vec{p}\cdot\vec{v})\vec{v}+(\vec{p}\cdot\vec{w})\vec{w}\qquad$  括号内相当于投影，将向量p分解成三个单位向量
- 运算
    - $(M \times N)(N \times P)=(M \times P)$
    e.g.
    $\begin{pmatrix} 3&2\\ 4&1\\ 2&5\\ \end{pmatrix}\begin{pmatrix} 1&6&2\\ 3&4&3\\ \end{pmatrix}=\begin{pmatrix} 3\times1+2\times3&3\times6+2\times4&3\times2+2\times3\\ 4\times1+1\times3&4\times6+1\times4&4\times2+1\times3\\ 2\times1+5\times3&2\times6+5\times4&2\times2+5\times3\\ \end{pmatrix}=\begin{pmatrix} 9&26&12\\ 7&28&11\\ 17&32&19\\ \end{pmatrix}$
- 特性
    - $(AB)C=A(BC)$
    - $A(B+C)=AB+AC$
    - $(A+B)C=AC+BC$
- 转置
    - $\begin{pmatrix} 3&2\\ 4&1\\ 2&5\\ \end{pmatrix}^T=\begin{pmatrix} 3&4&2\\ 2&1&5\\ \end{pmatrix}$
    - (AB)^T^=B^T^A^T^
- 单位矩阵与逆
    - $I_{3\times3}=\begin{pmatrix} 1&0&0\\ 0&1&0\\ 0&0&1\\ \end{pmatrix}$
    - $AA^{-1}=A^{-1}A=I$
    - $(AB)^{-1}=B^{-1}A^{-1}$
- 点乘
    $\vec{a}\cdot\vec{b}=\vec{a}^T\vec{b}=\begin{pmatrix} x_a&y_a&z_a\\ \end{pmatrix}\begin{pmatrix} x_b\\ y_b\\ z_b\\ \end{pmatrix}=x_ax_b+y_ay_b+z_az_b$
- 叉乘
    $\vec{a}\times\vec{b}=A^*b=\begin{pmatrix} 0&-z_a&y_a\\ z_a&0&-x_a\\ -y_a&x_a&0\\ \end{pmatrix}\begin{pmatrix} x_b\\ y_b\\ z_b\\ \end{pmatrix}$  &nbsp; $A^*$是$\vec{a}$的对偶矩阵
<br/>
<br/>

## 向量与图形的变换

### 线性变换
- 缩放
    $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} s_x&0\\ 0&s_y\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}$
- 斜切
    $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} 1&a\\ 0&1\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}$
- 旋转
    $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} cos\theta&-sin\theta\\ sin\theta&cos\theta\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}$
    <img src="./image/rotate.png" alt="矩阵旋转" width="300px"></img>
    补充：
    $R_\theta = \begin{bmatrix} cos\theta&-sin\theta\\ sin\theta&cos\theta\\ \end{bmatrix}$
    $R_{-\theta} = \begin{bmatrix} cos\theta&sin\theta\\ -sin\theta&cos\theta\\ \end{bmatrix}=R_{\theta}^T$
    $R_{-\theta} = R_\theta^{-1}$
    (矩阵的逆等于它的转置，这个矩阵是正交矩阵)
- 总结
    $x'=ax+by$
    $y'=cx+dy$
    $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} a&b\\ c&d\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}$
    $x'=Mx$
### 齐次坐标
- 为什么要引入其次坐标？
    - 上述均为线性变换，若为平移这种变换，将无法现成统一的$x'=Mx$形式
    - 平移公式为：
        $x'=x+t_x$
        $y'=y+t_y$
         $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} a&b\\ c&d\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}+\begin{bmatrix} t_x\\ t_y\\ \end{bmatrix}$
- 定义
    - 在原有的坐标急促上再加一个纬度
      对于2D的点：$(x, y, 1)^T$
      对于2D的向量：$(x, y, 0)^T$
    - 这样子，原有的2d向量变化就变为：
     $\begin{pmatrix} x'\\ y'\\ w'\\ \end{pmatrix} = \begin{pmatrix} 1&0&t_x\\ 0&1&t_y\\ 0&0&1\\ \end{pmatrix}\cdot\begin{pmatrix} x\\ y\\ 1\\ \end{pmatrix}=\begin{pmatrix} x+t_x\\ y+t_y\\ 1\\ \end{pmatrix}$
    - 在引入齐次坐标后，线性变化+平移变成了：
     $\begin{bmatrix} x'\\ y'\\ \end{bmatrix} = \begin{bmatrix} a&b\\ c&d\\ \end{bmatrix}\begin{bmatrix} x\\ y\\ \end{bmatrix}+\begin{bmatrix} t_x\\ t_y\\ \end{bmatrix}$ $\rightarrow$ $\begin{pmatrix} x'\\ y'\\ w'\\ \end{pmatrix} = \begin{pmatrix} a&b&t_x\\ c&d&t_y\\ 0&0&1\\ \end{pmatrix}\cdot\begin{pmatrix} x\\ y\\ 1\\ \end{pmatrix}$
- 变化
    - 缩放
    $S(s_x,s_y)=\begin{pmatrix} s_x&0&0\\ 0&s_y&0\\ 0&0&1\\ \end{pmatrix}$
    - 旋转
    $R(\alpha)=\begin{pmatrix} cos\alpha&-sin\alpha&0\\ sin\alpha&cos\alpha&0\\ 0&0&1\\ \end{pmatrix}$
    - 平移
    $T(t_x,t_y)=\begin{pmatrix} 1&0&t_x\\ 0&1&t_y\\ 0&0&1\\ \end{pmatrix}$
- 逆矩阵
    - 可通过逆矩阵$M^{-1}$对操作进行返回重置

### 组合移动
- 移动的表示
    <img src="./image/transform.png" alt="组合移动" width="300px"></img>
- 计算的顺序
    - $R_{45}\cdot T_{(1,0)} \neq T_{(1,0)}\cdot R_{45}$
    - 
    - 示例： $T_{(1,0)}\cdot R_{45} \begin{bmatrix} x\\ y\\ 1\\ \end{bmatrix}=\begin{bmatrix} 1&0&1\\ 0&1&0\\ 0&0&1\\ \end{bmatrix}\begin{bmatrix} cos45^{\circ}&-sin45^{\circ}&0\\ sin45^{\circ}&cos45^{\circ}&0\\ 0&0&1\\ \end{bmatrix}$ 

### 复杂的组合移动

