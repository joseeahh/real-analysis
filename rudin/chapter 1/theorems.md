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
2. Because $x < y$, then $0 < y - x$. By 1, there exists some $n \in \mathbb N$ such that
   $$n(y - x) > 1$$
