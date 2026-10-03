**Hannah Galang**
**30104279**
**Math 367**

**Q1**. 

**solution.** The domain is given by $Dom(f) = \{(x,y)|y\geq 1+x\}$. The boundary point for this function is $y=1+x$, and the interior points are given by $y > 1+x$. In this case, we have that the domain is closed, as it includes all of its boundary points. 

**Q2.**

**solution, a)**.  All directional derivatives exist for $\alpha \geq 2$. The proof is as shown below. 
**proof.** Let $\hat{u}=<u_{1},u_{2}>$ denote an arbitrary unit vector at the point (0,0) on the function, that is, a vector with length 1. Then, the expression for the directional derivative at that point is given by $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})-\vec{f}(0,0)}{t}$$
Evaluating the limit, we take the following steps: 

Noticing that $\vec{f}(0,0)=0$, this then becomes $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})-0}{t} = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})}{t}$$
we can then rewrite this above as $$\lim_{t \to 0}\frac{\vec{f}(0+tu_{1}, 0+tu_{2})}{t} \rightarrow \lim_{t \to 0}\frac{\vec{f}(tu_{1},tu_{2})}{t}$$as the zeros are redundant. Then, we write $$\lim_{t \to 0}\frac{\vec{f}(tu_{1},tu_{2})}{t} = \lim_{t \to 0}\frac{(tu_{1}tu_{2})^{\alpha}}{(tu_{1})^2+(tu_{2})^2}*\frac{1}{t}$$
and we can then write this as $$\lim_{t \to 0}\frac{(tu_{1}tu_{2})^{\alpha}}{(tu_{1})^2+(tu_{2})^2}*\frac{1}{t} = \lim_{t \to 0}\frac{1}{t}*\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^2u_{1}^2+t^2u_{2}^2}$$
$$\rightarrow \lim_{t \to 0}\frac{1}{t}*\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^2u_{1}^2+t^2u_{2}^2} = \lim_{t \to 0}\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^3(u_{1}^2+u_{2}^2)}$$
From here, we note that $(u_{1}^2+u_{2}^2)=1$, as $\hat{u}$ is a unit vector and $||\hat{u}||=1=\sqrt{u_{1}^2+u_{2}^2}=u_{1}^2+u_{2}^2$. We then have $$\lim_{t \to 0}\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^3}$$
From here, we note that if $\alpha = 1$, this results in the limit $$\lim_{t \to 0}\frac{u_{1}u_{2}}{t} = \infty$$
and the limit is not well defined for the directional derivative at (0,0). However, if $\alpha \geq 2$, this results in the limit $$\lim_{t \to 0}{t^{2\alpha-3}u_1^{\alpha}u_{2}^{\alpha}}$$
where $2\alpha-3$ is a positive integer and we have $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0}{t^{2\alpha-3}u_1^{\alpha}u_{2}^{\alpha}}=0$$
resulting in a well defined limit. Thus, the directional derivative exists in all directions at (0,0) for any $\alpha \geq 2$. 

**solution, b).** The function is totally differentiable at the point (0,0) for any $\alpha \geq 2$. The proof is as shown below. 
**proof.** Since we have shown that all directional derivatives exist at the point $(0,0)$, it suffices to show that $D\vec{f}(0,0) = 0$. First, note that $f_{x}(0,0)=0$, and $f_{y}(0,0)=0$, so we have that $J\vec{f}(0,0) = \begin{bmatrix} 0 & 0 \end{bmatrix}$. Plugging this into the definition of $D\vec{f}$, we have: $$D\vec{f}(0,0) = \lim_{(x,y) \rightarrow (0,0)} \frac{|f(x,y)-f(0,0)-\begin{bmatrix} 0 & 0 \end{bmatrix} \begin{bmatrix} x \\
y
\end{bmatrix}|}{||(x,y)||} \rightarrow \lim_{(x,y) \rightarrow (0,0)} \frac{|f(x,y)|}{||x,y||} $$
We then get: 
$$\lim_{(x,y) \rightarrow (0,0)} \frac{|f(x,y)|}{||x,y||} = \lim_{(x,y) \rightarrow (0,0)} \frac{(xy)^{\alpha}}{(x^2+y^2)^{\frac{3}{2}}}$$
We can convert this to polar coordinates: 

$$\lim_{(x,y) \rightarrow (0,0)} \frac{(xy)^{\alpha}}{(x^2+y^2)^{\frac{3}{2}}} = \lim_{r \rightarrow 0} \frac{r^{2\alpha}cos^{\alpha}(\theta)sin^{\alpha}(\theta)}{r^3}$$
Like in the previous case, we have that if $\alpha =1$, then the limit doesn't exist. However, when $\alpha \geq 2$, we have that $2 \alpha$ is a positive integer, and the limit is 0. Since we have then that $D\vec{f}(0,0) = \vec{f}(0,0)$, the function is differentiable at the point $(0,0)$.  

