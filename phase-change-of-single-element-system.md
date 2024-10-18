# 单元系的相变

相（phase）指物质存在的某种状态。如：

+ 单种物质的固态、液态、气态；
+ 单种固态物质的不同晶格结构（石墨和金刚石）；
+ 磁性材料中的铁磁态、反铁磁态、顺磁态等；
+ 超导态和正常态。

相变是指物质在不同相之间的转变。

## 复相热平衡判据

| 不变量 | 判据                             | 基本微分方程                                                 |
| ------ | -------------------------------- | ------------------------------------------------------------ |
| $U,V$  | $\delta S = 0 \\ \delta^2 S < 0$ | $\mathrm{d}S \geqslant \frac{\mathrm{d} U}{T} + \frac{p}{T} \mathrm{d} V$ |
| $T,V$  | $\delta F = 0 \\ \delta^2 F > 0$ | $\mathrm{d} F \leqslant - S \mathrm{d} T - p \mathrm{d} V$   |
| $T,P$  | $\delta G = 0 \\ \delta^2 G > 0$ | $\mathrm{d} G \leqslant - S \mathrm{d} T + V \mathrm{d} p$   |
| $S,V$  | $\delta U = 0 \\ \delta^2 U > 0$ | $\mathrm{d} U \leqslant T \mathrm{d} S - p \mathrm{d} V$     |
| $S,p$  | $\delta H = 0 \\ \delta^2 H > 0$ | $\mathrm{d} H \leqslant T \mathrm{d} S + V \mathrm{d} p$     |



## 开系的热力学方程

$$
U = nu\\
\mathrm{d}u = T \mathrm{d}s − p\mathrm{d}v\\
\begin{array}{ll}
\mathrm{d}U &= \mathrm{d}(nu) = n\mathrm{d}u + u\mathrm{d}n = n(T \mathrm{d}s − p\mathrm{d}v) + u\mathrm{d}n\\
&= T [\mathrm{d}(ns) − s\mathrm{d}n] − p [\mathrm{d}(nv) − v\mathrm{d}n] + udn\\
&= T \mathrm{d}S − p\mathrm{d}V + (u − T s + pv)\mathrm{d}n\\
* &= T \mathrm{d}S − p\mathrm{d}V + \mu \mathrm{d}n 
\end{array}
$$

$$
\mu = u − T s + pv = \frac{G}{n}
$$

其他的热力学基本方程可以推导出来：
$$
\begin{array}{ll}
\mathrm{d} U &= T \mathrm{d} S − p \mathrm{d} V + \mu \mathrm{d} n \\
\mathrm{d} H &= T \mathrm{d} S + V \mathrm{d} p + \mu \mathrm{d} n \\
\mathrm{d} F &= − S \mathrm{d} T − p \mathrm{d} V + \mu \mathrm{d} n \\
\mathrm{d} G &= − S \mathrm{d} T + V \mathrm{d} p + \mu \mathrm{d} n
\end{array}
$$
如选择$G$的微分方程做勒让德变换：
$$
\mathrm{d} G = − S \mathrm{d} T + V \mathrm{d} p + \mu \mathrm{d} n\\
\Rightarrow \mathrm{d} (G − \mu n) = −S \mathrm{d} T + V \mathrm{d} p − n \mathrm{d} \mu\\
G = \mu n\\
\Rightarrow − S \mathrm{d} T + V \mathrm{d} p − n \mathrm{d} \mu = 0
$$
三个强度量 $T,p,\mu$ 中只有两个是独立的。

一个热力学系统无法全部由强度量确定，需要至少有一个广延量。

## 单元复相系的平衡条件

<div>
    <center>
    <img src = "单元复相系的平衡条件.jpg"
         alt = "图片丢失"/>
        <br>
        单元复相系
    </center>
</div>

$$
U_\alpha + U_\beta = U_0\\
V_\alpha + V_\beta = V_0\\
n_\alpha + n_\beta = n_0
$$

