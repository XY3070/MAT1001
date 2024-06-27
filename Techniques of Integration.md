#math #calculus 

# Integration by Parts  
  
## Indefinite Integrals  
  
Suppose that $f$ and $g$ are **differentiable**. Then  $$\big(f(x)g(x)\big)'=f'(x)g(x)+f(x)g'(x),$$  
so  $$\int \Big(f'(x)g(x)+f(x)g'(x)\Big) \, dx =f(x)g(x)+C.$$  
**==Formula==** **(Integration by Parts)**  
  
$$\int f(x)g'(x) \, dx =f(x)g(x)-\int f'(x)g(x) \, dx .$$  
**Alternative Form:** $u=f(x)$ and $v=g(x)$. $du=f'(x)dx$ and $dv=g'(x)dx$  $$\int udv =uv-\int vdu$$  
Integration by parts is particularly effective when **one of** $f'g$ and $fg'$ is *easier to integrate* then the other.  
  
### Reduction Formula  
  
For $n\in \mathbb{N}$ with $n\geq 2$:  
$\int \sin^{n}x \, dx =-\cfrac{1}{n}\cos x\sin^{n-1}x+ \cfrac{n-1}{n}\int \sin^{n-2}x \, dx.$  
$\int \cos^{n}x \, dx= \cfrac{1}{n}\sin x\cos^{n-1}x+ \cfrac{n-1}{n}\int \cos^{n-2}x \, dx.$  
  
**Remark:**  It replaces an integral containing some power of a function with an integral of the same form having the **power reduced**  
  
## Definite Integrals  
  
By **FTC II**,  $$\int _{a}^{b}\Big(f(x)g'(x)+f'(x)g(x)\Big) \, dx =f(x)g(x)\Big|_{a}^{b}$$  
**==Formula==** **(Integration by Parts for Definite Integrals)**  
  
$$\int_{a}^{b} f(x)g'(x) \, dx =f(x)g(x)\Big]_{a}^{b}-\int_{a}^{b} f'(x)g(x) \, dx .$$  
## Tabular Integration  
  




# Trigonometric Integrals  

# Trigonometric Substitutions  






[[MAT1001 - Calculus|Back to Menu]]  
  