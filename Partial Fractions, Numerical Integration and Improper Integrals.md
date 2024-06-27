#math #calculus 

# Partial Fractions  

# Numerical Integration  

# Improper Integrals  
  
Definite (Riemann) integral $\int _{a}^{b}f(x) \, dx$ assume two conditions:  
* Interval $[a,b]$ is bounded, and  
* $f$ is bounded on $[a,b]$  
  
Define **Improper Integrals**: *a or b is infinite (unbounded domain)* or the range of the integrand *$f$ is infinite (unbounded integrand)*.    
  
## Type I  
  
Involves unbounded *intervals*.  

### Definition  
  
* Let $a\in \mathbb{R}$. If $f$ is **integrable** on $[a,b]$ for every $b\in [a,\infty)$, then  $$\int _{a}^{\infty}f(x) \, dx :=\lim_{ b \to \infty } \int _{a}^{b}f(x) \, dx .$$  
* Let $b\in \mathbb{R}$. If $f$ is **integrable** on $[a,b]$ for every $\in (-\infty,b]$, then  $$\int _{-\infty}^{b}f(x) \, dx :=\lim_{ a \to \infty } \int _{a}^{b}f(x) \, dx .$$  
### Definition  
  
* An improper integral is said to be **convergent** if the corresponding limit exists, and is said to be **divergent** if the limit D.N.E. (as a real number).  
* We define  $$\int_{-\infty}^{\infty}f(x) \, dx :=\int _{-\infty}^{c}f(x) \, dx +\int _{c}^{\infty}f(x) \, dx $$  
whenever both improper integrals on the right converge. $c$ is any real number.  
  
**Remark:** Our definition of $\displaystyle\int _{-\infty}^{\infty}$ is **NOT** the same as $\displaystyle\lim_{ a \to \infty }\int _{-a}^{a}$.  
  
**Discussion**  
  
Suppose $f(x)$ is odd.  
For **definite integral:**  $$\int _{-a}^{a}f(x) \, dx =0$$  
where **a is a constant** (not $\infty$).  
For **improper integral:**  $$\int _{-\infty}^{\infty}f(x) \, dx =\lim_{ a \to -\infty,b\to \infty } \int _{a}^{b}f(x) \, dx $$  
which **may not be zero**.  
  
### Type I Forms  
  
1. Upper limit  $$\int _{1}^{\infty} \frac{\ln x}{x^{2}} \, dx =\lim_{ b \to \infty } \int _{1}^{b} \frac{\ln x}{x^{2}} \, dx $$   
2. Lower limit  $$\int_{\infty}^{0} \frac{dx}{1+x^{2}}=\lim_{ a \to -\infty } \int _{a}^{0} \frac{dx}{1+x^{2}}$$   
3. Both limits  $$\int _{-\infty}^{\infty} \frac{dx}{1+x^{2}}=\lim_{ b \to -\infty } \int _{b}^{0} \frac{dx}{1+x^{2}}+\lim_{ c \to \infty } \int _{0}^{c} \frac{dx}{1+x^{2}}$$    
eg:  
*(a)*  $\displaystyle\int_{1}^{\infty} \cfrac{1}{x} \, dx=\infty$  
*(b)*  More generally,  $$\int_{1}^{\infty} x^{\alpha} \, dx= \begin{cases}
& -\frac{1}{\alpha+1}, \quad &\text{if }\alpha<-1; \\
& \quad\,\infty, \quad &\text{if }\alpha\geq-1.
\end{cases}$$   
*equivalently,*  $$\int_{1}^{\infty} \frac{1}{x^{p}} \, dx= \begin{cases}
& \cfrac{1}{p-1}, &\text{if }p>1 \quad\text{(convergent)} \\
& \;\;\;\infty, &\text{if }p\leq 1 \quad \text{(divergent)}
\end{cases} .$$  
*(c)*  $\displaystyle\int_{\infty}^{\infty} \cfrac{1}{1+x^{2}} \, dx =\pi$  $$\begin{align}
\int_{0}^{b} \frac{1}{1+x^{2}} \, dx &=\arctan b-\arctan 0 = \arctan b \\
\int_{0}^{\infty} \frac{1}{1+x^{2}} \, dx &=\lim_{ b \to \infty } \arctan b= \frac{\pi}{2}=:B \\
\int_{a}^{0} \frac{1}{1+x^{2}} \, dx &=-\arctan a \\
\int_{-\infty}^{0} \frac{1}{1+x^{2}} \, dx &=\lim_{ a \to -\infty } -\arctan a= -\left( -\frac{\pi}{2} \right)=\frac{\pi}{2}=:A \\
so,\;\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx&=A+B=\pi  
\end{align}$$  
## Type II  
  
