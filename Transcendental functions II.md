#math #calculus 

# Indeterminate Forms  
  
$\cfrac{0}{0},\; \frac{\infty}{\infty},\; \infty \cdot 0,\; \infty-\infty,\; 0^{0},\; 1^{\infty},\; \text{and }\infty^{0}$.   ^indeterminateForms
  
Such limits may or may not exist in general, but the limit D.N.E. for the function $F(x)$ under discussion by applying $L'H\hat{o}spi tal's\;Rule$.  
  
More generally, as $x\to c$ and $y\to \infty$, $x^{y}$ converges to $0$ for $|c|<1$, diverges to $\infty$ for $c>1$, oscillates (similar to vibrates) without converging for $c\leq-1$, and is indeterminate when $c=1$.  
  
# L'H$\hat{o}$pital's Rule  
  
**==Theorem==** ($L'H\hat{o}spi tal's Rule,\;or\;L'Hospi tal's Rule$)  
  
Let $c\in \mathbb{R}.$ Suppose that $f$ and $g$ are **differentiable** on $D:=(c-a, c+a)\backslash \{c\}$ for some $a>0$, and that $g'(x)\neq 0$ for all $x\in D$. Suppose that one of the following two conditions holds:  
* $\displaystyle\lim_{ x \to c }f(x)=0=\lim_{ x \to c }g(x)$;  
* $\displaystyle\lim_{ x \to c }f(x)\in \{ -\infty,\infty \}$ and $\displaystyle\lim_{ x \to c }g(x)\in \{ -\infty,\infty \}$.  
Then  $$\lim_{ x \to c } \frac{f(x)}{g(x)}=\lim_{ x \to c } \frac{f'(x)}{g'(x)},$$  
provided that *the limit on the right **exists** (or is $\pm\infty$)*  
  
**Remark**   
  
1) L'Hospital's rule is also valid if we replace "$\displaystyle\lim_{ x \to c }$" with "$\displaystyle\lim_{ x \to c^{+} }$" or "$\displaystyle\lim_{ x \to c^{-} }$".  
2) If $D$ is changed to an unbounded interval, then this rule is also valid if we replace "$\displaystyle\lim_{ x \to c }$" with "$\displaystyle\lim_{ x \to \infty }$" or "$\displaystyle\lim_{ x \to -\infty }$".  
3) L'Hospital's rule is a powerful tool for evaluating limits in **indeterminate forms**. [[Transcendental functions II#^indeterminateForms|What are indeterminate forms?]]  
  
**Notice that** L'Ho has its limitation.  
eg:  
* $\displaystyle\lim_{ x \to \infty } \cfrac{x^{2}+\sin x}{x^{2}}$.  
* $\displaystyle\lim_{ x \to \infty } \cfrac{e^{x}-e^{-x}}{e^{x}+e^{-x}}$.  
  
The proof of L'Ho is based on **Cauchy's Mean Value Theorem**  
  
**==Theorem==** **- Cauchy's Mean Value Theorem**    
  
Suppose $f$ and $g$ are **continuous** on $[a,b]$ and **differentiable** throughout $(a,b)$ and also suppose $g'(x)\neq 0$ throughout $(a,b)$. Then there exists a number $c$ in $(a,b)$ at which  $$\cfrac{f'(c)}{g'(c)}= \cfrac{f(b)-f(a)}{g(b)-g(a)},\quad g(a)\neq g(b).$$  
*When $g(x)=x$, this Theorem is the Mean Value Theorem in Chap.4.*  
  
## Limits of Products and Quotients  
  
Suppose that $\displaystyle\lim_{ x \to a } \cfrac{f(x)}{g(x)}=L.$ Then  $$\begin{align}
&\lim_{ x \to a } f(x)h(x)=\lim_{ x \to a } \frac{f(x)}{g(x)}g(x)h(x)= L \cdot \lim_{ x \to a } g(x)h(x) \\
&\lim_{ x \to a } \cfrac{f(x)}{h(x)}=\lim_{ x \to a } \cfrac{f(x)g(x)}{g(x)h(x)}=L \cdot \lim_{ x \to a } \cfrac{g(x)}{h(x)}
\end{align}$$  
provided that limits involved above **exist**.  
  
**Remark**  
  
* Replacing $f(x)$ with $Lg(x)$ in a product or quotient will keep the limit unchanged if it exists  
* It does not work with **sums** and **differences**, in general  
* "$\displaystyle\lim_{ x \to a }$" can be replaced with "$\displaystyle\lim_{ x \to \infty }$" and "$\displaystyle\lim_{ x \to \infty }$".  
  

# Relative Rates of Growth  
  
## Definition  
  
1. $f$ grows *faster than* $g$ as $x\to \infty$ if  $$\lim_{ x \to \infty } \cfrac{f(x)}{g(x)}=\infty$$   
or equivalently, if  $$\lim_{ x \to \infty } \cfrac{g(x)}{f(x)}=0.$$  
We also say that $g$ grows *slower than* $f$ as $x\to \infty$.  
2. $f$ and $g$ grow *at the same rate* as $x\to \infty$ if   $$\lim_{ x \to \infty } \frac{f(x)}{g(x)}=L \quad (L>0,\;L\in \mathbb{R}) $$  
where $L$ is finite and **positive**.  
  
If $f$ grows at the same rate as $g$ as $x\to \infty$, and $g$ grows at the same rate as $h$ as $x\to \infty$, then $f$ grows at the same rate as $x\to \infty$.  *(transition)*  
  
## Order and Oh-Notation  
  
### Definition  
  
1. $f$ is **of smaller order than** $g$ as $x\to \infty$ if $\displaystyle\lim_{ x \to \infty }=0$. We indicate this by writing $f=o(g)$ ("$f$ is little-oh of g").  
2. Let $f$ and $g$ be positive for $x$ *sufficiently large*. Then $f$ is **of at most the order of** $g$ as $x\to \infty$ if there is a *positive integer* $M$ for which  $$\cfrac{f(x)}{g(x)} \leq M,$$  
for $x$ sufficiently large. That means $\cfrac{f}{g}$ is *bounded* by $M$. We indicate this by writing $f=O(g)$ ("$f$ is big-oh of $g$").  
  
**Remark**  
  
If $\displaystyle\lim_{ x \to \infty } \cfrac{f(x)}{g(x)}=K\in\mathbb{R^{+}}$, then $f(x)=O\big(g(x)\big)$ as $x\to \infty$.  
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  