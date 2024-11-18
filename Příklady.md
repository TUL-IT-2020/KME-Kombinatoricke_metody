# Příklady ze cvičení

- [[KME_příklady_gen_fnc_web.pdf]]
- [[KME_příklady_rekurent_web.pdf]]
- [[KME_příklady_elem_komb_web.pdf]]

## K Zamyšlení:
### 1.

$$
S_n = min \{
k \in N^+\ | 
A_1, ..., A_n \sub \{1,2,...,k \}
\}
$$
$$
U A_i = \{1,2,3,...,k\} a \forall i,j \; A_i a A_j \neq \empty
$$

Existuje $A_i$ takové, že rovnice:

$$
x+y=z
$$
Má řešení v $A_i$.

## Příklad: Trojúhelníková čísla

$$
T_n , 
n \in N^+
$$

$T_3$:

![trojuhelník](https://e7.pngegg.com/pngimages/713/24/png-clipart-triangle-critical-graph-graph-theory-graph-of-a-function-triangle-angle-triangle.png)

$T_n = T_{n-1} + n$
$T_1 = 1$
$T_0 = 0$

Určete rekurentní vztah pro $T_n$.
### Postup

$$
T_n = \frac{n}{2}(n+1)
$$
## Příklad: Rychlý reaktor

- $a$ - rychlé n.
- $b$ - pomalé

$a -> 2a + b$
$b -> a + b$

$a_n, b_n$ - počet částic v čase $n$.

Sestavte soustavu rekurentních vztahů:
### Řešení
$$
a_{n+1} = 2a_n + b_n
$$

$$
b_{n+1} = a_n + b_n
$$

## Příklad
Rekurentní vztah:
$$
a_n = 8a_{n-1} - 16 a_{n-2}
$$
Je posloupnost řešením rekurentního vztahu?

| Posloupnost           | Je řešením? |
| --------------------- | ----------- |
| $a_n = 0$             |             |
| $a_n = 1$             |             |
| $a_n = 2^n$           |             |
| $a_n = 4^n$           |             |
| $a_n = n4^n$          |             |
| $a_n = 2*4^n + 3n4^n$ |             |
| $a_n = -4^n$          |             |
| $a_n = n^2*4^n$       |             |
### Postup

$(x^2-8x+16) = 0$
$(x-4)^2$
$x =4$

### Řešení
| Posloupnost           | Je řešením? |
| --------------------- | ----------- |
| $a_n = 0$             | ano         |
| $a_n = 1$             | ne          |
| $a_n = 2^n$           | ne          |
| $a_n = 4^n$           | ano         |
| $a_n = n4^n$          | ano         |
| $a_n = 2*4^n + 3n4^n$ | ano         |
| $a_n = -4^n$          | ne          |
| $a_n = n^2*4^n$       | ne          |


## Příklad
$$
\binom{5}{6} \binom{5}{2}
$$


$$
\begin{array}{c} 12 \\ 34 \end{array}
$$