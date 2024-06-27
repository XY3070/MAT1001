#calculus #math 

# Inverse Trigonometric Functions  

By restricting the **domain** of the function, we can make an **trigonometric fn** *one-to-one*.  

![[domain restrictions of the trigonometric fns.png]]

By *reflecting the graphs* through the line $y=x$, we can get the graphs of the **inverse trigonometric fns**.  

![[inverse trigonometric fns.png]]

## The Arcsine and Arccosine Functions  

$$\arcsin(-x) = -\arcsin x$$which indicates that the graph is symmetric about *the origin*. It's intuitive, because if the sine function takes a *minus* sign, the angle will be reflected by the $x$-axis, getting the angle also with a *minus* sign.  

The graph of $y=\arccos x$ has **NO** such symmetry.

$$\arccos x + \arccos(-x) = \pi,$$ or   
$$\arccos(-x) = \pi - \arccos x$$We can interpret that identity with some graphs.  

![[arccos x and arccos(-x) are supplementary angles.png]]

Also, we can see from the triangle that for $x>0,$  $$\arcsin x + \arccos x = \frac{\pi}{2}.$$  
![[arcsin x and arccos x are complementary angles.png]]

That equation holds for the other values of $x$ in $[-1,1]$ as well. However, that cannot be derived from the triangle directly.

> [!info] **How to understand "Arc" in the inverse fns?**  
> ![[the arc in arcsine and arccosine.png]]  
> For a *unit* circle and radian angles, the arc length equation $s=r\theta$ becomes $s=\theta$, so central angles and the *corresponding* arcs have the same magnitude.    
> If $x=\sin y$, then, the arc or angle $y$ *(match with the red angle)* has a sine with magnitude to be $x$.  
> Similarly, if $x = \cos y$, then, the arc or angle $y$ *(match with the blue angle)* has a cosine with magnitude to be $x$.  

## Inverse of $\tan x,\cot x, \sec x,$ and $\csc x$  

The graph of $y=\arctan x$ is symmetric about *the origin* because it is a branch of the graph $x=\tan y$ that is symmetric about *the origin*. Algebraically, this means 
$$\arctan(-x) = -\arctan x.$$the arctangent is an **odd** function. The graph of $y= \cot^{-1} x$ has **NO** such symmetry. 

> [!caution] 
> There is no general agreement about how to define $\sec^{-1}x$ for *negative values* of $x$. We choose angles in the second quadrant between $\frac{\pi}{2}$ and $\pi$. This makes $\sec^{-1}x = \cos^{-1}\left( \frac{1}{x} \right)$. It also makes $\sec^{-1}x$ an *increasing fn* on each interval of its domain.   
> $$\sec^{-1} x = \arccos \left( \frac{1}{x} \right) = \frac{\pi}{2} - \arcsin \left( \frac{1}{x} \right).$$  

# Derivatives  

## The Derivatives of Trigonometric Fns  

### $\tan x$  

$$\begin{align}
\frac{d}{dx} \tan x & = \frac{d}{dx} \left( \frac{\sin x}{\cos x} \right) \\
 & = \frac{1}{\cos ^{2}x} \left(  \frac{d(\sin x)}{dx}\cos x - \frac{d(\cos x)}{dx}\sin x \right) \\
 & = \frac{\cos ^{2}x + \sin ^{2}x}{\cos ^{2}x} \\
 & = \sec ^{2}x
\end{align}$$  
### $\cot x$  

$$\begin{align}
\frac{d}{dx} \cot x & = \frac{d}{dx}\left(  \frac{\cos x}{\sin x} \right) \\
 & = \frac{1}{\sin ^{2}x} \left( \frac{d(\cos x)}{dx}\sin x - \frac{d(\sin x)}{dx}\cos x \right) \\
 & = - \frac{\cos ^{2}x + \sin ^{2}x}{\sin ^{2}x} \\
 & = -\csc ^{2}x 
\end{align}$$
$\quad$ compare with $\tan x$'s. 

### $\csc x$  

$$\begin{align}
\frac{d}{dx} \csc x & = \frac{d}{dx} \frac{1}{\sin x} \\
 & = \frac{1}{\sin ^{2}x} \left( \frac{d(1)}{dx}\cos x - \frac{d(\cos x)}{dx}\cdot 1 \right) \\
 & = - \frac{\cos x} {\sin ^{2}x} \\
 & = -\csc x \cot x \quad \text{ (recommended expression)}
\end{align}$$

### $\sec x$  

$$\begin{align}
\frac{d}{dx} \sec x & = \frac{d}{dx} \frac{1}{\cos x} \\
 & = \frac{1}{\cos ^{2}x} \left( \frac{d(1)}{dx}\cos x - \frac{d(\cos x)}{dx}\cdot 1 \right) \\
 & = \frac{\sin x}{\cos ^{2}x} \\
 & = \sec x \tan x \quad \text{ (recommended expression)}
\end{align}$$
$\quad$ please compare that with $\csc x$'s.  

## The Derivatives of $y = \arcsin u(x)$

