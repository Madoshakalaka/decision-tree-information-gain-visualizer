Generate intermediate calculation for information gain algorithm


given table:

| X | Y | Z | Class |
|---|---|---|-------|
| 1 | 1 | 1 | A     |
| 1 | 1 | 0 | A     |
| 0 | 0 | 1 | B     |
| 1 | 0 | 0 | B     |

output:
```
G is shorthand for Gain, E is shorthand for Entropy

Information gain of splitting X:
G(X)= E(Class) - E(X, Class)
    = 1 - ( p(X=0)E(0, 1)+ p(X=1)E(2, 1))
    = 1 - ( 0.75 × 0+ 0.75×(-0.667 × log(0.667) - 0.333 × log(0.333)))
    = 0.31127812445913283

Information gain of splitting Y:
G(Y)= E(Class) - E(Y, Class)
    = 1 - ( p(Y=0)E(0, 2)+ p(Y=1)E(2, 0))
    = 1 - ( 0.5 × 0+ 0.5×0)
    = 1

Information gain of splitting Z:
G(Z)= E(Class) - E(Z, Class)
    = 1 - ( p(Z=0)E(1, 1)+ p(Z=1)E(1, 1))
    = 1 - ( 0.5 × (-0.5 × log(0.5) - 0.5 × log(0.5))+ 0.5×(-0.5 × log(0.5) - 0.5 × log(0.5)))
    = 0.0
```
