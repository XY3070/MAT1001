#math #calculus 

# Inverse Functions and Their Derivatives  
  
## Definition  
  
A function $f(x)$ is **one-to-one** on a domain $D$ if $f(x_{1})\neq f(x_{2})$ whenever $x_{1}\neq x_{2}$ in $D$.  

## The Horizontal Line Text for One-to-One Functions  
  
A function $y=f(x)$ is one-to-one **if and only if** its graph intersects each horizontal line **at most once**  
  
## Definition  
  
Suppose that $f$ is a one-to-one function on $D$ a=with range $R$. The **inverse function** $f^{-1}$ is defined by  $$f^{-1}(b)=a \quad \text{if}\quad f(a)=b.$$  
The domain of $f^{-1}$ is $R$ and the range of $f^{-1}$ is $D$.  
*Notice that the '"$-1$"is **NOT** an exponent. The domains of $f$ and $f^{-1}$ are interchanged.*  
  
**Remark:**  
* Composing a function and its inverse has the same effect  
	$(f^{-1}\circ f)(x)=x, \quad \text{for all }x \text{ in the domain of }f$  
	$(f\circ f^{-1})(y)=y, \quad \text{for all }y \text{ in the domain of }f^{-1}\text{(or range of }f\text{)}$  
* **Only** a one-to-one function can have an inverse  
* if $f$ is **monotonic** on $D$, then $f$ is one-to-one function on $D$, so inverse $f^{-1}$: $range(f)\to D$ must exist  
* Functions that neither increasing nor decreasing may still be one-to-one and have an inverse. eg.: $f(x)=\cfrac{1}{x}$ for $x\neq 0$.  
  
**Facts** (without proof)  
* If $f$ is continuous and $f^{-1}$ exists, then $f^{-1}$ is also continuous.  
* If $f$ is continuous and has domain being an interval, then $range(f)$ is also an interval.  
* If $f$ is one-to-one and continuous function on $I$, then $f$ is monotone on $I$.  
  
**==Theorem==** **-The Derivative Rule for Inverse**  
  
$$(f^{-1})(b)=\frac{1}{f^{'}\big(f^{-1}(b)\big)}$$  
or  $$\frac{df^{-1}}{dx}\Bigg|_{x=b}=\cfrac{1}{\cfrac{df}{dx}\bigg|_{x=f^{-1}(b)}}$$  
Based on Theorem 1:  
$f^{-1}$ is differentiable, and  $$(f^{-1})'(y_{0})=\cfrac{1}{f'(x_{0})}, \quad \forall y_{0}\in range(f),$$   
where $f(x_{0})=y_{0}$.  
**Note that** another way to write the conclusion above is  $$f^{-1}(y_{0})=\cfrac{1}{f'\big(f^{-1}(y_{0})\big)}.$$  
Theorem 1 makes two **assertions:**  
1. $f^{-1}$ is differentiable  
2. Calculation of $(f^{-1})'$  $$\begin{align} 
f(f^{-1}(x))&=x \quad& &\text{Inverse function relationship}\\
\frac{d}{dx}f\big(f^{-1}(x)\big)&=1 \quad& &\text{Differentiating both sides}\\
f'\big(f^{-1}(x)\big)\cdot \frac{d}{dx}f^{-1}(x)&=1 \quad& &\text{Chain Rule}\\
\frac{d}{dx}f^{-1}(x)&=\frac{1}{f'\big(f^{-1}(x)\big)}. \quad&  &\text{Solving for the derivative}
\end{align} $$  
## Inverse Trigonometric Functions  
  
The sine function is not *injective* on its natural domain $R$, so it does not have an inverse in this case.  
But $\sin:\left[ -\frac{\pi}{2},\frac{\pi}{2} \right] \to [-1.1]$ is increasing, so it is *injective* and has an inverse  $$\arcsin:[-1,1]\to \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right].$$  
This is the **inverse sine function**, which is also denoted by $\sin^{-1}$.  
  
Q: $\arcsin'(x)=?$  
Let $y_{0}\in(-1,1)$ and let $x_{0}\in \left( -\frac{\pi}{2}, \frac{\pi}{2}\right)$ be s.t.  $$\sin x_{0}=y_{0}$$  
Then, by inverse differentiation,  $$\arcsin'(y_{0})=\frac{1}{\sin'x_{0}}=\frac{1}{\cos x_{0}}=\frac{1}{\sqrt{ 1-\sin^{2}x_{0} }}=\frac{1}{\sqrt{ 1-y_{0}^{2} }}$$  
Hence:  $$\arcsin'x=\frac{1}{\sqrt{ 1-x^{2} }}, \quad \forall x\in (-1,1) \tag{*}$$  
**Remarks:**  
* $\arcsin'x$ does not exist at $x\pm 1$ **(infinite slope)**  
* The formula $(\ast)$ assumes that the domain of sine is $\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$. It may be different otherwise.  
  
**Six trigonometric functions and their inverse:**  
(Be aware of the given **default domains**)  
  
![[trigonometric functions and their inverse.png]]
  






# Natural Logarithm  
  
## Definition  
  
The **natural logarithm** is the function given by  $$\ln x=\int _{1}^{x} \cfrac{1}{t} \, dt, \quad x>0.$$    
## Properties of Logarithms  
  
**==Theorem==** **- Algebraic Properties of the Natural Logarithm**  
  
1. **Product Rule:** $\ln bx=\ln b+\ln x$  
2. **Quotient Rule:** $\ln \cfrac{b}{x}=\ln b-\ln x$  
3. **Reciprocal Rule:** $\ln \cfrac{1}{x}=-\ln x$  
4. **Power Rule:** $\ln x^{r}=r\ln x$  
  
**Proof**  
  
## Limits of Derivatives  
  
Since $\displaystyle\lim_{ x \to \infty }\ln'x=\lim_{ x \to \infty }\cfrac{1}{x}=0$, the graph $y-\ln x$ tends to have a "flat" tangent line as $x$ grows big, yet it is **bounded above**.  
  
If we take $g(x)=|x|$ with $D=\mathbf{R}\backslash \{ 0 \}$, then$g'(x)= \frac{|x|}{x}$. By the chain rule,  $$\frac{d}{dx}\ln|x|= \frac{1}{|x|} \cdot \frac{|x|}{x}= \frac{1}{x}.$$  
This means that on the intervals $(-\infty,0)$ and $(0,\infty)$, $\ln|x|$ is an antiderivative of $\cfrac{1}{x}$, i.e.  $$\int \frac{1}{x} \, dx =\ln|x|+C$$  
for any **ONE** of the two intervals above.  
  
More generally, id $g(x)=|f(x)|$ where $f$ is differentiable and never zero, then by the chain rule,  $$g'(x)= \frac{|f(x)|}{f(x) \cdot f'(x)},$$  
so,  $$\frac{d}{dx}\ln|f(x)|=\frac{1}{|f(x)|} \cdot \left(\frac{|f(x)|}{f(x) \cdot f'(x)}\right)=\frac{f'(x)}{f(x)} .$$  
If $u=f(x)$, then $du=f'(x)dx$ and  $$\int \frac{f'(x)}{f(x)} \, dx =\ln|f(x)| +C$$  
whenever $f(x)$ is a differentiable function that is never zero.  
  
