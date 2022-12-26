

## 复数 Complex



[TOC]



**Αα、Ββ、Γγ、Δδ、Εε、Ϝϝ、Ζζ、Ηη、Θθ、Ιι、Κκ、Λλ、Μμ、Νν、Ξξ、Οο、Ππ、Ρρ、Σσ、Ττ、Υυ、Φφ、Χχ、Ψψ、Ωω**



## 为何我们需要复数

|                                                              |                                                              |                                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="C:\Users\sky92\AppData\Roaming\Typora\typora-user-images\image-20221226122025484.png" alt="image-20221226122025484" style="zoom:50%;" /> | <img src="C:\Users\sky92\AppData\Roaming\Typora\typora-user-images\image-20221226122035289.png" alt="image-20221226122035289" style="zoom:50%;" /> | <img src="C:\Users\sky92\AppData\Roaming\Typora\typora-user-images\image-20221226122043188.png" alt="image-20221226122043188" style="zoom:50%;" /> |
| $z^2-1=0$                                                    | $z^2=0$                                                      | $z^2+1=0$                                                    |
| $z=1,-1$                                                     | $z=0$                                                        | $无实数解$                                                   |



但是我们可以引入虚数来解决无实数解的情况；即 $i \equiv \sqrt{-1}$  则 $i^2=-1$ ；

因此， $z^2+1=0 \rightarrow z^2 = -1 \rightarrow z = \pm \sqrt{-1} = \pm i $

故在代数层面虚数还有一些扩展：

$i^2 = -1 $

$i^3 = i^2 \cdot i = -i$

$ i^4 = i^2 \cdot i^2 = -1 \cdot -1 = 1$

## 复数和复数平面

我们可以将不同特性的数加在一起，则得到复数

$z = x+iy $   此处 x 为实部 y为虚部，我们可以在坐标轴上来表示出来；

<img src="1-1-Complex.assets/image-20221226123931782.png" alt="image-20221226123931782" style="zoom:50%;" />



复数的代数情况：

$z_1+z_2 = (x_1+iy_1)+(x_2+iy_2) = (x_1+x_2)+i(y_1+y_2) $

$z_1-z_2 = (x_1+iy_1)-(x_2+iy_2) = (x_1-x_2)+i(y_1-y_2) $

$z_1z_2 = (x_1+iy_1)(x_2+iy_2) = (x_1x_2-y_1y_2)+i(x_1y_2+y_1x_2) $

$\frac{z_1}{z_2} = \frac{x_1+iy_1}{x_2+iy_2}=\frac{(x_1+iy_1)(x_2-iy_2)}{(x_2+iy_2)(x_2-iy_2)} = \frac{(x_1x_2+y_1y_2)+i(y_1x_2-x_1y_2)}{x^2_2+y^2_2} = \frac{x_1x_2+y_1y_2}{x^2_2+y^2_2}+i\frac{y_1x_2+x_1y_2}{x^2_2+y^2_2}$



## 共轭复数

指和原复数虚部正负相反的复数  $\bar z = x=iy$

<img src="1-1-Complex.assets/image-20221226124639665.png" alt="image-20221226124639665" style="zoom:50%;" />

$\bar zz = (x-iy)(x+iy) = x^2+y^2$

共轭复数在复平面上表现为根据实数轴对称的两个点；

两个共轭复数相乘得到的是复数平面点对原点距离的平方；



## 极坐标方式表达

<img src="1-1-Complex.assets/image-20221226125200099.png" alt="image-20221226125200099" style="zoom:50%;" />

一般我们使用复平面上的点到原点距离以及到原点连线对实数正轴的夹角来表达复数；

modulus 模  $   |z|   = \sqrt{x^2+y^2} = \sqrt{\bar z z}$

argument 角度  arg z  ,角度的算法有点复杂 

一般来讲 $ \tan\theta = \frac{y}{x} \rightarrow arg z =\theta =\tan^{-1} \frac{y}{x} $   但是这样有纰漏，比如下例

