### Metric Space

#### Metric Space

​	**Definition.** A **metric space** is a pair $(X, d)$, where $X$ is a set and d is a metric on $X$ (or distance function on $X$), that is, a function defined on $X \times X$ such that for all $x, y, z \in X$ we have:

(M1)	$d$ is real-valued, finite and nonnegative.

(M2)	$d(x,y) = 0$ if and only if $x=y$.

(M3)	$d(x,y)=d(y,x)$	[*Symmetry*]

(M4)	$d(x,y) \le d(x,z) + d(z,y)$	[*Triangle inequality*]

​	In fact, the nonnegativity of a metric follows from (M2) to (M4):
$$
2d(x,y) = d(x,y) + d(y,x) \ge d(x,x) = 0.
$$
​	**Definition.** A **subspace** $(Y, d)$ of $(X, d)$ is obtained if we take a subset $Y \subset X$ and restrict $d$ to $Y \times Y$; thus the metric on $Y$ is the restriction
$$
\tilde d = d | _{Y\times Y}.
$$
$\tilde d$ is called the metric induced on $Y$ by $d$.

​	We shall now list examples of metric spaces (for the rest of the notes, if there is no other explanation, we will adopt these metrics by default for these spaces):

1. **Real line** $R$ with usual metric defined by $d(x,y) = |x-y|$.

2. **Euclidean plane** $R^2$ with *Euclidean metric* $d(x,y) = ||x-y||_2$.

3. **Euclidean space** $R^n$, **unitary space** $C^n$, **complex plane** $C$. The *Euclidean metric* defined on Euclidean space is
   $$
   d ( x , y ) = \sqrt { ( \xi _ { 1 } - \eta _ { 1 } ) ^ { 2 } + \cdots + ( \xi _ { n } - \eta _ { n } ) ^ { 2 } },
   $$
   where $x = ( \xi _ { 1 } , \cdots , \xi _ { n } ) , \quad y = ( \eta _ { 1 } , \cdots , \eta _ { n } )$. The space $C^n$ can define the following metric
   $$
   d ( x , y ) = \sqrt { | \xi _ { 1 } - \eta _ { 1 } | ^ { 2 } + \cdots + | \xi _ { n } - \eta _ { n } | ^ { 2 } }.
   $$
   When $n=1$, this is the complex plane $C$ with usual metric
   $$
   d(x,y) = |x-y|.
   $$

4. **Sequence space** $l^\infty$. As a set $X$ we take the set of all bounded sequences of complex numbers; that is, every element of $X$ is a complex sequence
   $$
   x = ( \xi _ { 1 } , \xi _ { 2 } , \cdots ) \quad \text { briefly } \quad x = ( \xi _ { j } )
   $$
   such that for all $j=1,2, \cdots$ we have
   $$
   |\xi _j| \le c_x,
   $$
   where $c_x$ is a real number which may depend on $x$, but does not depend on $j$. We choose the metric defined by
   $$
   d(x,y) = \displaystyle \sup _{j \in N} |\xi _j - \eta _j|.
   $$

5. **Continuous Functional space** $C[a,b]$. We can choose the metric (infinite norm) defined by
   $$
   d(x,y) = \displaystyle \max _{t \in J} |x(t)-y(t)|.
   $$
   We may also choose the following metric ($1$-norm) defined by integral
   $$
   \tilde d (x,y) = \int _a ^b |x(t)-y(t)| dt.
   $$
   
6. **Discrete metric space.** We take any set $X$ and on it the so-called discrete metric for $X$, defined by
   $$
   d(x,x) = 0; \quad d(x,y) =1 \text{ ($x\ne y$)}.
   $$
   
7. **Space** $l^p$. Let $p \ge 1$ be a fixed real number. By definition, each element in the space $l^p$ is a sequence $x=(\xi _i) = (\xi _1, \xi_2, \cdots)$ of numbers such that $|\xi_1|^p + |\xi_2|^p + \cdots$ converges; thus
   $$
   \displaystyle \sum _{j=1} ^\infty |\xi _i|^p < \infty
   $$
   and the metric is defined by 
   $$
   d(x,y) = (\displaystyle \sum _{j=1} ^\infty |\xi _j - \eta _j|^p)^{1/p}
   $$
   where $y=(\eta_j)$ and $\sum |\eta _j|^p < \infty$. It satisfies the triangle inequality according to the Minkowski inequality. If we take only real sequences, we get the real space $l^p$, and if we take complex sequences, we get the complex space $l^p$.

   In the case $p=2$, we have the famous *Hilbert sequence space* $l^2$ with metric defined by
   $$
   d(x,y) = \sqrt{\displaystyle \sum _{j=1} ^\infty |\xi _j - \eta _j|^2}.
   $$

#### Open Set, Closed Set, Neighbourhood

