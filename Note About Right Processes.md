Let us consider a measurable space $(E,\mathscr E)$. Suppose that $\mu$ is a $\sigma$-finite measure on $(E,\mathscr E)$. A set $N\subset E$ is called a $\mu$-mull set if there is $N_0\in \mathscr E$ so that $N \subset N_0$ and $\mu(N_0)= 0$. For $A,B\subset E$ we define the symmetric difference $A\Delta B:= (A\setminus B) \cup (B\setminus A)$. It is easy to show that 

$\mathscr E^\mu := \{A\subset E: A\Delta B\text{ is a $\mu$-null set for some $B\in \mathscr E$}\}$

is a $\sigma$-algebra, which is called the $\mu$-completion of $\mathscr E$. We can let $\mu(A)=\mu(B)$ for $B\in \mathscr E$ such that $A\Delta B$ is a $\mu$-null set to extend $\mu$ uniquely to a $\sigma$-finite measure on $(E,\mathscr E^\mu)$. The measure space $(E, \mathscr E,\mu)$ is said to be complete if $\mathscr E = \mathscr E^\mu$. The universal completion of $\mathscr E$ is the $\sigma$-algebra $\mathscr E^u$ defined to be the intersection of $\mu$-completions of $\mathscr E$ as $\mu$ runs over all finite measures on $(E,\mathscr E)$.

Proposition A.3: If $\sigma$-algebras satisfy $\mathscr E_1\subset \mathscr E_2\subset \mathscr E_1^u$ then $\mathscr E_2^u = \mathscr E_1^u$.

Suppose that $(E,\mathscr E)$ and $(F,\mathscr F)$ are measurable spaces. A $\sigma$-finite kernel from $(E,\mathscr E)$ to $(F,\mathscr F)$ is a function $K$ on $E\times \mathscr F$ have values in $[0,\infty]$ such that 

(1) for each $A\in \mathscr F$ the mapping $x\mapsto K(x,A)$ is $\mathscr E$-measurable;

(2) for each $x\in E$ the mapping $A\mapsto K(x,A)$ is a $\sigma$-finite measure on $(F,\mathscr F)$. 

A kernel $K$ is said to be bounded if $x\mapsto K(x,F)$ is bounded function on $E$. 

The kernel $K$ is called Markov or sub-Markov if $K(x,F) = 1$ or $K(x,F)\leq 1$, respectively, for each $x\in E$. A kernel from $(E,\mathscr E)$ to itself is simply called a kernel on $(E,\mathscr E)$. Given a bounded kernel $K$ from $(E,\mathscr E)$ to $(F, \mathscr F)$, for any $f\in b\mathscr F$ we can define $Kf\in b\mathscr E$ by
$$
Kf(x) = K(x,f) = \int_F f(y)K(x,\mathrm dy),\quad x\in E, 
$$
 ane for any finite measure $\mu$ on $(E,\mathscr E)$ we can define a finite measure $\mu K$ on $(F,\mathscr F)$ by
$$
\mu K(B) = \int_E K(x,B)\mu(\mathrm dx),\quad B\in \mathscr F.
$$
Proposition A.4: A bounded kernel $K$ from $(E, \mathscr E)$ to $(F,\mathscr F)$ extends in a unique way to a bounded kernel $K$ from $(E,\mathscr E^u)$ to $(F,\mathscr F^u)$. 

--------------------



Let $E$ be a Polish space. A family of sub-Markov kernels $(P_t)_{t\geq 0}$ on $(E,\mathscr E)$ where $\mathscr B^0 \subset\mathscr E = \mathscr B^\cdot(E)\subset \mathscr B^u$ is called a transition semigroup if $P_{t+s} = P_t P_s$ for $t,s\geq 0$. We say $(P_t)_{t\geq 0}$ is Markov of conservative if each $P_t$ is a Markov kernel. We say $P_t$ if normal if $P_0= I$ for each $x\in E$. 

Suppose that $(P_t)_{t\geq 0}$ is a normall Markov transition semigroup on $(E,\mathscr B^\cdot(E))$. The collection $\xi=(\Omega, \mathscr G, \mathscr G_t,\theta_t,\mathbf P_x)$ is called a $\mathscr B^\cdot(E)$-Markov process with transition semigroup $(P_t)_{t\geq 0}$ in case $\xi$ satisfies the following conditions:

(1) $(\Omega, \mathscr G, (\mathscr G_t)_{t\geq 0})$ is a filtered measurable space, and $(\xi_t)_{t\geq 0}$ is an $E$-valued process $\mathscr B^\cdot(E)$-adapted to $(\mathscr G_t)_{t\geq 0}$.