有 $ z_1 = x_1+iy_1 =1+i$ 

则 $ \tan\theta_1 = \frac{y_1}{x_1} = 1 $ 由于 实部虚部都是正数 那么点在第一象限

另 $ z_2 = x_2+iy_2 =-1-i$ 

则 $ \tan\theta_2 = \frac{y_2}{x_2} = 1 $ 由于 实部虚部都是负数 那么点在第三象限

那么出现了180度的区别；



## 复数平面三角关系

${x,y} \leftarrow \rightarrow (|z|,\theta)$

<img src="1-1-Complex.assets/image-20221226130611818.png" alt="image-20221226130611818" style="zoom: 50%;" />
$$
x = |z|cos\theta \\
y = |z|sin\theta
$$
因此可以将原有复数表达写为如下

$ z =x+iy = |z|\cos\theta + i |z|\sin\theta = |z|(\cos\theta+ i \sin \theta)  $

此时我们得到 一个modulus |z|  还有只和角度相phase有关的复数；



## 欧拉等式

$e^{i\theta} = cos\theta + i sin \theta$

证明：

对$e^z$ 泰勒展开 得到  $ e^z = 1 + z + \frac{z^2}{2!}+...+\frac{z^n}{n!}+... $

若 $ z = i\theta  $  其中  $\theta$为实数 带入上式

$e^{i\theta} \\ = 1 + i\theta + \frac{(i\theta)^2}{2!} + \frac{(i\theta)^3}{3!} +  \frac{(i\theta)^4}{4!} +...+ \frac{(i\theta)^n}{n!}+... \\ = 1 + i\theta - \frac{(\theta)^2}{2!} - i\frac{(\theta)^3}{3!} + \frac{(\theta)^4}{4!} +...+ \frac{(i\theta)^n}{n!}+...  \\=  \\ 1-\frac{\theta^2}{2!} +\frac{\theta^4}{4!}-\frac{\theta^6}{6!}+\frac{\theta^8}{8!}-... \\ + i(\theta-\frac{\theta^3}{3!}+\frac{\theta^5}{5!}-\frac{\theta^7}{7!}+\frac{\theta^9}{9!}-...) $

由于我们直到sin和cos函数的泰勒展开

$ \cos\theta = 1-\frac{\theta^2}{2!} +\frac{\theta^4}{4!}-\frac{\theta^6}{6!}+\frac{\theta^8}{8!}-...$

$\sin\theta=\theta-\frac{\theta^3}{3!}+\frac{\theta^5}{5!}-\frac{\theta^7}{7!}+\frac{\theta^9}{9!}-...$

则上式可并为 
$$
e^{i\theta} = \cos\theta + i \sin\theta
$$


由此得到欧拉等式；这是个非常优美的等式，可以再次用于复数的表达

<img src="1-1-Complex.assets/image-20221226132946174.png" alt="image-20221226132946174" style="zoom:50%;" />
$$
z = x+iy = re^{i\theta}
$$


## de Moivreó theorem

利用这个关系 $(e^{i\theta})^n=e^{in\theta}$

$(\cos\theta + i\sin\theta)^n = \cos\ n\theta + i\ \sin n\theta$

该特性早期需要使用复杂几何证明方法进行，而在复数域则简化了证明；

### 例题1

证 $\cos3\theta = 4\cos^3\theta -3\cos\theta$

$ (\cos\theta +i\sin\theta)^3 = \cos3\theta + i\sin3\theta$

$(\cos\theta +i\sin\theta)^3 = (\cos^3\theta - 3\cos\theta \sin^2\theta) + i (3\cos^2\theta \sin\theta -\sin^3\theta)$

实部虚部分别相等 得到

$(\cos^3\theta - 3\cos\theta \sin^2\theta) + i (3\cos^2\theta \sin\theta -\sin^3\theta)= \cos3\theta + i\sin3\theta $

 $  cos3\theta = cos^3\theta - 3cos\theta sin^2\theta =cos^3\theta - 3cos\theta (1-cos^2\theta) = 4cos^3\theta -3cos\theta $ 