设想发生一个虚变动：
$$
\delta U_\alpha + \delta U_\beta = 0\\
\delta V_\alpha + \delta V_\beta = 0\\
\delta n_\alpha + \delta n_\beta = 0
$$

$$
\mathrm{d} U = T \mathrm{d} S − p \mathrm{d} V + \mu \mathrm{d} n\\
\delta S_\alpha = \frac{\delta U_\alpha + p_\alpha \delta V_\alpha − \mu_\alpha \delta n_\alpha}{T_\alpha}\\
\delta S_\beta = \frac{\delta U_\beta + p_\beta \delta V_\beta − \mu_\beta \delta n_\beta}{T_\beta}\\
\begin{array}{ll}
\delta S &= \delta S_\alpha + \delta S_\beta \\ 
&= \delta U_\alpha \left(\frac{1}{T_\alpha} - \frac{1}{T_\beta} \right)
+ \delta V_\alpha \left(\frac{p_\alpha}{T_\alpha} - \frac{p_\beta}{T_\beta} \right)
- \delta n_\alpha \left(\frac{\mu_\alpha}{T_\alpha} - \frac{\mu_\beta}{T_\beta} \right)\\
&=0
\end{array}
$$

由于虚变动的任意性，必有：
$$
T_\alpha = T_\beta\\
p_\alpha = p_\beta\\
\mu_\alpha = \mu_\beta
$$
现在考虑平衡的稳定性：

考虑一个由两个子系组成的系统，有：
$$
\begin{array}{ll}
\delta U = 
&T_\alpha \delta S_\alpha − p_\alpha \delta V_\alpha + \mu_\alpha \delta n_\alpha \\ 
&+T_\beta \delta S_\beta − p_\beta \delta V_\beta + \mu_\beta \delta n_\beta \\
\end{array}
$$

$$
\begin{array}{ll}
\delta^2 U = 
& T_\alpha \delta^2 S_\alpha − p_\alpha \delta^2 V_\alpha + \mu_\alpha \delta^2 n_\alpha \\
& +\delta T_\alpha \delta S_\alpha − \delta p_\alpha \delta V_\alpha + \delta \mu_\alpha \delta n_\alpha \\
& + T_\beta \delta^2 S_\beta − p_\beta \delta^2 V_\beta + \mu_\beta \delta^2 n_\beta \\
& +\delta T_\beta \delta S_\beta − \delta p_\beta \delta V_\beta + \delta \mu_\beta \delta n_\beta \\
\end{array}
$$

