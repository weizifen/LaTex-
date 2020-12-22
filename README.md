# LaTex学习 常用的数学公式命令（数学排版）
## 学习动机
* 打数学公式的利器


## 分式和根式
### 分数
$ \frac{分子}{分母}$


### 根式
已知三条边求面基
海伦公式
$ S = \sqrt{p(p - a)(p - b)(p - c)}$
$ p(半周长) = \frac{a + b + c}{2}$

## 关系符和算符
在 LaTeX 中，除了一些常见的符号可以直接用键盘输入外，比如+ - = ! / () [] <> | ' : *，其他的符号需要用命令输入。
### 关系符
* =，>，<，直接输入
* 不等号≠ $\ne$
* 大于等于号 ≥ $\ge$
* 小于等于号 ≤ $\le$
* 约等号 ≈ $\approx$
* 等价 ≡ $\equiv$
### 算符
* 加减乘除 +、−、∗、/ 可直接输入
* 乘号 × $\times$
* 除号 ÷ $\div$
* 点乘 · $\cdot$
* 加减号 ± $\pm$ / ∓ $\mp$
#### 三角函数：
* $\sin$
* $\cos$
* $\tan$
* $\cot$
* $\angle ABC$
* $$

`举个三角函数的例子  上次我是草稿写的平移旋转 现在用md实现 不过在此之前我们应该学习一下插入方程`
#### 插入方程
复杂公式输入
多行公式(& 是对齐，\\ 是换行。)
$$\begin{align} 
a_{11}x_{1} - a_{12}x_{2} = b_{1}\\
a_{21}x_{1} - a_{22}x_{2} = b_{2}\\
\end{align}$$
##### 旋转
$$\begin{align} 
x = r\sin\theta\\
y = r\cos\theta\\
\end{align}$$

根据三角函数两角和公式
$\cos(a + b) = \cos a \cos b - \sin a \sin b$
$\sin(a + b) = \sin a \cos b + \cos a \sin b$
求得 旋转后的公式为
$$\begin{align} 
x^` = x\cos b - y\sin b\\
y^` = x\sin b + y\cos b\\
\end{align}$$

矩阵 X 基向量
$$
\vec{a}\times\vec{b}=
	\begin{bmatrix}
		a & b & c\\
		d & e & f\\
		g & h & i\\
	\end{bmatrix}
\times
	\begin{bmatrix}
		x\\
		y\\
		z\\
	\end{bmatrix}
 =
	\begin{bmatrix}
		x^、\\
		y^、\\
		z^、\\
	\end{bmatrix}
$$

求得
$$ \begin{align}
ax + by + cz = x^、 \\
dx + ey + fz = y^、 \\
gx + hy + iz = z^、 \\
\end{align}$$
比较矩阵求得x`y`z` 可得矩阵$\vec{A}$绕Z轴旋转中的值
即：(如果想对齐多组公式，可以用 align，公式之间也用 & 分隔。)
$$\begin{align}
a & = \cos{b} & b &= -\sin{b} & c & = 0 \\
d & = \sin{b} & e &= cos{b} & f & = 0 \\
z^{、} & = z & g &= 0 & h & = 0 \\
\end{align}$$

用矩阵表示旋转
$$
\vec{a}\times\vec{b}=
	\begin{bmatrix}
		\cos{b} & -sin{a} & 0\\
		\sin{a} & cos{b} & 0\\
		0 & 0 & 1\\
	\end{bmatrix}
\times
	\begin{bmatrix}
		x\\
		y\\
		z\\
	\end{bmatrix}
 =
	\begin{bmatrix}
		x^、\\
		y^、\\
		z^、\\
	\end{bmatrix}
$$

##### 平移(四阶矩阵)
$$\begin{align} 
x^、 = x + T_x \\
y^、 = y + T_y \\
y^、 = y + T_y \\
\end{align}
$$

$$
\begin{bmatrix} 
a & b & c & d \\
e & f & g & h \\
i & j & k & l \\
m & n & o & p \\
\end{bmatrix}
\times
\begin{bmatrix}
x \\
y \\
z \\
w \\
\end{bmatrix}
=\begin{bmatrix}
x^、 \\
y^、 \\
z^、 \\
w^、 \\
\end{bmatrix}
$$

$$
\begin{align}
ax + by + cz + dw = x^、\\
ex + fy + gz + hw = y^、\\
ix + jy + kz + lw = z^、\\
mx + ny + oz + pw = w^、\\
\end{align}
$$
推理可得
$$
\begin{align}
a &= 1 & b &= 0 & c &= 0 & d &= T_x \\
e &= 0 & f &= 1 & g &= 0 & h &= T_y \\
i &= 0 & j &= 0 & k &= 1 & l &= T_z \\
m &= 0 & n &= 0 & o &= 0 & p &= 1 \\
\end{align}
$$

求得
$$
\begin{bmatrix} 
1 & 0 & 0 & T_x \\
0 & 1 & 0 & T_y \\
0 & 0 & 1 & T_z \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
x \\
y \\
z \\
w \\
\end{bmatrix}
=\begin{bmatrix}
x^、 \\
y^、 \\
z^、 \\
w^、 \\
\end{bmatrix}
$$
##### 旋转(四阶矩阵 绕Z轴旋转)
根据三角函数两角和公式
$\cos(a + b) = \cos a \cos b - \sin a \sin b$
$\sin(a + b) = \sin a \cos b + \cos a \sin b$

推理可得
$$
\begin{align}
a &= \cos\theta & b &= -\sin\theta & c &= 0 & d &= 0 \\
e &= \sin\theta & f &= \cos\theta & g &= 0 & h &= 0 \\
i &= 0 & j &= 0 & k &= 1 & l &= 0 \\
m &= 0 & n &= 0 & o &= 0 & p &= 1 \\
\end{align}
$$
所以求得矩阵为
$$
\begin{bmatrix} 
\cos\theta & -\sin\theta & 0 & 0 \\
\sin\theta & \cos\theta & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
\end{bmatrix}
\times
\begin{bmatrix}
x \\
y \\
z \\
w \\
\end{bmatrix}
=\begin{bmatrix}
x^、 \\
y^、 \\
z^、 \\
w^、 \\
\end{bmatrix}
$$

#### 求极限
$\lim_{x\rightarrow{0}} \frac{\sin x}{x} = 1$
#### 求和
$\sum_{k = 1}^N k^2$
