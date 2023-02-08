# GAMES101

[TOC]

## 线性代数基础

### 定义与基本

- 向量定义：$\vec{AB} = B - A$
- 向量相加可以通过两种表示：三角形相加法、平行四边形相加法
- x 和 y 可以为任何向量，一般采用正交向量
  $A = \begin{pmatrix} x\\ y\\ \end{pmatrix}$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $A^T = \begin{pmatrix} x&y\\ \end{pmatrix}$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $|\!|\vec{A}|\!| = \sqrt{x^2 + y^2}$

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
  - $\vec{p}=(\vec{p}\cdot\vec{u})\vec{u}+(\vec{p}\cdot\vec{v})\vec{v}+(\vec{p}\cdot\vec{w})\vec{w}\qquad$ 括号内相当于投影，将向量 p 分解成三个单位向量
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
  $\vec{a}\times\vec{b}=A^*b=\begin{pmatrix} 0&-z_a&y_a\\ z_a&0&-x_a\\ -y_a&x_a&0\\ \end{pmatrix}\begin{pmatrix} x_b\\ y_b\\ z_b\\ \end{pmatrix}$ &nbsp; $A^*$是$\vec{a}$的对偶矩阵
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
    对于 2D 的点：$(x, y, 1)^T$
    对于 2D 的向量：$(x, y, 0)^T$
  - 这样子，原有的 2d 向量变化就变为：
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

### 组合移动(二维)

- 移动的表示
  <img src="./image/transform.png" alt="组合移动" width="300px"></img>
- 计算的顺序
  - $R_{45}\cdot T_{(1,0)} \neq T_{(1,0)}\cdot R_{45}$
  - 示例： $T_{(1,0)}\cdot R_{45} \begin{bmatrix} x\\ y\\ 1\\ \end{bmatrix}=\begin{bmatrix} 1&0&1\\ 0&1&0\\ 0&0&1\\ \end{bmatrix}\begin{bmatrix} cos45^{\circ}&-sin45^{\circ}&0\\ sin45^{\circ}&cos45^{\circ}&0\\ 0&0&1\\ \end{bmatrix}$

### 复杂的组合移动（三维）

- 齐次坐标定义
  对于 2D 的点：$(x, y, z, 1)^T$
  对于 2D 的向量：$(x, y, z, 0)^T$
  $(x, y, z, w)(w\neq0)$表示的点就是$(x/w, y/w, z/w)$
- 3D 仿射变换
  $\begin{pmatrix} x'\\ y'\\ z'\\ 1\\ \end{pmatrix} = \begin{pmatrix} a&b&c&t_x\\ d&e&f&t_y\\ g&h&i&t_z\\ 0&0&0&1\\ \end{pmatrix}\cdot\begin{pmatrix} x\\ y\\ z\\ 1\\ \end{pmatrix}$
  - 缩放
    $S(s_x,s_y,s_z)=\begin{pmatrix} s_x&0&0&0\\ 0&s_y&0&0\\ 0&0&s_z&0\\ 0&0&0&1\\ \end{pmatrix}$
  - 平移
    $T(t_x,t_y,t_z)=\begin{pmatrix} 1&0&0&t_x\\ 0&1&0&t_y\\ 0&0&1&t_z\\ 0&0&0&1\\ \end{pmatrix}$
  - 旋转（这个复杂点）
    $R_x(\alpha)=\begin{pmatrix} 1&0&0&0\\ 0&cos\alpha&-sin\alpha&0\\ 0&sin\alpha&cos\alpha&0\\ 0&0&0&1\\ \end{pmatrix}$
    $R_y(\alpha)=\begin{pmatrix} cos\alpha&0&sin\alpha&0\\ 0&1&0&0\\ -sin\alpha&0&cos\alpha&0\\ 0&0&0&1\\ \end{pmatrix}$
    $R_x(\alpha)=\begin{pmatrix} cos\alpha&-sin\alpha&0&0\\ sin\alpha&cos\alpha&0&0\\ 0&0&1&0\\ 0&0&0&1\\ \end{pmatrix}$
    为什么 y 会与众不同？因为有顺序存在，$\vec{x}\times\vec{z}=-\vec{y}$
- 复杂的旋转
  - 将复杂旋转分解成简单旋转
    $R_{xyz}(\alpha,\beta,\gamma)=R_x(\alpha)R_y(\beta)R_z(\gamma)$
    这三个角被称为欧拉角
  - 罗德里格旋转公式
    $R(n,\alpha)=cos(\alpha)I+(1-cos(\alpha))nn^T+sin(\alpha)\begin{pmatrix} 0&-n_z&n_y\\ n_z&0&-n_x\\ -n_y&n_x&0\\ \end{pmatrix}$
    沿$n$轴旋转$\alpha$度，$I$为单位矩阵

## VIEWING 变换

### 视图变换

- 定义一个相机
  - 位置 $\vec{e}$
  - 视线方向 $\widehat{g}$
  - 向上方向 $\widehat{t}$
- 关键点
  - 相机放于原点，向上方向为 Y， 看的方向为-Z
  - 并且随着相机变化物体
- 固定相机操作矩阵
  $M_{view}=R_{view}T_{view}$
  - 移动到原点
    $T_{view}=\begin{bmatrix} 1&0&0&-x_e\\ 0&1&0&-y_e\\ 0&0&1&-z_e\\ 0&0&0&1\\ \end{bmatrix}$
  - 旋转$g$到$-Z$，$t$到$Y$, $(g\times t)$到$X$
  - 因为上述操作复杂，先考虑逆旋转：$X$到$(g\times t)$，$Y$到$t$，$-Z$到$g$
    $R_{view}^{-1}=\begin{bmatrix} x_{\widehat{g}\times\widehat{t}}&x_t&x_{-g}&0\\ y_{\widehat{g}\times\widehat{t}}&y_t&y_{-g}&0\\ z_{\widehat{g}\times\widehat{t}}&z_t&z_{-g}&0\\ 0&0&0&1 \end{bmatrix}$
    $R_{view}=\begin{bmatrix} x_{\widehat{g}\times\widehat{t}}&y_{\widehat{g}\times\widehat{t}}&z_{\widehat{g}\times\widehat{t}}&0\\ x_t&y_t&z_t&0\\ x_{-g}&y_{-g}&z_{-g}&0\\ 0&0&0&1\\ \end{bmatrix}$
    因为旋转矩阵是正交矩阵，忘记了往上找

### 投影变换

#### 正交投影

- 简单理解
  - 相机摆放到原点位置，看向$-Z$，朝向上$Y$。
  - 扔掉$Z$坐标
  - 平移和缩放到$[-1, 1]^2$的范围内
    <img src="./image/define_ortho.png" alt="正交投影简单理解" width="300px"></img>
- 生成正交投影
  我们想要将一个长方体$[l,r]\times[b,t]\times[f,n]$转变为一个$[-1,1]^{3}$的标准正方体（canonical“正则，规范，标准”）
  <img src="./image/general_ortho.png" alt="正交投影的生成" width="600px"></img>
  - 移动矩阵
    $M_{ortho}=\begin{bmatrix} \frac{2}{r-l}&0&0&0\\ 0&\frac{2}{t-b}&0&0\\ 0&0&\frac{2}{n-f}&0\\\ 0&0&0&1\\ \end{bmatrix}\begin{bmatrix} 1&0&0&-\frac{r+l}{2}\\ 0&1&0&-\frac{t+b}{2}\\ 0&0&1&-\frac{n+f}{2}\\\ 0&0&0&1\\ \end{bmatrix}$
    **注意：这边采用右手系，为$-Z$。部分 API 如 OpenGL 采用左手系（$f>n$）**

#### 透视投影

- 前提
  - $(x,y,z,1),(kx,ky,kz,k\neq0)$,$(xz,yz,z^2,z\neq0)$都是表示同一个在 3D 中的点$(x,y,z)$
    这个后面很有用，你要问我为什么？不知道，还没学到后面
- 怎么做透视投影
  - 将锥体压缩成一个长方体$(n\rightarrow n, f\rightarrow f)(M_{persp\rightarrow ortho})$
  - 再做正交投影
    <img src="./image/persp_ortho.png" alt="如何做透视投影" width="400px"></img>
