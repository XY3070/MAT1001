#math #calculus 

# Volumes Calculation  
  
## Using Cross-Sections  
  
* Consider a partition $P:= \{x_{0},\;x_{1},\; \dots,\; x_{n-1},\;x_{n}\}$ be a partition of $[a,b]$.  
* When $\Delta x_{k}$ is small, the volume of the solid lying between $x=x_{k-1}$ and $x = x_{k}$ is approximately $A(x_{k})\Delta x_{k}$.  
* When $\Vert P \Vert$ is small, the volume of $S$ is approximately  $$\sum_{k=1}^{n}A(x_{k})\Delta x_{k}.$$  
### Definition  
  
$$V:=\int_{a}^{b} A(x) \, dx ,$$  
provided that the cross-section area function $A(x)$ is **Integrable** on $[a,b]$.  
  
*Hence, to find $V$, we can find a formula for the cross section area first.*  
  
#### Solid of Revolution  
  
If the Solid $S$ is generated by rotating the region  $$\{(x,y):0\leq y\leq R(x),\;a\leq x\leq b\}$$  
around the $x$-axis, then the cross-sections of $s$ are discs with radii $R(x)$. Consequently, $A(x)=\pi R(x)^{2}$, and  $$V=\int _{a}^{b}\pi R(x)^{2} \, dx .$$  
*Similarly,* if the Solid $S$ is generated by rotating the region  $$\{(x,y):0\leq r(x)\leq y\leq R(x),\;a\leq x\leq b\}$$  
around the $x$-axis, then  $$V=\int _{a}^{b}\pi \Big(R(x)^{2}-r(x)^{2}\Big) \, dx , \quad \text{where }A(x_{0})=\pi \Big[R(x_{0})^2-r(x_{0})^2\Big]$$  
The idea can be *similarly* applied to a solid obtained by revolving a region around the *$y$-axis*, or around *lines* of the form $y=K$ or $x=K$ in general.  
  
## Using Cylindrical Shells  
  
* Volume of "the thin cylindrical shell" $\approx \big(\text{circumference}\big)\cdot\big(height\big)\cdot \big(\text{thickness}\big)=2\pi x_{k}^{*}\cdot h(x_{k}^{*})\cdot \Delta x_{k}$  
* Riemann sum for volume $=\sum_{k=1}^{n}2\pi x_{k}^{*}h(x_{k}^{*})\Delta x_{k}$  
* Exact volume $= \text{limit of Riemann sums}$  
  
### Definition  
  
$$V=\int _{a}^{b}2\pi xh(x) \, dx .$$    
# Arc Length  
  
Consider a curve given by a continuous function $y=f(x)$ defined on the interval $[a,b]$, and let $P$ be a partition of $[a,b]$.  
  
If $y_{k}:=f(x_{k})$ and $\Delta y_{k} = y_{k}-y_{k-1}$, then the length of the curve between the points $(x_{k-1},y_{k-1})$ and $(x_{k},y_{k})$ is approximately  $$L_{k}=\sqrt{ (\Delta x_{k})^{2}+(\Delta y_{k}^2) }=\sqrt{ 1+\left(\frac{\Delta y_{k}}{\Delta x_{k}}\right)^{2} \Delta x_{k}}$$  
when $\Delta x_{k}$ is small. Then definition of art length is obtained by taking limit of $\displaystyle\sum_{k=1}^{n}L_{k}$ as $\Vert P \Vert \to 0$.  
  
## Definition  
  
Let $f$ be a function s.t. $f'$ is continuous on $[a,b]$. The **length** (of **arc length**) $L$ of the curve $y=f(x)$ between the points $(a,f(a))$ and $(b,f(b))$ is defined by  $$L:=\int _{a}^{b}\sqrt{ 1+\left(\frac{dy}{dx}\right)^{2} } \, dx = \int _{a}^{b}\sqrt{ 1+\big(f'(x)\big)^{2} } \, dx .$$  
**Remarks:**  
*Similarly,* if the curve is given by $x=g(y), \; c\leq y\leq d$, and $g'$ is continuous, then  $$L:=\int _{c}^{d}\sqrt{ 1+\left(\frac{dx}{dy}\right)^{2} } \, dy = \int _{c}^{d}\sqrt{ 1+\big(g'(y)\big)^{2} } \, dy .$$  
## Arc Length Differentials  
  