### 例题2

证$\cos^3\theta = \frac{1}{4}\cos3\theta +\frac{3}{4}\cos\theta $

设$z=e^{i\theta }$

$\cos\theta  = \frac{1}{2}(e^{i\theta }+e^{-i\theta }) = \frac{1}{2}(z+\frac{1}{z}) $

$\sin\theta  = \frac{1}{2i}(e^{i\theta }-e^{-i\theta }) = \frac{1}{2i}(z-\frac{1}{z}) $

$\cos^3\theta   = \frac{1}{2^3}(z+\frac{1}{z})^3 = \frac{1}{8}(z^3+\frac{1}{z^3})+\frac{3}{8}(z+\frac{1}{z}) = \frac{1}{4}cos3\theta+\frac{3}{4}cos\theta$

### 例题3

$z^3 = 1$

$z=re^{i\theta}$ 

$r^3e^{i3\theta}= 1 = e^{i2n\pi}$

可见 r=1 

$e^{i\theta}=e^{i\frac{2n\pi}{3}} = 1 , e ^{i\frac{2\pi}{3}} , e^{i\frac{4\pi}{3}} ,...$那么可在单位上可见三个解

<img src="1-1-Complex.assets/image-20221226141740936.png" alt="image-20221226141740936" style="zoom:80%;" />

若我们把所有不重复的解相加则得到  0 

$z_1+z_2+z_3 = 1 + \cos\frac{2\pi}{3} +i\sin\frac{2\pi}{3}+ \cos\frac{4\pi}{3} +i\sin\frac{4\pi}{3} = (1-\frac{1}{2}+\frac{1}{2})+i(\frac{\sqrt{3}}{2}-\frac{\sqrt{3}}{2}) =0$



## 物理应用

 <img src="1-1-Complex.assets/image-20221226142627889.png" alt="image-20221226142627889" style="zoom:50%;" />

上述内容一般需要常微分方程式来解，这里我们可以使用复数域来解 I(t) 电流；

根据电学内容 电容阻抗和频率有关 则 这里的容抗为 $i\frac{1}{\omega C}$

那么 整个电路的阻抗为 $Z= Z_R+Z_C = R +i \frac{1}{\omega C}$

$V =IZ  \rightarrow I(t)   $

$V(t) = Ve^{i\omega t}= V\cos\omega t + iV\sin\omega t$

RC阻抗为  $Z = |Z|e^{i\phi }$  

$I(t) = \frac{V(t)}{Z} = \frac{Ve^{i\omega t}}{|Z|e^{i\phi}} = \frac{V}{|Z|}e^{i(\omega - \phi)} = \frac{V}{|Z|}[\cos(\omega t -\phi)+i\sin(\omega t-\phi)] = \frac{V}{|Z|} \cos(\omega t -\phi)+ i \frac{V}{|Z|}  \sin(\omega t-\phi) $

可见 电流的频率和电压源频率有一个相位角差；

现在只需要实部虚部分别计算即可得到结果；

$|Z| = \sqrt{R^2 + (\frac{1}{\omega C})^2}$

$tan\phi =  \frac{虚部}{实部} = - \frac{1}{\omega RC}$ 注意由于物理量基本为正 故整个Z在复平面的第四象限内变化 故这里有个负号

那么问题在于 当频率不断升高  即 $\omega \rightarrow \infin$  那么 阻抗 $Z_C = \frac{1}{i\omega C } \rightarrow 0$

那么验证了高频电路中电容近似导线；



## 结

复数是否像二维向量

那么是否也有内积和外积特性

我们有

$z=x+iy ,\bar z=x-iy    $

$z_1+z_2 = (x_1+x_2)+i(y_1+y_2)$

$ \bar z_1 z_2 =(x_1-iy_1)(x_2+iy_2) = (x_1x_2+y_1y_2)+i(x_1y_2-y_1x_2)$