**Q3.**

**solution, a.** To find the set of points for which the function given by the question is satisfied, we will first find the jacobian of the matrix. The jacobian is given by

$$
\begin{bmatrix}
\frac{\delta F_{1}}{\delta x} & \frac{\delta F_{1}}{\delta y} \\
\frac{\delta F_{2}}{\delta x} & \frac{\delta F_{2}}{\delta y}
\end{bmatrix}
$$
We have that $F_{1}=3x-y$ and $F_{2}=x^2y^2$. From here, we can evaluate the jacobian under these functions: 

$$
\begin{bmatrix}
\frac{\delta F_{1}}{\delta x} & \frac{\delta F_{1}}{\delta y} \\
\frac{\delta F_{2}}{\delta x} & \frac{\delta F_{2}}{\delta y}
\end{bmatrix}
\rightarrow 
\begin{bmatrix}
3 & -1 \\
y^22x & x^22y
\end{bmatrix}
$$
We know from linear 1 that this matrix is invertible if and only if its determinant is not equal to 0. Since we know that the determinant of a 2x2 matrix is $ad-bc$, we can just take the determinant and solve for which x and y values will yield a 0 determinant:

$$
det
\begin{bmatrix}
3 & -1 \\
y^22x & x^22y
\end{bmatrix}
\rightarrow 6x^2y-(-y^22x) \rightarrow 6x^2y+y^22x 
$$
Setting this equal to 0, we have: $6x^2y+y^22x=0 \rightarrow x =0$ or $y=0$. 
So, we have that for any set of points in $R^2$ such that $x \neq 0$ and $y \neq 0$, the inverse function theorem is satisfied, and the function is invertible. 

**solution, b.** We first note that the inverse function theorem applies at the point (1,1), since $x \neq 0$ and $y \neq 0$.  

$$
\begin{bmatrix}
3 & -1 \\
y^22x & x^22y
\end{bmatrix}
$$
We can calculate $D\vec{f}(1,1)^{-1}$ by the following:

$$
\begin{bmatrix}
3 & -1 \\
2 & 2
\end{bmatrix}^{-1}
\rightarrow \frac{1}{8}
\begin{bmatrix}
2 & 1 \\
-2 & 3
\end{bmatrix}
$$
By the inverse function theorem, we have that $D\vec{f}(1,1)^{-1}=D\vec{g}(\vec{f}(1,1))$. We double check that $f(1,1) = (2,1)$: $$\vec{f}(1,1)=(3(1)-1, 1^2*1^2)=(2,1)$$
Since this is the case, have that $D\vec{f}(1,1)^{-1}=D\vec{g}(\vec{f}(1,1))=D\vec{g}(2,1)$. So, we've shown what we wanted to show. 

**Q4.**

**solution.** First, we set up our matrix of partial deirvatives: 

$$D\vec{f}(x,y,z,u,v)=
\begin{bmatrix}
3 & 2y & 0 & v & u \\
yz & xz &xy & v^2 & 2uv 
\end{bmatrix}
$$ 
Then we have that:

$$\left.D\vec{f}(y,v,x,u,z) \right|_{(1,1,1,1,1)} = \left. 
\begin{bmatrix}
2y & u & 3 & v & 0 \\
xz & 2uv & yz & v^2 & xy 
\end{bmatrix} \right|_{(1,1,1,1,1)}
\rightarrow
\begin{bmatrix}
2 & 1 & 3 & 1 & 0 \\
1 & 2 & 1 & 1 & 1 
\end{bmatrix}
$$
We have here that $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$. Since $detA=(2*2)-(1*1)=3 \neq 0$, we note that $A$ is invertible, which allows us to apply the implicit function theorem. Finding $D\vec{g}(1,1,1)$, we have: 

$$D\vec{g}(1,1,1) = A^{-1}B = \frac{1}{5}
\begin{bmatrix}
-2 & 1 \\
1 & -2 \\  
\end{bmatrix}
\begin{bmatrix}
3 & 0 & 1 \\
1 & 1 & 1 \\
\end{bmatrix}
=
\begin{bmatrix}
-1 & \frac{1}{5} & -\frac{1}{5} \\
\frac{1}{5} & -\frac{2}{5} & -\frac{1}{5}
\end{bmatrix}
$$
So, we have found $D\vec{g}(1,1,1)$, and we've shown what we needed to show. 