- 推导压缩矩阵
  - 利用相似三角形计算挤压的变形
    <img src="./image/similar_triangle.png" alt="通过相似三角形来挤压" width="400px"></img>
    $x'=\frac{n}{z}x$&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $y'=\frac{n}{z}y$
  - 远的平面：$M_{persp\rightarrow ortho}^{(4\times4)}\begin{pmatrix} x\\ y\\ z\\ 1\\ \end{pmatrix} \Rightarrow \begin{pmatrix} \frac{nx}{z}\\ \frac{ny}{z}\\ 不知道\\ 1\\ \end{pmatrix}==\begin{pmatrix} nx\\ ny\\ 不知道\\ z\\ \end{pmatrix}$
    用以上可以推导出：
    $M_{persp\rightarrow ortho}=\begin{pmatrix} n&0&0&0\\ 0&n&0&0\\ ?&?&?&?\\ 0&0&1&0\\ \end{pmatrix}$ &nbsp;&nbsp;&nbsp;&nbsp; 忘记了？代入乘一下就知道了，那么现在问题就是要把那几个问号填上值。
    我们就利用两点。 1. 任何在较近的面的点是不会改变的 2. 任何在 z 轴的点是不会改变的
  - 近的平面：$\begin{pmatrix} x\\ y\\ n\\ 1\\ \end{pmatrix}\Rightarrow\begin{pmatrix} x\\ y\\ n\\ 1\\ \end{pmatrix}==\begin{pmatrix} nx\\ ny\\ n^2\\ n\\ \end{pmatrix}$
    第三行值能是$\begin{pmatrix}0&0&A&B\\ \end{pmatrix}\begin{pmatrix}x\\y\\n\\1\\ \end{pmatrix}=n^2\rightarrow An+B=n^2$
    因为不存在 x 与 y 的值，**但！**这个第三行还没有完全算出来。（第一个性质）
    第二个性质，在远平面上，z 轴上的点也满足这个性质
    $\begin{pmatrix} 0\\ 0\\ f\\ 1\\ \end{pmatrix}\Rightarrow \begin{pmatrix} 0\\ 0\\ f\\ 1\\ \end{pmatrix}== \begin{pmatrix} 0\\ 0\\ f^2\\ f\\ \end{pmatrix}\rightarrow Af+b=f^2$
  - 通过上述两个式子就可以求得  
    $\left\{
        \begin{array}{ll}
            A=n+f \\
            B=-nf 
        \end{array}
    \right.$
  - 最终得到挤压矩阵是：
    $M_{persp\rightarrow ortho}=\begin{pmatrix} n&0&0&0\\ 0&n&0&0\\ 0&0&n+f&-nf\\ 0&0&1&0\\ \end{pmatrix}$
- 挤压变换
  $M_{persp}=M_{ortho}M_{persp\rightarrow ortho}$
  计算出变换矩阵与正交投影就能得出透视投影
- 图像学中定义透视投影
  - 垂直可视角度（fovY）水平长宽比也行
  - 长宽比
    <img src="./image/persp_fovY.png" alt="可视角与长宽比" width="400px"></img>
    $tan\frac{fovY}{2}=\frac{t}{|n|}$
    $aspect=\frac{r}{t}$

## 光栅化

完成 MVP 后，所有图像将会在一个正则立方体 $[-1,1]^3$ 中

- 屏幕「screen」
  1. 二维数组
  2. 数组里面每个元素是一个像素
  3. 是一种典型光栅呈现设备
  - 光栅化「Raster」
    把东西画在屏幕上
  - 像素（抽象简单理解，不完全对）
    - 一个个小方块
    - 里面是颜色的混合（<font color="red">红色</font>, <font color="green">绿色</font>, <font color="blue">蓝色</font>）
- 屏幕上像素点
  - 像素的坐标用$(x,y)$来表示，所以所有像素可以表示为$(0,0)$到$(width-1,height-1)$
  - 像素$(x,y)$的中心为$(x+0.5,y+0.5)$，所以整个品目是$(0,0)$到$(width,height)$
    <img src="./image/pixel_define.png" alt="可视角与长宽比" width="300px"></img>
- 把正则立方体映射到屏幕上
  - 去掉 z 轴
  - 变换 xy 平面：$[-1,1]^2$到$[0,width]\times[0,height]$
  - 视图变换矩阵：
    $M_{viewport}=\begin{pmatrix} \frac{width}{2}&0&0&\frac{width}{2}\\ 0&\frac{height}{2}&0&\frac{height}{2}\\ 0&0&0&0\\ 0&0&0&1\\ \end{pmatrix}$

### 三角形

- 为什么选择三角形？
  - 最基础的多边形
  - 任何多边形能拆成三角形
  - 三个点给定的三角形一定是平面的
  - 三角形的内外定义明确
  - 三角形三个点给不同属性，可以为三角形内部所有点插值
- 最简单的方法————采样
  - 定义
    将函数离散化
  - 采样三角形
    $inside(t,x,y)=
        \begin{cases}
            1 \quad Point(x,y)\;in\;triangle\;t \\
            0 \quad otherwise
        \end{cases}
    $
  - 如何采样
  ```C++
  for (int x = 0; x < xmax; ++x) {
      for (int y = 0; y < ymax; ++y) {
          image[x][y] = inside(tri, x+0.5, y+0.5);
      }
  }
  ```
  - 判断一个点是否在三角形内
    通过三条边与顶点到点的向量叉乘，判断点是不是在三条边的同一边，如果是，则在内部。
    （如果点正好边上，自己定义，说通就好。如果用 opengl 或 directX，上左算内，右下算外）
  - 没有必要去遍历所有的点
    解决：取最大与最小的 x 与 y，可以框出一个方形（轴线包围盒），缩小遍历范围。（缩写：AABB）
    还有很多其他的加速方法。 1. 每一行找最左最右
    等等
  <img src="./image/triangle_pixel.png" alt="可视角与长宽比" width="300px"></img>

## 反走样（抗锯齿）与深度缓冲

### 反走样

- 锯齿「走样」（Aliasing）
  <img src="./image/aliasing.png" alt="走样" width="300px"></img>
- Artifacts（瑕疵）
  图形上的各种看上去不太对的东西
  - 锯齿
  - 摩尔纹 （Moire pattern）
  - 车轮效应 （Wagon Wheel effet）
    原因：信号的变化太快，以至于采样的速度跟不上它
- 预滤波「预模糊」（Pre—Filtering）
  <img src="./image/pre-filtering.png" alt="预模糊" width="600px"></img>
  先对信号做模糊，再对结果进行采样
  **一定要先模糊再采样，专有名词：Blurred Aliasing** 为什么？
- 信号处理（主要为了了解一些底层的原因与实现逻辑）
  - 频域
    频域就是记录每个简单正弦信号的相位和频率的方式。可以采用傅里叶变换将一个复杂的信号转换成多个简单的正弦信号，并通过频域来记录
    <img src="./image/freq_domain.gif" alt="频域与时域" width="800px"></img>
  - 傅里叶变换
    - 将一个信号函数分解成多个简单的正弦信号
      <img src="./image/fourier.png" alt="傅里叶变换图" width="500px"></img>
      $f(x)=\frac{A}{2}+\frac{2Acos(t\omega)}{\pi}-\frac{2Acos(3t\omega)}{3\pi}+\frac{2Acos(5t\omega)}{5\pi}-\frac{2Acos(7t\omega)}{7\pi}+···$
    - 可以通过傅里叶变换将时域变换为频域，也可以用反傅里叶变换将频域变换成时域
      <img src="./image/fourier_inverse.png" alt="傅里叶可逆" width="500px"></img>
  - 采样不足
    - 可能导致高频信号看起来如同低频信号，从而造成走样
      <img src="./image/aliases.png" alt="采样不足" width="500px"></img>
  - 滤波
    排除掉一些指定的波频
    下面是一些例子，其中中心代表低频，旁边代表高频： - 原图：
    <img src="./image/filter1.png" alt="原图" width="200px"></img> - 滤掉高频（Egdes）：
    <img src="./image/filter3.png" alt="滤掉高频" width="200px"></img> - 滤掉低频（blur）：
    <img src="./image/filter2.png" alt="滤掉低频" width="200px"></img> - 滤掉高频与低频：
    <img src="./image/filter4.png" alt="滤掉高频与低频" width="200px"></img>
    <img src="./image/filter5.png" alt="滤掉高频与低频" width="200px"></img>
  - 卷积
    通过将周围的值以一定比例相加得到当前位置的值，可以使得图像模糊等
    - 卷积定理
      - 直接对时域做卷积
      - 转换频域做卷积 1. 转换为频域（傅里叶变换） 2. 乘上就按转换后的卷积核 3. 转换为频域（反傅里叶变换）
        <img src="./image/convolution_theorem.png" alt="滤掉高频与低频" width="400px"></img>
    - 归一化操作
      取周围总共九个像素来获取中间像素的值，就需要乘于$\frac{1}{9}$
  - 频域上的采样
    <img src="./image/sampling_fraq.png" alt="采样" width="400px"></img>
    (c)里面的箭头是离散函数，与(a)图乘积就是(a)的离散的点得到(e)图的结果。
    左边为时域，右边为频域
    采样就是再重复一个原始信号的频谱
  - 走样
    <img src="./image/aliasing_freq.png" alt="走样" width="400px"></img>
    采样点越稀疏，采样点大，对应到频谱上中间的间隔就会越小。原始信号与复制粘贴后中间重叠导致走眼。
  - 反走样
    - 增加采样率
    - 对原始信号进行模糊
      1. 砍掉高频信号
      2. 再进行复制粘贴，就不会造成重叠，从而防止走样
  - 把三角形变模糊
    对每一个像素做卷积操作，求平均值，从而达到滤波的效果。
    <img src="./image/dim.png" alt="模糊" width="400px"></img>
    对每个像素的覆盖区域计算平均
    - MSAA
      - 将一个像素划分成多个像素点，判断每个点重心的着色，将该像素里面所有值加起来做平均从而获得该像素的值。
        <img src="./image/msaa1.png" alt="MSAA" width="400px"></img>
        <img src="./image/msaa.png" alt="MSAA" width="400px"></img>
    - FXAA (Fast Approximate AA)
      1. 先得到有锯齿的图
      2. 找到边界，换成无锯齿边界
    - TAA (Temporal AA)
      - 通过上一帧的信息来做抗锯齿
  - 扩展：超分别率
    与抗锯齿相似
    - DLSS (Deep Learning Super Sampling)

### 深度缓冲

- 画家算法
  - 定义：
    从远处先画，再画前面的面来覆盖后面的面
  - 排序深度：
    复杂度：$O(nlogn)$
  - 缺陷:
    三角形深度不统一，无法进行排序
    <img src="./image/depth_wrong.png" alt="深度排序错误" width="400px"></img>
- 深度缓冲（Z-Buffer）
  - 定义
    对每个像素进行前后排序
  - 步骤
    同时渲染成品图片（frame buffer）与任何一个像素对应的像素（depth buffer「z-buffer」）
    **越小的$z\rightarrow$近，越大的$z\rightarrow$远**
  - 过程
    1. 初始化深度缓存，使得所有深度都是无限远的
    2.
    ```C++
    for(each triangle T)
        for(each sample (x,y,z) in T)
            if (z < zbuffer[x, y])          //比之前记录的深度更小
                framebuffer[x, y] = rgb;    // 更新颜色
                zbuffer[x, y] = z;          // 更新深度
            else
                ;                           // 什么也不做
    ```
    图解：
    <img src="./image/depth_triangle.png" alt="深度排序错误" width="400px"></img>
  - 复杂度
    深度缓冲复杂度为$O(n)$
    注意：这边没有排序

## 着色

图形学上着色是对不同的物体应用不同的材质

### 照明与着色

- Blinn-Phong 反射模型——基础着色模型
  - 着色三种部分
    1. 高光 Specular
    2. 漫反射 Diffuse
    3. 环境光照 Ambient
  - 定义局部着色着色点（shading point）
    - 法线 $\widehat{n}$
    - 观测方向 $\widehat{v}$
    - 光照方向 $\widehat{l}$
    - 平面参数 （颜色，shininess，...）
      <img src="./image/shading_point.png" alt="着色点" width="400px"></img>
  - 漫反射
    - 光打到一个点上，光会向各个方向反射出去
      <img src="./image/diffuse.png" alt="漫反射" width="300px"></img>
    - 接收：与角度有关系 $cos\theta=l\cdot n$
      <img src="./image/lambert.png" alt="反射角度" width="300px"></img>
    - 发射：点光源
      <img src="./image/light_falloff.png" alt="点光源能量" width="400px"></img>
      任何时刻，点光源辐射的能量一定在一个球壳上
      因为能量守恒，离中心越远，单位面积能量越小（与距离平方成反比 I）
    - 计算
      - $L_d=k_d(I/r^2)max(0,\widehat{n}\cdot \widehat{l})$
      - $L_d$漫反射反射的能量，$I$为单位距离一个点的能量强度，$k_d$为漫反射材质，$0$因为负数没有意义，从背面打过来的光。
    - 示例
      <img src="./image/diffuse_example.png" alt="漫反射例子" width="600px"></img>
  - 高光
    - 根据镜面反射获得光线的反射方向，视线所看到的高光强度取决于视线方向
      <img src="./image/specular_r.png" alt="反射与视线" width="200px"></img>
    - 优化模型，半程向量（容易计算）
      <img src="./image/specular.png" alt="半程向量" width="200px"></img>
      $\widehat{h} = bisector(\widehat{v},\widehat{l})$
      $\quad = \frac{\widehat{v}+\widehat{l}}{|\!|\widehat{v}+\widehat{l}|\!|}$ 通过两个向量相加除与长度，得到为单位长度的半程向量
      $L_s = k_s(I/r^2)max(0,cos\alpha)^p$
      $\quad\; = k_s(I/r^2)max(0,\widehat{n}\cdot\widehat{h})^p$
      这里指数$p$用于降低容忍度
      <img src="./image/lobe.png" alt="降低容忍度" width="600px"></img>
    - 示例
      <img src="./image/specular_example.png" alt="高光变化例子" width="600px"></img>
  - 环境光
    - 假设所有点接受到的光是一样的，保证没有一个点是全黑的
      <img src="./image/ambient.png" alt="环境光" width="200px"></img>
    - $L_a=k_aI_a$
    - 是个很大胆的假设，这是不真实的，更真实的是全局光照
  - 总结
    - 最终公式
      $L = L_a+L_d+Ls$
      $\quad = k_aI_a + k_d(I/r^2)max(0,\widehat{n}\cdot \widehat{l}) + k_s(I/r^2)max(0,\widehat{n}\cdot\widehat{h})^p$
      <img src="./image/blinn-phong.png" alt="Blinn-Phong反射模型" width="600px"></img>
- 着色频率
  - 三种着色频率
    - 平面着色频率（Flat shading）
      - 每个三角形平面同一法线，所以每个内部结果一致
      - 不够丝滑 ~~（德芙看了都摇头）~~
        <img src="./image/flat_shading.png" alt="平面着色频率" width="200px"></img>
    - 高洛德着色频率 （Gourand shading）
      - 在每个顶点进行着色，后对三角形里面的每个点进行插值
        <img src="./image/gourand_shading.png" alt="高洛德着色频率" width="200px"></img>
    - Phong 着色频率（Phong shading）
      - 求出三角形三个顶点的发现，后插值三角形每个点的法线，求出每个点的值
        <img src="./image/phong_shading.png" alt="Phong着色频率" width="200px">
  - 求顶点向量
    - 假设是一个球体，顶点向量就是从圆心到顶点的向量
    - 其他来说，根据周围的平面来算出平均的法线就是顶点法线
      $N_v=\frac{\sum_{i}N_i}{||\sum_{i}N_i||}$
      <img src="./image/vertex_normal.png" alt="顶点法线" width="200px"></img>
      可以根据顶点关于的面的面积进行加权
  - 法线插值问题
    - 需要使用重心坐标，往后看

### 图形管线（Real-time Rendering 实时渲染管线）

- 五个步骤
  1. 顶点处理：三维空间的点投影到屏幕上
  2. 三角形处理：连接点形成三角形
  3. 光栅化：离散的点光栅化
  4. 分片处理：着色
  5. 帧缓冲操作：显示
     <img src="./image/graph_pipeline.png" alt="图形管线过程" width="600px"></img>
     分步图例：
     <img src="./image/pipe1.png" alt="图形管线过程" width="600px"></img>
     <img src="./image/pipe2.png" alt="图形管线过程" width="600px"></img>
     <img src="./image/pipe3.png" alt="图形管线过程" width="600px"></img>
     <img src="./image/pipe4.png" alt="图形管线过程" width="600px"></img>
     <img src="./image/pipe5.png" alt="图形管线过程" width="600px"></img>
     着色与贴图在两个不同的地方都可能出现，这要看选取什么着色频率。
- 程序中的着色（顶点和像素）

  - shader 每个顶点或者像素通用的着色程序
    opengl 着色语言（简称 GLSL）程序：

  ```C++
  uniform sampler2D myTexture;                    // 材质全局变量
  uniform vec3 lightDir;                          // 光线方向全局变量
  varying vec2 uv;                                //
  varying vec3 norm;                              // 顶点的法线

  void diffuseShader()
  {
      vec3 kd;
      kd = texture2d(myTexture, uv);                      // 材质颜色
      kd *= clamp(dot(-lightDir, norm), 0.0, 1.0);        // l和n的方向点乘
      gl_FragColor = vec4(kd, 1.0);                       // 存储像素或者片段的颜色
  }
  ```

- GPU 和管线（了解，随手一记）
  - GPU 会完成很多图形的映射什么的
  - GPU 有很高很高的并行量，适合用于图形的计算

### 纹理映射

- 定义
  - 定义物理表面任何一个点的不同属性
  - 任何一个三维物体表面都是二维的
  - 将纹理拉伸，压缩变换，使得三维物体表面映射到二维纹理上
- 例子
  <img src="./image/texture.png" alt="纹理例子" width="600px"></img>
- uv 展开
  - 无论展开什么图形，一般认为 u 在 0-1 内，v 在 0-1 内
  - 三角形三个顶点，每个顶点都对应一个 uv 坐标
    <img src="./image/uv.png" alt="uv展开" width="600px"></img>
- 设计纹理（扩展）
  - 设计重复纹理，上下左右衔接无缝（tiled textures）
    - 其中一种算法：wang tiled
- 如何知道三角形每块对应的坐标
  - 重心坐标插值，下次一定

### 重心坐标

- 定义
  - 知道一个三角形的三个顶点，三角形的这个平面上的任何一个点都可以被表示成这三个点的线性组合
    <img src="./image/barycentric.png" alt="重心坐标" width="200px"></img>
  - $(x, y) = \alpha A+\beta B+\gamma C$
    $\qquad\qquad \alpha+\beta+\gamma=1$
  - 这三个点如果都是非负的，那这个点一定在三角形内
  - $\alpha = \frac{A_A}{A_A+A_B+A+C}$
    $\beta = \frac{A_B}{A_A+A_B+A+C}$
    $\gamma = \frac{A_C}{A_A+A_B+A+C}$
    <img src="./image/barycentric1.png" alt="重心坐标" width="200px"></img>
- 用途
  - 对于三角形内任意一个点，进行插值 - 颜色 - 深度 - 法线 - 等等
    <img src="./image/barycentric_color.png" alt="重心坐标插值颜色" width="200px"></img>
- 注意
  - 投影后的三角形重心坐标与原本并不相同
  - 所以应该先做插值后做投影（三维空间做插值对应到二维上）
- 纹理插值
  - 在纹理映射的时候，用重心坐标算出 uv，就可以将纹理贴到平面上。
  - 但是这样子做会出问题
    1. 纹理放大

       - texture： 纹理像素
         texel：映射后的像素
       - 描述：一堵墙有 4k 的分辨率，但是纹理只有 256\*256，这样子就会查到非整数的值

       - 解决 - Nearest： 将映射的非整数值四舍五入成整数 - Bilinear（双线性插值） - 找到距离左下角的横向和竖直距离 - $lerp(x, v_0, v_1)=v_0+x(v_1-v_0)$ [一维]线性插值（Linear interpolation） - $u_0=lerp(s,u_{00},u_{10})$
         $u_1=lerp(s,u_{01},u_{11})$ - $f(x,y)=lerp(t,u_0,u_1)$ - Bicubic：Bilinear 是取周围 4 个点插值，Bicubic 是取 16 个点
         <img src="./image/texel.png" alt="重心坐标" width="600px"></img>

    2. 纹理过大
       - 问题：纹理过大因为多个像素要被缩小成一个像素，就会导致走样，走样可能比纹理放大时还严重
         <img src="./image/texture_large.png" alt="重心坐标" width="400px"></img>
       - Mipmap（图像金字塔）
         - 特点：快速，大约，只能做近似正方形
         - 提前生成多张图，以便快速查询
           <img src="./image/mipmap.png" alt="mipmap" width="600px"></img>
           只需要$\frac{4}{3}$的空间就可以储存所有的 mipmap
         - 映射
           - 通过求纹理 uv 图两个临近点的距离，从而求出一个像素覆盖的区域长度（简单起见取最大的）
             <img src="./image/uv_mipmap.png" alt="纹理映射uv" width="500px"></img>
             $D=log_2L$
             $L=max(\sqrt{(\frac{du}{dx})^2+(\frac{dv}{dx})^2}\cdot \sqrt{(\frac{du}{dy})^2+(\frac{dv}{dy})^2}$
           - 问题：变化不连续，很奇怪
             <img src="./image/mipmap_example.png" alt="变化不连续的示例" width="500px"></img>
           - 三线型插值（Trilinear Interpolation）：选取两个相邻的金字塔 level，在完成两个层级中的双线性插值后，在两层级间再进行一次插值。
             <img src="./image/trilinear.png" alt="三线型插值" width="600px"></img>
             <img src="./image/trilinear_example.png" alt="三线型插值成果" width="500px"></img>
       - 过模糊
         - 就算使用了 mipmap，还会出现过模糊的问题
           <img src="./image/overblur.png" alt="三线型插值成果" width="400px"></img>
         - 因为图像上的方形区域并不对应纹理上的方形区域
           <img src="./image/texture_square.png" alt="三线型插值成果" width="400px"></img>
       - 各向异性过滤(Anisotropic Filtering)
         - 生成原本四倍储存大小的 map 图片，方便用于查询不同长宽比的对应纹理图
           <img src="./image/anisotropic.png" alt="各向异性过滤" width="400px"></img>
       - EWA 滤波
         1. 将不规则的图形用圆分割
         2. 然后反复查询
         - 缺点：因为需要反复查询，所耗资源较大

### 纹理应用

- 现代 GPU，纹理可以理解成有一块内存（数据），可以在这个范围内进行点查询或者范围查询（如：mipmap）
- 纹理的应用：
  - 环境映射（Environment Map）：
    存储周围环境到一张图里面
    <img src="./image/environment_map.png" alt="环境映射" width="400px"></img>
    （犹他茶壶）
  - 环境光（Environmental Lighting）
    环境光来自无限远，映射出一个四面八方的环境
    <img src="./image/environment_light.png" alt="环境光" width="400px"></img>
  - 球面环境映射（Spherical Environment Map）
    将周围环境映射到一个球体上
    <img src="./image/spherical_environment_map.png" alt="球面环境映射" width="400px"></img>
    - 问题： 会导致上下扭曲严重
  - 立方体贴图（Cube Map）
    将贴图折叠成六个面，将它映射于球体上
    <img src="./image/cube_map.png" alt="立方体贴图" width="400px"></img>
  - 纹理影响法线
    - 通过纹理来储存法线信息生成阴影
      <img src="./image/bump_texture.png" alt="凹凸贴图" width="400px"></img>
    - 计算高度偏移量计算法线，重新计算明暗
      定义每个像素高度相对位置的移动，从而计算法线
      <img src="./image/bump_mapping.png" alt="凹凸贴图映射" width="400px"></img>
    - 计算：
      - 二维
        原法线： $n(p) = (0,1)$
        求导 p 位置的变化： $dp = c * [h(p+1)- h(p)]$
        新法线： $n(p) = (-dp, 1).normalized()$
        (90 度旋转，xy 调换，x 乘-1)
        <img src="./image/comp_bump_mapping.png" alt="计算凹凸贴图" width="400px"></img>
      - 三维
        原法线：$n(p) = (0,0,1)$
        求导 p 位置的变化：
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\frac{dp}{du} = c1 * [h(u+1)- h(u)]$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\frac{dp}{dv} = c2 * [h(v+1)- h(v)]$
        新法线： $n=(-\frac{dp}{du}, -\frac{dp}{dv}, 1).normalized()$
      - 注意：可以定义局部坐标系，认为法线永远向上，如(0，0，1)。通过纹理贴图映射
    - 缺点：无法造成阴影映射到其他物体上
      <img src="./image/bump.png" alt="其他物体没有阴影" width="400px"></img>
  - 位移贴图
    - 通过纹理来储存高度信息，影响每个点
      <img src="./image/displacement_mapping.png" alt="影响高度有阴影" width="400px"></img>
  - 纹理的其他作用
    - 储存三维的信息，如用于医疗扫描等等
    - 预先储存环境光信息，对凹陷阴影处理更好，加载速度更快等等
    - 纹理可以用于代表很多东西

## 几何学

### 介绍

- 如何描述得到不同形状的几何
- 如何定义曲面
- 如何描述复杂形状的几何
- 布料要怎么在计算机图形中展示
- 水滴滴落要怎么展现，什么情况互相连接等等的复杂几何
- 几何多的情况如何优化几何，怎么存储，怎么渲染
- 微观细胞也可以是复杂几何
- 分形几何

### 分类
- 隐式几何（Implicit）
  - 定义：不告诉点在哪，告诉点之间满足的关系
  - 例子：
    - 球的隐式表示： 
      - 所有点在3D中，满足$x^2+y^2+z^2=1$
      - 可以写成$f(x,y,z)=x^2+y^2+z^2-1=0$
  - 通用公式：$f(x,y,z)=0$ 只要x,y,z满足公式，则可以表示点在平面上，找出所有的点构造平面
  - 优点：轻松计算一个点时候在这个面上（内、外），只需要代入计算
  - 缺点：很难从式子推导出一个图形
- 显式几何（Explicit）
  - 定义：将点直接表示出来或者通过参数映射定义来表名
  - 例子：通过一定的公式将二维的uv坐标上的点映射成三维形状（这是马鞍面）
    <img src="./image/via_parameter_mapping.png" alt="参数映射" width="600px"></img>
  - 缺点：很难判断一个点与表面的关系
  - 优点：根据公式可以轻松画出图形

### 隐式几何表示方法
- 代数方法（Algebraic Surfaces）
  - 很难通过代数知道图形是什么，也很难将一个几何写成一个代数公式
  <img src="./image/algebraic_surfaces.png" alt="代数表面" width="400px"></img>
- CSG（Constructive Solid Geometry）
  - 通过基本几何的布尔计算
  <img src="./image/csg.png" alt="图形布尔" width="600px"></img>
- 距离函数（Distance Functions）
  - 定义
    - 空间中一个点到你要表述的几何形体的最小距离
    - 这个距离可以是正的也可以是负的，一个点在物体外部则为正，一个点在物体内部则为负数
    <img src="./image/distance_function.png" alt="距离函数" width="800px"></img>
  - 例子
    - 例子1:
      - 希望将两张图片混合后得到一个均匀过渡左黑右白的图
      <img src="./image/distance_example.png" alt="距离函数例子" width="400px"></img>
      - （SDF的S表示sin）
      - 上面的是通过简单的叠加，并不能达到我们想要的效果
      - 下图则通过距离函数奖两图加起来，则可以得到均匀过渡
    - 例子2:
      - 通过距离函数就可以混合两个形状一起
      <img src="./image/distance_sharp_example.png" alt="距离函数例子" width="800px"></img>
    - 还可以做很多很多复杂的模型
  - 获取表面
    - 代数展示距离公式：知道了一个距离函数，通过将0找出来，就可以获得这个距离函数的表面
    - 水平集展示距离公式（Level Set Methods）：
      - 封闭式的方程很难描述复杂的形状，使用近似于函数的网络进行替代
      <img src="./image/level_set_methods.png" alt="水平集" width="400px"></img>
    - 应用
      - 可以用于医学3d实心建模
      - 水滴滴落，水花四溅的效果
- 分形（Fractals）
  - 分形容易走样，之后渲染有很大挑战
  <img src="./image/fractals.png" alt="分形例子" width="800px"></img>

### 显式几何表示方式
- 点云（Point Cloud）
  - 通过极其密的点来表示平面，只要点足够密，看起来就是一个平面
  - 应用：
    - 三维空间的扫描
  - 问题：
    - 如何从点云转换成面
- 多边形面（Polygon Mesh）
  - 将几何平面拆成一个个小多边形
  - 问题：
    - 连接关系：如何连接点形成三角形
  - 储存方法：
    - wavefront object file(.obj)
      - 顶点坐标
      - 法线
      - 纹理坐标
      - 以及面(由哪三个点组成，对应的法线是什么，纹理坐标是什么)

### 曲线与曲面
- 贝塞尔曲线
  - 定义与实现
    1. 将曲线从起始点到终点用时间t来表示，在起始点时间t为0，终点时间t为1
    2. 每条线段上取当前时间t的长度，将其连接
    3. 不断重复步骤，使得最后只取到一个点
    4. 这个点就是当前时间曲线会经过的点
    <img src="./image/bezier_point.png" alt="贝赛尔曲线" width="400px"></img>
    <img src="./image/bezier_curve.gif" alt="贝赛尔曲线" width="600px"></img>
  - 计算
    - 过程
      - $b_{0}^1(t)=(1-t)b_0+tb_1$
      - $b_{1}^1(t)=(1-t)b_1+tb_2$
      - $b_{1}^1(t)=(1-t)b_{0}^1+tb_{1}^{1}$
      - $b_{0}^2(t)=(1-t)^2b_{0}+2(1-t)b_{1}+t^2b_2$
      <img src="./image/compute_bezier.png" alt="计算贝塞尔曲线" width="400px"></img>
      - 满足杨辉三角形
    - 伯恩斯坦表示
      - $b^n(t)=b_{0}^n(t)=\sum_{j=0}^nb_jB_{j}^n(t)$
      - 伯恩斯坦多项式：$B_{i}^n(t)= \begin{pmatrix} n\\ i\\ \end{pmatrix}t^i(1-t)^{n-i}$ ($\begin{pmatrix} n\\ i\\ \end{pmatrix}$ 是$C_i^n$)
  - 特性：
    - 凸包性质：多个点画出的贝塞尔曲线一定是在这几个点生成的凸包内
     <img src="./image/convex_hull.png" alt="凸包" width="400px"></img>
  - 优化：
    - 如上图，多个点很难画出一个完整的贝塞尔曲线。
    - 一半将其分成每四个控制点来定义一条贝塞尔曲线，再将多个贝塞尔曲线连起来。
    - 中间的点一般不画出来
     <img src="./image/piecewise_bezier.png" alt="分段贝塞尔曲线" width="600px"></img>
    - 为了确保两条曲线之间光滑过度，可以将一个两边的控制点共线，距离相等
  - $C^0$连续
    - 几何上的连续（首位点相接）
    - $a_n=b_0$
  - $C^1$连续
    - 切线上的连续
    - $a_n=b_0=\frac{1}{2}(a_{n-1}+b_1)$
    <img src="./image/c1_continuity.png" alt="c1连续" width="600px"></img>
  - 其他曲线
    - 样条（Splines）
      - 连续的曲线，是由一些控制点决定的，在任意一个点都满足一定的连续性
      - B-样条（基函数样条）
        - 贝塞尔曲线的扩展，能力更强：贝塞尔曲线懂一个点，整条曲线都会有变化
        - B样条拥有局部性，改变一个点只会改变局部的曲线
        - 图形学里面一个很难的部分（之后学），还有个更复杂的NURBS[非均匀有理样条]
          - 网址：https://www.bilibili.com/video/av66548502?from=search&seid=65256805876131485
- 曲面
  - 贝塞尔曲面
    - 16个控制点，形成多条贝塞尔曲线进行线性插值
    - 两个时间，一个横向的u和一个纵向的v
    - 过程：
      1. 通过时间u来计算横向的四条曲线上的点
      2. 通过时间v与第一步的四个点，来找出当前u与v时间下所对应的点
       <img src="./image/bezier_curve.png" alt="贝塞尔曲面" width="600px"></img>

### 网格
- 网格操作：几何处理
  - 网格细化 (Mesh Subdivision)
  - 网格简化 (Mesh Simplification)
  - 网格规整化
  <img src="./image/mesh_operation.png" alt="几何网格操作" width="800px"></img>
- 网格细分
  - 过程
    1. 引入更多的三角形
    2. 调整三角形的位置
  - Loop细分【Loop是名字，不是循环】
    - 将每个三角形分成四个
    <img src="./image/split_triangle.png" alt="分割三角形" width="400px"></img>
    - 更新点位置
      - 三角形边上的点：
        <img src="./image/loop_update_edge.png" alt="三角形位置调整（边）" width="400px"></img>
      - 三角形顶点上的点：
        <img src="./image/loop_update_vertex.png" alt="三角形位置调整（顶点）" width="400px"></img>
  - Catmull-Clark细分
    - 为什么有loop细分还不够？
        - Loop细分只能支持三角形网格
    - 定义：
      - 非四边形面：不是四边形的面
      - 奇异点（极点）：度不为4的点
      <img src="./image/catmull_clark_subdivision1.png" alt="Catmull-Clark细分定义" width="400px"></img>
    - 变化过程
      1. 连接每个四方形对边的中点
      2. 非四边形面，每个边中点连至重心，将非四边形划分成多个四边形
      <img src="./image/catmull_clark_subdivision2.png" alt="Catmull-Clark细分定义" width="400px"></img>
      3. 不断重复步骤1，使得其被分割成更多的四边形，看起来跟顺滑
      <img src="./image/catmull_clark_subdivision3.png" alt="Catmull-Clark细分定义" width="400px"></img>
      <img src="./image/catmull_clark_subdivision4.png" alt="Catmull-Clark细分定义" width="400px"></img>
    - 计算公式（调整点的位置）：
      - 面中心的点：$f = \frac{v_1+v_2+v_3+v_4}{4}$
        <img src="./image/face_point_change.png" alt="变化面上的点" width="150px"></img>
      - 边中心的点：$e = \frac{v_1+v_2+f_1+f_2}{4}$
        <img src="./image/edge_point_change.png" alt="变化边上的点" width="150px"></img>
      - 定点上的点(老的顶点)： $e = \frac{f_1+f_2+f_3+f_4+2(m_1+m_2+m_3+m_4)+4p}{16}$
        <img src="./image/old_point_change.png" alt="变化顶点上的点" width="150px"></img>
- 网格简化
  - 简化模型可以用于提升性能，比如游戏渲染等，不同场合用不同复杂度的模型
  <img src="./image/mesh_simplification_example.png" alt="简化模型例子" width="400px"></img>
  - 边坍缩（edge collapsing）
    - 定义：边坍缩算法是一个迭代算法，通过不断迭代进行边坍缩操作达到简化模型的目的。
       <img src="./image/edge_collapsing_example.png" alt="边坍缩例子" width="400px"></img>
    - 二次误差度量（Quadric Error Metrics）
      - 目的：那些边重要不能捏一块，那些边不重要能捏一块
      - 二次误差意思不是做两次，是平方的意思
      - 二次误差：新的点满足到原本各个相关面的平方和最小
      <img src="./image/quadric_error.png" alt="二次误差" width="400px"></img>
      - 计算过程（如何选边）
        - 计算到表面的近似距离作为到包含三角形的平面的距离之和
        - 通过堆或者优先队列为上诉计算得到的分数进行排序
        - 从最小的分数开始边坍缩
        - 利用贪心算法做局部最优解

## 阴影（光线追踪准备）
  - 阴影贴图（shadow mapping）
    - 图像空间算法
      - 生成阴影不需要知道场景的集合信息
      - 会产生走样现象
    - 重要思想
      - 点不在阴影里，摄像机和光源都可以看到这个点
      - 点在阴影里，摄像机可以看到，光源则看不到这个点
  - 硬阴影
    - 定义：一个点只有在阴影内或阴影外，非0即1
    - 点光源
      1. 从光源处计算深度缓存
       <img src="./image/render_light1.png" alt="光源深度缓存" width="150px"></img>
      2. 从相机处观察能看到的点，然后投影回去光源的成像平面上，对比两个深度判断是否在阴影内
       <img src="./image/render_light2.png" alt="摄像机深度映射" width="150px"></img><img src="./image/render_light3.png" alt="摄像机深度映射" width="200px"></img>
    - 问题：
      - 两次渲染开销大
      - 浮点数精度问题，导致深度对比不准确
      - shadow map的分辨率问题
  - 硬阴影 vs. 软阴影
      - 图例：
        <img src="./image/hard_shadow.png" alt="硬阴影" width="198px"></img><img src="./image/soft_shadow.png" alt="软阴影" width="200px"></img>
      - 软阴影是因为自然界光有一定体积，这是基于自然规律
        - 被完全挡住的称为本影（umbra）
        <img src="./image/eclipse_sun.png" alt="日食" width="300px"></img>
        - 被挡住一般的称为半影（penumbra）

## 光线追踪
### Whitted-Style Ray Tracing
- 为什么要使用光线追踪？
  1. 软阴影不好实现，实现效果不佳
  2. 光线多次反射的情况无法很好的表现
- 光线追踪特点
  - 光线追踪慢，一般用于离线的。
  - 一帧需要10K CPU小时
- 光线定义（对于课程来说）：
  - 光线沿直线传播
  - 光线不会发生碰撞
  - 光线一定从光源发出不断反射到达眼睛（而且光路可逆「reciprocity」）
- 光线投影
  - 定义：假设成像平面上的每个像素与摄像机连一根线，这个线打到场景的某个位置，判定这个点是不是对光源可见，有多少能量。
  <img src="./image/ray_casting.png" alt="光线投影" width="400px"></img>
  - 弊端：光线会做多次反射折射
- 递归光线追踪 Whitted-Style
  - 过程
    - 计算从眼睛出来的光线的折射与反射，以及他们对应的能量
    - 在每一个弹射的点，与光源做一条连线，计算这些弹射的点着色的值，并把它们加起来。要包括能量损失。
    <img src="./image/whitted_style.png" alt="whitted光线追踪" width="600px"></img>
    - 专有名词：
      1. primary ray：射线从眼睛到物体
      2. secondary rays：经过物体后反射或折射后的射线
      3. shadow rays：从作色点到光源判定可见性的点
### 相机光线（空间转换）
- 栅格空间「raster space」$\rightarrow$ NDC「归一化空间」
  - 屏幕像素点转$[0,1]$空间
- NDC「归一化空间」$\rightarrow 屏幕空间
  - $[0,1]$空间转$[-1,1]$
  <img src="./image/NDC.png" alt="光线归一化" width="200px"></img>
- 公式：
  - $ImageAspectRatio = \frac{ImageWidth}{ImageHeight}$ 屏幕比，使得长方形转成正方形
  - $PixelCamera_x = (2 \times PixelScreen_x - 1) \times ImageAspectRatio$
  - $PixelCamera_y = (1 - 2 \times PixelScreen_y)$
- 考虑视野范围：
  - $PixelCamera_x = (2 \times PixelScreen_x - 1) \times ImageAspectRatio tan(\frac{\alpha}{2})$
  - $PixelCamera_y = (1 - 2 \times PixelScreen_y) \times tan(\frac{\alpha}{2})$
  <img src="./image/camera_field.png" alt="摄像机视野" width="300px"></img>
- 最后统一世界空间，方便所有物体在同一空间计算
- ref: [Ray-Tracing: Generating Camera Rays](https://www.scratchapixel.com/lessons/3d-basic-rendering/ray-tracing-generating-camera-rays)

### 焦点
- 射线（ray）
  - 定义：一个起点与一个方向
  - 图例：<img src="./image/ray_equation.png" alt="光线公式" width="300px"></img>
  - 公式：$r(t)=o+td$&nbsp;&nbsp;&nbsp;$0\leq t \lt\infty$
    任何光线上的点都可以用这个公式表示
- 射线与球的焦点
  - 光线：$r(t)=o+td$&nbsp;&nbsp;&nbsp;$0\leq t \lt\infty$
  - 球（隐式表示）：$p:(p-c)^2-R^2=0$
  - 焦点：$(o+td-c)^2-R^2=0$
  - 计算：$at^2+bt+c=0$ where 
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $a=d \times d$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $b=2(o-c) \times d$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $c=(o-c) \times (o-c) - R^2$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $t=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$
  根据$b^2-4ac$与0的关系则可判断射线与球的相交、相切、相离关系
  后计算较小的t则为光线与球的焦点
- 射线与隐式表面的焦点
  - 光线：$r(t)=o+td$&nbsp;&nbsp;&nbsp;$0\lt t \lt\infty$
  - 一般隐式表面：$p:f(p)=0$
  - 焦点：$f(o+td)=0$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;t解出来一定要是实数、正数
- 射线与三角形网格的焦点
  - 用处：
    - 判断光线是否可见，阴影等
    - 判断一个点是否在物体内。一个点如果在物体内随便作一条射线，那它的焦点一定是奇数
  - 如何计算场景物体与光线的焦点：
    - 计算每根射线与每个三角形的焦点
    - 缺点：计算量大，后期说优化
  - 求光线和三角形焦点：
    1. 第一种方法
      - 过程
        1. 光线和平面求焦点
        2. 判断焦点是否在三角形内
      - 平面定义
        - 定义一个法线与一个点
        <img src="./image/plane_def.png" alt="定义平面" width="300px"></img>
        - 公式：$p:(p-p') \cdot N = 0$ 将点展开成xyz可得 $ax+by+cz+d=0$
      - 焦点：$(p-p') \cdot N = (o+td-p') \cdot N = 0$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $t=\frac{(p'-o)\cdot N}{d\cdot N}$ Where $0\leq t \lt\infty$
    2. 第二种方法(Moller Trumbore算法)
      - 公式：$\vec{O}+t\vec{D}=(1-b_1-b_2)\vec{P_0}+b_1\vec{P_1}+b_2\vec{P_2}$ 后半部分为重心坐标
      - 转换：$\begin{bmatrix} t\\b_1\\b_2 \end{bmatrix}=\frac{1}{\vec{S_1}\cdot\vec{E_1}}\begin{bmatrix}\vec{S_2}\cdot\vec{E_2}\\\vec{S_1}\cdot\vec{S}\\\vec{S_2}\cdot\vec{D} \end{bmatrix}$ 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Where:
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\vec{E_1}=\vec{P_1}-\vec{P_0}$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\vec{E_2}=\vec{P_2}-\vec{P_0}$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\vec{S}=\vec{O}-\vec{P_0}$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\vec{S_1}=\vec{D}\times\vec{E_2}$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\vec{S_2}=\vec{S}\times\vec{E_1}$
        总共消耗：1次除法，27次乘法和1次加法
      - 判断是否满足：
        1. t是正的
        2. $(1-b_1-b_2), b_1, b_2$为正数，则点在三角形内
### 包围盒
- 前情提要：通过计算每个光线与每个平面是否相交，计算量大，速度慢
- 优化
  - 包围盒（Bounding Volumes）
    - 定义：
      - 将物体用一个简单几何包围起来
      - 光线如果不会碰到包围盒那就不会碰到物体
    - 方形包围盒：
      - 定义： 三个不同的对面(slabs)形成的交集
      <img src="./image/slabs.png" alt="对面" width="300px"></img>
    - 轴对齐包围合「Axis-Aligned Bounding Box (AABB)」
      - 定义：任何轴都是沿着x、y、z轴
    - 判定光线是否与包围盒相交
      - 2D例子
        1. 计算光线(这里用直线)与$x_0$与$x_1$平面的相交点
        2. 计算光线(这里用直线)与$y_0$与$y_1$平面的相交点
        3. 计算相交后中间线段的交集，这段光线就是再包围盒内部
          <img src="./image/AABB2D.png" alt="2D包围盒" width="600px"></img>
      - 要点
        - 光线进入包围盒仅在他们穿过所有对面的时候
        - 光线只要离开一个对面就是离开包围盒
      - 计算：
        - 每个平面都有一个$t_{max}$和$t_{min}$
        - 对于一个3D的包围盒，$t_{enter}=max(t_{min})$, $t_{exit}=max(t_min)$
        - 如果$t_{enter}\lt t_{exit}$，则光线穿过包围盒
      - 不同情况
        - $t_{exit}\lt0$: 光线在包围盒后面，不相交
        - $t_{exit}\geq0$，$t_{exit}\lt0$: 光线起点在包围盒内部，有相交
        - 总结：光线与AABB相交iff（当且仅当）$t_{enter}\lt t_{exit}$ && $t_{exit}\geq 0$
      = 为什么选与轴平行的面来做包围盒
        - 普通面
          $t=\frac{(p'-o)\cdot N}{d\cdot N}$
          <img src="./image/general_plate.png" alt="一般平面" width="300px"></img>
        - 与x轴平行的面
          $t=\frac{(p_{x}'-o_x)}{d_x}$
          <img src="./image/plate_with_x.png" alt="与x轴平行的平面" width="300px"></img>
#### 均匀格子（Uniform grids）
- 过程
  1. 找到场景，找出包围盒
   <img src="./image/uniform_grid1.png" alt="找出包围盒" width="300px"></img>
  2. 将包围盒划分成多个网格
  <img src="./image/uniform_grid2.png" alt="找出包围盒" width="300px"></img>
  3. 计算格子与物体表面是否相交
  <img src="./image/uniform_grid3.png" alt="找出包围盒" width="300px"></img>
  4. 计算光线与网格是否相交
  5. 相交情况下，计算光线与物体是否相交
  <img src="./image/uniform_grid4.png" alt="找出包围盒" width="300px"></img>
- 问题：
  - 如果格子划分的太少（极端点一个），计算后，得算每个光线与物体的焦点，与没用均匀格子无异
  - 如果格子划分的太多，会计算过多光线与格子的相交，浪费性能
- 结论
  - 三维中，格子数量$=27\times$物体数量
#### 空间划分（Spatial partitions）
- 空间划分例子
  - 八叉树
    - 定义：不断对一个空间进行切割，三维中每个节点与子节点切成八个（二维看起来是4个），最后来判断是否与物体有相交
    - 什么时候停下来？根据制定的规则
    - 缺点：划分太多，如果维度增加，格子数量将成倍增加
  - KD树
    - 定义；每次只会在一个区域交替沿着其中一个轴砍一刀分成两个
    - 比如三维中，会以x，y，z轴的顺序进行划分
  - BSP树
    - 定义：每次只会在一个区域交替砍一刀分成两个
    <img src="./image/spatial_partitions_example.png" alt="空间划分例子" width="600px"></img>
  - 对于包围盒中，与轴平行的利于计算，所以这边有限采用kd树
- KD树（KD-tree）
  - 图例
  <img src="./image/KDTree.png" alt="kd树图例" width="600px"></img>
  （PS: 1,2,3等节点还需要进一步划分，只是这边简化了节点树）
  - 内部节点存储结构
    - 根据哪个轴划分（x、y、z）
    - 划分的位置
    - 子节点（一定会事子节点）
    - 实际的物体不存在于子节点，只存在于叶子节点上
  - 叶子节点储存结构
    - 物体列表
  - 如何利用KD树加速光线追踪
    1. 从当前区域（最外层）开始进行判断是否与光线有交集
    <img src="./image/internal_node.png" alt="计算内部节点" width="400px"></img>
    2. 对叶子结点判断于光线是否有交集，有交集后把第二步当第一步继续递归
    <img src="./image/leaf_node.png" alt="计算叶子节点" width="400px"></img>
    3. 直到没有叶子结点为止，计算光线与当前区域内所有物体的焦点位置，计算最近的焦点
    <img src="./image/intersection_found.png" alt="求光线焦点" width="400px"></img>
  - KD树的问题（现在很少用kd树，近十年问题还没有解决[2020年]）
    - 不好判定一个三角形在包围盒内还是外
      简单通过三角形顶点判断的话，容易出现包围盒在三角形内，但是这个三角形却不算在包围盒内的三角形的错误情况
    - 有时候一个物体穿过多个盒子，容易储存到多个盒子中，重复计算
#### 物体划分（Object partition）
- 层次包围盒「Bounding Volume Hierarchy -- BVH」
  - 过程：
    - 找到最外层包围盒
    - 递归该步骤将当前包围盒划分成两个并重新判断包围盒
    - 直到叶子节点拥有较少的三角形
    <img src="./image/BVH1.png" alt="BVH" width="400px"></img>
    <img src="./image/BVH2.png" alt="BVH" width="400px"></img>
    <img src="./image/BVH3.png" alt="BVH" width="400px"></img>
    （PS：包围盒子可能相交，物体只会在一个包围盒中，尽可能重叠的少）
  - 划分技巧：
    1. 选择长的轴进行划分
    2. 取中间的物体进行划分
  - 存储
    - 内部节点
      - 包围盒信息
      - children节点指针
    - 叶子节点
      - 包围盒信息
      - 物体列表
  - 算法
    ``` C++
    Intersect(Ray ray, BVH node) {
      if (ray misses node.bbox) return;

      if (node is a leaf node)
        test intersection with all objs;
        return closest intersection;

      hit1 = Intersect(ray, node.child1);
      hit2 = intersect(ray, node.child2);
    }
    ```
#### 空间划分 VS 物体划分
- 空间划分
  - 包围盒不重叠
  - 物体可能在多个包围盒
- 物体划分
  - 包围盒重叠
  - 物体只会在一个包围盒

### 辐射度量学「Basic Radiometry」
- 为什么要使用辐射度量学
  - Blinn-Phong光比如用10，那么单位是什么
  - Whitted风格的光线追踪不够真实，其中做了很多的简化
    - 比如光线的反射到一定的区域里，而不是沿着完美的镜像方向去
    - 折射每次损失是多少？
  - 辐射度量学将给我们实际的光的物理量方法，我们可以将光准确的定义出来，包括精确的描述物体表面与光的作用，与光源材质，光源传播方法等
- 定义：如何去描述光，其中定义了一系列的方法与空间中属性，当还是几何光学（如直线传播没有波动性）
  - 光照属性：
    - radiant flux（辐射通量）
    - intensity（辐射强度）
    - irradiance（辐射照度）
    - radiance（辐射亮度）
#### 能量与通量
- Radiant Energy[辐射能量]
  - 定义：电磁辐射的能量
  - 单位：焦耳[Joule]
  - 符号：Q[J=Joule]
- Radiant Flux(Power)[辐射通量]
  - 定义：每单位之间放射、反射、转移或接受的能量
  - 单位：瓦特[W=Watt][lm=lumen]*
  - 符号：$\Phi=\frac{dQ}{dt}$
#### 光的测量
- 可参考：[辐射强度，辐射照度，辐射亮度](https://zhuanlan.zhihu.com/p/495584698)
- 三种测量
  - Radiant Intensity 辐射强度
  - Irradiance 辐照度
  - Radiance 辐亮度
  <img src="./image/light_measurements.png" alt="光线测量" width="400px"></img>
- 辐射强度
  - 定义：每单位立体角(solid angle)的能量
  - 公式：$I(\omega)\equiv\frac{d\Phi}{d\omega}$ ($\Phi$辐通量，$\omega$立体角)
  - 单位：$\frac{W}{sr}$ 或 $\frac{lm}{sr}=cd=candela$  ($sr$立体角)
  - 角度
    - 定义：圆弧长度与半径之比
    - 公式：$\theta=\frac{l}{r}$ 
    - 圆有$2\pi$的角度 （单位：radians）
    <img src="./image/angle.png" alt="角度" width="200px"></img>
  - 立体角
    - 定义：球体上的减去面积与半径平方的比率 
    - 公式：$\Omega=\frac{A}{r^2}$
    - 整个球有$4\pi$的立体角 （单位：steradians）
    <img src="./image/solid_angle.png" alt="立体角" width="200px"></img>
  - 微分立体角
    - 微分立体面积为：$dA=(rd\theta)(rsin\theta d\phi)=r^2sin\theta d\theta d\phi$
    <img src="./image/differential_solid_angles_area.png" alt="微分立体面积" width="600px"></img>
    现在的我不懂记录的，希望我以后不懂看一眼就懂：
      1. 其中弧度的定义就是其所对的单位圆的弧的长度，所以这里竖直区域的边长为$rd\theta$,水平的边长为$rsin\theta d\phi$，均为弧度制
      2. 通过$\theta$和$\phi$能定义一个立体角的位置
    - 可推导出：$d\omega=\frac{dA}{r^2}=sin\theta d\theta d\phi$
    - 所以如果把整个球里面所有单位立体角积分加起来应该就是$4\pi$
      Sphere:$S^2$
      $\Omega = \int_{S^2}d\omega$
      &nbsp;&nbsp;&nbsp;&nbsp;$=\int_{0}^{2\pi}\int_{0}^{\pi}sin\theta d\theta d\phi$
      &nbsp;&nbsp;&nbsp;&nbsp;$=4\pi$
  - 各向同性的点源
    - 能量：$\Phi = \int_{S^2}Id\omega$
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$=4\pi I$
    - 通量：$I=\frac{\Phi}{4\pi}$
      <img src="./image/isotropic_point_source.png" alt="各向同性的点源" width="400px"></img>
  - 现实例子
    - 下列灯泡输出815流明
    - 11w功率，60w是等效白炽灯
    - 假设是均匀扩散的光源，辐射强度（通量）为：
      $Intensity = 815\ lumens\ / \ 4\pi sr$
    <img src="./image/radiant_intensity_live.png" alt="辐射强度现实例子" width="400px"></img>
- 辐照度 Irradiance
  - 定义：一个表面点上所收到的能量。只有和入射光线相垂直的光线才算，如果不垂直，只能计算垂直的分量（如照明与着色中Blinn-Phong模型的漫反射中所说）
  - 公式：$E(x)\equiv\frac{d\Phi(x)}{dA}$
  - 单位：$\frac{W}{m^2}$ 或 $\frac{lm}{m^2} = lux$
  <img src="./image/irradiance1.png" alt="辐照度" width="200px"></img>
  <img src="./image/irradiance2.png" alt="能量衰减" width="500px"></img>
- 辐亮度 Radiance
  - 定义：每单位立体角和每单位投影面积上，由表面反射、发射或接收的能量。
  - 公式：$L(p,\omega)=\frac{d^2\Phi(p,\omega)}{d\omega dAcos\theta}$ （这边2是2次微分，$dAcos\theta$是A区域投影到垂直光线的面积，$p$为照射到的点）
  （PS：为什么cos在下面，那不是会出现角度越大，亮度越高吗？
    这个结论成立的前提条件是要确定辐射强度（即单位立体角内的辐射通量）和方向角的关系。像朗伯面是辐射强度与方向角的关系是满足余弦定律，最后计算的结果就是朗伯面在各个方向的辐射亮度相等。引用：https://www.zhihu.com/question/54561197）
  - 单位：$\frac{W}{sr\ m^2}$或$\frac{cd}{m^2}=\frac{lm}{sr\ m^2}=nit$
  <img src="./image/radiance.png" alt="能量衰减" width="500px"></img>
  - 根据前面辐通量辐照度的定义，我们还可以得到：
    - 辐亮度是每单位投影面积的辐通量
    - 辐亮度是每单位立体角的辐照度
  - 入射光线（Incident Radiance）
    - 公式：$L(p,\omega)=\frac{dE(p)}{d\omega cos\theta}$
    <img src="./image/incident_radiance.png" alt="入射光线" width="500px"></img>
  - 射出光线（Exiting Radiance）
    - 公式：$L(p,\omega)=\frac{dI(p,\omega)}{dAcos\theta}$
    <img src="./image/incident_radiance.png" alt="入射光线" width="500px"></img>
  - 辐射照度vs辐射亮度
    - 辐射照度与角度无关，是$dA$区域所收到全部能量
    - 辐射亮度$dA$区域接收来自$d\omega$单位立体角的能量
    - 可推导出：
      $dE(p,\omega)=L_i(p,\omega)cos\theta d\omega$
      积分后：
      $E(p)=\int_{H^2}L_i(p,\omega)cos\theta d\omega$
- 双向反射分布函数（Bidirectional Reflectance Distribution Function [BRDF]）
  - 定义：描述的是物体表面将光能从任何一个入射方向反射到任何一个视点方向的反射特性，即入射光线经过某个表面反射后如何在各个出射方向上分布(光可能向各个方向都有反射，BRDF就是在定义如何)
  <img src="./image/brdf.png" alt="BRFD" width="400px"></img>
  传入的辐照度「Differential irradiance incoming」：$dE(\omega_i)=L(\omega_i)cos\theta_i d\omega_i$
  传出的辐亮度「Differential radiance exiting」来自$dE(\omega_i)$: $dL_r(\omega_r)$
  - 公式：$f_r(\omega_i \rightarrow \omega_r) = \frac{dL_r(\omega_r)}{dE_i(\omega_i)} = \frac{dL_r(\omega_r)}{L_i(\omega_i)cos\theta_i d\omega_i}$
  - 单位：$(sr)^{-1}$
  - 一些理解：这个公式是一个函数，记录每个入射方向（$\omega_i$）与出射方向（$\omega_r$）能量的分配。
  - 反射方程（推导出）
    <img src="./image/reflection_equation.png" alt="反射方程" width="400px"></img>
    - $L_r(p, \omega_r) = \int_{H^2}f_r(p, \omega_i \rightarrow \omega_r)L_i(p,\omega_i)cos\theta_i d\omega_i$
    - 将所有对当前出射方向有贡献的入射方向提供的能量加起来，就可以反应出当前出射方向
    - 这是一个递归的函数，这次的入射可能是其他出射
- 渲染(绘制)函数「Rendering Equation」（下面单独详细讲）
  - 公式：$L_o(p, \omega_o) = L_e(p,\omega)+\int_{\Omega^+}L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)(n\cdot\omega_i)d\omega_i$
  - $L_e(p, \omega_o)$为自发光的辐射亮度
  - 所有方向默认为向外的，如$i$
  - $\Omega^+$与$H^2$都可以表示半球
#### 渲染函数
- 反射函数
  - 完整推导
    - 对于单个入射光照：
      <img src="./image/single_reflection.png" alt="单个光源反射方程" width="400px"></img>
      - 公式：$L_r(x,\omega_r)=L_e(x,\omega_r)+L_i(x，\omega_i)f(x,\omega_i,\omega_r)(\omega_i,n)$
      - $L_r(x,\omega_r)$ 为反射的光线，也是输出
      - $L_e(x,\omega_r)$ 为自发光辐射能量
      - $L_i(x，\omega_i)$ 为入射光线
      - $f(x,\omega_i,\omega_r)$ 为BRDF转换函数
      - $(\omega_i,n)$ 入射角度
    - 对于多个入射光照：
      <img src="./image/muli_reflection.png" alt="多个光源反射方程" width="400px"></img>
      - 公式：$L_r(x,\omega_r)=L_e(x,\omega_r)+\sum L_i(x，\omega_i)f(x,\omega_i,\omega_r)(\omega_i,n)$
    - 对于多个面光源
      <img src="./image/surface_reflection.png" alt="面光源反射方程" width="400px"></img>
      - 公式：$L_r(x,\omega_r)=L_e(x,\omega_r)+\int_\Omega L_i(x，\omega_i)f(x,\omega_i,\omega_r)(\omega_i,n)$
      - 把这个面光源所占据的立体角积分，将面光源考虑进去
    - 对于反射光源
      <img src="./image/inter_reflection.png" alt="反射光源反射方程" width="400px"></img>
      - 公式：$L_r(x,\omega_r)=L_e(x,\omega_r)+\int_\Omega L_r(x'，-\omega_i)f(x,\omega_i,\omega_r)cos\theta_i d\omega_i$
      - 把这个面光源所占据的立体角积分，将面光源考虑进去
      - 简化公式：$l(u)=e(u)+\int I(v)K(u,v)dv$
      - 利用操作符(泛符)再次简写：$L=E+KL$
      - 解出$L$:
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$L=E+KL$
        $IL-KL=E$ ($I$为单位矩阵)
        $(I-K)L=E$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$L=(I-K)^{-1}E$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;根据二项式定理（Binomial Theorem）
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$L=(I+K+K^2+K^3+...)E$
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$L=E+KE+K^2E+K^3E+...$
        可去参考陈文灯算子法解微分方程
      - 对于最终化简的全局光照函数$L=E+KE+K^2E+K^3E+...$
        - $E$为光源或自发光
        - $KE$为直接从光源发射后（直接光照）
        - $K^2E$为从光源出来反射一次平面再打到当前平面（间接光照）
        - $K^3E$为从光源出来反射两次平面再打到当前平面（更多的间接光照）
         <img src="./image/global_illumination1.png" alt="反射光源例子" width="200px"></img><img src="./image/global_illumination2.png" alt="反射光源例子" width="200px"></img><img src="./image/global_illumination3.png" alt="反射光源例子" width="200px"></img>
### 概率论
为什么插在这边说？因为要用到呗
#### 随机变量
- 定义： 代表潜在值的分布
- 概率密度函数(probability density function)：
- 简单例子：六面骰子
  $p(1)=p(2)=p(3)=p(4)=p(5)=p(6)$
- 复杂例子：
  <img src="./image/probabilities_ex.png" alt="随机变量例子" width="300px"></img>
  - 值$x_i$与对应概率$p_i$
- 总结：
  - $p_i \ge 0$ 每个概率一定大于等于0
  - $\sum_{i=1}^np_i=1$ 所有的概率加起来等于1
#### 随机变量期望
- 定义：重复取随机变量取平均值
- 公式：$E[X]=\sum_{i=1}^nx_ip_i$
- 骰子例子：$E[X]=\sum_{i=1}^n\frac{i}{6}=3.5$
#### 概率密度函数(probability density function [PDF])
- $X$ ~ $p(x)$ 
- 定义：一个随机变量X可以取一组连续值中的任何一个，其中一个特定值的相对概率由一个连续的概率密度函数p(x)给出
- $p(x)$:
  - $p(x)\geq 0$
  - $\int p(x)dx=1$
- $X$期望: $E[x]=\int xp(x)dx$ 
- 考虑函数满足$X$~$p(x)$和$Y=f(X)$
  - $E[Y]=E[f(X)]=\int f(x)p(x)dx$

### 蒙特卡洛路径追踪
#### 蒙特卡洛积分
- 目的：给任何一个函数，计算其定积分
  - 定积分：函数下的区域面积
  - 不定积分：一个表达式，是一个导数等于$f$的函数$F$，即$F′=f$
  - 可能一个函数是曲折的，无法写成一个式子，跳过不定积分直接计算定积分；
  - 黎曼积分：将函数从a到b均分成n份，每份取中间位置的高度计算该高度对应的面积，并将n份面积累加起来
- 直观实现：
  - 在积分域内不断做随机采用，然后根据x对应的高度y，假设整个函数是一个平的函数
  - 计算平的函数的区域面积
  - 最后对这些采样结果求平均
  <img src="./image/monte_carlo_integration.png" alt="蒙特卡洛积分" width="300px"></img>
- 具体定义：
  - 积分：$\int_a^b f(x)dx$ 对于f(x)函数，积分域为a到b
  - 随机变量：$X_i$ ~ $p(x)$
  - 蒙特卡洛近似：$F_N = \frac{1}{N}\sum_{i=1}^N\frac{f(X_i)}{p(X_i)}$
  - 均匀采样推导：
    - $X_i$~$p(x)=C$ 因为模特卡洛计算$p(x)$时候是固定的，即$C$是固定的
    - $\int_a^bp(x)dx=1$
      $\Rightarrow \int_a^bCdx=1$
      $\Rightarrow C=\frac{1}{b-a}$
  <img src="./image/monte_carlo_estimator.png" alt="蒙特卡洛预估" width="300px"></img>
    - 均匀随机变量：$X_i$ ~ $p(x) = \frac{1}{b-a}$
    - 基础蒙特卡洛近似：$F_N = \frac{b-a}{N}\sum_{i=1}^Nf(X_i)$
#### 路径追踪
- Whitted-Style Ray Tracing
  - 原理
    - 打到光滑物体，发生折射与反射
    - 打到粗糙物体，发射漫反射并停止
  - 问题：
    - 对于glossy材质，反射光还是延着镜面反射的方向是不对的
    - 对于漫反射，停止光漫反射后的传播，这是不对的
- Whitted-Style是错的，渲染方程是对的
- 渲染方程两个计算问题：
  - 积分
  - 递归
- 解渲染方程：
  - 公式：$L_o(p, \omega_o) = L_e(p,\omega)+\int_{\Omega^+}L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)(n\cdot\omega_i)d\omega_i$
  - 利用模特卡洛方法解渲染方程
    - 假设我们要渲染一个像素的直接光照是什么
    - 对于一个着色点看到的光，等同于四面八方来的光和PRDF作用后反射到观察方向
    - 利用蒙特卡洛方法，对半球的入射光线进行随机采样，求最终积分的所有光的值
    - 对于蒙特卡洛积分
      - $f(x)$为$L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)(n\cdot\omega_i)$
      - pdf为$p(\omega_i)=\frac{1}{2\phi}$（对于均匀采样的话）
    - $L_o(p,\omega_o)=\int_{\Omega^+}L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)(n\cdot\omega_i)d\omega_i$
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$\approx\frac{1}{N}\sum_{i=1}^N\frac{L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)(n\cdot\omega_i)}{p(\omega_i)}$
  - 延伸算法（直接光照）
    ```
    shade(p, wo)  // wo为光线出来的方向
      随机选择N个不同的方向，按照wi的pdf  // wi为光线入射方向
      Lo = 0.0
      For each wi
        Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
        if ray r hit the light
          Lo += (1 / N) * Li * fr * cosine / pdf(wi)
      Return Lo
    ```
  - 全局光照算法
    ```
    shade(p, wo)  // wo为光线出来的方向
      随机选择N个不同的方向，按照wi的pdf  // wi为光线入射方向
      Lo = 0.0
      For each wi
        Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
        If ray r hit the light
          Lo += (1 / N) * Li * fr * cosine / pdf(wi)
        Else If ray r hit an object at q
          Lo += (1 / N) * shade(q, -wi) * fr * cosine / pdf(wi)
      Return Lo
    ```
    <img src="./image/global_illumination_path_tracing.png" alt="全局路径追踪" width="600px"></img>
    - 但是每次投射出的光线数量会以指数倍的速度增加
    <img src="./image/explosion_ray_bound.png" alt="指数倍增加光线" width="600px"></img>
  - 避免上述问题，N=1，每次只随机一条的光线
    ```
    shade(p, wo)  // wo为光线出来的方向
      随机选择1个方向，按照wi的pdf 
      Lo = 0.0
      For each wi
        Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
        If ray r hit the light
          Lo += (1 / N) * Li * fr * cosine / pdf(wi)
        Else If ray r hit an object at q
          Lo += (1 / N) * shade(q, -wi) * fr * cosine / pdf(wi)
      Return Lo
    ```
    - 这里可以注意到，一个点上只会接收一条光线，会导致噪点严重，与实际偏差很大。但是可以利用增加透过一个像素的光线数量来规避这个问题。
    <img src="./image/more_path_per_pixel.png" alt="更多光线通过一个" width="400px"></img>
      - 如何计算求从相机经过一个像素到物体的路径
        ```
        ray_generation(camPos, pixel)
          均匀在像素内取N个采样点
          pixel_radiance = 0.0
          for each sample in the pixel
            Shoot a ray r(camPos, cam_to_sample)
            If ray r hit the scene at p
              pixel_radiance += 1 / N * shade(p, sample_to_cam)
          Return pixel_radiance
        ```
    - 还有一个问题，算法不会停止
  - 添加终止条件
    - 不能直接设置次数的终止，直接设置次数终止会导致后面的反射丢失，从而导致能量损失，亮度与真实差异过大
    - 解决：俄罗斯轮盘赌算法
      - 定义：当在概率$P$中，你是ok的，在$1-P$的概率中，你将中弹。其中$0\lt P\lt 1$
    - 运用于路径追踪
      - 我们最后得到的着色点的出射光线为$L_o$
      - 定一个概率$P$, 其中$0\lt P\lt 1$
      - 如果在概率$P$中，发射光线，并且返回结果$\frac{Lo}{P}$
      - 如果在概率$1-P$中，不发射光线，且返回结果为0
      - 通过上述方法，你仍然可以期望最终得到的结果为$L_o$
        $E = P * (\frac{L_o}{P}) + (1 - P) * 0 = L_o$
        ```
        shade(p, wo)  // wo为光线出来的方向
          人工生成一个特殊概率P_RR
          随机在[0, 1]均匀选择一个ksi
          If (ksi > P_RR) return 0.0;

          随机选择1个方向，按照wi的pdf 
          Lo = 0.0
          For each wi
            Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
            If ray r hit the light
              Lo += (1 / N) * Li * fr * cosine / pdf(wi) / P_RR  // 除P_RR是补偿概率下的能量损失
            Else If ray r hit an object at q
              Lo += (1 / N) * shade(q, -wi) * fr * cosine / pdf(wi) / P_RR  // 除P_RR是补偿概率下的能量损失
          Return Lo
        ```
        **这个为路径追踪的最后公式**
  - 小问题，小优化
    - 在低采样的时候噪声还是严重，但这个路径追踪已经是对的
    <img src="./image/low_spp.png" alt="低采样的噪声" width="400px"></img>
    - 原因：
      - 如果光源较小，那如果我们采用均匀采样就会导致有很多的光线被浪费，无法发射到光源上，需要有更多的光线才能找到光源
      <img src="./image/more_rays.png" alt="光源更少，光线要更多才能找到光源" width="400px"></img>
    - 优化：
      - 如果可以对光源进行采样的话，就不会有光线被浪费了
      - 对于光源进行均匀采样：$pdf = \frac{1}{A}$ 因为$\int pdf\, dA=1$
      - 但是渲染方程是在积分单位立体角：$L_o=\int Li\, fr\, cos\, d\omega$
       
    - 通过换元，将对立体角积分转为对光源平面进行积分
      <img src="./image/sample_from_ray.png" alt="单位立体角与光源" width="400px"></img>
      - $d\omega = \frac{dAcos\theta'}{||x'-x||^2}$ $dAcos\theta'$为将光源平面转为投影于立体角平面的方向，后除两个位置的距离的平方，即算出单位半球的投影面积
      - $L_o(p, \omega_o) = L_e(p,\omega)+\int_{\Omega^+}L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)cos\theta d\omega_i$
       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $= L_e(p,\omega)+\int_{A}L_i(p,\omega_i)f_r(o,\omega_i,\omega_o)\frac{cos\theta cos\theta'}{||x'-x||^2} dA$
    - 这样子就可以把问题分成两部分
      - 直接光照 不需要轮盘赌 
      - 间接光照 需要轮盘赌
       <img src="./image/sample_light.png" alt="渲染方程区分" width="400px"></img>
      - 伪代码实现：
      ```
        shade(p, wo)  // wo为光线出来的方向
          // 从光源产生贡献
          均匀在x'位置的光源平面采样（pdf_light = 1 / A）
          L_dir = Li * fr * cosθ * cosθ' / |x' - p|^2 / pdf_light


          // 从其他反射面产生贡献
          L_indir = 0.0
          使用P_RR概率测试俄罗斯轮盘赌，具体看前面
          均匀的在半球立体角wi上进行采样（pdf_hemi = 1 / 2pi）
          Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
          If ray r hit a 不会发光的 object at q
            L_indir = shaed(q, -wi) * fr * cosθ / pdf_hemi / P_RR

          Return L_dir + L_inder
      ```
      - 上述还有个小小问题：如果光源于p点中有物体遮挡
      ```
        shade(p, wo)  // wo为光线出来的方向
          // 从光源产生贡献
          均匀在x'位置的光源平面采样（pdf_light = 1 / A）
          L_dir = Li * fr * cosθ * cosθ' / |x' - p|^2 / pdf_light


          // 从其他反射面产生贡献
          L_indir = 0.0
          使用P_RR概率测试俄罗斯轮盘赌，具体看前面
          均匀的在半球立体角wi上进行采样（pdf_hemi = 1 / 2pi）
          从p点向x‘位置放出一条光线
          If the ray is not blocked in the middle
            Trace a ray r(p, wi)  // 从着色点朝方向wi打出一个光线
            If ray r hit a 不会发光的 object at q
              L_indir = shaed(q, -wi) * fr * cosθ / pdf_hemi / P_RR

          Return L_dir + L_inder
      ```
- 总结：
  - 路径追踪是一个近乎100%正确的算法
  - 光线追踪：以前 vs. 现代概念
    - 以前：
     - 光线追踪 = whitted-style 光线追踪
    - 现代：
      - 包含各种光线传播算法
        - Path tracing
        - Photon mapping
        - Metropolis light Transport
        - VCM / UPBP ...
  - 采样理论
    - 怎么样对一个函数进行均匀采样
  - 采样
    - 以后还有重要性采样
  - 随机数的质量有没有问题？
    - 有的，低差异序列
  - 结合光源于采样点结合起来
    - multiple imp. sampling
  - 为什么平均像素多个光线的辐射就是最终的值？
    - pixel reconstruction filter
  - radiance是不是颜色？
    - 不是，还得做gamme矫正，曲线，颜色空间
  - 路径追踪仍然是indroductory的

## 材质与外观
- 外观是光照和材质共同作用的结果
- 不同的材质，在光线作用下获得不同的结果，同样的模型也会渲染出不同结果
  <img src="./image/materials_appearances.png" alt="材质与外观" width="400px"></img>
- brdf来决定材质，所以$Material==BRDF$
### 不同反射材质
#### 漫反射/朗伯[Lambertian]材料
- 假设入射光是均匀的，那么入射光的radiance和出射光的是一样的，且完全不吸收能量
  <img src="./image/diffuse_material.png" alt="漫反射材质" width="400px"></img>
- 渲染方程：$L_o(\omega_o)=\int_{H^2}f_rL_i(\omega_i)cos\theta_id\omega_i$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;$=f_rL_i\int_{H^2}\sout{(\omega_i)}cos\theta_id\omega_i$
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;$=\pi f_rL_i$
  - 因为入射radiance等于出射的radiance，所以$L_i=L_o$
  - $f_r=\frac{\rho}{\pi}$ $\rho$为反射率，可以是单通道，也可以是rgb等等
#### Glossy材料
- 很像镜面反射，但是不完全是镜面反射，稍微有点粗糙。类似金属抛光后的感觉
  <img src="./image/glossy_material.png" alt="glossy材质" width="400px"></img>
  <img src="./image/glossy_example.png" alt="glossy材质例子" width="400px"></img>
#### 理想反射/折射材料（BSDF）
- 同时具有反射和折射，经典的如玻璃与水
  - $BSDF = BRDF + BTDF$

  <img src="./image/bsdf_material.png" alt="bsdf材质" width="400px"></img>
  <img src="./image/bsdf_example.png" alt="bsdf材质例子" width="400px"></img>

### 折射与反射
#### 完美镜面反射
- 拆解光线到$\theta$与$\phi$两个方向
  - $\theta$方向
    <img src="./image/reflection_theta.png" alt="反射theta方向" width="300px"></img>
    $\theta=\theta_o=\theta_i$
    $\omega_o+\omega_i=2cos\theta\vec{n}=2(\omega_i\cdot\vec{n})\vec{n}$
    $\omega_o=-\omega_i+2(\omega_i\cdot\vec{n})\vec{n}$
  - $\phi$方向
    <img src="./image/reflection_phi.png" alt="反射phi方向" width="300px"></img>
    $\phi=(\phi_i+\pi)mod2\pi$
#### 镜面折射
- 斯涅尔定律
  <img src="./image/snell1.png" alt="反射phi方向" width="300px"></img>
  $\eta_i sin\theta_i=\eta_t sin\theta_t$ $\eta$代表折射率
  <img src="./image/snell2.png" alt="反射phi方向" width="300px"></img>
  $\varphi_t = \varphi_i\pm\pi$
  - $cos\theta_t = \sqrt{1-sin^2\theta_t}$
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$= \sqrt{1-(\frac{\eta_i}{\eta_t})^2sin^2\theta_i}$
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;$= \sqrt{1-(\frac{\eta_i}{\eta_t})^2(1-cos^2\theta_i)}$
  - 为了结果有意义，所以 $1-(\frac{\eta_i}{\eta_t})^2(1-cos^2\theta_i) \lt 0$
  - 又因为$1-cos^2\theta_i一定小于1$，所以$\frac{\eta_i}{\eta_t} \gt 1$
  - 如果入射介质的折射率大于折射介质的折射率就会发生全反射
- Snell’s Window / Circle
  - 因为水的折射率比较大，所以超过一定角度后，就会发生全反射现象
  <img src="./image/snell_window.png" alt="snell窗口现象" width="400px"></img>
#### Fresnel Refection/Term 菲涅尔项
- 定义：反射率取决于入射角（和光的偏振）
- 例子：<img src="./image/fresnel_example.png" alt="菲涅尔例子" width="400px"></img>
- 绝缘体与导体不同的菲涅尔项
  - 折射率为1.5的绝缘体的菲涅尔项（虚线是两个方向的极化）
  <img src="./image/fresnel_dielectric.png" alt="绝缘体" width="400px"></img>
  - 导体的菲涅尔项
  <img src="./image/fresnel_conductor.png" alt="导体" width="400px"></img>
- 计算：
  - 准确：
    $R_s = \lvert\frac{n_1cos\theta_i-n_2cos\theta_t}{n_1cos\theta_i+n_2cos\theta_t}\rvert^2 = \lvert\frac{n_1cos\theta_i-n_2\sqrt{1-(\frac{n_1}{n_2}sin\theta_i)^2}}{n_1cos\theta_i+n_2\sqrt{1-(\frac{n_1}{n_2}sin\theta_i)^2}}\rvert^2$
    $R_p = \lvert\frac{n_1cos\theta_t-n_2cos\theta_i}{n_1cos\theta_t+n_2cos\theta_i}\rvert^2 = \lvert\frac{n_1\sqrt{1-(\frac{n_1}{n_2}sin\theta_i)^2}-n_2cos\theta_i}{n_1\sqrt{1-(\frac{n_1}{n_2}sin\theta_i)^2}+n_2cos\theta_i}\rvert^2$
    $R_{eff}=\frac{1}{2}(R_s+R_p)$
  - 大约：Schlick近似
    $R(\theta)=R_0+(1-R_0)(1-cos\theta)^5$
    $R_0=(\frac{n_1-n_2}{n_1+n_2})^2$

### 微表面「Microfacet」
- 离物体足够远的时候，就看不到其中的细节。我们只能看到物体对表面的作用
- 从远处看，看到材质与外观
  从近处看，看到的是几何
- 每个微表面都有自己的法线
- 微表面brdf模型
  - 微表面上的法线分布
    - 集中的 $\Leftrightarrow$ glossy
    <img src="./image/microfacet_concentrated.png" alt="法线分布集中" width="400px"></img>
    - 分散的 $\Leftrightarrow$ 漫反射材质
    <img src="./image/microfacet_spread.png" alt="法线分布分散" width="400px"></img>
  - brdf计算
    - $f(i, o)= \frac{F(i,h)G(i,o,h)D(h)}{4(n,i)(n,o)}$
    - $F(i,h)$ 菲涅尔项：根据入射方向，有不同程度的反射
    - $G(i,o,h)$ 几何项：微表面的自身互相遮挡。对于接近grazing angle的光线，容易发生自遮挡
    - $D(h)$ 法线分布：任何一个给定方向上，给定的值是多少。给定半程向量，为了计算只有法线方向与半程向量方向相同的时候，才会将入射反射到出射
    <img src="./image/microfacet_brdf.png" alt="微表面brdf" width="400px"></img>
### 各项同性与各向异性[Isotropic&Anisotropic]
- 区别：
  - 各项同性的法线分布均匀，方向性弱
  - 各项异性的法线分布不均匀，方向性明显
  <img src="./image/iso_anisotropic.png" alt="法线分布分散" width="400px"></img>
- 表现在$BRDFs$上
  - $f_r(\theta_i,\phi_i;\theta_r,\theta_r) \neq f_r(\theta_i,\theta_r,\phi_r-\phi_i)$
  - 解释：旋转后入射角与出射角后，看到的是相同的$BRDF$那就是各项同性，反之亦然
- 各项同性例子
  <img src="./image/isotropic_example1.png" alt="各项同性例子" width="300px"></img>
- 各项异性例子
  <img src="./image/anisotropic_example1.png" alt="各项异性例子" width="300px"></img>
  <img src="./image/anisotropic_example2.png" alt="各项异性例子" width="300px"></img>
  <img src="./image/anisotropic_example3.png" alt="各项异性例子" width="300px"></img>
  <img src="./image/anisotropic_example4.png" alt="各项异性例子" width="300px"></img>
  <img src="./image/anisotropic_example5.png" alt="各项异性例子" width="300px"></img>
- $BRDFs$性质
  - 能量非负：$f_r(\omega_i\rightarrow\omega_r)\ge0$
  - 线性：$L_r(p, \omega_r)=\int^{H^2}f_r(p,\omega_i\rightarrow\omega_r)L_i(p,\omega_r)cos\theta_id\omega_i$
  <img src="./image/brdfs_linear.png" alt="brdfs的线性" width="300px"></img>
  - 可逆性[reciprocity]：$f_r(\omega_r\rightarrow\omega_i)=f_r(\omega_i\rightarrow\omega_r)$
  <img src="./image/brdfs_reciprocity.png" alt="brdfs的可逆性" width="300px"></img>
  - 能量守恒: $\forall\omega_r\int_{H^2}(\omega_i\rightarrow\omega_r)cos\theta_id\omega_i\le1$
  - 如果为各向同性：$f_r(\theta_i,\phi_i;\theta_r,\theta_r) = f_r(\theta_i,\theta_r,\phi_r-\phi_i)$
    由于可逆性：$f_r(\theta_i,\theta_r,\phi_r-\phi_i) = f_r(\theta_r,\theta_i,\phi_i-\phi_r) = f_r(\theta_i,\theta_r,|\phi_r-\phi_i|)$
    <img src="./image/isotropic_prop.png" alt="各项同性的推导公式" width="300px"></img>
### 测量$BRFDs$
- 基础操作
  <img src="./image/brdfs_measure.png" alt="测量brdfs" width="300px"></img>
- 一般操作
  ```
  foreach outgoing direction wo
    move light to illuminate surface with a thin beam from wo
    for each incoming direction wi
      move sensor to be at direction wi from surface
      measure incident radiance
  ```
- 优化计算
  - 如果各项异性，可以从4D减到3D(4D指，相机两个方向移动，光源两个方向移动)
  - 根据可逆性，可以砍掉一半的计算量
  - 采样若干方向，猜出来等等
- 存储
  - 压缩
  - 神经网络等等
- 扩展
  - 有名BRDF材质库：MERL

## 渲染中的高级话题
### 高级的光线传输
- 无偏的光线传播方法
  - Bidirectional path tracing(BDPT) 双向路径追踪
  - Metropolis light transport(MLT) 梅特罗波利斯光传输
- 有偏的光线传播方法
  - Photon mapping 光子映射
  - Vertex connection and merging(VCM) 光子映射与双向路径追踪的结合
- 即时辐射度算法
  - VPL
  - ...
### 有偏[biased]与无偏[unbiased]
- 无偏
  - 无偏的蒙特卡洛方法不会有任何的系统误差，无论使用多少个样本，期望得出来的估计值永远是积分的情况
- 有偏
  - 估计出来的值它的期望与最终得到的值不同，就是有偏的
  - 特殊的有偏估计——consistent：当取样无穷大时没有系统误差
### 双向路径追踪
- 过程：
  1. 从光源与摄像机同时打出一条子路径
  2. 将两个子路径的末尾连接起来
  <img src="./image/bdpt.png" alt="bdpt" width="300px"></img>
- 适合场景  
  - 在光源一侧具有复杂的光线传播
  - 例子：
  <img src="./image/bidirectional_example.png" alt="双向路径追踪例子" width="300px"></img>
  - 分析：在这个场景中，可以看到左边的光源只想上打出光线，意味着场景中的很多点通过随机路径最终很难去找到光源，这样子就会导致噪点很多。但是如果双向路径追踪的话，将从光源向其他方向随机路径，后再将两边连起来计算，可以轻松的从相机找到场景再找到光源。
- 缺点
  - 难以实现
  - 计算速度慢
#### 梅特罗波利斯光传输
- 马尔可夫链蒙特卡洛(MCMC)应用：根据当前样本生成跟它靠近的下一个样本
- 一个很好的**局部**方法来探索复杂的光路
  <img src="./image/mcmc.png" alt="马尔可夫链蒙特卡洛" width="600px"></img> 
- 例子：
  <img src="./image/mlt.png" alt="mlt例子" width="600px"></img> 
  - 在第一个场景中，光源只有从门缝中进来，只有门处是被光线直接着凉
  - 在第二个场景中，光线从空气中进入水面，后打到池子地地面漫反射，后再通过折射再出水面。specular-diffuse-specular[SDS]
- 缺点：
  - 难以分析渲染的收敛速度
  - 所有操作都是局部的，有的像素收敛的快，有的像素收敛的慢。导致结果很脏
  - 因为不知道什么时候收敛，就没办法用于渲染动画。上一帧和这一帧可能收敛不同，画面抖动严重
#### 光子映射
- 它是一个有偏的方法
- 对于处理之前SDS情况非常擅长，生成caustics[焦散]由于光线的聚焦，产生一些很强的图案
  <img src="./image/photo_mapping.png" alt="光子映射例子" width="600px"></img> 
- 实现方法（其中一种）
  - 操作：
    - 第一步：光子路径
      - 光子从光源被发射出来，与物体发生反射折射，直到遇到漫反射物体，光子就停在那边
      <img src="./image/photo_mapping_first_stage.png" alt="光子映射第一步" width="400px"></img>
    - 第二步：光子收集
      - 从眼睛[摄像机]射出子路径，同样与物体发生反射与折射，直到撞击到漫反射面停止
      - 计算局部密度估计：
        - 对于每个着色点，找临近的N个光子与所占的面积，即算出光子的密度
      <img src="./image/photo_mapping_second_stage.png" alt="光子映射第二步" width="400px"></img>
  - 如果N小，就会有很多噪点。如果N大，会导致图片模糊
  - 为什么是有偏的？
    - $dN/dA != \Delta N/\Delta A$ 我们给一定光子数与对应的面积，所以它们不等于前者，只有给定的面积足够
      1. 打出更多的光子
      2. 在同样的N个临近光子下，$\Delta A$的面积更小
      3. $\Delta A$会更接近$dA$
      - 所以当光子打出无限多的时候，就会得到正确的结果
    - 所以这是个有偏的方法，但是是一致的方法
      - 得到结果如果有一点模糊，那它就是有偏的
      - 如果取的样本足够多，能让它收敛到不模糊的结果，它就是一致的
  - 思考：能不能采用固定的面积，看里面有多少光子来确定密度？
    - 理论上与前面方法结果相同
    - 但这种方法是有偏的，并且不是一致的。因为面积固定，$\Delta A$无法接近$dA$
#### 光子映射与双向路径追踪的结合[VCM]
- 结合了光子映射与双向路径追踪
- 要点：
  - 不浪费$BDPT$子路径，比如两个终点不可以被连接，但是可以被合并
  - 使用光子映射去处理可以被合并的接近的光子
   <img src="./image/vcm.png" alt="vcm" width="400px"></img>
#### 实时辐射度算法[Instant Radiosity(IR)]
- 也被称为多光源方法
- 要点：被照亮的表面也当成是光源
- 方法：
  - 假设每个光线子路径的端点都是一个虚拟点光源（VPL）
  - 渲染场景根据这些点光源
  <img src="./image/vcm.png" alt="vpl" width="400px"></img>
- 优点：在一些复杂场景中速度快，而且效果好
- 缺点：
  - 当VPL接近着色点的时候会尖峰。比如在一些缝隙，因为在之前所说，将立体角采样改成对面积的采样，所以面积*cos/两个点之间距离，如果两个点极近，就会导致数值极大。
  - 不能被用于glossy材质中