可见 这里的  实部为内积$ z_1 \cdot z_2 $  虚部为外积$ z_1 \times z_2 $

那么我们获得了几何意义  

$ \overrightarrow r_1 = (x_1,y_1) , \overrightarrow r_2 = (x_2,y_2) $

inner product  内积  $\overrightarrow r_1 \cdot \overrightarrow r_2 = x_1x_2+y_1y_2$

outer product 外积   $\overrightarrow r_1 \times \overrightarrow r_2 =(x_1y_2-y_1x_2 ) \hat k$
$$
\left | \begin{matrix}
\hat i & \hat j   & \hat k \\
x_1 &y_1 & 0 \\
x_2 &y_2 & 0\\
\end{matrix} \right |
$$

$$
Re(\bar z_1 z_2) =\overrightarrow z_1 \cdot \overrightarrow z_2 \\
Im(\bar z_1 z_2) = (\overrightarrow z_1 \times \overrightarrow z_2)_z
$$



## 复变函数

一个简单的例子 polynomial

$z = x+ iy \rightarrow f(z)=u+iv$

这在数学上是个简单的映射 即从 $(x,y) $映射到$ (u,v)$ , 一个空间向量 映射到 另一个空间的向量

$f(z) = (x+iy)^2 = (x^2 -y^2)+i(2xy)$

$u(x,y) = x^2 - y^2 \\ v(x,y) = 2xy$

<img src="1-1-Complex.assets/image-20221226161233468.png" alt="image-20221226161233468" style="zoom:50%;" />

曲线在交点处垂直，且在整个平面内 处处保持垂直；

harmonic function 调和函数，也就是 满足 拉普拉斯方程的 函数 ；  

拉普拉斯方程 规则为： 函数对x偏微分两次 和 函数对y偏微分两次的结果相同；

$\frac{\part^2u}{\part x^2}-\frac{\part^2u}{\part y^2} = 2-2=0 \rightarrow \nabla^2u=0 $ 



## 与三角函数和双曲函数关系

定义
$$
e^{iz} = \cos z + i \sin z \\

\cos z  = \frac{1}{2}(e^{iz }+e^{-iz })   \\

\sin z  = \frac{1}{2i}(e^{iz }-e^{-iz })
$$
定义双曲函数 hyperbolic function
$$
cosh z  = \frac{1}{2}(e^{z} +e^{-z })   \\

sinh z  = \frac{1}{2i}(e^{z }-e^{-z })
$$
当 z = x

|                                                              |                                                              | 开关函数                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="1-1-Complex.assets/image-20221226163037159.png" alt="image-20221226163037159" style="zoom:50%;" /> | <img src="1-1-Complex.assets/image-20221226163525729.png" alt="image-20221226163525729" style="zoom:50%;" /> | <img src="1-1-Complex.assets/image-20221226163920906.png" alt="image-20221226163920906" style="zoom:50%;" /> |
| $\cosh x  = \frac{1}{2}e^{x} + \frac{1}{2}e^{-x }  $ 为偶函数 | $\sinh z  = \frac{1}{2i}e^{z }-\frac{1}{2i}e^{-z }$ 为奇函数 | $\tanh x=\frac{\sinh x}{\cosh x}=\frac{e^x-e^{-x}}{e^x+e^{-x}}$ 为奇函数 |
| $ sech x = (\cosh x)^{-1}$  为偶函数                         | $ csch x = (\sinh x)^{-1}$  为奇函数                         | $\coth x =(\tanh x)^{-1}$为奇函数                            |

从实部到虚部变化

$z=iy \rightarrow \cos z=\cos(iy) = \frac{1}{2}(e^{i(iy)}+e^{i(iy)}) = \frac{1}{2}(e^{-y}+e^y) =\cosh y$

同样的 $\sin(iy) = \frac{1}{2i}(e^{-y}-e^y) = i\frac{1}{2}(e^y-e^{-y})=i\sin hy$