By the thm we already learned,  
$$\begin{align}
(f^{-1})'(x) & = \frac{1}{f'\big(f^{-1}(x)\big)} \quad & & \text{Theorem} \\
 & = \frac{1}{\cos(\arcsin x)} & & f'(u)=\cos u  \\
 & = \frac{1}{\sqrt{ 1-\sin^{2}(\arcsin x) }} & & \cos u = \sqrt{ 1-\sin^{2}u } \\
 & = \frac{1}{\sqrt{ 1-x^{2} }}. & & \sin(\arcsin x) = x
\end{align}$$  
If $u$ is a *differentiable* function of $x$ with $|u|<1,$ we apply the **Chain Rule** to get the general formula  
$$\frac{d}{dx}( \arcsin u ) = \frac{1}{\sqrt{ 1-u^{2} }} \frac{du}{dx}, \quad |u|<1.$$  
eg:   $u=x^{2}$
$$\frac{d}{dx}(\arcsin x^{2}) = \frac{1}{\sqrt{ 1-(x^{2})^{2} }} \cdot \frac{d}{dx}(x^{2}) = \frac{2x}{\sqrt{ 1-x^{4}}}.$$  
## The Derivative of $y=\arctan u$  

Similarly, 
$$\begin{align}
(f^{-1})'(x) & = \frac{1}{f'\big(f^{-1}(x)\big)} & \quad & \text{Theorem} \\
 & = \frac{1}{\sec^{2}(\arctan x)} & & f'(u) = \sec^{2}u \\
 & = \frac{1}{1+ \tan ^{2}(\arctan x)} & & \sec ^{2}u = 1 + \tan ^{2}u \\
 & = \frac{1}{1+x^{2}}. & & \tan(\arctan x) = x
\end{align}$$  
The derivative is defined for *all real numbers*. If $u$ is a *differentiable* fn of $x$, we get the Chain Rule form  
$$\frac{d}{dx}(\arctan u) = \frac{1}{1+u^{2}} \frac{du}{dx}.$$  
## The Derivative of $y = \sec^{-1}u$  

Since the derivative of $\sec x$ is *positive* for $(0, \pi)$ and $\left( \frac{\pi}{2}, \pi \right)$, Thm says the inverse fn $y=\sec^{-1}x$ is differentiable. Instead of applying for the thm directly, we find the derivative of $y=\sec^{-1}x,\;|x|>1$, using **implicit differentiation** and the Chain Rule:  
$$\begin{align}
y & = \sec^{-1}x   \\
\sec y & = x \quad & & \text{Inverse fn relationship} \\
\frac{d}{dx}(\sec y) & = \frac{d}{dx}x\\
\sec y\tan y \frac{dy}{dx} & = 1 & & \text{Chain Rule} \\
\frac{dy}{dx} & = \frac{1}{\sec y\tan y}. & & \text{Since }|x|>1, \sec y\tan y \neq 0. 
\end{align}$$
  
To express the result in terms of $x$, we use the relationships  
$$\sec y = x \; \text{ and } \; \tan y = \pm \sqrt{ \sec^{2}y-1 }= \pm \sqrt{ x^{2}-1 }$$

to get  
$$\frac{dy}{dx} = \pm \frac{1}{x\sqrt{ x^{2}-1 }}.$$  
To deal with the $\pm$ sign, 
$$\frac{d}{dx}\sec^{-1}x = \begin{cases}
& + \cfrac{1}{x\sqrt{ x^{2}-1 }} \;\text{ if }x>1 \\
& - \cfrac{1}{x\sqrt{ x^{2}-1 }} \; \text{ if }x< -1.
\end{cases}$$  
With the *absolute value symbol*, we can write a single expression  
$$\frac{d}{dx}\sec^{-1}x = \frac{1}{|x|\sqrt{ x^{2}-1 }}.$$  
If $u$ is *differentiable* with $|u|>1,$ we have  
$$\frac{d}{dx}(\sec^{-1}u) = \frac{1}{|u|\sqrt{ u^{2}-1 }} \frac{du}{dx}, \quad |u| >1.$$   
eg:  $u=5x^{4}$  
$$\begin{align}
\frac{d}{dx}\sec^{-1}(5x^{4}) & = \frac{1}{|5x^{4}|\sqrt{ (5x^{4}_{^{2}}-1) }} \frac{d}{dx}(5x^{4}) \\
 & = \frac{1}{5x^{4}\sqrt{ 25x^{8}-1 }}(20x^{3})  \quad 5x^{4}>1>0 \\
 & = \frac{4}{x\sqrt{ 25x^{8}-1 }}.
\end{align}$$  
> [! tips] Here we can make a brief summary.  
> 1. $d(\arcsin x) = \cfrac{dx}{\sqrt{ 1-x^{2} }}$, $|x|<1$
> 2. $d(\arccos x)= -\cfrac{dx}{\sqrt{ 1-x^{2} }}$, $|x|<1$ 
> 3. $d(\arctan x)=\cfrac{dx}{1+x^{2}}$  
> 4. $d(\cot^{-1} x)= -\cfrac{dx}{1+x^{2}}$  
> 5. $d(\csc^{-1}x) = -\cfrac{dx}{|x|\sqrt{ x^{2}-1 }},$ $|x|>1$  
> 6. $d(\sec^{-1}x)= \cfrac{dx}{|x|\sqrt{ x^{2}-1 }},$ $|x|>1$ 

