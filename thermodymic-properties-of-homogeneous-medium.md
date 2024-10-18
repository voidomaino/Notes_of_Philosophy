# 数学基础

&emsp;&emsp;下面的结论来自多变量微积分的知识。

## 全微分

当 $f$是独立变量 $(x, y)$ 的函数，即$f = f(x,y)$，$f$的全微分：
$$
\mathrm{d}f(x,y) = 
\left(\frac{\partial f}{\partial x} \right)_x \mathrm{d}x + 
\left(\frac{\partial f}{\partial y} \right)_y \mathrm{d}y
$$

## 平滑函数的二阶导数

$f$足够连续，偏微分次序可交换：
$$
\frac{\partial^2 f}{\partial x \partial y} =
\frac{\partial^2 f}{\partial y \partial x} 
$$

## 勒让德变换

可以变换微分项的独立变量：
$$
\mathrm{d}(xy) = 
x \mathrm{d}y + y \mathrm{d}x \\
\Rightarrow 
x \mathrm{d}y = 
\mathrm{d}(xy) - y \mathrm{d}x
$$

## 倒数关系

对$f = f(x,y)$，有：
$$
\left(\frac{\partial f}{\partial x} \right)_y \left(\frac{\partial x}{\partial f} \right)_y = 1
$$

## 循环关系

当$x,y,z$存在某种函数关系$f(x,y,z) = 0$，有：
$$
\left(\frac{\partial x}{\partial y} \right)_z 
\left(\frac{\partial y}{\partial z} \right)_x 
\left(\frac{\partial z}{\partial x} \right)_y 
= -1
$$

## 链式关系

四个变量$u,v,x,y$中有两个独立变量，有链式求导法则：
$$
\left(\frac{\partial u}{\partial x} \right)_y =
\left(\frac{\partial u}{\partial v} \right)_y
\left(\frac{\partial v}{\partial x} \right)_y\\
\Rightarrow
\left(\frac{\partial x}{\partial u} \right)_y
\left(\frac{\partial u}{\partial v} \right)_y
\left(\frac{\partial v}{\partial x} \right)_y
= 1
$$

$$
\left(\frac{\partial u}{\partial x} \right)_y =
\left(\frac{\partial u}{\partial x} \right)_v +
\left(\frac{\partial u}{\partial v} \right)_x
\left(\frac{\partial v}{\partial x} \right)_y\\
\Rightarrow
\left(\frac{\partial u}{\partial x} \right)_y -
\left(\frac{\partial u}{\partial x} \right)_v =
\left(\frac{\partial u}{\partial v} \right)_x
\left(\frac{\partial v}{\partial x} \right)_y
$$

# 热力学基础

## 四种状态函数的全微分

### 内能

$$
\mathrm{d} U = T \mathrm{d} S - p \mathrm{d} V
$$

### 焓

$$
H = U + p V\\
\mathrm{d}H = \mathrm{d} U + p \mathrm{d} V + V \mathrm{d} p\\
\mathrm{d}H = T \mathrm{d} S - p \mathrm{d} V + p \mathrm{d} V + V \mathrm{d} p\\
\mathrm{d}H = T \mathrm{d} S + V \mathrm{d} p
$$

### 自由能

$$
F = U - T S\\
\mathrm{d} F = \mathrm{d} U - T \mathrm{d} S - S \mathrm{d} T\\
\mathrm{d} F = T \mathrm{d} S - p \mathrm{d} V - T \mathrm{d} S - S \mathrm{d} T\\
\mathrm{d}F = - p \mathrm{d} V - S \mathrm{d} T
$$

### 吉布斯函数

$$
G = F + p V \\
\mathrm{d} G = \mathrm{d} F + p \mathrm{d} V + V \mathrm{d} p\\
\mathrm{d} G = - p \mathrm{d} V - S \mathrm{d} T + p \mathrm{d} V + V \mathrm{d} p\\
\mathrm{d} G = - S \mathrm{d} T + V \mathrm{d} p
$$

### 总结

$$
\begin{array}{ll}
\mathrm{d} U &= T \mathrm{d} S - p \mathrm{d} V\\
\mathrm{d} H &= T \mathrm{d} S + V \mathrm{d} p\\
\mathrm{d} F &\leqslant -S \mathrm{d} T  - p \mathrm{d} V\\
\mathrm{d} G &\leqslant - S \mathrm{d} T + V \mathrm{d} p
\end{array}
$$

热力学函数$(U, H, F, G)$是状态量$(T, S, p, V)$的函数。

* 状态方程使$(T, p, V)$中减掉一个独立变量。

* $S$也是状态函数，是$(T, p, V)$的函数。

**因此，$(T, S, p, V)$中仅有两个独立变量。**

# 麦氏关系