​	**Definition.** Given a point $x_0 \in X$ and a real number $r>0$, we define three types of sets:

​	(a)	$B ( x _ { 0 } ; r ) = \{ x \in X | d ( x , x _ { 0 } ) < r \} \quad $[**Open ball**]

​	(b)	$\tilde { B } ( x _ { 0 } ; r ) = \{ x \in X | d ( x , x _ { 0 } ) \leq r \} \quad$[**Closed ball**]

​	(c)	$S ( x _ { 0 } ; r ) = \{ x \in X | d ( x , x _ { 0 } ) = r \}\quad$[**Sphere**]

In all three cases, $x_0$ is called the *center* and $r$ the *radius*.

​	**Definition.** A subset $M$ of a metric space $X$ is said to be **open** if it contains a ball about each of its points. A subset $K$ of $X$ is said to be **closed** if its complement (in $X$) is open, that is, $K^\text C = X-K$ is open.

​	**Definition.** An open ball $B(x_o; \varepsilon)$ of radius $\varepsilon$ is often called an $\varepsilon$-neighbourhood of $X_0$. By a **neighbourhood** of $x_0$ we mean any subset of $X$ which contains an $\varepsilon$-neighbourhood of $x_0$.

​	**Definition.** We call $x_0$ an **interior point** of a set $M \subset X$ if $M$ is a neighbourhood of $x_0$. The **interior** of $M$ is the set of all interior points of $M$ and may be denoted by $M^0$ or $\text {Int} (M)$. $\text{Int}(M)$ is open and the largest open set contained in $M$.

​	Let's show that the collection of all open subsets of $X$, call it $\mathscr T$, has the following properties:

(T1)	$\varnothing \in \mathscr T$, $X \in \mathscr T$.

(T2)	*The union of any members of $\mathscr T$ is a member of $\mathscr T$.*

(T3)	*The intersection of finitely many members of $\mathscr T$ is a member of $\mathscr T$.*

​	It follows from (T1) to (T3) that we've defined a *topological space* $(X, \mathscr T)$ to be a set $X$ and a collection $\mathscr T$ of subsets of $X$. In other words, *a metric space is a topological space*.

​	**Definition.** Let $X=(X,d)$ and $Y=(Y,\tilde d)$ be metric spaces. A mapping $T:X\longrightarrow Y$ is said to be **continuous at a point** $x_0\in X$ if for every $\varepsilon >0$ there is a $\delta >0$ such that 
$$
\tilde { d } ( T x , T x _ { 0 } ) < \varepsilon \quad \text { for all } x \text { satisfying } \quad d ( x , x _ { 0 } ) < \delta.
$$
$T$ is said to be **continuous** if it is continuous at every point of $X$.

​	*A mapping $T$ of a metric space $X$ into a metric space $Y$ is continuous if and only if the inverse image of any open subset of $Y$ is an open subset of $X$.*

​	**Definition.** A point $X_0$ of $X$ (which may or may not be a of $M$) is called an **accumulation point** of $M$ if every neighbourhood of $x_0$ contains at least one point $y \in M$ distinct from $x_0$. The set consisting of the points of $M$ and the accumulation points of $M$ is called the **closure** of $M$ and is denoted by $\bar M$. *It's the smallest closed set containing $M$.*

​	**Definition.** A subset $M$ of a metric space $X$ is said to be **dense** in $X$ if $\bar M = X$. $X$ is said to be **separable** if it has a countable subset which is dense in $X$.

​	Let's consider some important examples mentioned previously:

1. *Real line $R$ is separable.*
2. *Complex plane $C$ is separable.*
3. *A discrete metric space $X$ is separable if and only if $X$ is countable.*
4. *The space $l^p$ with $1\le p < +\infty$ is separable.*

#### Convergence, Cauchy Sequence, Completeness

​	**Definition.** A sequence $(x_n)$ in a metric space $X=(X,d)$ is said to **converge**  if there is an $x \in X$ such that
$$
\lim _{n\rightarrow \infty} d(x_n,x) = 0.
$$
$x$ is called the **limit** of $(x_n)$ and we write $\displaystyle\lim _{n \rightarrow \infty} x_n = x$ or $x_n \longrightarrow x$.

​	**Definition.** We call a nonempty subset $M \subset X$ a **bounded** set if its *diameter* $\delta (M) = \displaystyle \sup _{x,y \in M} d(x,y)$ is finite. And we call a sequence $(x_n)$ in $X$ a **bounded sequence** if the corresponding point set is a bounded set of $X$.

​	Let $X=(X,d)$ be a metric space. *A convergent sequence in $X$ is bounded and its limit is unique*. And *if $x_n \longrightarrow x$ and $y_n \longrightarrow y$ in $X$, then $d(x_n,y_n) \longrightarrow d(x,y)$.*

