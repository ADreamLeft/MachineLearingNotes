f is learned classifier from training data $(x_1,y_1),(x_2,y_2),\cdots,(x_n,y_n)$
training err :$\frac{1}{n}\sum I[y_i \neq f(x_i)]$
test err: $P(Y\neq f(X))= E\{I[Y\neq f(X)]\}$
# Procedure
- collect data
- training learn $f \in \mathcal{F}$
## Oversimplified setting
$|\mathcal{F}|<\infty,\quad f \quad is \quad learned \quad from \quad (x_1,y_1),(x_2,y_2),\cdots$
$$
P(\frac{1}{n}\sum I[y_i \neq f(x_i)]- P(Y\neq f(X))\leq |\mathcal{F}|e^{-2n\epsilon^2}
$$
Union bound
# Representation Power of Neural Network
*Universal Approximation Theorem*
$\forall$ target func f(x) $x\in\textbf{R}^k$(f is a continuous function)
$$
\forall \epsilon > 0,\exists Neural Network\quad NN(\cdot),\quad s.t.||f-NN||_2\leq \epsilon
$$