Given $y=f(t)$ defined on some interval $I$, fix $a \in I$. Define  $$s(x):=\int _{a}^{x}\sqrt{ 1+f'(t)^{2} } \, dt $$  
for $x\in I$. Then$s(x)$ is the **signed distance** from $(a,f(a))$ to $(x,f(x))$ along the curve $y=f(t)$ (When $x<a$, this signed distance is *negative*).  
* By **FTC I**, $s'(x)=\sqrt{ 1+f'(x)^{2} }$,  
* $ds=\sqrt{ 1+f'(x)^{2} }dx$ is called the **arc length differential**  
* Note that  $ds=\sqrt{ 1+\left(\cfrac{dy}{dx}\right)^{2} }dx =\sqrt{ (dx)^{2}+(dy)^{2} }$.  
  
# Areas of Surfaces of Revolution  
  
Consider a surface generated by revolving about the $x$-axis a curve $y=f(x)$, where $f$ is **Nonnegative**, for $x\in [a,b]$.  $$A_{k}\approx 2\pi f(x_{k})L_{k}\approx 2\pi f(x_{k})\sqrt{ 1+\left(\frac{\Delta y_{k}}{\Delta x_{k}}\right)^2}\Delta x_{k}.$$  
## Surfaces of a Cone (without base)  
  
1. $\text{Area }= \cfrac{\theta}{2\pi}\pi l^{2}$; want to express without $\theta$.  
2. $\cfrac{\theta}{2\pi}= \cfrac{\overset{\LARGE{\frown}}{AB}}{2\pi l}=\cfrac{\text{circumference of cone base }}{2\pi l}=\cfrac{2\pi r}{2\pi l}=\cfrac{r}{l}$  
1,2 $\Rightarrow \text{Area }= \cfrac{r}{l}\pi l^{2}=\pi rl$    
  
## Surfaces of a Conical Frustum  
  
![[conical frustum.png]]  
  
$$\begin{align}
\text{Area of fustum}&=\text{Area of Big cone}-\text{Area of Small cone} \\
&=\pi |OA|R-\pi |OC|r \\
&=\pi(|OC|+L)R-\pi|OC|r \quad \quad \text{want to elimate }|OC| \tag{3}\\
\frac{|OC|}{|OC|+l}&=\cfrac{r}{R} \Rightarrow \frac{|OC|}{R}=|OC|e+Lr \\
&\Rightarrow |OC|=\frac{Lr}{R-r} \tag{4} \\ \\
&\Rightarrow |OC|+L=\frac{Lr+LR-Lr}{R-r}=\frac{LR}{R-r} \tag{5}\\
\text{Sub 4 \& 5 in 3}: \\
\text{Area}&=\pi(|OC|+L)R-\pi|OC|r \\
&=\frac{\pi LR}{R-r}R-\pi\frac{Lr}{R-r}r =\pi\frac{L}{R-r}(R^{2}-r^{2})\\
&=\pi(R+r)L
\end{align}$$  
## Definition  
  
$$S=\int _{a}^{b}2\pi f(x)\sqrt{ 1+\left( \frac{dy}{dx} \right)^{2} } \, dx =\int _{a}^{b}2\pi f(x)\sqrt{ 1+\big(f'(x)\big)^{2} } \, dx ,$$  
where $\sqrt{ 1+\big(f'(x)\big)^{2}  }dx$ is the **arc length differential**.  
*Similarly* defined about $y$-axis.  
  
# Work and Fluid Forces  
  
## The Pressure-Depth Equation  
  
In a fluid that standing still, the pressure $p$ at depth $h$ is the fluid's weight-density $w\;(N/m^{3})$ times $h$:  $$p=wh.$$  
therefore, $F= \text{total force}=\text{force per unit area} \times \text{area}=pA=whA$.  
* For a flat plate submerged *horizontally*, the **downward force** acting on its upper face due to the liquid pressure is given by $F=pA=whA$  
* If the plate is submerge *vertically*, then the pressure against it will be different at different depths.  
  
## Fluid Pressure and Forces  
  
![[fluid force.png]]
  
$$\begin{align}
\Delta F&=(\text{pressure alomng bottom edge})\times (\text{area}) \\
&=w \cdot (\text{strip depth})\cdot \Delta y. \\
F&\approx \sum_{k=1}^{n}\big(w\cdot(\text{strip depth})_{k}\cdot L(y_{k})\big)\Delta y_{k}.
\end{align}$$  
### Definition  
  
$$F=\int_{a}^{b}w\cdot(\text{strip depth})\cdot L(y) \, dy $$
  
  
[[MAT1001 - Calculus|Back to Menu]]    
  