(2) $(\theta_t)_{t\geq 0}$ is a collection of shift operators for $\xi$, that is, maps of $\Omega$ into itself satisfying $\theta_s\circ \theta_t = \theta_{s+t}$ and $\xi_s\circ\theta_t = \xi_{s+t}$ identically for $t,s\geq 0$.

(3) For every $x\in E$, $\mathbf P_x$ is a probability measure on $(\Omega,\mathscr G)$ and $x\mapsto \mathbf P_x(H)$ is $\mathscr B^\cdot(E)$-measurable for each $H\in b\mathscr G$. 

(4) For every $x\in E$, we have $\mathbf P_x\{\xi_0 = x\}=1$ and for any $x\in E$,
$$
\mathbf P_x[f(\xi_t)|\mathscr G_r] = P_{t-r} f(\xi_r), \quad r\leq t\in I, f\in b\mathscr B^\cdot(E).
$$
We way $\xi$ is right continuous if $t\mapsto \xi_t(\omega)$ is right continuous for every $\omega \in \Omega$. Given those collection , for any finite measure $\mu$ on $(E, \mathscr B^\cdot(E))$ we may define the finite measure $\mathbf P_\mu$ on $(\Omega, \mathscr G)$ by 
$$
\mathbf P_\mu(H) = \int_E \mathbf P_x(H) \mu(\mathrm dx), \quad H\in \mathrm b\mathscr G.
$$
In the sequel, we always assume $\mu$ is a probability measure unless stated other wise.

Let $\mathscr G^\mu$ denote the $\mathbf P_\mu$-completion of $\mathscr G$ and let $\mathscr N^\mu(\mathscr G)$ denote the family of $\mathbf P_\mu$-null sets in $\mathscr G^\mu$. Then define:
$$
\bar {\mathscr G} = \cap_\mu \mathscr G^\mu; \quad \mathscr N(\mathscr G) = \cap_\mu \mathscr N^\mu(\mathscr G);\quad \mathscr G_t^\mu = \sigma(\mathscr G_t \cup \mathscr N^\mu(\mathscr G));\quad \bar {\mathscr G_t} = \cap_\mu \mathscr G^\mu_t. 
$$
We call $(\bar {\mathscr G}, \bar {\mathscr G}_t)$ the augmentation of $(\mathscr G, \mathscr G_t)$ by the system of probabilities $\{\mathbf P_\mu:\mu \in \mathcal P(E)\}$. It is easy to see that $\mathbf P_\mu$ extends uniquely to $\bar{\mathscr G}$. $P_t$ can be extended uniquely as a kernel on $(E,\mathscr B^u(E))$.

Proposition: $(\Omega, \bar {\mathscr G}, \bar{\mathscr G_t},\theta_t,\xi_t,\mathbf P_x )$ is a $\mathscr B^u(E)$-Markov process. 

---------------------------------------------

We say $(\Omega, \bar {\mathscr G}, \bar {\mathscr G_t}, \theta_t, \xi_t, \bar P_t,\bar{\mathbf P}_x)$ is the argumentation of $$(\Omega, \mathscr G, \mathscr G_t, \theta_t, \xi_t, P_t,\mathbf P_x)$$. We say a system if argumented if it is identical to its augementation. Argumentation of some system is always argumented. 

(1) $(\Omega, \mathscr G, \mathscr G_t, \theta_t, \xi_t, P_t,\mathbf P_x)$ is an right continuous argumented Markov system.

(2) $\{s\mapsto P_{t-s}f(\xi_s)\mathbf 1_{[0,t)}(s) \text{ is not right continuous}\} \in \mathscr N(\mathscr G)$ for every $t\geq 0$ and every $f\in b\mathscr B^u(E)$.

(3) $\mathscr G_t$ is right continuous.

Proposition: Let $(\Omega, \mathscr G, \mathscr G_t, \theta_t, \xi_t, P_t,\mathbf P_x)$ be the argumentation of a right continuous natural Markov system. Suppose that $\{s\mapsto P_{t-s}f(\xi_s)\mathbf 1_{[0,t)}(s) \text{ is not right continuous}\} \in \mathscr N(\mathscr G)$ for every $t\geq 0$ and every $f\in b\mathscr B^u(E)$. Then $(\mathscr G_t)$ are right continuous.  $(\mathscr G^\mu_t)$ be right continuous.

-------------------

