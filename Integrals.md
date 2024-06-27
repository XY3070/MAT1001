#math #calculus 

# Mean Value Theorem for Definite Integrals  
  
**Note that:** *continuity* condition **cannot** be skipped  
  
# Fundamental Theorem of Calculus  
  
If $f(t)$ is an **integrable** function over a **finite** interval $I$, the the interval from any fixed number $a \in I$ to another number $x\in I$ defines a new function $F$ whose value at $x$ is $$\begin{align}
F(x)&=\int_{a}^{x} f(t) \, dt .\tag{1}  \\
\frac{d}{dx}F(x)&=f(x)
\end{align}$$  
**==Theorem==** **- The fundamental Theorem of Calculus, Part I**  
  
If $f$ is **continuous** on $[a,b]$, then $F(x)=\displaystyle\int_{a}^{x} f(t) \, dt$ is **continuous** on $[a,b]$ and **differentiable** on $(a,b)$ and its derivative is $f(x)$:  $$F'(x)=\frac{d}{dx}\int f(t) \, dt =f(x). \tag{2}$$  
*Also works for $x=a$ and $b$ with one-sided derivatives.*  
  
**Remarks about FTC1:**   
* $\displaystyle\int_{a}^{x} f(t) \, dt = \int_{a}^x f(s) \, ds$: the inner variable is a **dummy variable**, so the choice of letter is not important.  However, **DO NOT write** $\displaystyle\int_{a}^{x} f(x) \, dx$.      
* FCT1 implies that any continuous function on $I$ must have an antiderivative on $I$:  
$$F(x):= \int_{a}^{x} f(t) \, dt \;\text{ is an antiderivative of }f.$$  
**Remark:** If $F(u)=\displaystyle\int_{a}^{u} f(t) \, dt$, then $\displaystyle\int_{a}^{g(x)} f(t) \, dt = (f\circ g)(x)$, which means $\cfrac{d}{dx}\displaystyle\int_{a}^{g(x)} f(t) \, dt = F^{'}\big(g(x)\big)g^{'}(x) \stackrel{FTC1}{\longrightarrow} f\big(g(x)\big)g^{'}(x).$  
  
**==Theorem==** **- Fundamental Theorem of Calculus, Part II**  
  
$$\int_{a}^{b} f(x) \, dx = F(b)-F(a).$$  
**Remarks:**   
* The FTC connects definite integrals with indefinite integrals.  
* In particular, part II implies that one can evaluate definite integrals with integrand $f$ by finding an antiderivative of $f$.  
* For convenience, it is common to write $F(x)\Big|_{a}^{b}$ to mean $F(b)-F(a)$  
  
**Q1:** If $c(x)$ is the total cost for producing $x$ units of product, what is the meaning of  
$$\int_{a}^{b} c'(x) \, dx? \quad \text{ (Here }a<b.)$$  
**Q2:** What is the **average slope** of all the tangent lines to the curve $y=f(x)$ over the interval $[a,b]$?  ($f$ is differentiable)  
  
**A2:**  $$\cfrac{1}{b-a}\int_{a}^{b} f'(x) \, dx =\cfrac{f(b)-f(a)}{b-a}=\text{the slope of the secant line}$$  
  
# Areas between Curves  
  
## The Area between a Curve and the $x$-axis  
  
### Definition  
  
$$A:=\int _{a}^{b} \Big|f(x)\Big| \, dx .$$  
**Remark:** If $f$ is integrable and **nonnegative** on $[a,b]$, then the area above becomes  $$A:=\int _{a}^{b} f(x) \, dx .$$  
## The Area between Two Curves  
  
### Definition  
  
$$A:=\int _{a}^{b} \Big|f(x)-g(x)\Big| \, dx .$$  
**Remark 1:** *$x$-axis is a special case by taking $g(x)\equiv 0$.*   
  
**Remark 2:** Area $A$ between curves $x=f(y)$ and $x=g(y)$, from $y=a$ to $y=b$, can be defined similarly: $$A:=\int_{a}^{b} \Big|f(y)-g(y)\Big| \, dy $$
  
# Indefinite Integrals and Substitution Method  
  
## Substitution Method  
  
*a few techniques for finding $F$*  
  
**Idea:** Running the Chain Rule Backwards  
  
If $u$ is a differentiable function of $x$, the simpler expression $du$ can be substituted for $\cfrac{du}{dx}dx$ when computing an integral.   
  
1. Substitute $u=g(x)$ and $du=\cfrac{du}{dx}dx=g^{'}(x)dx$ to obtain $\int f(u) \, du$.  
2. Integrate w.r.t. $u$.  
3. Replace $u$ by $g(x)$.  
  
**Hint:** *Observe that a power of $x$ appears in the ==integrand== that is **one less** than that in the ==argument== of a function -- try a substitution for the **higher power** of $x$.*  
  
==to be continued==  



# Definite Integral Substitutions  
  
**==Theorem==** **- Substitution in Definite Integrals  
  
$$\int_{a}^{b} f\big(g(x)\big)\cdot g'(x) \, dx = \int_{g(a)}^{g(b)} f(u) \, du .$$  
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  