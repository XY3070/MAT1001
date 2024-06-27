#math #calculus 

## 1. Substitute in directly

* The formula should be meaningful after substitution  
*eg:*$$
\lim_{ x \to 1 }(2x^2+x+1)=4
$$  
  
## 2. Judge directly

* Involved with one infinity in the numerator or denominator, and we can directly get the result go to infinity or zero  
*eg:*$$
\lim_{ x \to 1 } \frac{2x}{x-1}
=(\frac 2 0)
=\infty
$$  
  
## 3.  $\cfrac{0} {0}$ method

1. **Factoring**  
	* $\cfrac{polynomial}{polynomial}$  
	* to get rid of the zero factor  
	* back to method 1 or 2  
	*eg:*$$
	\lim_{ x \to 1 } \frac{x^2-1}{x-1}
	=lim_{x\to1}(x+1)
	=2  
	\tag{3.1}
	$$  
  
2. **Multiply the same fact both up and down so as to get (square - square)**   
	* involved with (root $\pm$ root)   
	*eg:*$$
	\begin{align}
	\lim_{ x \to 0 } \frac{\sqrt{1+x}-\sqrt{1-x}}{2x}
	&=\lim_{ x \to 0 } \frac{(\sqrt{1+x}-\sqrt{1-x})\cdot(\sqrt{1+x}+\sqrt{1-x})}{2x\cdot(\sqrt{1+x}+\sqrt{1-x})}\\
	&=\lim_{ x \to 0 } \frac{2x}{2x\cdot(\sqrt{1+x}+\sqrt{1-x})}\\
	&=\frac 1 2  \tag{3.2}
	\end{align}
	$$  
  
1. **Equivalent substitution**   
	* $\arcsin x\sim x$ (let $u = \arcsin{x}$, so $x = \sin{u}$)    
	* $\sin x \sim x$  
	* $\tan x\sim x$  
	* $1-\cos x \sim \cfrac{1}{2}x^{2}$  
	*eg:*$$
	\lim_{x\to0}\frac{\arcsin{x}\cdot\tan{x^3}}{1-\cos{x^2}}
	=\lim_{x\to0}\frac{x\cdot{x^3}}{\frac 1 2 (x^2)^2}
	=2
	$$  
  
> Consider equivalent substitution first rather than *L'H$\hat{o}$spital rule*   
  
## 4. $\cfrac{\infty}{\infty}$ method  
  
 * $\cfrac{polynomial}{polynomial}$   
 * Divide both up and down by the highest order of the denominator    
	*eg:*$$
	\begin{align}
	\lim_{ n \to \infty } \frac{n^3+2n+1}{4n^3-2n}
	&=\lim_{ n \to \infty } \frac{1+2n^{-2}+n^{-3}}{4-2n^{-2}}\\
	&=(\frac{0+0+1}{4-0})\\
	&=\frac 1 4
	\end{align}
	$$  
  
## 5. $\infty-\infty$ method  
  
1. **Already a fraction**   
	* reduction of fractions to a common denominator   
	* back to method 1 or 2   
	*eg:*$$
	\lim_{ x \to 1 } (\frac{1}{x-1}-\frac{1}{x^2-1})=\lim_{ x \to 1 } \frac{(x+1)-1}{x^2-1}=(\frac 1 0)=\infty  \tag{5.1}
	$$  
  
1. **Not a fraction**   
	* make it a fraction: multiply and then divide a fact   
	*eg:*$$
	\begin{align}
	\lim_{x\to\infty}(\sqrt{n+1}-\sqrt{n})
	&=\lim_{x\to\infty}\frac{(\sqrt{n+1}-\sqrt{n})\cdot(\sqrt{n+1}+\sqrt{n})}{\sqrt{n+1}+\sqrt{n}}\\
	&=\lim_{x\to\infty}\frac{1}{\sqrt{n+1}+\sqrt{n}}\\
	&=(\frac{1}{\infty})\\
	&=0
	\tag{5.2}
	\end{align}
	$$  
  
## 6.  $1^\infty$ method  
  
* Use the important limit: $\displaystyle\lim_{x \to \infty} (1+\frac{1}{x})^x=e$   
* i.e. $\displaystyle\lim_{x \to 0} (1+x)^{(\frac{1}{x})}=e$   
  
1. Figure out what the $x$ refers to    
2. Make up/Construct the format of the formula    
3. Compare and finish the whole formula    
	*eg:*$$
	\begin{align}
	\lim_{x\to0}(1+3x)^{\frac{2}{x}}
	&=\lim_{x\to0}(1+3x)^{{\frac{1}{3x}}\cdot{6}}\\
	&=\lim_{x\to0}[(1+3x)^{\frac{1}{3x}}]^6\\
	&=e^6
	\end{align}
	$$  
  
## 7. Variable substitution  
  
* Use $t$ or something to substitute a whole part   
	*eg:*$$
	\begin{align}
	\lim_{x\to\frac{\pi}{2}}\sin{x}^{\frac{1}{\cos{x}}}\\
	&let\;\;t=\frac{\pi}{2}-x,\\
	then\;we\;have\;\;\;&\lim_{t\to0}\sin{(\frac{\pi}{2}-t)}^{\frac{1}{\cos{(\frac{\pi}{2}-t)}}}\\
	=&\lim_{t\to0}\cos{t}^{\frac{1}{\sin{t}}}\\
	=&\lim_{t\to0}[1+(\cos{t}-1)]^{\frac{1}{\cos{t}-1}\cdot\frac{\cos{t}-1}{\sin{t}}}\\
	=&\lim_{t\to0}\left([1+(\cos{t}-1)]^{\frac{1}{\cos{t}-1}}\right)^{\frac{\cos{t}-1}{\sin{t}}}\\
	=&e^{\lim_{t\to0}{\frac{\cos{t}-1}{\sin{t}}}}\\
	=&e^{\lim_{t\to0}\frac{-\frac 1 2 t^2}{t}}\\
	=&1
	\end{align}
	$$
*ps: if $\lim f(x) = A$, $\lim g(x) = B$, then $\lim f(x)^{g(x)} = A^B$*  

Usually if the answer gives a Taylor Expansion method, and it may be not the only way to solve out the limitation.  
*eg:*
$$\begin{align}
method \;\; 1 \; (answer) & \\
& \lim_{x\to0}\frac{\tan{x}-\sin{x}}{\sin{x^3}}=( \; * \; )\\
\tan{x}=x+\frac{x^3}{3} & +..., \;\;\;
\sin{x}=x-\frac{x^3}{3!}+...\\
so &\;\; \tan{x}-\sin{x}=\frac 1 2 x^3\\
& (\; * \;)=\lim_{x\to0}\frac{\frac 1 2 x^3}{x^3}\\
& \,\;\;\;\;\;\;\;=\frac 1 2
\end{align}
$$  
$$\begin{align}
method \;\; 2 \; (recommended) & \\
& \lim_{x\to0}\frac{\tan{x}-\sin{x}}{\sin{x^3}}\\
=&\lim_{x\to0}\frac{\sin{x}(\frac{1}{\cos{x}}-1)}{x\cdot{x^2}}\\
=&\lim_{x\to0}\frac{1-\cos{x}}{\cos{x}\cdot{x^2}}\\
=&\lim_{x\to0}(\frac 1 2\cdot{\frac{1}{\cos{x}}})\\
=&\frac 1 2
\end{align}
$$  
  
  
[[MAT1001 - Calculus|Back to Menu]]  
  