By this sheet, we can generate a relationship between the **derivative** and the **integral**.  

> [!tips] Let me give you some useful integration formulas. They hold for any constant $a>0$.   
> 1. $\displaystyle\int \frac{du}{\sqrt{ a^{2}-u^{2} }}= \sin^{-1} \left( \frac{u}{a} \right)+C$   (Valid for $u^{2}<a^{2}$)
> 2. $\displaystyle\int \frac{du}{a^{2}+u^{2}}= \frac{1}{a} \tan^{-1} \left( \frac{u}{a} \right)+C$   (Valid for all $u$)
> 3. $\displaystyle\int \frac{du}{u\sqrt{ u^{2}-a^{2} }} = \frac{1}{a} \sec^{-1} \Big|\frac{u}{a}\Big|+C$   (Valid for $|u|>a>0$)

You can generate the rest by yourself. Only through simple *substitution*.

# Integration  

## The Integration of Trigonometric Fns 

### $\tan x$  

$$\begin{align}
\int \tan x \, dx & = \int \frac{\sin x}{\cos x} \, dx  \\
 & = - \int \frac{-\sin x}{\cos x} \, dx \\
 & = - \int \frac{d\cos x}{\cos x} \, \\
 & = -\ln|\cos x| + C  \\
 & = \ln|\sec x| + C 
\end{align}$$

### $\cot x$

$$\begin{align}
\int \cot x \, dx  & = \int \frac{\cos x}{\sin x} \, dx  \\
 & = \int \frac{d\sin x}{\sin x} \, \\
 & = \ln{|\sin x|}+C 
\end{align}$$
$\quad$ compare with $\tan x$'s.  
  
### $\csc x$  

$$\begin{align}
\int \csc x \, dx  & = \int \frac{-\sin x}{-\sin ^{2}x} \, dx  \\
 & = \int \frac{d\cos x}{\cos ^{2}x-1} \\
 & = \int \frac{d\cos x}{(\cos x+1)(\cos x-1)} \\
 & = \frac{1}{2} \int \left(  \frac{1}{\cos x-1}- \frac{1}{\cos x+1} \right) \, d\cos x  \\
 & = \frac{1}{2}\Big(\int \frac{d(\cos x-1)}{\cos x-1}- \int \frac{d(\cos x+1)}{\cos x+1}\Big) \\
 & = \frac{1}{2} \ln \Big|\frac{(\cos x-1)}{(\cos x+1)}\Big| +C  
\end{align}$$

$\quad$ Note that actually there are many *equivalent* kinds of *expression* forms for $\csc x$. There are also many ways to integrate it. You know, $\frac{1}{2} \ln|\frac{\cos x-1}{\cos x+1}|= \frac{1}{2} \ln | \frac{ 2\sin ^{2} \frac{x}{2} }{2\cos ^{2} \frac{x}{2}}| = \ln|\tan \frac{x}{2}|$, and $-\ln|\csc x+\cot x| = -\ln|\frac{(1+\cos x)}{\sin x}| = \ln| \frac{\sin x}{1+\cos x}| = \ln|\tan \frac{x}{2}|$.

### $\sec x$  

$$\begin{align}
\int \sec x \, dx  &  = \int \frac{\cos x}{\cos ^{2}x} \, dx  \\
 & = \int \frac{d(\sin x)}{1-\sin ^{2}x} \\
 & = \int \frac{d(\sin x)}{(1+\sin x)(1-\sin x)} \\
 & = \frac{1}{2} \int \left(  \frac{1}{1-\sin x}+ \frac{1}{1+\sin x} \right) \, d\sin x \\
 & = -\frac{1}{2} \left( \int \frac{d(1-\sin x)}{1-\sin x}+ \int \frac{d(1+\sin x)}{1+\sin x}  \right) \\
 & = \frac{1}{2} \ln \Big| \frac{1+\sin x}{1-\sin x} \Big| +C
\end{align}$$
$\quad$ Similarly, it also has many *equivalent expressions*. Omitted.   

## Integration of Inverse Trigonometric Fns  

Here I don't want to talk about this. You can try **Integration by Parts** to solve integrals like $\int \arcsin x \, dx$. Since they're not that commonly seen, we omit this part here.  

## The Integration of Complicated Trigonometric Fns  

The idea is to use identities to transform the integrals to ones that are easier to work with.

### Products of Sines and Cosines  

Integrals of the form $$\int \sin^{m}x\cos^{n}x \, dx ,$$where $m$ and $n$ are *nonnegative integers*. We can divide the cases according to $m$ and $n$ being *odd or even*.  

==Case 1== $m$ odd  

We write $m$ as $2k+1$ and use the identity $\sin ^{2}x = 1-\cos ^{2}x$ to obtain $$\sin^{m}x=\sin^{2k+1}x = (\sin ^{2}x)^{k}\sin x=(1-\cos^{2}x)^{k}\sin x.$$  









