---
layout: post
title: "Recurrent Problems"
mathjax: MathJax
categories: "Concrete Mathematics"
---


##  1.16 four-parameter recurrence


$$
\begin{align}
 g(1) & =\alpha\\
 g(2n+j) & =3g(n)+{\gamma}n+\beta_j;j=0,1,n>=1\\
\end{align}
$$

### Solution:


Assume the closed form to be 

$$g(n)=A(n)\alpha+B(n)\beta_0+C(n)\beta_1+D(n)\gamma$$

From (1.18), we know that:

$$
A(n)\alpha+B(n)\beta_0+C(n)\beta_1=(\alpha\ \beta_{b_{m-1}}\ \beta_{b_{m-2}}\ ...\ \beta_{b_{1}}\ \beta_{b_{0}})_3
$$

where $$n=(1b_{m-1}b_{m-2}...b_{1}b_{0})_2$$.

Let $$(\alpha,\beta_0,\beta_1,\gamma)=(1,0,0,0)$$, and we have $$A(n)=(1\ \underbrace{0\ ...\ 0}_{\text{m}})_3$$.

Let $$(\alpha,\beta_0,\beta_1,\gamma)=(0,0,1,0)$$, then we get $$C(n)=(\beta_{b_{m-1}}\ \beta_{b_{m-2}}\ ...\ \beta_{b_{1}}\ \beta_{b_{0}})_3$$. Meanwhile, we have $$\beta_0=0,\beta_1=1$$ and $$b_x=0$$ or $$b_x=1$$, thus

$$C(n)=(b_{m-1}b_{m-2}...b_{1}b_{0})_3$$

Setting $$g(n)=n$$ implies $$\alpha=1, \beta_0=0, \beta_1=1, \gamma=-1$$; hence
	
$$A(n)+C(n)-D(n)=n$$

That is $$D(n)=A(n)+C(n)-n$$.

Thus,

$$
\begin{align}
	g(n)&=A(n)\alpha+B(n)\beta_0+C(n)\beta_1+D(n)\gamma\\
		&=A(n)\alpha+B(n)\beta_0+C(n)\beta_1+(A(n)+C(n)-n)\gamma\\
		&=(\alpha\ \beta_{b_{m-1}}\ \beta_{b_{m-2}}\ ...\ \beta_{b_{1}}\ \beta_{b_{0}})_3
			+\gamma((1\ \underbrace{0\ ...\ 0}_{\text{m}})_3+(\beta_{b_{m-1}}\ \beta_{b_{m-2}}\ ...\ \beta_{b_{1}}\ \beta_{b_{0}})_3-(1b_{m-1}b_{m-2}...b_{1}b_{0})_2)\\
		&=(\alpha\ \beta_{b_{m-1}}\ \beta_{b_{m-2}}\ ...\ \beta_{b_{1}}\ \beta_{b_{0}})_3
		  +\gamma(1b_{m-1}b_{m-2}...b_{1}b_{0})_3
		  -\gamma(1b_{m-1}b_{m-2}...b_{1}b_{0})_2\\
\end{align}
$$