**Remark**  
  
The above equation tells us how to *integrate some trigonometric functions*.  
  
eg:  $$\begin{align}
\int \tan x \, d&=\int \cfrac{\sin x}{\cos x} \, dx = \int -\cfrac{du}{u}& &u=\cos x >0 \;on\;\left( -\frac{\pi}{2}, \cfrac{\pi}{2} \right),\;du=-\sin x dx\\
 & =\ln|u|+C = -\ln|\cos x|+C \\
 & =\ln \frac{1}{|\cos x|}+C=\ln|\sec x|+C.& &\text{Reciprocal Rule}  \\
\int \cot x \, dx &=\int \cfrac{\cos xdx}{\sin x} = \int \frac{du}{u}& &u=\sin x,\;du=\cos xdx  \\
 & \ln|u|+C=ln|\sin x|+C=-\ln|\csc x| + C.    
\end{align}$$  
eg:  $$\begin{align}
\int \sec x \, dx &= \int \sec x \frac{\sec x+\tan x}{\sec x+\tan x} \, dx = \int \frac{\sec^{2}x+\sec x\tan x}{\sec x+\tan x} \, dx \\
 & = \int \frac{du}{x} =\ln|u|+C=\ln|\sec x+\tan x|+C \\
( \;u=\csc x+\cot x&,\;du=(-\csc x\cot x-\csc^{2}x)dx \;)  
\end{align}$$  
eg:  $$\begin{align}
\int \csc \, dx &= \int \csc x \frac{\csc x+\cot x}{\csc x+\cot x} \, dx =\int \frac{\csc^{2}x+\csc x\cot x}{\csc x+\cot x}  \, dx  \\
 & = \int -\frac{du}{u}=-\ln|u|+C = \ln|\csc x+\cot x|+C \\
(\; u=\csc x+\cot x&,\;du=(-\csc x\cot x-\csc^{2}x)dx \;) 
\end{align}$$  
## Logarithmic Differentiation  
  
For the derivatives of **positive functions**, we *take the natual logarithm of both sides* before differentiating.  
  
# Exponential Functions  
  
## Natural Exponentials  
  
### Definition   
   



[[MAT1001 - Calculus|Back to Menu]]  
  