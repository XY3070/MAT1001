#math #calculus 

# Models and Differential Equations  
  
## Population Growth (I) - Malthusian growth model  
  
One model for the growth of a population is based on the assumption that the population grows at a rate proportional to the size of the population. If $P(t)$ represents the population at time $t$, then this model is represented by the **differential equation**  $$\frac{dP}{dt}=kP$$  
for some constant $k$.  
  
## Population Growth (II) - Logistic growth model  
  
However, the previous model is too ideal, since population is not likely to grow indefinitely due to limited resources and other constrains. A more practical model would assume:  
* initially, the growth of $P$ is approximately proportional to $P$;  
* the growth will decrease as $P$ gets closer to a certain **carrying capacity** $M$.  
  
Set $k:=K\left( 1- \frac{P}{M} \right),$  $$\frac{dP}{dt} = KP\left( 1- \frac{P}{M} \right)=kP\quad \text{Logistic differential equation}$$  
where $K>0$ is a constant depending on the environment.  
  
* $k\approx K$ when $P$ is small (far below $M$).  
* $k$ decreases as $P$ increases.  
* When $P=M$, $k=0$ and $P$ stops growing.  
* When $P>M$, $k<0$ and $P$ would decrease.  
  
## Basic Terminologies  
  
* All the previous two models involve **ordinary differential equations** (ODE).  
* By the default, we will use $y$ to denote the dependent variable and use $x$ to denote the independent variable.  
* By "solving a differential equation", we mean to find **all** functions $y=y(x)$ that satisfy the differential equation.  
  
## First-Order Differential Equations   
  
Here we will study FODE of the form  $$\frac{dy}{dx} = F(x,y) \tag 1$$   
* $y$ is the dependent variable and $x$ is the independent variable  
* A **solution** to $(1)$ is a function $y=y(x)$ defined on some interval $I$ s.t.  $$y'(x)=F\big(x,y(x)\big),\,\forall x\in I$$  
	The **general solution** to $(1)$ is the collection of all solutions to $(1)$  
  
### Initial Value Problems and Particular Solutions  
  
* A **first order initial value problem** (IVP) is a first order equation together with an *initial value condition*:  
$$\begin{cases}
 & \cfrac{dy}{dx} = F(x,y) \\
 & y(x_{0})=y_{0}
\end{cases}$$  
* A **particular solution** is a solution that satisfies the IVP. 
* Pictorially, a particular solution represents a graph that passes through the point $(x_{0},y_{0})$.  
  
eg:  
Consider the D.E. $y'= \cfrac{x^{2}}{y^{2}}$, then $y=(x^{3}+C)^{ \frac{1}{3}}$ is a solution for every constant $C$, since $$y'= \frac{1}{3}(x^{3}+C)^{-\frac{2}{3}} \cdot 3x^{2}= \frac{x^{2}}{(x^{3}+C)^{\frac{2}{3}}}= \frac{x^{2}}{y^{2}}, \quad \forall x\in \mathbb{R}$$  
If we require $y_{0}=2$ (initial condition), then by solving for $C$, we see that $y=(x^{3}+8)^{\frac{1}{3}}$ is the particular solution.  
(We will see how one can find the general solution above).  
  
### Slope Fields  
  
In general, a differential equation has many solutions (called the *general solutions*). Its solutions can be *visualized* using the following **Slope field**.  
  
**Slope field** of $\cfrac{dy}{dx}=F(x,y)$  
* Choose many points on $xy-plane$ (called *grid points*);  
* For each point $(x,y)$, draw a short line segment with $slope=\cfrac{dy}{dx}=F(x,y)$.  
  
![[slope field.png]]
  
# Separable Differential Equations  
  
A FODE having the form  $$\frac{dy}{dx} = g(x)f(y).$$  
eg: $y'=e^{ x+y }$ is separable, while $y'=e^{ x }+e^{ y }$ **is not**.  
  