​	**Definition.** A sequence $(x_n)$ in a metric space $X = (X, d)$ is said to be **Cauchy** if for every $\varepsilon > 0$ there is an $N=N(\varepsilon)$ such that
$$
d ( x _ { m } , x _ { n } ) < \varepsilon \quad \text { for every } m , n > N.
$$
The space $X$ is said to be **complete** if every Cauchy sequence in $X$ converges.

​	Every convergent sequence in a metric space is a Cauchy sequence, but the convergence of a Cauchy sequence depend on the completeness of the corresponding space.

​	*The real line and the complex plane are complete metric spaces. The rational line $Q$ and the open interval $(a,b)$ in $R$ are incomplete metric space.*

​	We can prove the following three important theorems:

​	**Theorem.** *Let $M$ be a nonempty subset of a metric space $(X,d)$ and $\bar M$ its closure. Then:*

​	*(a)	$x \in \bar M$ if and only if there is a sequence $(x_n)$ in $M$ such that $x_n \longrightarrow x$.*

​	*(b)	$M$ is closed if and only if the situation $x_n \in M$, $x_n \longrightarrow x$ implies that $x \in M$.* 

​	**Theorem.** *A subspace $M$ of a complete metric space $X$ is itself complete if and only if the set $M$ is closed in $X$.*

​	**Theorem.** *A mapping $T$: $X\rightarrow Y$ of a metric space $(X,d)$ into a metric space $(Y,\tilde d)$ is continuous at a point $x_0 \in X$ if and only if* 
$$
\vec { x _ { n } } \rightarrow x _ { 0 } \quad \text { implies } \quad T x _ { n } \rightarrow T x _ { 0 }.
$$
​	To prove completeness, we take an arbitrary Cauchy sequence $(x_n)$ in $X$ and show that it converges in $X$. For different spaces, such proofs may vary in complexity, but they have approximately the same general pattern:

1. Construct an element $x$ (to be used as a limit).
2. Prove that $x$ is in the space considered.
3. Prove convergence $x_n\longrightarrow x$ (in the sense of the metric).

​	We shall present completeness conclusions for some metric spaces which occur quite frequently:

1. *Euclidean space $R^n$ and unitary space $C^n$ are complete.*

2. *The space $l^\infty$ is complete.*

3. *The space $c$ consisting of all convergent sequences $x = (\xi _j)$ of complex numbers, with the metric induced from the space $l^\infty$ is complete.*

4. *The space $l^p$ is complete, where $p$ is fixed and $1 \le p < +\infty$.*

5. *The continuous function space $C[a,b]$ is complete under infinite-norm metric, but incomplete under $1$-norm metric. Here, $[a,b]$ is any given closed interval on $R$.*

   We give a counterexample for $1$-norm metric:
   $$
   x_n(t) = \begin{cases}
   0 \quad & 0\le t \le \frac 1 2 \\
   n(x-\frac 1 2) \quad & \frac 1 2 < t < \frac 1 2 + \frac 1 n\\
   1 \quad & \frac 1 2 + \frac 1 n \le t \le 1
   \end{cases}
   $$
   Here is an illustration:

   <img src="D:\2020_fall\Notes\Figures\Counter-Example-for-C[a,b]-of-1-Norm.JPG" alt="Counter-Example-for-C[a,b]-of-1-Norm" style="zoom:67%;" />

6. *The space $Q$ is incomplete.*

#### Completion of Metric Spaces

We know that the rational line $Q$ is not complete but can be "enlarged" to the real line $R$ which is complete. And this "completion" $R$ of $Q$ is such that $Q$ is dense in $R$. It is quite
important that an arbitrary incomplete metric space can be "completed" in a similar fashion, as we shall see. 

​	**Definition.** Let $X=(X,d)$ and $\tilde X = (\tilde X,d)$ be metric spaces. Then: A mapping $T$ of $X$ into $\tilde X$ is said to be **isometric** or an **isometry** if $T$ preserves distances, i.e. it for all $x,y \in X$, 
$$
\tilde d(Tx,Ty) = d(x,y),
$$
where $Tx$ and $Ty$ are the images of $x$ and $y$, respectively. The space $X$ is said to be **isometric** with the space $\tilde X$ if there exists a bijective isometry of $X$ onto $\tilde X$. The spaces $X$ and $\tilde X$ are then called **isometric spaces**.

​	We can now state and prove the theorem that every metric space can be completed. The space $X$ occurring in this theorem is called the **completion** of the given space $X$.

​	**Theorem.** *For a metric space $X=(X,d)$ there exists a complete metric space $\hat X = (\hat X ,\hat d)$ which has a subspace $W$ that is isometric with $X$ and is dense in $\hat X$. This space $\hat X$ is unique except for isometries, that is, if $\tilde X$ is any complete metric space having a dense subspace $\tilde W $ isometric with $X$, then $\tilde X$ and $\hat X$ are isometric.* 

