
> [!question] 
> Kolika různými způsoby lze vybrat k objektů?

## Rozklad množiny A

Podmnožiny B jsou neprázdné.
$B_1, ..., B_2 \subeq A$ tvoří rozklad A, jestliže:

1) $B_1 u B_2 u ... u B_k = A$
2) $\forall i \neq j; b_i a b_j = \empty$

$B_1, ..., B_k$ jsou takzvané třídy rozkladu. 

## Entice

> [!note]
>- Uspořádaná k-tice - $()$
>- Neuspořádaná k-tice - $\{\}$

![[Entice]]

## Kombinatorická pravidla
### Pravidlo součtu

$A = \{a_1,...,a_m\}$
$B = \{b_1,...,b_n\}$

Potom jeden prvek z A nebo B lze vybrat m+n různými způsoby.

$A prunik B = \notempty -> | A sjednoceni B | = |A| + |B|$

### Pravidlo součinu

$A = \{a_1,...,a_m\}$
$B = \{b_1,...,b_n\}$

$A a B = \empty$
Potom uspořádanou dvojici $(a,b)$, kde $a \in A, b \in B$ lze vybrat $m*n$ , možnými způsoby.

Počet prvků kartézského součinu:

$|A*B| = |A|*|B|$

## Dirichletův princip
![[Dirichletův princip]]

## Princip inkluze a exkluze (IE)

- $N$ - clkový počet objektů
- $\alpha_1, ..., \alpha_n$ - potencionální vlastnosti objektů
- $N(\alpha_{i1},....,\alpha_{ik})$ - počet objektů z celkového počtu které mají vlastnosti uvedené v závorce
- $\alpha_{i1}$ - objekt s uvedenou vlastností
- $N(\bar \alpha_{1},....,\bar \alpha_{n})$ - počet objektů, které nemají žádnou vlastnost $\alpha_1, ...,\alpha_n$

$$
N(\bar \alpha_{1},....,\bar \alpha_{n}) = 
N - 
\sum_{i=1}^n N(\alpha_i) +
\sum_{1 \leq i_1 \leq i_2 \leq n} N(\alpha_{i1},\alpha_{i2})
+ ...
+ (-1)^k \sum_{1 \leq i_1 \leq i_2 \leq ... \leq n} N(\alpha_{i1},..,\alpha_{ik})
$$


## n-objektů -> vytváření k-tic

Variace
Uspořádání k-tice
- $A^k_n$ bez opakování
- $\bar A ^k_n$ s opakování

Permutace
n = k
Uspořádání n-tice
- bez opakování
- s opakování

Kombinace
Neuspořádaná k-tice
- bez opakování
- s opakování

### Variace
![[Variace]]

### Permutace
![[Permutace počet]]

### Kombinace
![[Kombinace]]


## Zobecněný Pascalův trojúhelník
![[Pascalův trojúhelník]]

## Binomická věta
![[Binomická věta]]
## Multinomická věta
![[Multinomická věta]]

## Newtonův vzorec
![[Newtonův vzorec]]