显然地，有关系：
$$
\delta S_\alpha= − \delta S_\beta,
\delta V_\alpha= − \delta V_\beta,
\delta n_\alpha= − \delta n_\beta\\
\delta^2 S_\alpha= − \delta^2 S_\beta,
\delta^2 V_\alpha= − \delta^2 V_\beta,
\delta^2 n_\alpha= − \delta^2 n_\beta
$$
同时系统满足复相平衡条件：
$$
T_\alpha = T_\beta\\
p_\alpha = p_\beta\\
\mu_\alpha = \mu_\beta
$$
代入上式，得：
$$
\begin{array}{ll}
\delta^2 U = 
& \delta T_\alpha \delta S_\alpha − \delta p_\alpha \delta V_\alpha + \delta \mu_\alpha \delta n_\alpha + \\
& \delta T_\beta \delta S_\beta − \delta p_\beta \delta V_\beta + \delta \mu_\beta \delta n_\beta \\
\end{array}
$$
引入：
$$
S = ns, V = nv\\
\delta S = n \delta s + s \delta n, \delta V = n \delta v + v \delta n
$$
得
$$
\begin{array}{ll}
\delta^2 U = 
&n_\alpha(\delta T_\alpha \delta s_\alpha − \delta p_\alpha \delta v_\alpha ) + \\
&n_\beta(\delta T_\beta \delta s_\beta − \delta p_\beta \delta v_\beta ) + \\
&(s_\alpha \delta T_\alpha − v_\alpha \delta p_\alpha + \delta \mu_\alpha )\delta n_\alpha + \\
&(s_\beta \delta T_\beta − v_\beta \delta p_\beta + \delta \mu_\beta )\delta n_\beta
\end{array}
$$
又因为：
$$
\delta µ = − s \delta  T + v \delta p
$$
最后：
$$
\delta^2 U = n_\alpha(\delta T_\alpha \delta s_\alpha − \delta p_\alpha \delta v_\alpha ) +
n_\beta(\delta T_\beta \delta s_\beta − \delta p_\beta \delta v_\beta ) > 0
$$
上式对任意$n_i > 0$成立，各相必有：
$$
\delta T \delta s − \delta p \delta v > 0
$$
利用：
$$
\delta s = \left(\frac{\partial s}{\partial v} \right)_T + \left(\frac{\partial s}{\partial T} \right)_v\\
\delta p = \left(\frac{\partial p}{\partial v} \right)_T + \left(\frac{\partial p}{\partial T} \right)_v
$$
代入得到：
$$
\left(\frac{\partial s}{\partial T} \right)_v (\delta T)^2 -
\left(\frac{\partial p}{\partial v} \right)_T (\delta V)^2 > 0\\
\frac{C_v}{T} (\delta T)^2 + \frac{1}{v \kappa_T} (\delta V)^2 > 0
$$
再利用虚位移的任意性：
$$
C_v > 0, \kappa_T > 0
$$

## 相变平衡的曲线

### 克拉珀龙方程

设$(T, p)$和$(T + \mathrm {d} T, p + \mathrm {d} p)$为两相平衡曲线上邻近的两点。
$$
\mu_\alpha(T,p) = \mu_\beta(T,p)\\
\mu_\alpha(T + \mathrm {d} T, p + \mathrm {d} p) = \mu_\beta(T + \mathrm {d} T, p + \mathrm {d} p)
$$
相减，得到：
$$
\mathrm{d} \mu_\alpha = \mathrm{d} \mu_\beta\\
− s_\alpha \mathrm{d} T + v_\alpha \mathrm{d} p = − s_\beta \mathrm{d} T + v_\beta \mathrm{d} p
$$

$$
\frac{\mathrm{d} p}{\mathrm{d} T} = 
\frac{s_\beta - s_\alpha}{v_\beta - v_\alpha}
$$

定义相变潜热：
$$
L = T(s_\beta - s_\alpha)
$$
得到克拉珀龙方程：
$$
\frac{\mathrm{d} p}{\mathrm{d} T} = 
\frac{L}{T(v_\beta - v_\alpha)}
$$
实际求解中的近似处理：

* 凝聚相的摩尔体积远小于气相的摩尔体积， 因此可以被略去。 

* 把气体看作理想气体。

简化后的克拉珀龙方程：
$$
\frac{1}{p} \frac{\mathrm{d} p}{\mathrm{d} T} = 
\frac{L}{RT^2}
$$
如果进一步认为相变潜热与温度无关，可将上 式积分，得到：
$$
p = p_0 e^{- \frac{L}{R} (\frac{1}{T} - \frac{1}{T_0} )}
$$

### 相变曲线上的临界点

<div>
    <center>
    <img src = "相变曲线上的临界点.jpg"
         alt = "img failed"/>
        <br>
        相变曲线上的临界点
    </center>
</div>

* 临界点温度以上为气态

* 临界点温度以下分气相区、气液混合区和液相区

临界点的性质
$$
\left(\frac{\partial p}{\partial v} \right)_T = 0\\
\left(\frac{\partial^2 p}{{\partial v}^2} \right)_T = 0
$$

## 相变气体的范氏模型



### 范氏模型的修正



## 相变的分类

