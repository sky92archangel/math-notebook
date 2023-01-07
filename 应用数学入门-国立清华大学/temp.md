
$$
R = 
\left (\begin{matrix}
a & b   \\
c & d   \\ 
\end {matrix}\right )
$$


 



### 矩阵



$|y\rangle = A | x \rangle \rightarrow \sum\limits_j A_{ij} x_j = y_i $
$$
A_{ij}=\langle \hat e_i | A | \hat e_j \rangle
$$
该公式即为 一个矩阵 对两个基向量分别做投影，仅保留这两个基向量在矩阵内产生的影响值，以确定矩阵该处的元素值；

狄拉克符号  bra & ket

$|a\rangle = \sum\limits_{i=1}^{N}a_i  | \hat e_i \rangle $       ，ket ， 竖向量

$ \langle a| = \sum\limits_{i=1}^{N}  \langle\hat e_i | a_i^* $      ，bra， 横向量

内积 

$\langle x| y \rangle = \sum\limits_ix_i^* y_i \ , \  \langle y|x \rangle = \sum\limits_i y_i^* x_i = \langle x|y \rangle ^*$



### 矩阵规则

$$
(A+B)_{ij} = A_{ij} + B_{ij} \\ 
(\lambda A)_{ij}=\lambda A_{ij} \\
(AB)_{ij} = \sum\limits_k A_{ik}B{kj}
$$

#### 例1 三维空间转动

<img src="temp.assets/image-20230107134154842.png" alt="image-20230107134154842" style="zoom:50%;" />

有向量 $\vec v$

$ R_z(\theta)\vec v = \vec v'$

$v_x' = v_x\cos\theta -v_y\sin\theta$

$v_y' = v_x\sin\theta +v_y\cos\theta$

$v_z' =v_z  $

我们可以将其写为矩阵
$$
\left (\begin{matrix}
v_x' \\ v_y' \\ v_z'  
\end {matrix}\right )
=  
\left (\begin{matrix}
\cos\theta & -\sin\theta & 0   \\
\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right )
\left (\begin{matrix}
 v_x  \\ v_y  \\ v_z   
\end {matrix}\right )
$$
我们开始考察基向量旋转的情况

<img src="temp.assets/image-20230107135258859.png" alt="image-20230107135258859" style="zoom:50%;" />

可见

$\hat i' = \cos\theta\hat i+\sin\theta\hat j$ 

$\left (\begin{matrix}
i_x' \\ i_y' \\ i_z'  
\end {matrix}\right )
=  
\left (\begin{matrix}
\cos\theta &  [] & []   \\
\sin\theta &  [] &  []  \\
0 & []  &  [] \\ 
\end {matrix}\right )
\left (\begin{matrix}
1  \\ 0  \\ 0   
\end {matrix}\right )$

针对其他基向量也是一样的操作，

那么最后就能够将中间的矩阵构建出来





那么沿着三个轴旋转的矩阵就能够得到
$$
R_z(\theta)
=  
\left (\begin{matrix}
\cos\theta & -\sin\theta & 0   \\
\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right ) \\
R_x(\theta)
=  
\left (\begin{matrix}
1  & 0 &  0	\\ 
0 & \cos\theta & -\sin\theta \\
0 & \sin\theta & \cos\theta  \\
\end {matrix}\right )\\
R_y(\theta)
=  
\left (\begin{matrix}
\cos\theta& 0 &  \sin\theta    \\
0 & 1 & 0  		\\ 
-\sin\theta& 0 & \cos\theta     \\
\end {matrix}\right )
$$

>  定义 交换子 commutator
>
> $[A,B]\equiv AB-BA$

我们构造一个交换子式子，该式表达为 【绕x转转动】 【绕y轴转动】  两个动作先后不同导致的结果是否一样？

$[R_x,R_y] =R_x R_y-R_y R_x $ 

直接将旋转90度带入上述旋转式子即可证明，旋转动作的先后会导致结果不同；

所以 

$[R_x,R_y] =R_x R_y-R_y R_x \neq 0 $ 





### 矩阵转置

转置简单表现为将一个矩阵 行列互换

$(A^\top)_{ij} = A_{ji}$

#### 例 

$R_z(\theta)
=  
\left (\begin{matrix}
\cos\theta & -\sin\theta & 0   \\
\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right ) \\
R_z^\top(\theta)
=  
\left (\begin{matrix}
\cos\theta & \sin\theta & 0   \\
-\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right ) \\$

$(R^\top)_{ij} = R_{ji}$

把它们乘起来

$R_z(\theta)R_z^\top(\theta)
=  
\left (\begin{matrix}
\cos\theta & -\sin\theta & 0   \\
\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right )
\left (\begin{matrix}
\cos\theta & \sin\theta & 0   \\
-\sin\theta & \cos\theta  & 0   \\
0 & 0 & 1  		\\ 
\end {matrix}\right ) 
=  
\left (\begin{matrix}
1 & 0 & 0   \\
0 & 1 & 0   \\
0 & 0 & 1   \\ 
\end {matrix}\right ) = \delta_{ij} $



### 正交矩阵

定义为 ，和自己的转置相乘的结果为单位阵

$R_z R_z^\top =\delta_{ij} =\mathbf{1} $



### 赫尔米特共轭 / 厄米共轭

当矩阵运算中带有复数的时候，变换后需进行厄米共轭 ，匕首dagger 符号即为 共轭并转置

$(A^\dagger)_{ij}=A^*_{ji}$  也就是 $ A^\dagger  = (A^*)^\top $

若整个矩阵为实数矩阵 ，那么其厄米共轭的结果和dagger结果一样

$A_{real}^* = A_{real}^\dagger$



例 
$$
(AB)^\dagger =B^\dagger A^\dagger
$$
$[(AB)^\dagger]_{ij} = (AB)^* _{ji} = \sum\limits_kA_{jk}^*B_{ki}^* = \sum\limits_k(A^\dagger)_{kj}(B^\dagger)_{ik}= \sum\limits_k(B^\dagger)_{ik}(A^\dagger)_{kj}=(B^\dagger A^\dagger)_{ij}$

同样的证明方法用在实数矩阵上就证明 $(AB)^\top =B^\top A^\top $





















