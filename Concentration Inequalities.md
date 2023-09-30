# Warm up
## Markov Ineq
$$r.v.\quad X \geq 0, \quad EX \quad exists.\quad\forall k \ge 0, \quad P(X\geq k)\leq \frac{EX}{k}$$
## Chebychev Ineq
$$r.v.\quad X, \quad EX, \quad Var(X)\quad exists.\quad P(|X-EX|\geq 0)\leq \frac{Var(X)}{k^2}$$
## More accurate one
$$r.v. \quad X, \quad EX,EX^2,\cdots , EX^r.\quad \forall k\geq 0, \quad P(X\geq k)\leq min \frac{EX^t}{k^t}$$
## Generating Function
### Preparations
$$r.v. \quad X, \quad EX,EX^2,\cdots , EX^r.\quad Ee^{tx} = \sum_{i=0}\frac{i!}{t^i}EX^t$$
### Chernoff Ineq
$$r.v. \quad X, \quad EX,EX^2,\cdots , EX^r.\quad \forall k\geq 0, \quad P(X\geq k)\overset{\forall t >0}=P(e^{tx}\geq e^{tk})\leq inf (e^{-tk}Ee^{tk})$$
## (Simple) Concentration Ineq
$$r.v.\quad X_1,X_2,\cdots,X_n \quad i.i.d\quad Bernoulli,\quad EX=P(x=1)=p,\quad Var(X)=p(1-p).\quad P(|\frac{1}{n}\sum_{i=1}x_i-EX|\geq \epsilon) \leq \frac{p(1-p)}{n\epsilon^2}$$
$C.L.T. \quad e^{-O(n)}$
## Chernoff Bound 
### 1st case
$$\begin{aligned}&r.v. X,X_1,X_2,\cdots,X_n\quad i.i.d. \quad Bernoulli \quad EX=P(X=1)=p,\quad Var(X)=p(1-p)\\ &\quad P(\frac{1}{n}\sum_{i=1}X_i-p\geq\epsilon) \\&=P(\sum X_i\geq n(p+\epsilon))\\&\leq inf Ee^{t\sum X_i}e^{-nt(p+\epsilon)} \\&= inf (pe^t+1-p)^ne^{-nt(p+\epsilon)}\\&=e^{-nD_B(p+\epsilon||p)}\end{aligned}$$
### 2nd case
$$\begin{aligned}&r.v. X,X_1,X_2,\cdots,X_n\quad i.i.d. X \in [0,1].EX=p\in[0,1]\\ &\quad P(\frac{1}{n}\sum_{i=1}X_i-p\geq\epsilon) \\&=P(\sum X_i\geq n(p+\epsilon))\\&\leq inf Ee^{t\sum X_i}e^{-nt(p+\epsilon)} \\&\leq inf (pe^t+1-p)^ne^{-nt(p+\epsilon)}\\&=e^{-nD_B(p+\epsilon||p)}\end{aligned}$$
### 3rd case
$$\begin{aligned}&r.v. X,X_1,X_2,\cdots,X_n\in [0,1],\quad  EX=p_i, \quad let\quad p = \frac{1}{n}\sum p_i \\ &P(\frac{1}{n}\sum X_i - P \geq \epsilon ) \\&\leq Ee^{t\sum X_i}e^{-nt(p+\epsilon)}\\&=\prod Ee^{tX_i}e^{-nt(p+\epsilon)}\\&\leq\prod (p_ie^t+1-p_i)e^{-nt(p+\epsilon)}\\&\leq (pe^t+1-p)^n e^{-nt(p+\epsilon)}\\&=e^{-nD_B(p+\epsilon||p)}\end{aligned}$$
### Simplified inequality(Additive Chernoff Bound)
$$
D_B(P+\epsilon ||p) \geq2\epsilon^2
$$

## Hoeffding Inequality
$$
\begin{aligned}&r.v. \quad  X_1, X_2,\cdots,X_n, \quad independent ,X_i\in[a_i, b_i],\mu = E\frac{1}{n}\sum X_i\\ &P(\frac{1}{n}X_i-\mu\geq\epsilon)\leq e^{-\frac{2n^2\epsilon^2}{\sum(b_i-a_i)^2}}\end{aligned}
$$
# Draw w/o replacement
Assume $a_1, a_2,\cdots,a_N\in\{0,1\}$.Randomly draw $X_1,\cdots,X_n$ from $\{a_i\}$
- Draw with replacement  $\frac{1}{n}\sum X_i$ concentration
- Draw without replacement (直觉上更容易集中)
# Stable function
Assume $f(x_1, x_2,\cdots, x_n)$ is a stable function.
$$
\begin{aligned}
&\forall x_1, x_2,\cdots,x_n\in [0,1], f(x_1,x_2,\cdots,x_n)\\
&|f(x_1,x_2,\cdots,x_i,\cdots,x_n)-f(x_1,x_2,\cdots,x_i',\cdots,x_n)|\leq c_i\\
&P(f-Ef\geq \epsilon)\leq e^{-\frac{\epsilon^2}{\sum c_i^2}}
\end{aligned}
$$
# Appendixes
## Entropy: 
$$r.v. \quad X .\quad prob \quad distribution(p_1,p_2,\cdots,p_n)\quad H(x):=-\sum_{i=1}p_i\log_2{p_i}(bits)$$
## Relative Entropy:
$$P=(p_1, p_2,\cdots,p_n), Q=(q_1,q_2,\cdots,q_n),\quad D(P||Q):=\underset{i}{\sum}p_i\log_2\frac{p_i}{q_i}.(bits)$$
## Bernoulli Entropy
$$P=(p,1-p), Q=(q, 1-q),\quad D_B(P||Q)=p\ln\frac{p}{q}+(1-p)\ln\frac{1-p}{1-q}$$