Suppose that $y'=g(x)f(y)$ and $f$ is not the zero function. Then   $$\begin{align}
\frac{1}{f(y)}y'&=g(x) \\
\stackrel{\int  \, dx \text{ both sides}}{\implies}\int \frac{1}{f(y)}y' \, dx & =\int g(x) \, dx  \\
\implies \int \frac{1}{f(y)} \, dy  & =\int g(x) \, dx  
\end{align}$$  
After integration, $y$ is written as an implicit function of $x$, and sometimes we may solve $y$ explicitly in terms of $x$.  
  
**Shortcut**  
If $\cfrac{dy}{dx}=g(x)f(y)$, then $\cfrac{dy}{f(y)}=g(x)dx$ and $$\int g(x) \, dx =\int \frac{1}{f(y)} \, dy $$  
*A $\times$B means A can be separated from B by divide to the other side.*  
  
eg 1:  
Solve $y' = e^{ x+y }$.  
$\underline{Sol}:$ $\cfrac{dy}{dx}=e^{ x }e^{ y } \Rightarrow \displaystyle\int \cfrac{1}{e^{ y }} \, dy=\int e^{ x } \, dx$  
		$\implies e^{ -y }=-e^{ x }+C$  
		$\implies -y=\ln(-e^{ x }+C)$  
		$\implies y=-\ln(c-e^{ x })$  
		$D=\{ x\in \mathbb{R}:c-e^{ x }>0 \}$ for a given $C>0$.  
Check: $e^{ y }=e^{ \ln \frac{1}{c-e^{ x }} }=\cfrac{1}{c-e^{ x }},\;\;y= \cfrac{(-1)(-e^{ x })}{c-e^{ x }}=\cfrac{e^{ x }}{c-e^{ x }}=e^{ x }e^{ y }$  
  
eg 2:  
Solve $y'=x^{2}y.$  
 $\underline{Sol}:$ Note that $y \equiv 0$ (*zero function*) is a solution.  
	 Suppose $y$ is not the zero function. Then  
	 $\cfrac{dy}{dx}=x^{2}y\;\implies\;\displaystyle\int \cfrac{1}{y} \, dy=\int x^{2} \, dx$  
	 $\implies \ln|y|= \cfrac{1}{3}x^{3}+K\;\implies \;|y|=e^{ K }e^{ \frac{1}{3}x^{3} }$  
	 $\implies y=\pm e^{ K }e^{ \frac{1}{3}x^{3} }=Ce^{ \frac{1}{3}x^{3} }$, where $C:=\pm e^{ K }$ is a constant.  
Since the zero function is also a solution, the general solution is   $$y=Ce^{ \frac{1}{3}x^{3} },\quad C\in \mathbb{R}$$  
Check: $y'=Ce^{ \frac{1}{3}x^{3} }\cdot x^{2}= x^{2}y$  
  
eg 3:  
Solve the IVP $y'=\left( \cfrac{x}{y} \right)^{2}$, $y(0)=2$.  
$\underline{Sol}:$ $\cfrac{dy}{dx}= \cfrac{x^{2}}{y^{2}}\implies \displaystyle\int y^{2} \, dy=\int x^{2} \, dx$  
	 $\implies \frac{1}{3}y^{3}= \frac{1}{3}x^{3}+C\;\implies\;y^{3}=x^{3}+3C$  
	 $\implies y = (x^{3}+3C)^{\frac{1}{3}}.$  
	 Since $y(0)=2$, $2=(3C)^{\frac{1}{3}} \implies 8=3C$  
	 So Particular solution is   $y= (x^{3}+8)^{\frac{1}{3}}$.  
   
# First-Order Linear Differential Equations   
  