麦克斯韦关系的思想就是通过测量可测的状态参量$(T, p , V)$和某些表征物质性质的参量$(\alpha, \beta, \kappa_T, C_V, C_p)$来求得不可测的状态函数$(U, H, F, G, S)$。
$$
\begin{array}{ll}
\mathrm{d} U = T \mathrm{d} S - p \mathrm{d} V &\Rightarrow 
\left(\frac{\partial U}{\partial S} \right)_V = T \qquad 
\left(\frac{\partial U}{\partial V} \right)_S = -p \\
\mathrm{d} H = T \mathrm{d} S + V \mathrm{d} p &\Rightarrow 
\left(\frac{\partial H}{\partial S} \right)_p = T  \qquad
\left(\frac{\partial H}{\partial p} \right)_S = V \\
\mathrm{d} F = - S \mathrm{d} T - p \mathrm{d} V  &\Rightarrow 
\left(\frac{\partial F}{\partial T} \right)_V = -S \qquad
\left(\frac{\partial F}{\partial V} \right)_T = -p \\
\mathrm{d} G = - S \mathrm{d} T + V \mathrm{d} p &\Rightarrow 
\left(\frac{\partial G}{\partial T} \right)_p = -S \qquad
\left(\frac{\partial G}{\partial p} \right)_T = V \\
\end{array}
$$

$$
\begin{array}{lll}
p &= - \left(\frac{\partial U}{\partial V} \right)_S &= - \left(\frac{\partial F}{\partial V} \right)_T\\
V &= \left(\frac{\partial H}{\partial p} \right)_S &= \left(\frac{\partial G}{\partial p} \right)_T\\
T &= \left(\frac{\partial U}{\partial S} \right)_V &= \left(\frac{\partial H}{\partial S} \right)_p\\
S &= - \left(\frac{\partial F}{\partial T} \right)_V &= - \left(\frac{\partial G}{\partial T} \right)_p
\end{array}
$$

根据[平滑函数的二阶导数](#平滑函数的二阶导数)可以进一步分析：
$$
\frac{\partial^2 U}{\partial S \partial V} = 
\left(\frac{\partial T}{\partial V} \right)_S = 
\left(\frac{\partial (- p)}{\partial S} \right)_V\\
\frac{\partial^2 H}{\partial S \partial p} = 
\left(\frac{\partial T}{\partial p} \right)_S = 
\left(\frac{\partial V}{\partial S} \right)_p\\
\frac{\partial^2 F}{\partial T \partial V} = 
\left(\frac{\partial (- S)}{\partial V} \right)_T = 
\left(\frac{\partial (- p)}{\partial T} \right)_V\\
\frac{\partial^2 G}{\partial T \partial p} = 
\left(\frac{\partial (- S)}{\partial p} \right)_T = 
\left(\frac{\partial V}{\partial T} \right)_p
$$
整理一下：
$$
\begin{array}{rr}
\left(\frac{\partial T}{\partial V} \right)_S = 
- \left(\frac{\partial p}{\partial S} \right)_V\\
\left(\frac{\partial T}{\partial p} \right)_S = 
\left(\frac{\partial V}{\partial S} \right)_p\\
\left(\frac{\partial S}{\partial V} \right)_T = 
\left(\frac{\partial p}{\partial T} \right)_V\\
- \left(\frac{\partial S}{\partial p} \right)_T = 
\left(\frac{\partial V}{\partial T} \right)_p
\end{array}
$$


## 总结

$$
\left(\frac{\partial A}{\partial B} \right)_C = D
$$

* $A$为$(U, H, F, G)$

* $(B, C)$为$(T, S, p, V)$

* $(B, C)$非共轭

* $(B, C)$为$A$的基本热力学微分方程的独立变量

* $(B, D)$共轭

$$
\left(\frac{\partial A}{\partial B} \right)_C = \left(\frac{\partial D}{\partial C} \right)_B
$$

* $(A, B, C, D)$为$(T, S, p, V)$

* $(A, B)$非共轭

* $(A, C)$共轭

* $(B, D)$共轭

# 基本热力学函数

物态方程、内能、熵。

# 特性函数

对给定的两个独立变量，只要知道一个热力学函数，就能通过求偏导得到其他所有的热力学函数。

## 以 $(T, V)$为独立变量的特性函数$F(T, V)$：

证明：由$F(T, V)$可以得到其它热力学函数

$F$的基本微分方程 
$$
\mathrm{d}F = −S \mathrm{d} T − p \mathrm{d} V
$$
系统的熵
$$
S = - \left(\frac{\partial F}{\partial T} \right)_V
$$
系统的压强
$$
p = - \left(\frac{\partial F}{\partial V} \right)_T
$$
系统的内能
$$
U = F + T S
$$
系统的焓
$$
H = U + p V
$$
系统的吉布斯函数
$$
G = F + p V
$$

## 以$(T, p)$为独立变量的特性函数$G(T, p)$：

证明：由$G(T, p)$可以得到其它热力学函数

$G$的基本微分方程
$$
\mathrm{d} G = - S \mathrm{d} T + V \mathrm{d} p
$$
系统的熵
$$
S = - \left(\frac{\partial G}{\partial T} \right)_p
$$
系统的体积
$$
V = \left(\frac{\partial G}{\partial p} \right)_T
$$
系统的自由能
$$
F = G - p V
$$
系统的焓
$$
H = G + T S
$$
系统的内能
$$
U = H - p V
$$
## 