​	*Sketch of Proof.* First, we construct $\hat X = (\hat X, d)$ and an isometry $T$ of $X$ onto $W$, where $\bar W = \hat X$. Then we prove the completeness of $\hat X$ and the uniqueness of $\hat X$ (except for isometries).

​	*Proof.* **(a) (Construction of $\hat X = (\hat X, d)$)** Let $(x_n)$ and $(y_n)$ be Cauchy sequences in $X$. Define $(x_n)$ to be equivalent to $(y_n)$, written $(x_n) \sim (y_n)$, if 
$$
\lim _ { n \rightarrow \infty } d ( x _ { n } , x _ { n } ^ { \prime } ) = 0.
$$
Let $\hat X$ be the set of all equivalence classes $\{\hat x, \hat y, \cdots\}$ of Cauchy sequences in $X$. We write $(x_n) \in \hat x$ to mean that $(x_n)$ is a member of $\hat x$ (a *representative* of the class $\hat x$). We are to define a metric on $\hat X$:
$$
\hat { d } ( \hat { x } , \hat { y } ) = \lim _ { n \rightarrow \infty } d ( x _ { n } , y _ { n } ).
$$
To show that the above metric definition is valid, we need to ensure that:

1. The limit $\displaystyle \lim _ { n \rightarrow \infty } d ( x _ { n } , y _ { n } )$ always exists and is independent of the particular choice of representatives.
2. $\hat d$ satisfies (M1) to (M4), thus being a metric.

These are not difficult to prove.

​	**(b) (Construction of $W$, dense subspace, isometry)** With each $b \in X$, we associate the class $\hat b \in \hat X$ which contains the constant Cauchy sequence $(b,b,\cdots)$. This defines a mapping $T: X\longrightarrow W$ onto the subspace $W=T(X) \subset \hat X$. The mapping $T$ is given by $b \mapsto \hat { b } = T b$, where $(b,b,\cdots) \in \hat b$.

​	It's not difficult to show that:

1. $W$ is dense in $\hat X$.
2. $W$ is isometric with $X$.

​	**(c) (Completeness of $\hat X$)** Let $(\hat x_n)$ be any Cauchy sequence in $\hat X$. Since $W$ is dense in $\hat X$, for every $\hat x_n$ there is a $\hat z_n \in W$ such that
$$
\hat d(\hat x_n, \hat z_n) < \frac 1 n.
$$
Hence, by triangle inequality,
$$
\begin{aligned}
\hat { d } ( \hat { z } _ { m } , \hat { z } _ { n } ) &\leq \hat { d } ( \hat { z } _ { m } , \hat { x } _ { m } ) + \hat { d } ( \hat { x } _ { m } , \hat { x } _ { n } ) + \hat { d } ( \hat { x } _ { n } , \hat { z } _ { n } ) \\
& <\frac { 1 } { m } + \hat { d } ( \hat { x } _ { m } , \hat { x } _ { n } ) + \frac { 1 } { n },
\end{aligned}
$$
which indicates that $(\hat z_n)$ is a Cauchy sequence. Let $\hat x \in \hat X$ be the class to which $(z_n = T^{-1}\hat z_n)$ belongs. Then $\hat x$ is the limit of $(\hat x_n)$.

Hence the arbitrary Cauchy sequence $(\hat x_n)$ in $\hat X$ has the limit $\hat x \in \hat X$, and $\hat X$ is complete.

​	**(d) (Uniqueness of $\hat X$ except for isometries)** If $(\tilde X, \tilde d)$ is another complete metric space with a subspace $\tilde W$ dense in $\tilde X$ and isometric with $X$, for any $\tilde x,\tilde y \in \tilde X$ we have sequences $(\tilde x_n), (\tilde y_n)$ in $\tilde W$ such that $\tilde x_n \longrightarrow \tilde x$ and $\tilde y_n \longrightarrow \tilde y$; hence
$$
\tilde d(\tilde x,\tilde y) = \lim _{n\rightarrow \infty} \tilde d(\tilde x_n, \tilde y_n)
$$
follows from
$$
| \tilde { d } ( \tilde { x } , \tilde { y } ) - \tilde { d } ( \tilde { x } _ { n } , \tilde { y } _ { n } ) | \leq \tilde { d } ( \tilde { x } , \tilde { x } _ { n } ) + \tilde { d } ( \tilde { y } , \tilde { y } _ { n } ) \quad \rightarrow \quad 0.
$$
Since $\tilde W$ is isometric with $W \subset \hat X$ and $\bar W = \hat X$, the distances on $\tilde X$ and $\hat X$ must be the same. Hence $\tilde X$ and $\hat X$ are isometric. ■