An equation of the form  
$$\frac{dy}{dx}+P(x)y=Q(x).$$  
Considering *multiplying both sides* of the differential equation by a certain function $v(x)$:  
$$v(x)y' + v(x)P(x)y=v(x)Q(x).\tag 1$$  
If we can choose $v(x)$ s.t. the L.H.S. is $\big(v(x)y\big)':$  
$$v(x)y'+v(x)P(x)y=\big(v(x)y\big)'.$$  
The equation $(1)$ above becomes  
$$\big(v(x)y\big)'=v(x)Q(x),$$  
which is equivalent to   
$$v(x)y= \int v(x)Q(x) \, dx .$$  
Therefore, the solution to $y'+P(x)y=Q(x)$ is  
$$y=\frac{1}{v(x)}\int v(x)Q(x) \, dx .$$  
A nonzero function $v(x)$ that satisfies  
$$v(x)y'+v(x)P(x)y=\big(v(x)y\big)' \tag 2$$  
is called an **integrating factor**. By solving Equation $(2)$, one can show that $v(x)$ has the form  
$$Ce^{\int P(x) \, dx},$$  
where $C$ is any zero *nonzero* constant. Since any such function $v$ would solve the differential equation, we may pick $C=1$, and we may pick $\displaystyle\int P(x) \, dx$ to be *any* antiderivative of $P(x)$.  
  
*The IF method is one of the most commonly used and straightforward approaches for solving first-order LDEs.*  
  
