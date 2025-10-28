


### Introduction
1. Gneral form of an optimization problem
2. Terminology & Concept

### Algorithms and Convergence
1. Convergent sequence: $\lim_{k\to \infty}||x_k - x^*||_2 = 0$ 
2. Globally convergent algorithms(any intial point can congverge to local / global optimal solution) vs Locally convergent algorithms(only in a neighborhood of optimal solution can converge to optimal solution)
3. Asymptotic Convergence rate
	- Generally, it describes the _final behavior_ of the algorithm after it has settled down and is very close to the solution $x^*$ : $\lim_{k \to \infty} \frac{\|x^{k+1} - x^*\|}{\|x^k - x^*\|} = c < 1$ . This statement only tells you what the error ratio _approaches_ as $k$ gets infinitely large. It gives **no guarantee** about the error at a finite, small value of $k$ (e.g., $k=100$).
	- Q-linear convergence: $\|x^{k+1} - x^*\|_2 \le c\|x_k - x^*\|_2$
	- Q-superlinear convergence: $\|x^{k+1} - x^*\|_2 \le \alpha_k \|x_k - x^*\|_2$, where $\lim_{k \to \infty} \alpha_k = 0$
	- Q-sublinear convergence: $\|x^{k+1} - x^*\|_2 \le \alpha_k \|x_k - x^*\|_2$, where $\lim_{k \to \infty} \alpha_k = 1$
	- Q-quadratic convergence: $\|x^{k+1} - x^*\|_2 \le c\|x_k - x^*\|_2^2$ 
4. Non-asymptotic convergence rate
	- Generally,  it describes $\|x_k - x^*\| \le \frac{C}{\text{function}(k)}$ (Iterate Distance or Solution Convergence) or $f(x_k) - f^* \le \frac{C}{k^\alpha}$ (Optimality Gap or Objective Value Convergence). The bound is a concrete inequality that holds for all $k$, hence it is a non-asymptotic linear rate, which is much stronger than the asymptotic one. It provide a finite-time, absolute guarantee on the error, rather than just a limiting ratio.