Involves discontinuous *integrands*.  
In particular, it covers cases like $f(x)=\cfrac{1}{x}$ which has an infinite discontinuity at $x=0$.  
  
### Definition   
  
* If $f$ is **continuous** on $[a,b)$ and is **discontinuous** at $b$, then  $$\int _{a}^{b}f(x) \, dx :=\lim_{ c \to b^{-} } \int _{a}^{c}f(x) \, dx .$$  
* If $f$ is **continuous** on $(a,b]$ and is **discontinuous** at $a$, then  $$\int _{a}^{b}f(x) \, dx := \lim_{ c \to a^{+} }\int _{c}^{a}f(x)\,dx.$$  
### Definition  
  
If $f$ is **discontinuous** at $c$, where $a<c<b$, and is **continuous** on $[a,b]\backslash\{c\}$, then  $$\int _{a}^{b}f(x) \, dx :=\int _{a}^{c}f(x) \, dx +\int _{c}^{b}f(x) \, dx ,$$  
provided that both improper integrals on the right **converge**.  
4. Upper endpoint  $$\int _{0}^{1} \frac{dx}{(x-1)^{\frac{2}{3 }}}= \lim_{ b \to 1^{-} } \int _{0}^b \frac{dx}{(x-1)^{\frac{2}{3}}}$$  

5. Lower endpoint  $$\int_{1}^{3} \frac{dx}{(x-1)^ \frac{2}{3 }}=\lim_{ d \to 1^{-} } \int _{d}^{3}\frac{dx}{(x-1)^ \frac{2}{3}}$$  
6. Interior point  $$ \int_{0}^{3} \frac{dx}{(x-1)^ {\frac{2}{3}}} =\int_{0}^{1} \frac{dx}{(x-1)^ {\frac{2}{3}}} + \int_{1}^{3} \frac{dx}{(x-1)^ {\frac{2}{3}}}$$    
**Remark**  
  
* If $f$ is **continuous** on $[a,b)$ but $\displaystyle\lim_{ x \to b^{-} }f(x)\in \{ -\infty,\infty \}$, then $\displaystyle\int_{a}^{b} f(x) \, dx$ is **NOT** a Riemann integral (*since unbounded function is not Riemann integrable*) although the notation looks the same.  
* If $f$ is **continuous** on $[a,b)$ and $f$ has a *jump / removable **left** discontinuity*, at $b$, then it can be shown that the improper integral "$\displaystyle\int_{a}^{b} f(x) \, dx$" has the same value as the Riemann integral "$\displaystyle\int_{a}^{b} f(x) \, dx$". (Proof omitted)  
  
eg:  
*(d)*  If $p>0$, then $\cfrac{1}{x^{p}}\to \infty$ as $x\to 0^{+}$, and  $$\int_{0}^{1} \frac{1}{x^{p}} \, dx =\begin{cases}
& \cfrac{1}{1-p},\quad &\text{if }0<p<1; \\
& \;\;\;\infty,\quad &\text{if }p\geq 1. 
\end{cases}$$  
*(e)*  $\displaystyle\int_{0}^{3} \frac{1}{x-1} \, dx$ is undefined according to our definition.  
*(f)*  Suppose $p>0$. $\displaystyle\int_{0}^{1} \cfrac{1}{x^{p}} \, dx=?$  
* $\displaystyle\lim_{ x \to 0^{+} } \frac{1}{x^{p}}=\infty,$ essential discontinuity at $x=0$. Continuous on $(0,1]$.  
* $\displaystyle\int_{a}^{1} \cfrac{1}{x^{p}} \, dx = \frac{1}{-p+1}x^{-p+1}\bigg|_{a}^{1}= \frac{1}{1-p}\left( 1- \frac{1}{a^{p-1}} \right),\quad \text{if }p\neq 1$  
* If $p=1$, $\displaystyle\int_{0}^{1} \frac{1}{x} \, dx=\lim_{ a \to 0^{+} }(\ln 1-\ln a)=\infty$  
* Hence, $$\int_{0}^{1} \frac{1}{x^{p}} \, dx \begin{cases}
 & \text{converges to } \frac{1}{1-p},\quad &\text{if }0<o<1; \\
 & \text{diverges (to }\infty \text{),}\quad &\text{if }p\geq 1.
