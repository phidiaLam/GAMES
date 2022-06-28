# GAMES101
[TOC]


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

### 组合移动(二维)
- 移动的表示
    <img src="./image/transform.png" alt="组合移动" width="300px"></img>
- 计算的顺序
    - $R_{45}\cdot T_{(1,0)} \neq T_{(1,0)}\cdot R_{45}$
    - 示例： $T_{(1,0)}\cdot R_{45} \begin{bmatrix} x\\ y\\ 1\\ \end{bmatrix}=\begin{bmatrix} 1&0&1\\ 0&1&0\\ 0&0&1\\ \end{bmatrix}\begin{bmatrix} cos45^{\circ}&-sin45^{\circ}&0\\ sin45^{\circ}&cos45^{\circ}&0\\ 0&0&1\\ \end{bmatrix}$ 

### 复杂的组合移动（三维）
- 齐次坐标定义
    对于2D的点：$(x, y, z, 1)^T$
    对于2D的向量：$(x, y, z, 0)^T$
    $(x, y, z, w)(w\neq0)$表示的点就是$(x/w, y/w, z/w)$
- 3D仿射变换
    $\begin{pmatrix} x'\\ y'\\ z'\\ 1\\ \end{pmatrix} = \begin{pmatrix} a&b&c&t_x\\ d&e&f&t_y\\ g&h&i&t_z\\ 0&0&0&1\\ \end{pmatrix}\cdot\begin{pmatrix} x\\ y\\ z\\ 1\\ \end{pmatrix}$
    - 缩放
        $S(s_x,s_y,s_z)=\begin{pmatrix} s_x&0&0&0\\ 0&s_y&0&0\\ 0&0&s_z&0\\ 0&0&0&1\\ \end{pmatrix}$
    - 平移
        $T(t_x,t_y,t_z)=\begin{pmatrix} 1&0&0&t_x\\ 0&1&0&t_y\\ 0&0&1&t_z\\ 0&0&0&1\\ \end{pmatrix}$
    - 旋转（这个复杂点）
        $R_x(\alpha)=\begin{pmatrix} 1&0&0&0\\ 0&cos\alpha&-sin\alpha&0\\ 0&sin\alpha&cos\alpha&0\\ 0&0&0&1\\ \end{pmatrix}$
        $R_y(\alpha)=\begin{pmatrix} cos\alpha&0&sin\alpha&0\\ 0&1&0&0\\ -sin\alpha&0&cos\alpha&0\\ 0&0&0&1\\ \end{pmatrix}$
        $R_x(\alpha)=\begin{pmatrix} cos\alpha&-sin\alpha&0&0\\ sin\alpha&cos\alpha&0&0\\ 0&0&1&0\\ 0&0&0&1\\ \end{pmatrix}$
        为什么y会与众不同？因为有顺序存在，$\vec{x}\times\vec{z}=-\vec{y}$
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
    - 相机放于原点，向上方向为Y， 看的方向为-Z
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
    **注意：这边采用右手系，为$-Z$。部分API如OpenGL采用左手系（$f>n$）**

#### 透视投影
- 前提
    - $(x,y,z,1),(kx,ky,kz,k\neq0)$,$(xz,yz,z^2,z\neq0)$都是表示同一个在3D中的点$(x,y,z)$
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
    $M_{persp\rightarrow ortho}=\begin{pmatrix} n&0&0&0\\ 0&n&0&0\\ ?&?&?&?\\ 0&0&1&0\\ \end{pmatrix}$  &nbsp;&nbsp;&nbsp;&nbsp; 忘记了？代入乘一下就知道了，那么现在问题就是要把那几个问号填上值。
    我们就利用两点。
        1. 任何在较近的面的点是不会改变的
        2. 任何在z轴的点是不会改变的
    - 近的平面：$\begin{pmatrix} x\\ y\\ n\\ 1\\ \end{pmatrix}\Rightarrow\begin{pmatrix} x\\ y\\ n\\ 1\\ \end{pmatrix}==\begin{pmatrix} nx\\ ny\\ n^2\\ n\\ \end{pmatrix}$
    第三行值能是$\begin{pmatrix}0&0&A&B\\ \end{pmatrix}\begin{pmatrix}x\\y\\n\\1\\ \end{pmatrix}=n^2\rightarrow An+B=n^2$
    因为不存在x与y的值，**但！**这个第三行还没有完全算出来。（第一个性质）
    第二个性质，在远平面上，z轴上的点也满足这个性质
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
    完成MVP后，所有图像将会在一个正则立方体$[-1,1]^3$中
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
    - 去掉z轴
    - 变换xy平面：$[-1,1]^2$到$[0,width]\times[0,height]$
    - 视图变换矩阵：
    $M_{viewport}=\begin{pmatrix} \frac{width}{2}&0&0&\frac{width}{2}\\ 0&\frac{height}{2}&0&\frac{height}{2}\\ 0&0&0&0\\ 0&0&0&1\\ \end{pmatrix}$

### 三角形
- 为什么选择三角形？
    - 最基础的多边形
    - 任何多边形能拆成三角形
    - 三个点给定的三角形一定是平面的
    - 三角形的内外定义明确
    - 三角形三个点给不同属性，可以为三角形内部所有点插值

