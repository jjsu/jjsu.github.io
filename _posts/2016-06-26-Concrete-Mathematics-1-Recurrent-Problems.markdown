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
 g(2n+j) & =3g(n)+{\gamma}n+\beta_j;j=0,1,n\ge1\\
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


## 1.19 Is it possible to obtain $$Z_n$$, regions with $$n$$ bent lines when the angle at each zig is $$30^{\circ}$$?

### Solution:

Assume that we can obtain $$Z_n$$ regions from $$n$$ bent lines, where the $$$$th bent line which consists of a $$\theta_i$$ degree half-line and a $$\theta_i+30^{\circ}$$ degree half-line ($$1\le{i}\le{n}$$).

There are 4 intersection points between $$i$$th and $$j$$th bent lines,if and only if 
$$30^{\circ} \lt | {\theta_i - \theta_j} | \lt 150^{\circ}, (i\ne j)$$.

Let $$\theta_1 \lt \theta_2 \lt ... \lt \theta_n$$, thus we have

$$
\begin{align}
30^{\circ} &\lt  {\theta_2 - \theta_1}  &\lt 150^{\circ}\\
30^{\circ} &\lt  {\theta_3 - \theta_2}  &\lt 150^{\circ}\\
&...  &... \\
30^{\circ} &\lt  {\theta_n - \theta_{n-1}} &\lt 150^{\circ}\\

\end{align}
$$

Hence, $$30^{\circ}(n-1) \lt  {\theta_n - \theta_{1}} \lt 150^{\circ}$$. So we get $$n \lt 6$$.
