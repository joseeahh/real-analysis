# Chapter 1 Theorems

## Theorem 1.11 - Greatest Lower Bound

Suppose $S$ is an ordered set with the least-upper-bound property, $B \subset S$, $B$ is not empty, and $B$ is bounded below. Let $L$ be the set of all lower bounds of $B$. Then
$$\alpha = \sup(L)$$
exists in $S$, and $\alpha = \inf(B)$. In particular, $\inf(B) \in S$.

_Proof:_ Our first goal is to show that $\sup(L)$ exists. Since $S$ has the least-upper-bound property, this defaults to showing that $L$ is not empty and is bounded above. Since $B$ is bounded below, then it has a lower bound. Then $L$ is not empty. By definition, $L=$ $`\{\ell \in S : \forall b \in B, \ell \leq b\}`$. Then every element of $B$ serves as an upper bound of every element in $L$. Then $L$ is bounded above. It then follows that $\sup(L)$ exists in $S$; call it $\alpha$.

Our second goal is to show that $\alpha = \inf(B)$. This devolves into showing that $\alpha \in L$, and it is the greatest lower bound. 
* Suppose, for contradiction, that $b < \alpha$ for some $b \in B$. Then $b$ is not an upper bound of $L$. This contradicts that every element of $B$ is an upper bound of $L$. It must be that $\alpha \leq b$. Then $\alpha$ is a lower bound of $B$, and $\alpha \in L$.
* To show that it is the greatest lower bound, suppose some $\beta \in S$ such that $\alpha < \beta$. Since $\alpha$ is an upper bound of $L$, then $\beta \not \in L$ so that $\beta$ is not a lower bound of $B$.

Then $\alpha = \inf(B)$, and $\inf(B) \in S$. Hence, $S$ has the **greatest lower bound property**.

## Theorem 1.20 - Archimedian Property of $\mathbb R$, Density of $\mathbb Q$ in $\mathbb R$
1. If $x, y \in \mathbb R$ where $x > 0$, then there exists some $n \in \mathbb N$ such that
   $$nx > y$$
2. If $x, y \in \mathbb R$ where $x < y$, there then exists some $q \in \mathbb Q$ such that $x < q < y$.

_Proof:_
1. Define the set $A =$ $`\{nx : n \in \mathbb N\}`$. Assume, for contradiction, that $A$ is bounded above. Since $\mathbb R$ has the least-upper-bound property, we may put $\alpha = \sup(A)$. Since $x > 0$, then $\alpha - x < \alpha$ so that $\alpha - x$ is not an upper bound of $A$. Then $\alpha - x < mx$ for some $m \in \mathbb N$. But then $\alpha < (m + 1)x \in A$, since $m + 1 \in \mathbb N$, contradicting that $A$ is bounded above.
2. Because $x < y$, then $0 < y - x$. By (1), there exists some $n \in \mathbb N$ such that
   $$n(y - x) > 1$$
   We then use (1) again to furnish integers $r$ and $s$ such that $nx < r$ and $s> -nx \implies -s < nx$. Then the following relation holds
   $$-s < nx < r$$
   By the properties of $\mathbb Z$, there exists some $t$ such that $-s \leq t \leq r$. Then
   $$t - 1 \leq nx < t$$
   where $t - 1 \leq nx$, since it may be the case that $nx$ is an integer. Then $t \leq nx + 1$, and
   $$nx < t \leq nx + 1 < ny$$
   Since $n(y - x) > 1 > 0$, and $(y - x) > 0$, then $n > 0$, and it follows that
   $$x < \frac tn < y$$

## Theorem 1.21 - Existence of $n$ th Roots
For every $x \in \mathbb R^+$ and $n \in \mathbb N$, there exists one and only one $y \in \mathbb R^+$ such that $y^n = x$. We denote this as $y = \sqrt[n]x$ or $y = x^{1/n}$.

_Proof:_ If there was another $y_0$ such that $y_0^n = x$, then it must be that either $y_0 < y$ or $y_0 > y$. However, since $0 < a < b \implies 0 < a^n < b^n$ (which is trivial to prove by induction), then no such $y_0$ can exist. Now, let $E = $ $`\{t \in \mathbb R^+ : t^n < x\}`$. Our goal is to show that $E$ is not empty and is bounded above, so that we may invoke the least-upper-bound property of $\mathbb R$ and prove the existence of $\sup(E)$. To that end, consider the following:
* Since $x > 0$, then $x + 1 > 0$ so that $t = \frac{x}{x + 1} > 0$. Similarly, it follows that
  $$x > 0 \implies x^2 > 0 \implies x^2 + x > x \implies x > \frac{x}{x + 1}$$
  Additionally, we have that
  $$x^{n - 1} \leq (x + 1)^{n - 1} \implies (x + 1)x^n \leq x(x + 1)^n \implies \left(\frac{x}{x + 1}\right)^n \leq \frac{x}{x + 1}$$
  Then $0 < t < 1 \implies t^n \leq t < x$ so that $t \in E$.
* If $t > 1 + x > x$, then $t^n \geq t > x$ so that $1 + x$ serves as an upper bound of $E$.

By the least-upper-bound property of $\mathbb R$, $\sup(E)$ exists; call it $y$. To prove that $y^n = x$, we must show that it is not possible for $y^n < x$ nor $y^n > x$. For the first,
