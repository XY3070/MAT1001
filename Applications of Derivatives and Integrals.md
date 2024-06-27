#math #calculus 

# Antiderivatives  
  
## Definition  
  
Let $F$ and $f$ be functions defined on an interval $I$. Then $F$ is called an **antiderivative** of $f$ on $I$ if $F'(x) = f(x)$ for all  $x\in I$.  
  
Recall the following corollary of the mean value theorem:  
**Corollary (2)**  
If $G'{(x)} = F'(x)$ for all $x \in (a,b)$, then there exists a constant $C$ such that $G(x) = F(x) + C$ for all $x \in (a,b)$  
  
The interval $(a,b)$ above can be replaced with any interval $I$.  
Therefore:  
  
**==Theorem==**  
  
if $F$ is an antiderivative of $f$ on an interval $I$, then all the antiderivatives of $f$ on $I$ are exactly the functions  
$$F(x)+C$$
where $C$ is any real constant *(so it's a set of the all the solutions)*  
  
Where does a function have an antiderivative? The following theorem gives a **sufficient condition**.  
  
**==Theorem==**  
  
If a function $f$ is **continuous** on an interval $I$, then it has an antiderivative on $I$.  
**Remark**  
All the *elementary functions* have *antiderivatives* on their domains since they are continuous.  
  
**Some antiderivative formulas**  
* $\sec^{2} {kx} \to \cfrac{1}{k} \tan {kx} + C$  
* $\csc^{2}{x} \to -\cfrac{1}{k}\cot{kx} + C$  
* $\sec{kx}\tan{kx} \to \cfrac{1}{k}\sec{kx}+C$  
* $\csc{kx}\cot{kx} \to -\frac{1}{k}\csc{kx}+C$  
  
# Indefinite Integrals  
  
## Definition  
  
If $F$ is an antiderivative of $f$, then we may write  
$$
\int f(x) \, dx = F(x) + C
$$
The function $f$ is called **integrand** of the integral, and $x$ is called the **variable of integration**.  
  
For the **linearity** of differentiation, we have the theorem  
**Theorem** (Linearity of Integration)  
For any real constants $\alpha$ and $\beta$,  
$$\int \Big(\alpha f(x) + \beta g(x)\Big) \, dx = \alpha \int f(x) \, dx + \beta \int g(x) \, dx .$$
  
## Motivations of Integrals  
  
**Integration:** calculate the areas and volumes of very general shapes  
**Definite integral:** calculate many important quantities, such as areas, volumes, lengths, lengths of curved paths, probabilities, averages, energy consumption...   
**Idea:** break the quantities into small pieces, and then sum up the contributions from each piece  
  
# Area and Estimating with Finite Sums  
  
## Finding Area  
  
We may approximate R by summing areas of rectangles  
Intuitively, the approximation will be better if we divide an interval into more subintervals   
  
eg:  
![[finding area.png]]
  
In the above example:  
* We divide $[0,1]$ into $n$ subintervals of **equal length** $\Delta x = \cfrac{1}{n}$, corresponding to points $x_{0}, x_{1}, \dots, x_{n}$, where  
* $$x_{0} = 0,\; x_{1} = \cfrac{1}{n},\; x_{2} = \cfrac{2}{n},\;\dots,\; x_{n}=\cfrac{n}{n}=1$$  
* The approximation area is   
$$\cfrac{1}{n} \Big( f(c_{1})+f(c_{2})+\dots +f(c_{n})\Big) = \cfrac{1}{n}\sum_{i=1}^{n}f(c_{i}),$$
	where each $c_{i} \in [x_{i-1},x_{i}]$ is chosen to be the **left endpoint** $x_{i-1}$.  
* In this example, the function is **decreasing**, so $f(c_{i}) = f(x_{i-1})$ always gives the **maximum** $f$-value on $[x_{i-1}, x_{i}]$; when $c_{i}$ is chosen to give maximum, the sum $\cfrac{1}{n}\Sigma_{i=1}^{n}f(c_{i})$ is called an **upper sum.**  
  
Instead of using **left endpoints**, one may also use **right endpoints** or the **midpoints** of the subintervals.  
* Right-hand sum is a **lower sum**(under-estimated)  
* Left-hand sum is an **upper sum**(over-estimated)  
* Midpoint sum is a **lower sum** when the curve is concave **down**; is an **upper sum** when the curve is concave **up**  
  
### Riemann Sum  
  
#### Definition  
  
A **partition** of the interval $[a,b]$ is a set $P:= \{x_{0},\;x_{1},\; \dots,\; x_{n-1},\;x_{n}\}$  s.t.   $$a=x_{0}<x_{1}<\dots < x_{n-1}<x_{n}=b$$
  
#### Definition  
  
Let $f: [a,b] \to R$ be a function, and let $P:= \{x_{0},\;x_{1},\; \dots,\; x_{n-1},\;x_{n}\}$ be a partition of $[a,b]$. A **Riemann sum** of $f$ (w.r.t. $P$) is a sum of the form $$f(c_{1})\Delta x_{1} + f(c_{2})\Delta x_{2} + \dots + f(c_{n})\Delta x_{n},$$  
where $c_{k}$ is any number in $[x_{k-1},x_{k}]$, and $\Delta x_{k} = x_{k} = x_{k-1}$, with $k \in \{1,2,\dots,n\}$ *(the $c_{k}$ may be in different length)*  
  
*Note that there are **many** Riemann sums for a function $f$: a Riemann sum depends on the partition $P$ and the points $c_{k}$ chosen from the subintervals. The left-hand, right-hand, and midpoint sums are all **special cases** of a Riemann Sum.*    
  
# Sigma Notation and Limits of Finite Sums  
  
## Sigma Notation  
  
### Properties  
  
1. Sum Rule (the same for Difference Rule)  
	$\displaystyle\sum_{k=1}^{n}(a_{k}+b_{k})=\sum_{k=1}^{n}a_{k}+\sum_{k=1}^{n}b_{k}$  
2. Constant Rule  
	$\displaystyle\sum_{k=1}^{n}ca_{k} = c \cdot \sum_{k=1}^{n}a_{k}$  
3. Constant Value Rule  
	$\displaystyle\sum_{k=1}^{n}c=n \cdot c$  
*$k$, $i$, and $j$ etc. are called **dummy variable***   
  
**Some useful identities**  
* $\displaystyle\sum_{k=1}^{n}k=1+2+\dots+n = \cfrac{1}{2}n(n+1)$  
* $\displaystyle\sum_{k=1}^{n}k^{2}=1^{2}+2^{2}+\dots+n^{2} = \cfrac{1}{6}n(n+1)(2n+1)$  
* $\displaystyle\sum_{k=1}^{n}k^{3}=1^{3}+2^{3}+\dots+n^{3} = \cfrac{1}{4}n^{2}(n+1)^{2}=\Big(\cfrac{n(n+1)}{2}\Big)^2$   
  
## Norm of a Partition  
  
### Definition   
  
Let $P:= \{x_{0},\;x_{1},\; \dots,\; x_{n-1},\;x_{n}\}$ be a partition of $[a,b]$. The **norm** of $P$. denoted by  
$$\Vert P\Vert:= \max_{k:1\leq k\leq n} \Delta x_{k}.$$
That is, $\mid\mid P\mid\mid$ is the length of the **largest** subinterval given by $P$.  
  
## The Limit of Riemann Sums  
  
$$\lim_{ \Vert P \Vert \to 0 } \sum_{k=1}^{n}f(c_{k})\Delta x_{k}=J$$
*$\Vert P \Vert \to 0$ is the same as $n \to \infty$*  
  
# Definite Integral  
  
## Definition  
  


## Integrable Functions  
  
**==Theorem==**  
  
**(a)** If $f$ is **continuous** in $[a,b]$, then $f$ is integrable in $[a,b]$  
**(b)** If $f$ is **bounded** and has only **finitely many points of discontinuity** on $[a,b]$, then $f$ is integrable on $[a,b]$  
  
**Idea for (a)**  
  
* Define $U_{p}(f)$ and $L_{p}(f)$ as before, and show that $U_{p}(f)-L_{p}(f) \to 0$ as $\Vert P \Vert \to 0$.  
* By continuity, as long as we choose $\Vert P \Vert$ to be small enough, $M_{k}-m_{k}$ can be arbitrarily small $\forall k$, and $U_{p}-L_{p}$ can be arbitrarily small.  
$\Rightarrow$ Formally, for any given $\epsilon > 0$, choose $\Vert P \Vert$ small enough s.t. $M_{k}-m_{k} < \cfrac{\varepsilon}{b-a}$, $\forall k$.  
$\Rightarrow$ Then, ...
  
## Properties of Definite Integrals  
  
1. Order of Integration: $\displaystyle\int_{a}^{b} f(x) \, dx=-\int_{b}^{a} f(x) \, dx$  *A definition*  
2. Zero Width Interval: $\displaystyle\int_{a}^{b} f(x) \, dx =0$  *A definition when $f(a)$ exists*  
3. Constant Multiple: 
4. Sum and Difference:  
5. Additivity:  
6. Max-Min Inequality:  
7. Domination:  
  
![[intuition of properties 3 to 7 in terms of area.png]]
  
**==Theorem==**  
  
If $f$ is integrable on $[a, b]$ and $g$ is the same as $f$ on $[a,b]$, except at **finitely many** points $x_{1}, \; x_{2}, \; \dots, \; x_{m}$, then $g$ is integrable on $[a,b]$, and  $$\int_{a}^{b} g(x) \, dx = \int_{a}^{b} f(x) \, dx $$  
![[intuition of integral of discontinuity.png]]  
  
## Mean Value Theorem of Definite Integrals   
  
### Average Values / Means  
  
#### Definition  
  
Let $f$ be a function that is **integrable** on $[a,b]$. The **mean value** (or **average value**) of $f$ is defined to be the number $$\cfrac{1}{b-a}\int_{a}^{b} f(x) \, dx .$$  
***Remark***: $f$ *may not be nonnegative in the definition above.*   
  
**==Theorem==**  
  
If $f$ is **continuous** on $[a,b]$, then at some point $c$ **in** $[a,b]$, $$f(c)=\cfrac{1}{b-a}\int_{a}^{b} f(x) \, dx .$$  
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  