

```python
import numpy as np

import matplotlib
import matplotlib.pyplot as plt
```

## Task 1

<i>
    Find the dimensions (height - $ h $, radius - $ r $) that will minimize 
the surface areaof the metal to manufacture a circular cylindrical can of volume $ V $.
</i>

### Solution

$$
\begin{cases}
    V = \pi r^2 h = const \\
    min_{h, r} S(h, r) = 2 \pi r h + 2 \pi r^2
\end{cases}
\implies
\begin{cases}
    h = \dfrac{V}{\pi r^2} \\
    min_{r} A(r) = \dfrac{2 V}{r} + 2 \pi r^2
\end{cases}
$$

Point that minimize $ A(r) $ must satisfy to the condition $$ d A(h, r) = 0, d^2 A(r) > 0 $$

$$
\dfrac{d A}{d r} = -\dfrac{2 V}{r^2} + 4 \pi r = \dfrac{- 2 V + 4 \pi r^3}{r^2} = 0 \\
\begin{cases}
    - 2 V + 4 \pi r^3 = 0 \\
    r \ne 0 \\
    h = \dfrac{V}{\pi r^2}
\end{cases} \implies
\begin{cases}
    r = {\left ( \dfrac{V}{2 \pi} \right ) }^{\dfrac{1}{3}} \\
    h = \dfrac{V}{\pi {\left ( \dfrac{V}{2 \pi} \right ) }^{\dfrac{2}{3}}}
\end{cases} \implies
\begin{cases}
    r = {\left ( \dfrac{2 V}{4 \pi} \right ) }^{\dfrac{1}{3}} \\
    h = \dfrac{V^{\dfrac{1}{3}}}{\pi {\left ( \dfrac{1}{2 \pi} \right ) }^{\dfrac{2}{3}}} \\
    \textbf{For all } V \geq 0
\end{cases}
$$

## Task 2

Consider the unconstrained optimization problem to minimize the function 
$$ f(x) = \dfrac{3}{2} (x^2_1 + x^2_2) + (1 + a) x_1 x_2 − (x_1 + x_2) + b $$
, where $ a $ and $ b $ are real-valued parameters. Find all values of $ a $ and $ b $ such that the problem has a unique optimal solution.

### Solution

$ f(x_1, x_2) = \dfrac{3}{2} (x^2_1 + x^2_2) + (1 + a) x_1 x_2 − (x_1 + x_2) + b $
Criteria for minimum:
$$
\begin{cases}
    d f(x_1, x_2) = 0 \\
    d^2 f(x_1, x_2) \geq 0
\end{cases}
\implies
\begin{cases}
    d f(x_1, x_2) = \left (3 x_1 + (1 + a) x_2 - 1 \right ) d x_1 + \left (3 x_2 + (1 + a) x_1 - 1 \right ) d x_2 \\
    d^2 f(x_1, x_2) = 7 + a \geq 0
\end{cases}
$$

In matrix form:
$$
\begin{bmatrix}
    3 & 1 + a \\
    1 + a & 3
\end{bmatrix} 
\begin{bmatrix}
    x_1 \\
    x_2
\end{bmatrix} = 
\begin{bmatrix}
    1 \\
    1
\end{bmatrix} \implies
$$
<strong>Cramer's rule</strong>
$$
\begin{cases}
    det = 9 - ({1 + a}^2) \neq 0 \\
    det_{x_1} = 3 - (a + 1) \\
    det_{x_2} = 3 - (a + 1)
\end{cases} \implies
x_1 = x_2 = \dfrac{1}{4 + a} \implies a \neq 0
\implies
\begin{cases}
    a \geq -7 \\
    a \neq 2 \\
    a \neq -4 \\
    \textbf{For all } b
\end{cases} \implies
$$

## Task 3