\end{cases}$$  
Combined with Type-I improper integrals, this means that:  
* If $0<p<1$: $\displaystyle\int_{0}^{1} \frac{1}{x^{p}} \, dx$ converges, $\displaystyle\int_{1}^{\infty} \frac{1}{x^p} \, dx$ diverges.  
* If $p>1$: $\displaystyle\int_{0}^{1} \frac{1}{x^{p}} \, dx$ diverges, $\displaystyle\int_{1}^{\infty} \frac{1}{x^p} \, dx$ converges.  
* If $p=1$: $\displaystyle\int_{0}^{1} \frac{1}{x^{p}} \, dx$ and $\displaystyle\int_{1}^{\infty} \frac{1}{x^p} \, dx$ diverge.  
  
### Convergence Tests  
  
Sometimes it is impossible or difficult to find a closed expression for an improper integral and yet it is important to know whether the integral is convergent or divergent. In this case, convergence tests can be used.  
  
**==Theorem==** **(Direct Comparison Test)**  
  
Suppose that $a\in \mathbb{R}$, and suppose that $f$ and $g$ are **integrable** on $[a,b]\;\forall b\geq a$ functions. If there exists $c\in [a, \infty]$ s.t. $0\leq f(x)\leq g(x)$ for all $x\in[c,\infty]$, then the following statements hold:  
*(i)*  If $\displaystyle\int_{a} ^{\infty} g(x) \, dx$ converges, then $\displaystyle\int_{a}^{\infty}f(x) \, dx$.  
*(ii)*  If $\displaystyle\int_{a}^{\infty}f(x) \, dx$ diverges, then $\displaystyle\int_{a}^{\infty}g(x) \, dx$ diverges.  
  
* Let $F(t):=\displaystyle\int_{c}^{t}f(x) \, dx$ and $G(t):=\displaystyle\int_{c}^{t}g(x)  \, dx$, for $t\geq c$.  
* Since $0\leq f(x)\leq g(x)$ for all $x\in[c, \infty]$, we have $0\leq F(t)\leq G(t),\;\forall t\in[c,\infty]$.  
* Assume that $\displaystyle\int _{c}^\infty g(x)\, dx$ converges. Then $\displaystyle\lim_{ t \to \infty }G(t)=L$ for some $L\in\mathbb{R}$.  
* Then $F(t)$ is bounded above by $L$ and has a "least upper bound", say $A$. *(This makes use of the "least upper bound property" of $\mathbb{R}$, which states that any nonempty set that is bounded above must have a least upper bound.)*  
* Then $\displaystyle\lim_{ t \to \infty }F(t)=A$, so $\displaystyle\int_{c}^\infty f(x) \, dx=A$ (convergent).  
  
eg:  
The improper integral $\displaystyle\int_{0}^\infty e^{-x^{2}} \, dx$ converges. This is true by the direct comparison test because:  
* $0\leq e^{-x^{2}}\leq e^{-x}$ on $[1,\infty),$ and;  
* $\displaystyle\int_{0}^{\infty}e^{-x} \, dx=\lim_{ b \to \infty }(-e^{-b}+e^{-0})=1$, so $\displaystyle\int_{0}^{\infty}e^{-x} \, dx$ converges.  
  
**==Theorem==** **(Limit Comparison Test)**  
  
Suppose that $a\in \mathbb{R}$, and suppose that $f$ and $g$ are *positive* **integrable** on $[a,b],\;\forall b\geq a$. If  $$\lim_{ x \to \infty } \frac{f(x)}{g(x)}=L$$  
for some $L\in \mathbb{R}^{+},$ then   $$\int_{a}^{\infty}f(x) \, dx \quad\text{ and}\quad \int_{a}^{\infty}g(x) \, dx $$  
both converge or both diverge.  
*The limit comparison test may be more convenient sometimes.*  
  
**Remark**  
  
* The limit comparison test can be extended. If $f$ and $g$ are **positive** and **continuous** on $[a,\infty)$ and  $$\lim_{ x \to \infty } \frac{f(x)}{g(x)}=L$$  
then  
1) if $L=0$ and $\displaystyle\int_{a}^{\infty}g(x) \, dx$ converges, then $\displaystyle\int _{a}^{\infty}f(x) \, dx$ converges.  
2) if $L=\infty$ and $\displaystyle\int _{a}^{\infty}g(x) \, dx$ diverges, then $\displaystyle\int _{a}^{\infty}f(x) \, dx$ diverges.  
* The test also applies to **Type II** improper integrals.  
  
**==Theorem==** **(Absolute Convergence Test)**    
  
If $\displaystyle\int_{a}^{\infty}|f(x)| \, dx$ converges, then $\displaystyle\int _{a}^{\infty} f(x) \, dx$ converges.    
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  