故
$$
\cos(iy)  =\cosh\  y \\
\sin(iy)  =i\cdot \sinh\ y
$$
三角函数在虚轴上的值基本就是双曲函数在实轴上的值



## 应用于微分和积分

### 例1

$f(x)=e^{3x}\cos4x$ 可以当作某个函数的实数部分

$f'(x) =(e^{3x}\cos4x)'=3e^{3x}\cos4x-4e^{3x}\sin4x = e^{3x}(3\cos4x-4\sin4x) $

$g(x) = e^{3x}(\cos4x+i\sin4x) = e^{3x}e^{i4x} = e^{(3+4i)x}$

$\frac{dg}{dx} =g'(x)= (3+4i)e^{(3+4i)x}$ 将原有的g函数带入

$e^{3x} (3+4i) (\cos4x+i\sin4x) =e^{3x}(3\cos4x-4\sin4x)+ie^{3x}(4\cos4x+3\sin4x) $

可见

$Re[g'(x)]=e^{3x}(3 \cos4x-4\sin 4x)=f'(x)$

故有时候求一个函数的微分可以先求其作为实部的复数的微分然后结果取实部即可

### 例2

$I = \int e^{ax}\cos bx\ dx$

设函数 

$g(x) = e^{ax}(cosbx+isinbx)=e^{ax}e^{ibx}=e^{(a+ib)x}$

$w=\int g(x)dx=\frac{1}{a+bi}e^{(a+bi)x} + const = \frac{e^{ax}}{a^2+b^2}(a\cos bx+b\sin bx)+ i \frac{e^{ax}}{a^2+b^2}(a\sin bx-b\cos bx)+const$

$I=Re(w)=\frac{e^{ax}}{a^2+b^2}(a\cos bx+b\sin bx)+const$



## 复变对数函数

自然对数情况下 我们遇到了一些问题

$z = re^{i\theta} = re^{i(\theta+2n\pi)} \rightarrow \ln z= \ln[re^{i(\theta+2n\pi)}] = \ln r + i(\theta+2n\pi)$

我们根据计算方法获得了自然对数的多个解，但是这违背了函数唯一映射结果的定义 ；

此时复数域的自然对数函数成为多值函数；

我们有

$\ln 1  = ln(e^{i2n\pi} )= i2n\pi = 0,\pm 2\pi i,\pm 4\pi i,...$

$\ln i  = ln[e^{i(\frac{\pi}{2}+2n\pi)} ]= i(\frac{\pi}{2}+2n\pi)=...,-\frac{3}{2}\pi i, \frac{1}{2}\pi i, \frac{5}{2}\pi i,...$

那么
$$
\ln \theta = \ln r + i \theta , -\pi < \theta \leq\pi
$$
<img src="1-1-Complex.assets/image-20221226174009838.png" alt="image-20221226174009838" style="zoom:50%;" />

当我们对相角规定范围的时候，在负实轴处则破坏了连续性 如同螺丝转一圈无法回到原有平面而是回到投影后的相同位置；

我们可以在负实轴上下取点进行考察：

$\ln(-1+i\epsilon ) =\ln[1e^{i(\pi-\delta)}]= i(\pi-\delta) = i\pi$

$\ln(-1-+i\epsilon ) =\ln[1e^{-i(\pi-\delta)}]= -i(\pi-\delta) = -i\pi$

那么两者差不为0 ，此处出现了跳变 ；



## 复数域指数函数

如下

$2^i = e^{\ln 2^i}=e^{i(\ln 2 + i2n\pi)} = e^{i\ln2}\cdot e^{-2n\pi} = [\cos(\ln2)+i\sin(\ln2)]e^{-2n\pi} $

可见复数域指数函数依旧是多值函数；

$i^2 = e^{\ln(i^2)} = e^{2\ln i} = e^{2\ln(1e^{i(\frac{\pi}{2}+2n\pi)})} = e^{(4n+1)\pi i} = -1$

显然多值函数所有结果都相等，可见多值函数变为单值函数； 故我们一开始对虚部的定义是属于特殊情况；

















































