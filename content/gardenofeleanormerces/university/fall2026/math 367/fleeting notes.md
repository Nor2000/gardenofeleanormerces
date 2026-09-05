# dr trefor bazett: overview of vector calculus

- vector field: 2 dimensional, 3 dimensional
- what is a vector space? 
	- at any point in space we can put a vector
	- example: gravity: the force of gravity working on a particle can be represented as a vector field
	- example: water running through a river
	- vector fields everywhere in physics, math, engineering, etc
	- vector field as curves? 
		- suppose that we have a disk sitting in 3d space on the x-y plane. this can be represented as a function
			- however, we can also have another function that lives "above" our function
			- bounded vs unbounded curve
			- surface intervals: 
				- example: suppose we 
			- relationship between curves and surfaces and vector fields
				- what kinds of questions can we ask? 
					- **flux**: to what degree is the vecotr field dispersing across the boundary? 
					- to what degree is the vecotr field aligned in relation to a norm of my boundary? 
					- **flow**: tendency for the vector field to be aligned  with the tangents of the curve rather than the pushing out of the boundary? 
		- **big question**: how do local properties relate to global properties? 
			- how do the parts relate to the global properties? 

## week one notes, w2026

- what is the classical derviative? 
	- definition, etc
	- implies: f(x) is  ==well approximated== by a linear function at x=a (namely, the tangent)
	- taylors theorem:
		- a function is well approximated by a function $P_{n}(x)$ 
		- $P_{n}(x) = a_{0}+a_{1}(x-a)+a_{2}(x-a)^2+....+a_{n}(x-a)^n$
		- we can pick our coefficients such that the 'kth' derivative at the point a of our polynomial, we want this t be equal to the kth derivative of our function at the point a. 
			- ==why is this relevant?==
				- if we've already assumed that $P_{n}$ well approximates $f(x)$. 
- basic object of study in this course will be a function that takesa subset from $R^n$, defined as $U$, to $R^m$. 
	- ==what are the valid function operations? because if we have that it is equipped with vector addition and scalar multiplication, it is a vector space==
	- where there are n input variables and m output variables
- **classical case**: m=n=1
	- "traditional" calculus you learn in high school: one input, one output
	- "multivariate scalar functions" 
		- multiple inputs, one single output
	- "parametric curves"
		- the curve defined by variables are separate functions of an independent variable, such as time, which is also known as a parameter
	- "vector fields" 
		- vector fields versus vector spaces: vector spaces are more generalized and are entire algebraic areas where vectors can be added or scaled, versus a vector field which follows the rules that fields generally follow
			- vector fields assign a vector to every point within a space
			- ==function built on top of a space==
		- vector space is an underlying algebraic set/framework; a vector field is a function or assignment
			- if an analogy were to be made, a vector space is a branch of ethics, such as utlitarianism, and a vector space would be the specific instructions a person creates for how to perform utilitarianism
	- "affine maps" (generalization of a line)
		- linear maps need to send the origin to (0,0), affine maps relax this rule by adding a shift or translation, meaning the origin does not need to stay fixed
			- included operations: rotation, scaling, shearing, reflection, translation
			- preserved properties: straight lines stay straight, and parallel lines remain parallel
				- ratios of distances also remain constant
			- unpreserved properties: angles and absolute lengths do not always stay the same

### the topology of $R^n$

- aka properties of $R^n$ that stay the same when the space is bent, twisted, or stretched
	- open ball, closed ball, sphere
	- r: the radius around any given point in space
- ==in the classical deriavtive, we require the point at which we are differentiating to reside in an open interval within the domain==
	- $f(x)$ needs to be defined in a small open interval containing $a$. 
	- [[interior]] definition
		- basically, if there exists a radius r that is greater than 0 such that the [[open ball]] with radius r centered around $a$ is a subset of $U$, which is a subset of $R^n$, then we say that $\vec{a}$ is interior to U. 
			- we say that U is open if U = to its interior(i.e. every point in U is interior)
			- 