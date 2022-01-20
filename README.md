# Evolutionary Strategy

We explore the use of the Evolutionary Strategy zeroth-order oracle for minimizing a generic cost function. 

The algorithm assumes the access to a zeroth order oracle that returns the cost $f(x)$ for any $x$ in a given domain. The goal is to use a small number of oracle calls to compute the value of the gradient of function $`\nabla f(x)`$ at a given point $x$. To do so, the evolutionary strategy generates a set of random evaluation points, $`x_1, \ldots, x_k`$, where $x_i$ is generated by applying a small random perturbation to the current coordinate value $x$. It then evalutes the funtional values at all $`k`$ points, and calculates a sum of weighted differences in the cost, $`f(x_i)-f(x)`$, to generate an approximation of $`\nabla f(x)`$. 

The algorithm is based on a variant of the derivation described here: https://en.wikipedia.org/wiki/Natural_evolution_strategy#Search_gradients. 