Q: How can we find an integrating factor?  
We want  
$$\begin{align}
v(x)y'+v'(x)y&=\big(v(x)y\big)'=v(x)y'+v(x)P(x)y \\
\Leftrightarrow v'(x)y&=v(x)P(x)y \\
\Leftrightarrow v'(x)&=v(x)P(x) \\
\end{align}$$  
(May assume $y \neq 0$, since one can directly check if zero function is a solution.)  
$$\begin{align}
\Leftrightarrow \frac{dv}{dx}&=v \cdot P(x) \quad \text{separable}\\
\int \frac{1}{v} \, dv &= \int P(x) \, dx. \\
\Leftrightarrow \ln|v|&=F(x)+C \quad \big(F'(x))=P(x)\big)\\
\Leftrightarrow |v|&=e^{F(x)+C} \\
\Leftrightarrow v &= \pm e^{F(x)+C}
\end{align}$$  
Since we only need one integrating factor $v$ to solve the linear D.E., we may pick "+" above, and we may pick $F(x)$ to be *ANY particular* antiderivative of $P(x)$.  
  
To solve $y'+P(x)y=Q(x)$, we follow the steps below:  
1. Let $v(x):=e^{\int P(x) \, dx}$ (an integrating factor), where $\displaystyle\int P(x) \, dx$ is *any* antiderivative of $P(x)$.  
2. The general solution is given by   
$$y= \frac{1}{v(x)}\int v(x)Q(x) \, dx .$$  
*General solution contains "$+C$".    
  
eg 4:  
Solve the IVP  $xy'+2y=x^{2}-x+1,\;x>0,\;y(1)= \frac{1}{2}$.  
$\underline{Sol}:$  Standard form  $$y'+ \frac{2}{x}y = x-1+ \frac{1}{x}.$$  
Integrating factor:  $\displaystyle\int P(x) \, dx= \int \cfrac{2}{x} \, dx=2\ln x+K\;(x>0)$.  
			   Let $v(x):= e^{ 2\ln x }= x^{2}$  
General solution:  $y= \cfrac{1}{v(x)}\displaystyle\int v(x)Q(x) \, dx = \cfrac{1}{x^{2}}\int x^{3}-x^{2}+x \, dx$  
		 $\implies y=\cfrac{1}{x^{2}}\left( \cfrac{1}{4}x^{4}- \cfrac{1}{3}x^{3}+ \cfrac{1}{2x^{2}+C} \right)$.  
$y(1)=\cfrac{1}{2}\implies C=\cfrac{1}{12}$.  
So the particular solution is  $y=\frac{1}{4}x^{4}-\frac{1}{3}x^{3}+\frac{1}{2}+\frac{1}{12x^{2}}$.  
  
eg 5:  
Solve the D.E.  $\cos (x)y'+\sin(x)y=2\cos ^{3}(x)\sin(x)-1,\;0\leq x< \frac{\pi}{2}$  
$\underline{Sol}:$  Standard form  $y'+\tan(x)y=2\cos ^{2}(x)\sin(x)-\sec x$  
Integrating factor:  $\displaystyle\int P(x) \, dx=\int \tan x \, dx=\ln|\sec x|+K=\ln(\sec x)+K.\;\left( 0\leq x< \frac{\pi}{2} \right)$  
		Let $v(x):=e^{ \ln(\sec x) }=\sec x$  
$$\begin{cases}
y&= \cfrac{1}{v(x)}\displaystyle\int v(x)Q(x) \, dx =\cos x \int\big(2\cos(x)\sin(x)-\sec ^{2}x\big)\,dx \\
 & =\cos\left( 2\displaystyle\int \sin x \, d\sin x - \int \sec ^{2}x \, dx \right)  \\
 & =\cos x(\sin ^{2}x-\tan x+C)
\end{cases}$$  
So the general solution is  $y=\cos x(\sin ^{2}x-\tan x+C)$  
  
# Applications  



## Orthogonal Trajectories  
  
Let $S$ be a family of curves. A curve $C$ is called an **orthogonal trajectory** of $S$ if $C$ intersects every curve in $S$ orthogonally. (i.e. $\bot$)  


# Autonomous differential equation and Phase Lines  
  
## Definition  
  
An **autonomous equation** is a differential equation of the form  $$\frac{dy}{dx}=f(y)$$  
eg:  
* $\cfrac{dP}{dt}=kP$,  (Malthusian growth model)    
* $\cfrac{dP}{dt}=KP\left( 1-\frac{P}{M} \right)$,  (Logistic growth model)  
* $\cfrac{dH}{dt}=k(H-R)$,  (Newton's law of cooling)  
  
## Definition  
  
Given an autonomous equation $\cfrac{dy}{dx}=f(y)$, for any root $K$ of $f$:  
* $K$ is called an **equilibrium value**.  
* The constant function $y\equiv K$ is called an **equilibrium solution** to the autonomous equation.  
  
## Phase-line analysis  
  
* Construct a graphical solution (understand behavior of solutions)  
* It is a plot on the $y$-axis that shows the equilibrium values along with the intervals where $\cfrac{dy}{dx}$ and $\cfrac{d^{2}y}{dx^{2}}$ are positive and negative.  
* In physics, "**phase**" means the condition of matter of a system.  
  
## Euler's Method (optional)  
  
Given  $$\begin{cases}
 & \cfrac{dy}{dx}=f(x, y); \\
 & y(x_{0})=y_{0}
\end{cases}$$  
we can approximate the solution $y=y(x)$ by its linearization  
$L(x)=y(x_{0})+y'(x_{o})(x-x_{0})$  or equivalently  $L(x)=y_{0}+f(x_{0}, y_{0})(x-x_{0}).$  
So the function $L(x)$ gives a good approximation to the solution $y(x)$ in a short interval about $x_{0}$  
  
**Idea:** patch together a string of linearizations to approximate the curve over a longer stretch.  
* **Step 1:** Using equally spaced values for $x$  
	* $x_{1}=x_{0}+dx$  
	* $x_{2}=x_{1}+dx$  
	* ...  
	* $x_{n}=x_{n-1}+dx$.
* **Step 2:** calculate the approximations to the solution $y$  
	* $y_{1}=y_{0}+f(x_{0}, y_{0})dx$  
	* $y_{2}=y_{1}+f(x_{1},y_{1})dx$  
	* ...  
	* $y_{n}=y_{n-1}+f(x_{n-1}, y_{n-1})dx.$  
* The *errors* can accumulate if $n$ is too large.  
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  