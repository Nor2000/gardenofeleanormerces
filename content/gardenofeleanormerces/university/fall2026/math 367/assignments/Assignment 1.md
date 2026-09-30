
**Q1**

**Q2.**

**solution, a)**.  All directional derivatives exist for $\alpha \geq 2$. The proof is as shown below. 
**proof.** Let $\hat{u}=<u_{1},u_{2}>$ denote an arbitrary unit vector from the point (0,0) on the function, that is, a vector with length 1 "comign out of" (0,0). Then, the expression for the directional derivative at that point is given by $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})-\vec{f}(0,0)}{t}$$
Evaluating the limit, we take the following steps: 

i) Noticing that $\vec{f}(0,0)=0$ (from the way the function is defined), this then becomes $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})-0}{t} = \lim_{t \to 0} \frac{\vec{f}(0+tu_{1}, 0+tu_{2})}{t}$$
ii) we can then rewrite this above as $$\lim_{t \to 0}\frac{\vec{f}(0+tu_{1}, 0+tu_{2})}{t} \rightarrow \lim_{t \to 0}\frac{\vec{f}(tu_{1},tu_{2})}{t}$$as the zeros are redundant. Then, looking at the way the piecewise function is defined, we write $$\lim_{t \to 0}\frac{\vec{f}(tu_{1},tu_{2})}{t} = \lim_{t \to 0}\frac{(tu_{1}tu_{2})^{\alpha}}{(tu_{1})^2+(tu_{2})^2}*\frac{1}{t}$$
and we can then write this as $$\lim_{t \to 0}\frac{(tu_{1}tu_{2})^{\alpha}}{(tu_{1})^2+(tu_{2})^2}*\frac{1}{t} = \lim_{t \to 0}\frac{1}{t}*\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^2u_{1}^2+t^2u_{2}^2}$$
$$\rightarrow \lim_{t \to 0}\frac{1}{t}*\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^2u_{1}^2+t^2u_{2}^2} = \lim_{t \to 0}\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^3(u_{1}^2+u_{2}^2)}$$
iii) From here, we note that $(u_{1}^2+u_{2}^2)=1$, as $\hat{u}$ is a unit vector and $||\hat{u}||=1=\sqrt{u_{1}^2+u_{2}^2}=u_{1}^2+u_{2}^2$. We then have $$\lim_{t \to 0}\frac{t^{2\alpha}u_1^{\alpha}u_{2}^{\alpha}}{t^3}$$
From here, we note that if $\alpha = 1$, this results in the limit $$\lim_{t \to 0}\frac{u_{1}u_{2}}{t} = \infty$$
and the limit is not well defined for the directional derivative at (0,0). However, if $\alpha \geq 2$, this results in the limit $$\lim_{t \to 0}{t^{2\alpha-3}u_1^{\alpha}u_{2}^{\alpha}}$$
where $2\alpha-3$ is a positive integer and we have $$D_\hat{u}\vec{f}(0,0) = \lim_{t \to 0}{t^{2\alpha-3}u_1^{\alpha}u_{2}^{\alpha}}=0$$
resulting in a well defined limit. Thus, the directional derivative exists in all directions at (0,0) for any $\alpha \geq 2$. 

**solution, b).** The function is totally differentiable at the point (0,0) for any $\alpha \geq 2$. The proof is as shown below. 
proof. Since we have shown that all directional derivatives (including partial derivatives) exist for $\alpha \geq 2$ at the point (0,0), it suffices to show that they are also continuous at the point (0,0), that is, i) that $f(0,0)$ is defined, ii) $\lim_{(x,y) \to (0,0)}f(x,y)$ exists, and that iii) $\lim_{(x,y) \to (0,0)}f(x,y) = f(0,0)$. 

For i) note that the function explicitly says that $f(0,0)=0$. So $f(0,0)$ is defined. 

For ii), we find the partial derivatives as follows: $$\frac{\delta}{\delta x} \frac{x^{\alpha}y^{\alpha}}{x^2+y^2} = y^{\alpha} \frac{\delta}{\delta x} \frac{x^{\alpha}}{x^2+y^2} \to \frac{\delta}{\delta x} \frac{x^{\alpha}}{x^2+y^2} = \frac{\frac{(x^2+y^2)(\alpha x^{\alpha}-2x^2(x^{\alpha})}{x}}{(x^2+y^2)^2}$$
$$\rightarrow \frac{\frac{(x^2+y^2)(\alpha x^{\alpha}-2x^2(x^{\alpha})}{x}}{(x^2+y^2)^2} = \frac{x^{\alpha}(\alpha(x^2+y^2)-2x^2)}{(x^2+y^2)^2}$$

**Q3.**

**solution, a.** To find the set of points for which the function given by the question is satisfied, we will first find the jacobian of the matrix. The jacobian is given by

$$
\begin{bmatrix}
\frac{\delta F_{1}}{\delta x} & \frac{\delta F_{1}}{\delta y} \\
\frac{\delta F_{2}}{\delta x} & \frac{\delta F_{2}}{\delta y}
\end{bmatrix}
$$
In the context of this question, we have that $F_{1}=3x-y$ and $F_{2}=x^2y^2$. From here, we can evaluate the jacobian under these functions: 

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
Setting this equal to 0, we have: $$6x^2y+y^22x=0 \rightarrow x,y=0$$
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

$$D\vec{f}(y,v,x,u,z) = 
\begin{bmatrix}
2y & u & 3 & v & 0 \\
xz & 2uv & yz & v^2 & xy 
\end{bmatrix}
\rightarrow
\begin{bmatrix}
2 & 1 & 3 & 1 & 0 \\
1 & 2 & 1 & 1 & 1 
\end{bmatrix}
$$
We have here that $A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$. Since $detA=(2*2)-(1*1)=3 \neq 0$, we note that $A$ is invertible, which allows us to apply the implicit function theorem. Finding $D\vec{g}(\vec)